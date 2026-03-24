# The Anatomy of an Agent Harness（Agent Harness 的解剖）

**作者：** Viv (@Vtrivedy10, LangChain 团队)
**发布时间：** 2026年3月11日
**来源：** https://x.com/Vtrivedy10/status/2031408954517971368
**数据：** 47回复、360转帖、1729喜欢、4314书签、66.6万观看

---

## TL;DR

**Agent = Model + Harness**

Harness engineering is how we build systems around models to turn them into work engines. The model contains the intelligence and the harness makes that intelligence useful.

---

## 一、什么是 Harness？

### 核心定义

**Agent = Model + Harness**

**If you're not the model, you're the harness.**

A harness is every piece of code, configuration, and execution logic that isn't the model itself. A raw model is not an agent. But it becomes one when a harness gives it things like state, tool execution, feedback loops, and enforceable constraints.

### Harness 包含的内容

**Concretely, a harness includes things like:**

1. **System Prompts**（系统提示词）
2. **Tools, Skills, MCPs + and their descriptions**（工具、技能、MCP及其描述）
3. **Bundled Infrastructure**（打包的基础设施）
   - Filesystem（文件系统）
   - Sandbox（沙盒）
   - Browser（浏览器）
4. **Orchestration Logic**（编排逻辑）
   - Subagent spawning（子Agent生成）
   - Handoffs（移交）
   - Model routing（模型路由）
5. **Hooks/Middleware for deterministic execution**（钩子/中间件）
   - Compaction（压缩）
   - Continuation（继续）
   - Lint checks（代码检查）

---

## 二、为什么需要 Harness？（从模型的视角）

### 模型无法直接做到的事情

**There are things we want an agent to do that a model cannot do out of the box. This is where a harness comes in.**

**Models (mostly) take in data like text, images, audio, video and they output text. That's it. Out of the box they cannot:**

1. **Maintain durable state across interactions**（在交互之间保持持久状态）
2. **Execute code**（执行代码）
3. **Access realtime knowledge**（访问实时知识）
4. **Setup environments and install packages to complete work**（设置环境并安装包来完成工作）

**These are all harness level features.**

The structure of LLMs requires some sort of machinery that wraps them to do useful work.

---

## 三、从期望的 Agent 行为反向推导 Harness 设计

### 设计模式

**Behavior we want (or want to fix) → Harness Design to help the model achieve this.**

Harness Engineering helps humans inject useful priors to guide agent behavior. And as models have gotten more capable, harnesses have been used to surgically extend and correct models to complete previously impossible tasks.

---

## 四、核心 Harness 组件

### 1. Filesystems for Durable Storage and Context Management（文件系统）

**为什么需要？**

We want agents to have durable storage to interface with real data, offload information that doesn't fit in context, and persist work across sessions.

**Models can only directly operate on knowledge within their context window.** Before filesystems, users had to copy/paste content directly to the model, that's clunky UX and doesn't work for autonomous agents.

**解决方案：**

Harnesses ship with filesystem abstractions and tools for fs-ops.

**文件系统是 Harness 最基础的原语，因为它解锁了：**

1. **Agents get a workspace to read data, code, and documentation.**（Agent获得工作空间来读取数据、代码和文档）
2. **Work can be incrementally added and offloaded instead of holding everything in context.**（工作可以增量添加和卸载，而不是把所有东西都保存在上下文中）
   - Agents can store intermediate outputs and maintain state that outlasts a single session.（Agent可以存储中间输出并维持跨会话的状态）
3. **The filesystem is a natural collaboration surface.**（文件系统是天然的协作表面）
   - Multiple agents and humans can coordinate through shared files. Architectures like Agent Teams rely on this.（多个Agent和人类可以通过共享文件协调。Agent Teams架构依赖于此）

**Git adds versioning** to the filesystem so agents can track work, rollback errors, and branch experiments.

---

### 2. Bash + Code as a General Purpose Tool（Bash + 代码作为通用工具）

**为什么需要？**

