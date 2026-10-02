# Workflow Agent Pack: open sample

Openable sample pack from **Crom Services**. FAQ / support lite. One business workflow, not a whole-company AI programme.

## What it is

We seat specialist agents for one workflow on your tools: rules, escalate map, test checklist, handoff. You pay your own LLM/runtime.

This repo is a **finished pack you can open**, not only a shape note. The filled sample uses a fictional Australian small business (**Northline Supplies**). No live client data.

| Artefact | What it is |
| --- | --- |
| [prompts/faq-support-agent.md](prompts/faq-support-agent.md) | Specialist system prompt for one desk: order status, shipping, and returns FAQ. Paste-ready. |
| [escalate-hard-stop-map.md](escalate-hard-stop-map.md) | When to hand off to a human, and absolute refuses. |
| [test-checklist.md](test-checklist.md) | Happy / edge / refuse rows to run after seating. |
| [seating-steps.md](seating-steps.md) | How to paste and run on ChatGPT, Claude, or other LLM tools with **your** keys. |
| [pack.config.json](pack.config.json) | The sample's settings: business name, workflow, channels, escalation contacts, refuse list. |
| [templates/](templates/) | Placeholder versions of the four artefacts, for a new job. |

Placeholder company and sample order rows only. No personal names. No live job-status `/j/` tokens.

### In

- One named workflow (FAQ/support, lead follow-up, ops digest, or similar)
- 2–4 specialist prompts **or** a single FAQ/support agent pack (this sample is the single-desk shape)
- Hard stops + escalate map + test pack (happy / edge / refuse)
- Seating steps on **client** ChatGPT, Claude, or other LLM keys
- One revision round

### Out

- Crom Services bots/computer access; our API keys as free runtime
- Whole-company AI transformation
- Live chat staffing, Zendesk/KB programmes, workshops, MVP platforms
- Hosting or running the agent for you after handoff

### Runtime / keys

Client tools and client keys only. Crom Services builds and seats the pack; it does not host the agent or meter tokens.

## What it proves

- One workflow can be fenced: the agent answers from the pack, hands off, or refuses. There is no fourth path.
- The guardrails are written down and testable: every escalate and refuse rule has a matching row in the test checklist.
- It runs on the client's own tools and keys, with nothing hosted by us.
- It is reusable: the same pack shape is re-filled for a new business from one config file (see below).

## Live link

There is no hosted app: this pack is markdown you paste into your own LLM tool. Try it like this:

1. Open [seating-steps.md](seating-steps.md) and sit the prompt on an account you control.
2. Paste the fenced system prompt from [prompts/faq-support-agent.md](prompts/faq-support-agent.md).
3. Keep [escalate-hard-stop-map.md](escalate-hard-stop-map.md) next to the model.
4. Tick [test-checklist.md](test-checklist.md) (happy / edge / refuse).

Other packs: https://cromservices.github.io/job-page-sample/packs/

## Reuse for a new job

The Northline files at the repo root are the **filled sample**. [`templates/`](templates/) holds the same four artefacts with `{{TOKEN}}` placeholders.

1. **Copy the templates.** Copy everything in `templates/` (keeping `prompts/`) and `pack.config.json` into a new folder or repo for the job.
2. **Edit `pack.config.json`.** Replace the Northline values with the client's: business name, workflow, channels, escalation contacts, refuse list, hours, lookup fields and sample records.
3. **Replace the tokens.** Each `{{TOKEN}}` is the upper-case form of a config key (`business_name` → `{{BUSINESS_NAME}}`). Text values go in as written. List values go in one item per line, as `- ` bullets (or as table rows where the template shows a table).
4. **Fill the job-specific rows.** `<FILL: ...>` lines are prompts to write job-specific content (policy facts, happy-path tests, workflow-specific escalates). Use the Northline files as the worked example.
5. **Check nothing is left.** `grep -rn --exclude=README.md -e '{{' -e '<FILL' .` should print nothing. Then run the test checklist on the client's tool before go-live.

### Client checklist (paid seating)

1. Name the one workflow (one sentence)
2. Which client accounts/tools hold the agents
3. Where secrets live (you keep the keys)
4. Done-when test (happy / edge / refuse)

---

[Crom Services, Australia](https://cromservices.com.au)
