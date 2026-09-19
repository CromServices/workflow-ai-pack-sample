# Client seating steps

**What you are seating:** the Northline Supplies FAQ / support-lite agent  
**Prompt file:** [`prompts/faq-support-agent.md`](prompts/faq-support-agent.md)  
**Guardrails:** [`escalate-hard-stop-map.md`](escalate-hard-stop-map.md)  
**Done-when:** [`test-checklist.md`](test-checklist.md)

This pack sits on **your** ChatGPT, Claude, Grok, or similar account. You pay that vendor. Crom Services does not take your API keys, does not host the agent, and does not run a token meter for this desk.

---

## Before you paste

1. Name the workflow in one sentence (this sample is already named: order status / shipping / returns).  
2. Open the destination on an account **you** control.  
3. Keep keys where they already live (vendor billing, password manager, company secret store). Do not send keys to Crom Services.  
4. Have the test checklist open in another tab so you can run it immediately after seating.

If you are adapting the sample for a real desk, replace Northline names, postcodes, and policy numbers **before** staff use it. Do not add live job-status `/j/` links — this pack does not use them.

---

## ChatGPT (custom instructions, Project, or GPT)

1. Sign in to the ChatGPT account that will own the desk.  
2. Create a Project (or a Custom GPT if that is how your workspace works).  
3. Copy **only** the fenced system prompt from `prompts/faq-support-agent.md` into system / custom instructions.  
4. Paste the escalate + hard-stop map into the same Project files / knowledge, or keep it in the instruction footer as “follow the seated map”.  
5. Turn off browsing / extra tools unless you have a separate, paid reason. This sample desk must not invent live tracking from the open web.  
6. Start a **new** chat in that Project. Send: `You are seated. Stay in the Northline Supplies support desk. Ready for a customer message.`  
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

## Grok (custom instructions or a pinned first message)

1. Sign in to the xAI / Grok account that will own the desk.  
2. Put the fenced system prompt in custom instructions. If the product has no instruction field, pin the prompt as the first message and start each shift with the seated line.  
3. Paste or attach the escalate map in the same place.  
4. Disable live search if it would fetch carrier pages this sample does not authorise.  
5. Run the test checklist.  
6. Billing stays on your Grok / xAI plan.

---

## Other OpenAI-compatible or studio UIs

Same pattern:

1. System role = fenced prompt.  
2. Optional second file = escalate map.  
3. User tests = checklist rows, one turn each.  
4. API key = **yours**, in **your** secret store. Environment variable or vendor vault — never the repo, never a Crom inbox.

If the UI offers “share a public link”, keep the sample private to your workspace. This repo is the public sample; your seated copy is not.

---

## After seating

- Walk H1–H6, then the edge and refuse rows. One fail = fix the instruction, do not “coach” the model in the customer thread.  
- One revision round in a paid pack means prompt + map + checklist edits, not a new product.  
- Staff handoff: who reads escalate notes, during which AEST hours, on which **client** channel (inbox, Slack, ticket tool you already pay for).  
- Do not add a Crom-hosted bot, a mailto CTA, or a fabricated `/j/` status token to go live.

---

## Not part of seating

- Crom Services logging into your accounts  
- Crom API keys as free runtime  
- Zendesk / Intercom build-out  
- 24/7 live chat staffing  
- Whole-company multi-agent programmes