We want agents to autonomously solve problems without humans needing to pre-design every tool.

**The main agent execution pattern today is a ReAct loop**, where a model reasons, takes an action via a tool call, observes the result, and repeats in a while loop. But harnesses can only execute the tools they have logic for.

Instead of forcing users to build tools for every possible action, a better solution is to **give agents a general purpose tool like bash.**

**解决方案：**

Harnesses ship with a bash tool so models can solve problems autonomously by writing & executing code.

**Bash + code exec is a big step towards giving models a computer and letting them figure out the rest autonomously.** The model can design its own tools on the fly via code instead of being constrained to a fixed set of pre-configured tools.

---

### 3. Sandboxes and Tools to Execute & Verify Work（沙盒和工具）

**为什么需要？**

Agents need an environment with the right defaults so they can safely act, observe results, and make progress.

We've given models storage and the ability to execute code, but all of that needs to happen somewhere. **Running agent-generated code locally is risky and a single local environment doesn't scale to large agent workloads.**

**解决方案：**

**Sandboxes give agents safe operating environments.** Instead of executing locally, the harness can connect to a sandbox to run code, inspect files, install dependencies, and complete tasks. This creates secure, isolated execution of code. For more security, harnesses can allow-list commands and enforce network isolation.

**Sandboxes also unlock scale** because environments can be created on demand, fanned out across many tasks, and torn down when the work is done.

**Good environments come with good default tooling.** Harnesses are responsible for configuring tooling so agents can do useful work. This includes:
- Pre-installing language runtimes and packages
- CLIs for git and testing
- Browsers for web interaction and verification

**Tools like browsers, logs, screenshots, and test runners give agents a way to observe and analyze their work.** This helps them create **self-verification loops** where they can write application code, run tests, inspect logs, and fix errors.

---

### 4. Memory & Search for Continual Learning（记忆和搜索）

**为什么需要？**

Agents should remember what they've seen and access information that didn't exist when they were trained.

**Models have no additional knowledge beyond their weights and what's in their current context.** Without access to edit model weights, the only way to "add knowledge" is via **context injection.**

**解决方案：**

**For memory, the filesystem is again a core primitive.** Harnesses support memory file standards like **AGENTS.md** which get injected into context on agent start. As agents add and edit this file, harnesses load the updated file into context. This is a form of **continual learning** where agents durably store knowledge from one session and inject that knowledge into future sessions.

**Knowledge cutoffs mean that models can't directly access new data** like updated library versions without the user providing them directly. For up-to-date knowledge, **Web Search and MCP tools like Context7** help agents access information beyond the knowledge cutoff like new library versions or current data that didn't exist when training stopped.

---

### 5. Battling Context Rot（对抗上下文腐烂）

**为什么需要？**

Agent performance shouldn't degrade over the course of work.

**Context Rot describes how models become worse at reasoning and completing tasks as their context window fills up.** Context is a precious and scarce resource, so harnesses need strategies to manage it.

**Harnesses today are largely delivery mechanisms for good context engineering.**

**解决方案：**

1. **Compaction**（压缩）
   - Addresses what to do when the context window is close to filling up
   - Intelligently offloads and summarizes the existing context window so the agent can continue working

2. **Tool call offloading**（工具调用卸载）
   - Helps reduce the impact of large tool outputs that can noisily clutter the context window
   - The harness keeps the head and tail tokens of tool outputs above a threshold number of tokens and offloads the full output to the filesystem

3. **Skills**（技能）
   - Address the issue of too many tools or MCP servers loaded into context on agent start which degrades performance before the agent can start working
   - Skills are a harness level primitive that solve this via **progressive disclosure**

---

### 6. Long Horizon Autonomous Execution（长期自主执行）

**为什么需要？**

We want agents to complete complex work, autonomously, correctly, over long time horizons.

**Autonomous software creation is the holy grail for coding agents.** But today's models suffer from:
- Early stopping（过早停止）
- Issues decomposing complex problems（分解复杂问题的问题）
- Incoherence as work stretches across multiple context windows（跨多个上下文窗口工作的不连贯）

