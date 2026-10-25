# AI Agents & n8n: Study Notes

## 1. Learning Checklist

- [ ] Explain what an AI agent is and why the term can be confusing.
- [ ] Describe the earlier definition of an AI agent.
- [ ] Explain the definition: an LLM controls the workflow.
- [ ] Explain the definition: an LLM runs tools in a loop to achieve a goal.
- [ ] Differentiate a fixed workflow from an agentic workflow.
- [ ] Explain what n8n does and why it is useful.
- [ ] Differentiate n8n Cloud from self-hosting.
- [ ] Explain Fair Code versus open-source software.
- [ ] Explain what you can and cannot do under n8n's described licensing model.
- [ ] Explain when white-label licensing may be relevant.
- [ ] Answer the important AI-agent interview questions without looking at the notes.

---

## 2. What Is an AI Agent?

The term *AI agent* has been used loosely, and different people have used different definitions. However, practitioners have increasingly adopted a more specific definition.

An earlier general definition described AI agents as AI systems that can independently do work for you. For example, you could ask an AI system to find a Chinese restaurant with a reservation available for three people at 9 p.m. that evening in New York. The system could independently open a browser, search for options, and perform actions on your behalf.

### Three Ways to Define an AI Agent

**1. Earlier definition: An AI system that works independently**
The AI performs work on your behalf instead of simply answering a question.

**2. Evolving definition: An LLM controls the workflow**
The Large Language Model (LLM) decides what should happen next based on the available possibilities, rather than relying entirely on a fixed sequence of coded steps.

**3. Practitioner's definition in the transcript: An LLM runs tools in a loop to achieve a goal**
The LLM can select tools, use their results, decide what to do next, and repeat the process until the goal is achieved or another stopping condition is reached.

> **Remember this interview definition:** An AI agent is an LLM-based system that runs tools in a loop to achieve a goal.

The third definition is the key one emphasized in the transcript for the course's main projects.

---

## 3. How Does an AI Agent Work?

The transcript emphasizes two important concepts: the LLM controls what happens next, and the LLM uses tools in a loop.

### Fixed Workflow vs. Agentic Workflow

**A. Fixed workflow**

1. Step A: Search data
2. Step B: Process data
3. Step C: Produce output

The developer defines the sequence in advance: do A, then B, then C.

**B. Agentic workflow**

- **Goal:** Complete the task
- The LLM decides which action to take:
  - Search tool
  - Calculator tool
  - Browser tool
  - Finish or retry
- Observe results → decide again → repeat

The LLM determines the next action using the task and the results of previous actions. It can repeat the tool-use cycle to work toward its goal.

> **An important distinction:** a fixed workflow can still contain AI. The key distinction in this transcript is whether the LLM controls the workflow and uses tools in a loop, rather than simply following a predetermined sequence.

---

## 4. Important AI-Agent Terminology

| Term | Meaning in simple words |
|---|---|
| **LLM** | A Large Language Model that processes language and generates responses or decisions. |
| **Workflow** | The sequence of steps used to complete a task. |
| **Orchestration** | Coordinating which step or action happens next. |
| **Tool** | A capability the AI can use, such as a browser, search function, or calculator. |
| **Tool calling** | The model requests that a tool perform an action. |
| **Loop** | A repeated cycle of selecting an action, using a tool, and processing its result. |
| **Goal** | The outcome the agent is trying to achieve. |
| **Agentic AI** | An AI system designed to act toward a goal with some autonomy. |

> **Interview memory trick:** Goal → Decide → Tool → Observe → Decide again → Finish.

---

## 5. What Is n8n?

n8n is compared with Zapier, an established automation service. The instructor highlights n8n's streamlined interface and its integrations with other tools, making it possible for both technical and non-technical users to build useful automations.

### Key Points from the Transcript

- It is a workflow automation platform.
- It was founded in Berlin in 2019, according to the transcript.
- It supports integrations and AI workflows.
- It provides a visual workflow-building experience.
- It can be used to build automations for your own business or for clients.
- The course uses n8n to build AI agents, including workflows with an AI Agent node and tools.

### Why Use n8n to Build AI Agents?

Imagine a business receives hundreds of customer support emails daily. An n8n workflow could be configured to:

1. Receive a new email.
2. Send its content to an LLM.
3. Let the model determine the appropriate next action.
4. Use a connected tool to retrieve relevant information or perform an action.
5. Return a response or route the request to a human when necessary.

This example illustrates how workflow automation and AI-agent capabilities can work together. The actual degree of autonomy depends on how the workflow is designed.

---

## 6. n8n Deployment and Licensing

The transcript distinguishes two main ways to run n8n and introduces a third option for embedding it in another product.

