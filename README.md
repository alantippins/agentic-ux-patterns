# UX for Agentic Systems

_Design heuristics for building trustworthy, human-centered interfaces in systems that act on our behalf._

---

## 🌐 What is this?

This is a living framework of heuristics for designing agentic systems—tools and interfaces where users delegate tasks to AI agents that can act autonomously or semi-autonomously.

As software shifts from passive interfaces to active collaborators, we need new UX principles to support delegation, transparency, explainability, and trust. This repo offers a structured set of rules, examples, and design implications for creating better human-agent interactions.

---

## 📚 Heuristics

Each heuristic includes:

- A **rule** – a guiding design principle
- **Why it matters** – the user need or trust gap it addresses
- **Design implications** – how it applies in product
- A **real or fictional example** – to ground the idea

### 1. Design for delegation, not interaction (Adapted)
Rule: Users aren’t here to click, they’re here to get something done.
Why it matters: In traditional UX, we design flows. In agentic systems, users care about the outcome, not always how it gets done.
Design implications:
- Start with what the user wants to achieve, not what they need to click through. Minimize or abstract the steps unless the user explicitly wants control.
- Let users set intent (e.g., "Fix this bug") without walking them through every task. Offer override or review options only when needed.

Action: Ask, “What would the user delegate if they could wave a wand?”

🔍 Example: Linear for Agents
Linear is exploring agent collaboration, enabling agents to be assigned to issues and suggest actions like PRs. The interface centers on outcomes, not steps.

### 2. Clarify intent before acting (Adapted)
Rule: Agents need enough context to understand what the user means before acting.
Why it matters: Misunderstood intent can lead to incorrect or harmful outcomes.
Design Implications:
- Ask clarifying questions when user input is ambiguous.
- Enable users to revise and clarify goals before action.

Action: Let users refine intent. Try designing the agent’s first response as a clarifying question.

🔍 Example: Zapier Agents
Zapier prompts for user goals. If unclear which tools to use, the agent asks follow-ups and pauses until clarified.

### 3. Design for Uncertainty (Adapted)
Rule: Let agents reveal confidence and admit gaps when unsure.
Why it matters: Transparency builds trust.
Design Implications:
- Visualize confidence levels through UI cues.
- Offer fallback or escalation options when confidence is low.

Action: Surface confidence and fallback options.

🔍 Example: Fin by Intercom
In customer support contexts, Fin signals when it’s unsure and escalates to human agents.

### 4. Always provide a way to undo (Adapted)
Rule: Users must be able to inspect, reverse, or stop agent actions.
Why it matters: Trust depends on recoverability.
Design Implications:
- Integrate audit logs, previews, and undo states.
- Show upcoming agent actions and allow cancellation.

Action: Sketch the “oh no” moments. What would the user want to undo, or preview, and how?

🔍 Example: Devin (Cognition)
Devin previews diffs and lets users approve or reject changes before merging.

### 5. Feedback loops should drive behavior (Adapted)
Rule: Agents should learn from user feedback and improve.
Why it matters: Perceived learning builds engagement and trust.
Design Implications:

- Collect and surface feedback controls (e.g., thumbs up/down).
- Reflect back how agent behavior changes as a result.

Action: Show changes based on feedback.

🔍 Example: Zapier AI AgentsZapier’s agents adjust how they build workflows based on user edits and confirmations. 

### 6. Design for adjustable autonomy (Adapted)
Rule: Let users set and change how much control agents have.
Why it matters: Different users have different comfort levels with how much an agent acts on their behalf. Adjustable autonomy keeps users in control of delegation, rather than forcing a one-size-fits-all mode of interaction.
Design Implications:
- Offer different autonomy levels for users to select.
- Make autonomy modes transparent and changeable mid-flow.

Action: Offer control modes: "always ask", "ask once", or "auto".

🔍 Example: Auto-Ordering Assistant (Fictional)
Users could toggle autonomy from suggest → approve → auto-submit. Autonomy level is visible and changeable at any point.

### 7. Use memory responsibly (New)
Rule: Personalization should serve the task and not overreach into the user's data or behavior in unexpected ways.
Why it matters: When users don’t understand what an agent remembers or why, trust can be broken.
Design Implications:
- Make the agent’s memory transparent: what’s remembered, for how long, and why.
- Use memory only when it improves the experience—avoid unnecessary retention.

Action: Let users view, edit, reset agent memory.

🔍 Example: Fin by Intercom
Fin retains short-term issue history but limits persistent memory unless configured.

### 8. Surface what the agent can see (New)
Rule: Clarify the agent’s field of view. What it knows, what it has access to, and what it’s acting on.
Why it matters: Users often overestimate or misunderstand what agents can see. By surfacing the agent’s data sources and scope of access, you build understanding, trust, and better collaboration.
Design Implications:
- Visualize the agent’s inputs. What apps, files, or fields it's drawing from.
- Let users manage the agent’s access: toggle visibility, revoke sources, or set scopes.
- Consider showing a “field of view” preview: "The agent is currently looking at X, Y, and Z."

Action: Provide a visible data/context scope.

