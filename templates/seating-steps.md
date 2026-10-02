# Client seating steps

**What you are seating:** the {{BUSINESS_NAME}} FAQ / support-lite agent  
**Prompt file:** [`prompts/faq-support-agent.md`](prompts/faq-support-agent.md)  
**Guardrails:** [`escalate-hard-stop-map.md`](escalate-hard-stop-map.md)  
**Done-when:** [`test-checklist.md`](test-checklist.md)

This pack sits on **your** LLM account. You pay that vendor. Crom Services does not take your API keys, does not host the agent, and does not run a token meter for this desk.

**Where this desk is seated:**
{{CHANNELS}}

---

## Before you paste

1. Name the workflow in one sentence (this pack: {{WORKFLOW}}).  
2. Open the destination on an account **you** control.  
3. Keep keys where they already live (vendor billing, password manager, company secret store). Do not send keys to Crom Services.  
4. Have the test checklist open in another tab so you can run it immediately after seating.

Do not add live job-status `/j/` links — this pack does not use them.

---

## ChatGPT (custom instructions, Project, or GPT)

1. Sign in to the ChatGPT account that will own the desk.  
2. Create a Project (or a Custom GPT if that is how your workspace works).  
3. Copy **only** the fenced system prompt from `prompts/faq-support-agent.md` into system / custom instructions.  
4. Paste the escalate + hard-stop map into the same Project files / knowledge, or keep it in the instruction footer as “follow the seated map”.  
5. Turn off browsing / extra tools unless you have a separate, paid reason. The desk must not invent live facts from the open web.  
6. Start a **new** chat in that Project. Send: `You are seated. Stay in the {{BUSINESS_NAME}} support desk. Ready for a customer message.`  
7. Run the happy / edge / refuse list in `test-checklist.md`.  
8. Billing stays on your OpenAI (or ChatGPT) plan. No Crom runtime.

---

## Claude (Project or custom instructions)

1. Sign in to the Claude account that will own the desk.  
2. Create a Project. Set the system / project instructions to the fenced prompt.  
3. Upload `escalate-hard-stop-map.md` as a project file if you want the table in-context; otherwise paste the decision order into the instructions.  
4. Do not upload customer exports or card data.  
5. New conversation in that Project. Send the same seated line as above.  
6. Run the test checklist.  
7. Billing stays on your Anthropic / Claude plan.

---

## Other LLM chat products (client keys)

1. Sign in to the vendor account that will own the desk.
2. Open custom instructions, a project/system prompt, or a pinned first message — whichever that product supports.
3. Paste `prompts/faq-support-agent.md` (and keep `escalate-hard-stop-map.md` handy for the human).
4. Run the happy / edge / refuse rows in `test-checklist.md` before go-live.
5. Billing stays on **your** LLM / vendor plan. Crom Services does not meter tokens for this pack.

## Other OpenAI-compatible or studio UIs

Same pattern:

1. System role = fenced prompt.  
2. Optional second file = escalate map.  
3. User tests = checklist rows, one turn each.  
4. API key = **yours**, in **your** secret store. Environment variable or vendor vault — never the repo, never a Crom inbox.

If the UI offers “share a public link”, keep the desk private to your workspace.

---

## After seating

- Walk the happy rows, then the edge and refuse rows. One fail = fix the instruction, do not “coach” the model in the customer thread.  
- One revision round in a paid pack means prompt + map + checklist edits, not a new product.  
- Staff handoff: escalate notes go to {{HANDOFF_CHANNEL}}, read during {{DESK_HOURS}} by:
{{ESCALATION_CONTACTS}}
- Do not add a Crom-hosted bot, a mailto CTA, or a fabricated `/j/` status token to go live.

---

## Not part of seating

- Crom Services logging into your accounts  
- Crom API keys as free runtime  
- Zendesk / Intercom build-out  
- 24/7 live chat staffing  
- Whole-company multi-agent programmes
