# Chapter 6: Do the Math

> "Beware of little expenses; a small leak will sink a great ship."
> — Benjamin Franklin

The average US employee costs $85,000 a year in salary. But salary is just the start. Add health insurance ($7,000–$15,000), payroll taxes (7.65%), retirement contributions, paid time off, equipment, software licenses, office space, management overhead, HR, training, and the expense nobody budgets for (turnover, at 50–200% of annual salary per departure) and the real cost lands between $120,000 and $170,000 per person per year.

An AI agent on Paperclip costs $50 to $500 a month.

That gap is not a marginal improvement. It is a structural shift. If you are deciding between hiring your first employee and building your first AI org chart, this chapter is where you make the call.

## What One Employee Actually Costs

Most founders think in salary. The real number runs 1.4 to 2x that.

**Direct compensation.** Salary, bonuses, commissions, the number in the job posting.

**Benefits.** Health insurance alone averages $7,911 for individual coverage and $22,463 for family coverage per year (2024 Kaiser Family Foundation data). Add dental, vision, life insurance, and disability.

**Payroll taxes.** Social Security (6.2%), Medicare (1.45%), federal and state unemployment. You pay these on top of salary. They are not deducted from it.

**Retirement.** A competitive 401(k) match costs 3–6% of salary.

**Paid time off.** The average US worker gets 10 vacation days, 8 sick days, and 7–10 paid holidays, roughly 5–6 weeks of pay for zero output. On an $85,000 salary, that is about $8,000 in paid non-productivity.

**Equipment and software.** Laptop, monitor, phone, desk, licenses. Budget $3,000–$5,000 per employee per year.

**Office space.** Average cost per employee: $12,000–$18,000 per year in a mid-tier US city. Much more in San Francisco, New York, or Los Angeles.

**Management overhead.** Every employee needs managing. The standard ratio is one manager per 5–8 direct reports. That manager's time and salary spread across the team.

**HR and administration.** Payroll, compliance, hiring, onboarding, performance reviews, conflict resolution, offboarding. Either you do it (and your time has a cost) or you hire HR, which means more employees.

**Training.** New employees take 3–6 months to reach full productivity. During ramp-up, you pay full price for partial output.

**Turnover.** The average US voluntary turnover rate runs about 25% annually. When someone leaves, you lose institutional knowledge, spend months hiring, and restart the training cycle. Estimated cost: 50–200% of the role's annual salary.

Add it up. An $85,000 employee really costs $120,000–$170,000. A five-person team runs $600,000–$850,000 a year before anyone ships a thing.

## What One Agent Costs

AI agent costs come from three sources.

**API calls.** This is the main expense. Every time an agent uses a model, to write, analyze, decide, or communicate, it makes an API call priced by token count (roughly, word count). Current pricing for capable models:
- Fast, good-enough work (Claude Haiku-class): $0.25–$1.25 per million tokens
- High-quality work (Claude Sonnet-class): $3–$15 per million tokens
- Premium, complex reasoning (Claude Opus-class): $15–$75 per million tokens

A million tokens is roughly 750,000 words, about ten novels. A typical business task (writing an article, analyzing data, summarizing research) uses 2,000–10,000 tokens. That is fractions of a cent to a few cents per task at the lower tiers.

**Compute and hosting.** Paperclip runs locally with an embedded Postgres database. On your own machine, the incremental cost is zero. You use hardware you already own. For 24/7 availability on a cloud server, budget $20–$100 a month.

**Third-party tools.** If your agents need paid APIs (email services, data providers, marketing platforms) those costs exist. But you would pay them with human employees too.

**Realistic monthly costs by workload:**
- Light agent (a few tasks per day): $20–$50/month
- Moderate agent (steady daily work): $50–$200/month
- Heavy agent (continuous, complex work): $200–$500/month

## $427,000 vs. $6,600

A concrete comparison. Take a small content marketing operation, the kind thousands of founders run right now.

**Traditional Team (5 employees):**
| Role | Salary | Fully Loaded |
|------|--------|-------------|
| Content Writer #1 | $55,000 | $77,000 |
| Content Writer #2 | $55,000 | $77,000 |
| Editor | $65,000 | $91,000 |
| SEO Specialist | $60,000 | $84,000 |
| Project Manager | $70,000 | $98,000 |
| **Total** | **$305,000** | **$427,000/year** |

**Paperclip AI Company:**
| Agent Role | Model Tier | Monthly Cost |
|-----------|-----------|-------------|
| Writing Agent #1 | Sonnet-class | $150 |
| Writing Agent #2 | Sonnet-class | $150 |
| Editing Agent | Sonnet-class | $100 |
| SEO Agent | Haiku-class | $50 |
| Project Coordination Agent | Haiku-class | $50 |
| Hosting (VPS) | — | $50 |
| **Total** | | **$550/month = $6,600/year** |

$427,000 versus $6,600. A **98.5% cost reduction.**