A good harness has to design around all of this.

**解决方案：**

Long-horizon work requires durable state, planning, observation, and verification to keep working across multiple context windows.

1. **Filesystems and git for tracking work across sessions.**
   - Agents produce millions of tokens over a long task so the filesystem durably captures work to track progress over time
   - Adding git allows new agents to quickly get up to speed on the latest work and history of the project
   - For multiple agents working together, the filesystem also acts as a shared ledger of work

2. **Ralph Loops for continuing work.**
   - The Ralph Loop is a harness pattern that intercepts the model's exit attempt via a hook and reinjects the original prompt in a clean context window, forcing the agent to continue its work against a completion goal
   - The filesystem makes this possible because each iteration starts with fresh context but reads state from the previous iteration

3. **Planning and self-verification to stay on track.**
   - Planning is when a model decomposes a goal into a series of steps
   - Harnesses support this via good prompting and injecting reminders how to use a plan file in the filesystem
   - After completing each step, agents benefit from checking correctness of their work via **self-verification**
   - Hooks in harnesses can run a pre-defined test suite and loop back to the model on failure with the error message

---

## 五、Harness 的未来

### 1. The Coupling of Model Training and Harness Design（模型训练和Harness设计的耦合）

**Today's agent products like Claude Code and Codex are post-trained with models and harnesses in the loop.** This helps models improve at actions that the harness designers think they should be natively good at like filesystem operations, bash execution, planning, or parallelizing work with subagents.

**This creates a feedback loop:**
- Useful primitives are discovered, added to the harness
- Then used when training the next generation of models
- As this cycle repeats, models become more capable within the harness they were trained in

**But this co-evolution has interesting side effects for generalization.** It shows up in ways like how changing tool logic leads to worse model performance. A good example is described in the **Codex-5.3 prompting guide** with the apply_patch tool logic for editing files. A truly intelligent model should have little trouble switching between patch methods, but training with a harness in the loop creates this overfitting.

**But this doesn't mean that the best harness for your task is the one a model was post-trained with.**

**The Terminal Bench 2.0 Leaderboard** is a good example. Opus 4.6 in Claude Code scores far below Opus 4.6 in other harnesses.

In a previous blog, we showed how we improved our coding agent **Top 30 to Top 5 on Terminal Bench 2.0 by only changing the harness.** There's a lot of juice to be squeezed out of optimizing the harness for your task.

---

### 2. Where Harness Engineering is Going（Harness Engineering 的方向）

**As models get more capable, some of what lives in the harness today will get absorbed into the model.** Models will get better at planning, self-verification, and long horizon coherence natively, thus requiring less context injection for example.

**That suggests harnesses should matter less over time.** But just as prompt engineering continues to be valuable today, it's likely that **harness engineering will continue to be useful for building good agents.**

It's true that harnesses today patch over model deficiencies, but **they also engineer systems around model intelligence to make them more effective.** A well-configured environment, the right tools, durable state, and verification loops make any model more efficient regardless of its base intelligence.

---

### 3. LangChain 的研究方向

Harness engineering is a very active area of research that we use to improve our harness building library **deepagents** at LangChain. Here are a few open and interesting problems we're exploring today:

1. **Orchestrating hundreds of agents working in parallel on a shared codebase**（编排数百个Agent在共享代码库上并行工作）
2. **Agents that analyze their own traces to identify and fix harness-level failure modes**（分析自己的trace来识别和修复Harness级别故障模式的Agent）
3. **Harnesses that dynamically assemble the right tools and context just-in-time for a given task instead of being pre-configured**（为给定任务动态组装正确的工具和上下文的Harness，而不是预先配置）

---

## 总结

**This blog was an exercise in defining what a harness is and how it's shaped by the work we want models to do.**

**The model contains the intelligence and the harness is the system that makes that intelligence useful.**

**To more harness building, better systems, and better agents.**

---

*保存时间：2026-03-23*
*保存人：小然 (OpenClaw)*
