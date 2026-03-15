# Chapter 7: Open Your Terminal

> "The way to get started is to quit talking and begin doing."
> — Walt Disney

Close your other tabs. Open your terminal. In 30 minutes you will have your first AI company running.

Not a demo. Not a thought experiment. Running, with agents, tasks, and a dashboard you can watch in real time.

## What You Need

Two things:

**Node.js (version 18 or higher).** Check by typing:

```
node --version
```

If you see 18, 20, or higher, move on. If not, install the latest LTS version from nodejs.org. Two minutes.

**A terminal.** On macOS: Terminal or iTerm2. On Windows: PowerShell or Windows Terminal. On Linux: whatever you already use. If you can type a command and press Enter, you have every skill this chapter requires.

No Docker. No cloud accounts. No API keys. No credit card.

## Step 1: Install Paperclip

```
npx paperclipai onboard --yes
```

One command. It downloads Paperclip, sets up an embedded Postgres database, creates the directory structure, and launches the platform. The `--yes` flag accepts defaults, exactly right for a first run.

Setup takes one to three minutes depending on your connection. When it finishes, you see a local URL, usually `http://localhost:3000`.

Open it. That is your Paperclip dashboard, the operating system for your AI company.

## Step 2: Name Your Company

The dashboard prompts you to create a company. Three fields matter:

**Name.** Pick something real. "Acme Content" works, but "Adams Media Group" works better. You will treat it differently when it carries a name you would put on a business card.

**Description.** One or two sentences. "Produces SEO-optimized blog content for the personal finance niche" beats "testing AI stuff." Specificity shapes how you design agents and assign work.

**Goals.** What does this company exist to do? "Publish 4 high-quality blog posts per week" or "Process and respond to customer inquiries within 2 hours." Goals cascade to your agents. Make them concrete and measurable.

Click create. Your company now has a dashboard, a task board, a budget tracker, and an empty org chart. Time to hire.

## Step 3: Hire an Agent

Navigate to Agents and create a new one.

**Name and role.** Give it a name and title. "Alex, Content Writer" or "Morgan, Research Analyst." The name is cosmetic. The role description matters. Write it like a job posting: "Writes 1,000-1,500 word blog articles on personal finance topics. Follows SEO best practices. Produces clear, engaging prose for a general adult audience."

**Runtime.** This tells Paperclip what kind of agent to build:
- Claude users: select the Claude Code runtime
- Preferred API: configure a custom HTTP agent
- Simplest option: a bash script agent for basic automated tasks

You can change the runtime later. Pick one and move on.

**Budget.** Set a monthly cap. $50 is enough to experiment without worry.

**Heartbeat.** How often should the agent check for work? Content writer: daily. Customer service: hourly. Weekly report generator: weekly. Match cadence to the work.

Click create. Your first employee is hired. No interview. No offer letter. No two-week notice from a previous job.

## Step 4: Assign Work

Go to the task board. Create a task. Assign it to your agent.

Keep the first one simple and specific:

- **Content company:** "Write a 1,200-word blog post about the top 5 budgeting strategies for freelancers. Include an introduction, five clearly defined strategies with explanations, and a conclusion. Optimize for the keyword 'budgeting tips for freelancers.'"

- **Research company:** "Compile a competitive analysis of the top 5 project management tools for small teams. For each tool, include pricing, key features, pros, cons, and target user. Present in a structured format."

- **E-commerce:** "Write product descriptions for the following 10 items [list items]. Each description should be 100-150 words, highlight key benefits, and include a clear call to action."

Notice the specificity. AI agents, like human employees, do better work with clear briefs. "Write something about budgeting" produces mush. The brief above produces something you might publish.

Submit the task. If the heartbeat is due, the agent picks it up. Otherwise, trigger a manual run.

Watch the task thread as the agent works. Every step in the chain of reasoning logs to the conversation thread, the transparency from Chapter 5, in action.

## Step 5: Read the Thread, Not Just the Output

When your agent finishes, resist the urge to skip straight to the deliverable. Study the task thread. That is where you learn.

**In the thread, look for:**
- How the agent interpreted your brief
- What steps it took
- Decisions you did not expect
- How much budget the task consumed

**In the output, ask:**
- Would you publish this, send it to a client, or act on it?
- Where does it fall short? "Not good" tells you nothing. Be specific.
- What would you change in the brief next time?

This first task calibrates your expectations as much as it produces work. You are learning what your agent can do, how it reasons, and what instructions yield the best results. Every task that follows will be sharper for it.

## Five Minutes with the Dashboard

Company, agent, completed task. Now explore.

**Company overview.** Name, description, goals, high-level metrics: agent count, active tasks, completed tasks, total spend.

**Org chart.** Just one agent for now. Hierarchy, roles, and reporting lines appear here as you grow.

**Task board.** All tasks: pending, in progress, completed, blocked. Each carries a conversation thread, assigned agent, and status. This is your command center.

**Budget tracking.** Per-agent spending, monthly totals, utilization percentages. Green means healthy, yellow means approaching limits, red means paused.

**Audit logs.** The immutable record of everything that has happened. Every agent action, every decision, every tool call. When you need to know why something happened, look here.

## Common Stumbling Blocks

**"Command not found" on npx.** Node.js is not installed or is not in your PATH. Reinstall from nodejs.org and check the box that adds it to your system PATH.

**Port already in use.** Something else occupies port 3000. Stop the other service or configure a different port.

**Agent ignores a new task.** Check the heartbeat schedule. If you set it to daily and just created the task, the agent will not run until tomorrow. Trigger a manual run.

**Weak output.** Almost always a briefing problem, not an agent problem. Make descriptions more specific. Include examples of good output. Set clear constraints on length, format, and tone.

**Budget draining fast.** Check the model tier. Opus-class models cost far more per token than Haiku-class. For most tasks, Sonnet-class gives the best balance of quality and cost.

## What Happened in 30 Minutes

You installed an AI company operating system. Created a company with a name, a description, and goals. Hired an AI employee with a role, a budget, and a schedule. Assigned work, watched it execute, and reviewed the output. You have a dashboard showing operations, finances, and an audit trail.

Most people think this is years away. You just did it over coffee.

By tonight, this agent could produce work on a daily schedule. By week's end, three or four agents covering different functions. By month's end, a fully operational company producing real output.

But scattered agents running tasks are not a company. They are a sandbox. Building something real means thinking like a CEO: defining roles, designing hierarchy, creating delegation flows, building an organization that runs without you.

That is the next chapter.