### Option 1: n8n Cloud

n8n hosts the software, and you access it online. The transcript describes a paid subscription after a trial period, with pricing dependent on the plan.

### Option 2: Self-Hosted n8n

You install and run the software on your own computer or a server you control. The transcript describes this as free to run under its licensing terms, although hosting infrastructure and maintenance can still cost money.

### Option 3: White-Label or Embedded Use

If you want to embed n8n within a product you own, the transcript says to contact n8n about the relevant commercial terms.

### Fair Code vs. Open Source

The instructor explains that n8n is **Fair Code**, not exactly open source.

According to the transcript, the licensing model allows users to download, run, and modify the software, build internal business automations, and deliver automation services to clients. However, it restricts directly competing with n8n by selling the product itself or offering a competing hosted platform.

| Activity | What the transcript says |
|---|---|
| Download and run n8n yourself | Allowed |
| Modify the software | Allowed under the stated terms |
| Build automations for your business | Allowed |
| Build automation projects for clients | Allowed |
| Sell n8n itself as a competing product | Not allowed under the described terms |
| Host a competing platform based on n8n | Restricted under the described terms |
| Embed n8n in your own commercial product | Contact n8n about commercial licensing |

> **Important:** These are the transcript's simplified descriptions, not a substitute for the current license. Check the official n8n licensing documentation before commercial deployment. The exact rights depend on the applicable license and use case.

---

## 7. Interview Preparation: Important Questions and Answers

### Q1. What is an AI agent?

An AI agent is an AI-based system that works toward a goal by making decisions and taking actions. In the practitioner's definition emphasized in this transcript, an LLM runs tools in a loop to achieve a goal, using the results of previous actions to decide what to do next.

**Why this matters:** It tests whether you understand the core concept instead of merely knowing the term.

### Q2. What is the difference between an AI chatbot and an AI agent?

A typical chatbot primarily responds to user messages. An AI agent can go further by selecting and using tools, observing their results, and taking additional actions toward a goal. A chatbot can also have agentic capabilities, so the distinction depends on its behavior and architecture.

**Why this matters:** Interviewers want to know whether you can distinguish conversation from action-oriented systems.

### Q3. What does it mean that an LLM controls the workflow?

It means the LLM helps determine which action should happen next based on the task, context, and available options. Instead of the developer specifying every step in a fixed sequence, the model can choose between possible next actions.

**Why this matters:** This tests your understanding of orchestration and decision-making.

### Q4. What does "an LLM runs tools in a loop to achieve a goal" mean?

The LLM selects a tool, the tool performs an action, and its output is returned to the system. The LLM then uses that output to decide whether to use another tool, repeat an action, or finish the task. This cycle continues until a stopping condition is reached.

**Why this matters:** This is the most direct test of the transcript's main definition of an AI agent.

### Q5. Is every AI-powered workflow an AI agent?

No. A workflow can use an LLM for a single step while the rest of the sequence remains predetermined. Under the stricter definition in the transcript, a true agentic system has the LLM running tools in a loop to achieve a goal.

**Why this matters:** It tests whether you can distinguish ordinary AI automation from agentic behavior.

### Q6. What is n8n, and how can it be used to build AI agents?

n8n is a workflow automation platform that connects applications, services, and AI components. Its visual workflows can connect an LLM with tools and other systems. An AI Agent node can be configured to use tools and execute a goal-oriented process.

**Why this matters:** It checks your practical understanding of the technology used in the course.

### Q7. What is the difference between a fixed workflow and an agentic workflow?

In a fixed workflow, the developer specifies the sequence of actions in advance. In an agentic workflow, the LLM has a role in deciding the next action based on the current context and results from previous steps.

**Why this matters:** This is a common design question when discussing workflow automation.

### Q8. What is the difference between n8n Cloud and self-hosted n8n?

With n8n Cloud, the provider hosts and maintains the platform as a service. With self-hosting, you run it on infrastructure you control and take responsibility for deployment, maintenance, and security. Their costs and operational responsibilities differ.

**Why this matters:** It tests your ability to choose an appropriate deployment approach.

### Q9. Is n8n open source?

The transcript describes n8n as Fair Code rather than traditional open-source software. Its license permits certain uses and modifications but imposes restrictions, particularly on competing with the n8n product. The exact permitted use should be verified against the current license.

**Why this matters:** It tests licensing awareness and your understanding of commercial constraints.

### Q10. When would you need a commercial or white-label agreement?

If I wanted to embed n8n within a commercial product I own, I would review the applicable license and contact n8n to determine whether a separate commercial agreement is required.

**Why this matters:** It tests whether you understand that building automations and redistributing or embedding the platform are different use cases.