🔍 Example: Zapier Agents
Zapier shows connected apps and granted permissions during setup. Users explicitly authorize what the agent can access and can remove access at any time.

### 9. Coordinate between multiple agents (New)
Rule: In multi-agent systems, make collaboration flows and handoffs visible.
Why it matters: When multiple agents are involved, users can lose track of which agent is doing what.
Design Implications:
- Clearly label each agent’s role or function (e.g. Planner, Builder, Tester).
- Visualize task sequences or show handoff chains when multiple agents are involved.
- Log agent actions and decision points for transparency and troubleshooting.

Action: Create a timeline of agent actions. Would a user know who did what, and when?

🔍 Example: Devin (Cognition)
Devin breaks tasks into subprocesses, like test runner, fix recommender, and code generator. Users can see each step, making the agent chain legible and auditable.

### 10. Preview before you execute (Adapted)
Rule: Let users see what agents plan to do.
Why it matters: Previews offer a moment to course-correct, clarify intent, or catch mistakes. They also reinforce the feeling of collaboration, not automation happening behind the scenes.
Design Implications:
-Show previews or summaries before committing irreversible actions (e.g., send, deploy, delete).
-Use plain language and editable fields where possible.
-Consider offering a “preview mode” for more complex operations.

Action: What’s the last safe moment in your flow? 

🔍 Example: Linear for Agents
Before taking action (like opening a PR), Linear agents display a diff preview—giving users a clear, editable summary of what’s about to happen.

### 11. Align role, persona, and expectations (Adapted)
Rule: Match the agent’s tone, language, and capability to its intended role.
Why it matters: Users build mental models quickly. Clear, consistent role-setting helps users know what to expect, how much to rely on the agent, and when to step in.
Design Implications:
-Let users choose or preview the agent’s role: Advisor, Assistant, Executor, etc.
-Align tone and authority level with the agent’s actual capabilities and scope.
-Reaffirm the agent’s role through its responses, UI framing, and fallback behavior.

Action: Align tone and authority level with the agent’s actual capabilities and scope.

🔍 Example: Fin by Intercom
Fin presents itself as a helpful support assistant. Not an all-knowing agent. Its scope is clearly framed, and its tone remains helpful throughout.

### 12. Onboard the agent like a teammate (New)
Rule: Introduce agents the way you’d onboard a new team member.
Why it matters: A good onboarding experience builds confidence, reduces friction, and helps the agent and users collaborate on workflows faster.
Design Implications:
- Create onboarding flows that clearly explain the agent’s purpose, strengths, and limitations.
- Use examples and walkthroughs to show ideal tasks and interactions.
- Reaffirm these capabilities later—through tooltips, sidebars, or inline suggestions.

Action: Draft your agent’s first day. What would it show and say? 

🔍 Example: Zapier Agents
Zapier guides users through setting up each agent, clarifying the goals, connected tools, and what the agent is expected to handle, just like helping setup a new design hire on their first project.

### 13. Model and Expose Tradeoffs (New)
Rule: Show the reasoning behind the agent’s decisions; especially when tradeoffs are involved.
Why it matters: Agents can optimize for things users don’t see. Without transparency, these decisions could feel arbitrary. When users understand the why, they’re more likely to trust the outcome, or adjust it.
Design Implications:
- Use plain language to explain why the agent made a particular choice.
- Let users set optimization goals (e.g., speed vs quality, cost vs durability).
- Expose tradeoffs and alternatives when relevant, especially for a high-impact action.

Action: Highlight a moment where tradeoffs exist. Could the interface show why it chose this path? 

🔍 Example: Devin (Cognition)
When Devin selects a fix, it explains: “I chose this solution because it runs faster and fits your existing architecture.” This helps users understand the logic, and make adjustments if needed.

---

## 🧠 Why This Matters

Agentic systems are no longer speculative. They're already here. If we don’t design intentional patterns around delegation, memory, and autonomy, the market will define them by accident.

This framework helps teams build systems that users can:
- Confidently **delegate** and **collaborate** with
- Clearly **understand**
- And meaningfully **stay in the loop** with

---

## 🛠 Who This Is For

- Product builders making AI-driven tools
- PMs and founders designing agent-powered workflows
- Researchers exploring the future of human-agent collaboration

---

## ✨ Get Involved

This is an open framework. Feel free to fork, remix, challenge, or extend the ideas here.

Open an issue to suggest a new heuristic, submit a pull request with edits, or just reach out if you're working on similar problems.

---

## 🙏 Acknowledgments

Inspired by work from:
- [Tina He – The Race to Redesign Everything for Agents](https://every.to/thesis/the-race-is-on-to-redesign-everything-for-ai-agents)
- [Matthias Biilmann - Introducing AX: Why Agent Experience Matters ] (https://biilmann.blog/articles/introducing-ax/)
- [Agent Experience](https://agentexperience.ax)
- Zapier, Linear, Intercom, Cognition, Replit, and others building at the frontier

---

## 📬 Connect

Built by [@atippins](https://atippins.substack.com)  
Got thoughts? Edits? Suggestions? Critiques? [Open an issue](https://github.com/alantippins/agentic-ux-patterns/issues) or reach out.

---