This comparison is not perfectly apples-to-apples. The human team brings judgment, relationships, and creative instincts that current AI agents cannot replicate. The AI team requires your oversight, and your time has value. Some tasks will always need a human writer.

But for the bulk of content marketing (blog posts, SEO articles, social media, email newsletters) the AI team produces comparable output at a fraction of the cost. The quality gap narrows every quarter.

The question is not whether AI matches humans at everything. It is whether AI handles enough tasks well enough to justify the shift. For a growing number of business functions, it does.

## 8,760 Hours a Year

One cost dimension never appears in salary comparisons: time.

A human employee works roughly 2,000 hours a year. Subtract meetings, email, lunch, and context-switching. Productivity studies show most knowledge workers produce 3–4 hours of actual output per day, and you get 750–1,000 productive hours per year.

A Paperclip agent with heartbeat scheduling works 24 hours a day, 365 days a year: 8,760 hours. At a conservative 80% utilization (accounting for task queuing, processing time, and idle periods), that is about 7,000 productive hours.

One AI agent produces 7–9x the productive hours of one human employee. You can run many agents at once.

This is not about AI being "better" than humans. It is an asymmetry in available time. When your competitors' employees go home at 5 PM, your AI company keeps running. Weekends, holidays, sick days. Your agents do not stop.

Over a year, that compounds into an enormous operational gap.

## Flat Marginal Cost

Traditional companies face a hard truth: scaling requires more people, which means more cost, more management, more complexity, and often less efficiency. Going from 5 employees to 50 does not cost 10x more. It costs 12–15x more. You need middle management, HR, bigger offices, and the communication overhead that grows exponentially with team size.

AI companies scale in the opposite direction. Adding an agent to your Paperclip org chart costs $50–$500 a month, the same whether you have 3 agents or 30. No management overhead. No benefits. No ramp-up time. No office expansion. The marginal cost of growth stays nearly flat.

This is why AI-native startups require 22% less capital than traditional startups, according to recent industry data. Not just cheaper to start, but dramatically cheaper to grow.

And this is the math behind Altman's one-person billion-dollar company. One person does not do the work of a thousand. One person orchestrates AI agents whose costs scale linearly while output scales exponentially. Those margins drive valuations into the stratosphere.

## Budget Controls in Paperclip

Cheap and controlled are not the same thing. The most common fear about AI agents is not that they will fail. It is that they will work too hard and run up huge API bills.

Paperclip addresses this directly.

**Per-agent monthly budgets.** Every agent has a hard spending cap. Not a guideline, a limit.

**Soft warnings at 80%.** When an agent hits 80% of its budget, you get notified. Time to decide: increase the budget, reduce the workload, or let it hit the cap and pause.

**Automatic pause at 100%.** When an agent exhausts its budget, it stops. No exceptions. No surprises. No runaway costs. It pauses until the next cycle or until you increase the allocation.

**Granular cost tracking.** Spending by agent, by task, by project, across the entire company. You can spot problems fast. Maybe your writing agents are cost-effective but your research agent burns budget on unnecessary depth.

This gives you better financial visibility than most companies have over their human workforce. Ask any manager what a specific employee cost to produce a specific deliverable, and you will get a blank stare. Paperclip tells you exactly, down to the penny.

## Where Humans Still Win

AI does not replace humans in every function. Not yet, and perhaps not ever in some areas.

**High-stakes relationships.** Closing a $500,000 deal, managing a key partnership, handling a customer crisis. These demand emotional intelligence, rapport, and judgment under pressure that AI does not reliably provide.

**Original creative work.** AI produces strong content within established patterns. It struggles with truly original vision, the kind that defines a brand, launches a cultural moment, or creates something the market has never seen.

**Strategic judgment.** AI can analyze data and present options. It cannot feel the market, read between the lines of a competitor's move, or make the gut calls that experienced founders make from years of pattern recognition.

**Ethical navigation.** When the right decision is ambiguous, when values conflict, stakeholders disagree, or the legal answer and the moral answer diverge, you want a human making that call.

The smartest approach for many founders: AI agents handle the 80–90% of work that is systematic, repeatable, and scalable. You spend your energy on the 10–20% where humans are irreplaceable.

Even in a "zero-employee" company, one employee matters enormously: you. The economics of zero are not about eliminating human judgment. They are about making it more valuable by freeing it from everything that does not require it.

## Estimating Your Costs

Before Part III, where you build your company, a quick framework:

1. List the roles you would hire for a traditional team
2. Estimate fully loaded cost (salary x 1.4 minimum)
3. Identify which roles AI agents could handle (most operational, analytical, and content roles qualify)
4. Estimate agent costs: light ($30/mo), moderate ($150/mo), heavy ($350/mo)
5. Add hosting ($50/mo) and third-party API costs
6. Compare the totals

For most small business operations, savings run 90–98%. Even conservative estimates show 80%+ reduction.

The economics are clear. The tools are free. Let's build.
