# gohighlevel ai chatbot cost: what's included, what stacks on top, and how to price it per client

Ask five GoHighLevel users what their AI chatbot costs and you'll get five answers. One says $50. One says $97. Someone else says "$0, I'm on pay-per-use." Another one starts talking about cents per minute. Everyone is technically right, which is exactly why this question is hard to answer with a single number.

The cost isn't one line item. It's a stack, and the stack has a specific shape: a platform subscription, an AI fee that gets charged **per enabled sub-account**, and then a layer of usage charges that don't care what plan you bought. Get the order wrong when you're pricing a client and you'll quote $97 for something that bills out at $400.

Here's how the layers actually work, where the numbers come from, and how third-party options like CloseBot change the math.

## The three layers of a GoHighLevel AI chatbot bill

**Layer 1: the platform.** HighLevel's own plans run $97 (Starter, 3 sub-accounts), $297 (Unlimited sub-accounts) and $497 (Agency Pro, with SaaS Mode). You pay this regardless of whether you ever switch an AI feature on.

**Layer 2: AI Employee, billed per location.** This is the part people miss. HighLevel's AI subscription isn't priced per agency. It's priced per sub-account that has AI enabled. If you run 10 client locations on AI Employee Unlimited, that's 10 × $97 before your own subscription even shows up on the invoice.

**Layer 3: usage that sits outside the plan.** Phone system minutes, SMS, Agent Studio, WhatsApp, A2P registration. "Unlimited" applies to specific AI products, not to your whole bill.

Once you separate these, the confusion mostly disappears. A $97 AI plan on a $297 platform plan with 10 active locations isn't $394. It's $1,267, and that's before anyone texts anybody.

## What HighLevel charges for its own AI chatbot

HighLevel documents three ways to pay for AI, all per enabled location. Prices below are from HighLevel's published AI product pricing documentation.

| AI plan | Monthly fee per location | What's included | What's still metered |
| --- | --- | --- | --- |
| Pay-Per-Use | $0 | Access to supported AI products, billed only when something runs | Conversation AI tokens, Voice AI components, Agent Studio, web searches, phone system |
| AI Employee Growth | $50 | 1,000 Conversation AI responses, 100 Voice AI minutes, unlimited Reviews AI and Content AI | Overages, Agent Studio, phone system, messaging |
| AI Employee Unlimited | $97 | Unlimited Conversation AI and Voice AI, unlimited Reviews AI and Content AI, 3× Ask AI and AI Studio usage | Agent Studio, phone system, messaging |

The word "unlimited" is doing a lot of work in that third row, and HighLevel attaches a fair-use policy to it: the company reserves the right to throttle, limit or require an upgrade if usage is judged excessive. Read that before you promise a client a flat rate.

### Conversation AI is billed in tokens, not messages

Under pay-per-use, Conversation AI charges are calculated from token consumption — input tokens for what gets sent to the model (customer messages, conversation history, instructions, knowledge base content) and output tokens for what the model writes back. HighLevel publishes the current model rates:

- GPT-5: $1.25 per 1M input tokens, $10.00 per 1M output tokens
- GPT-5 Mini: $0.25 / $2.00
- GPT-4.1: $2.00 / $8.00
- GPT-4.1 Mini: $0.40 / $1.60

HighLevel's own worked example: a conversation using 100,000 input tokens and 25,000 output tokens on GPT-5 works out to roughly $0.375. Swap in GPT-5 Mini and that same conversation lands closer to $0.075. The model you pick moves your bill more than almost any other setting, and two conversations of identical length can cost different amounts for the same reason.

### Voice AI adds a per-minute floor

Pay-per-use voice pricing splits into three parts: a voice engine charge, a text-to-speech charge, and the language model's token cost. The voice engine is currently listed at $0.045 per minute, OpenAI and Cartesia TTS at $0.015 per minute — so about $0.06 per minute before tokens and telephony. ElevenLabs V2.5 pushes that base to $0.08 per minute, and ElevenLabs V3 to $0.215. Speech-to-speech models are quoted flat: $0.10 per minute for Gemini 3.1 Flash Live and $0.20 for OpenAI GPT Realtime.

Run a 10-minute call on OpenAI TTS and the AI voice portion is roughly $0.60, before tokens and before the phone system, which bills separately on every plan.

> Agent Studio is not included in any AI Employee plan. It stays pay-per-use whether you're on Pay-Per-Use, Growth, or Unlimited. Web searches through it are listed at $0.01 each.

## Two agencies, same "unlimited" plan, very different invoices

**Agency A** runs 10 client locations, all on AI Employee Unlimited, on the $297 platform plan. Recurring software cost: $297 + (10 × $97) = **$1,267/month**, before a single SMS or call. Ten of those locations is $970 in AI fees alone — more than three times the platform subscription the agency thinks of as "its bill."

**Agency B** runs three locations with light lead volume and leaves them on pay-per-use. At a few hundred Conversation AI responses a month on a cheaper model, the AI line item stays in the low double digits, and there's no AI subscription at all.

Both agencies are making a defensible choice. The trap is quoting a client as if you're Agency B when your configuration behaves like Agency A.

If you're doing this math for clients and starting to feel like the per-location fee gets steep, that's the point where most agencies start comparing third-party AI layers. 👉 [See how CloseBot's plans price out against per-location AI fees](https://app.closebot.com/a?fpr=li87) — the plans below show why.

## Why per-location pricing gets awkward as you grow

There's nothing underhanded about charging per enabled location. HighLevel's AI operates inside each sub-account, and every location that uses it consumes compute. The problem is the shape of the curve.

Your platform subscription is largely flat once you're on the Unlimited tier. Your AI cost is linear and uncapped in the sense that every new client adds another $50 or $97 to the recurring total. An agency with 40 locations on AI Employee Unlimited is looking at $3,880/month in AI fees alone. Rebill it with a markup and it's revenue, so the model isn't broken — but it does mean your margin depends entirely on what you can charge per client, and your floor rises every time you sign someone.

HighLevel does support rebilling AI usage to locations, though the documentation notes AI Employee rebilling requires the $497/month Agency Pro plan. Worth checking before you build a client offer around it and assume the $297 plan covers you.

## Where CloseBot changes the cost model

CloseBot is a conversational AI platform built for lead qualification and appointment booking, designed to run inside a CRM rather than replace it. It connects natively with HighLevel and HubSpot and also works with Salesforce and Podio, then takes over the text conversations already flowing through that CRM.

The relevant difference for this article is structural, not a feature list: **CloseBot does not charge per connected sub-account.** Its plans scale on job flows, messages and seats instead. For an agency whose whole business is client locations, that's a different cost curve — one that doesn't add $50 or $97 every time you onboard someone.

Two things worth knowing before you put numbers on a client proposal, because CloseBot's own documentation isn't fully consistent:

- The plans page FAQ states agency accounts are billed a flat $0.012 per message that can be rebilled. The help center article on plans lists **$0.006** per message for agency accounts. The two pages disagree — confirm the live rate in your account before you build margin assumptions on it.
- Older V2 documentation says customers bring their own AI provider API keys and cover token costs directly. The current plans page FAQ says the opposite for security reasons ("bring your own key" isn't allowed) and that business plans have no additional per-message cost. The token-cost question has clearly changed at least once, so verify which model applies to the plan you're buying.

That second point matters more than it sounds. "Included message costs" and "you also pay OpenAI" are very different monthly outcomes at 20,000 messages.

## CloseBot's full plan lineup

Everything below is from CloseBot's plans page and its plans documentation. Prices are in USD.

| Plan | Core configuration | Price | Billing | Buy |
| --- | --- | --- | --- | --- |
| Free | 1 agent, 1 user seat, 100 messages/month, 1 MB storage, unlimited account connections, 1 job flow | $0 | Always free | [Start on the CloseBot free plan](https://app.closebot.com/register?fpr=li87) |
| Business — 1 job flow | 1 job flow, 500 messages/month included, 15+ templates, human support | $64/month | Monthly, or $53/month billed as $640/year | [View the CloseBot Business plan](https://app.closebot.com/settings?tab=subscription&plan=business&toggle=monthly&fpr=li87) |
| Business — 3 job flows | 3 job flows, 500 messages/month included, all paid features unlocked | $197/month | Monthly | [Compare the 3-job-flow Business tier](https://app.closebot.com/settings?tab=subscription&plan=business&toggle=monthly&fpr=li87) |
| Business — 10 job flows | 10 job flows, 500 messages/month included | $297/month | Monthly | [Check the 10-job-flow tier](https://app.closebot.com/settings?tab=subscription&plan=business&toggle=monthly&fpr=li87) |
| Business — unlimited job flows | Unlimited job flows, 500 messages/month included | $397/month | Monthly | [See the unlimited Business plan](https://app.closebot.com/settings?tab=subscription&plan=business&toggle=monthly&fpr=li87) |
| Agency | Unlimited agents across unlimited sources, white-label client portal, rebill all costs, client seats | $397/month | Monthly, roughly $331/month equivalent on annual billing | [Review the CloseBot Agency plan](https://app.closebot.com/settings?tab=subscription&plan=agency&toggle=monthly&fpr=li87) |
| Growth | 50+ templates, HIPAA compliance, quarterly audits, 99.99% priority uptime, priority support | Custom quote | Custom | [Request CloseBot Growth pricing](https://app.closebot.com/a?fpr=li87) |

Add-ons apply on paid plans: extra user seats are $5 each, and knowledge library storage beyond the included 1 MB runs $0.10–$3.00 per MB per month on business plans depending on volume, or $0.006 per MB per day on agency plans. Business plans also let you raise your monthly message ceiling, which lowers your effective per-message cost as volume grows. The free plan's ceiling is hard at 100 messages, with overage at $0.08 per message if you go past it.

Two commercial details that affect your planning: CloseBot states plainly that there are **no refunds**, and instead offers a free-forever plan under 100 messages plus a 7-day trial of any paid plan before billing starts. Plans run month to month.

## Native HighLevel AI versus CloseBot: which bill is smaller

The honest answer depends on volume, not on brand loyalty.

| Question | HighLevel native AI | CloseBot |
| --- | --- | --- |
| Entry cost | $0 on pay-per-use, $50 Growth, $97 Unlimited — per location | $0 free plan, $64/month business entry |
| Cost as locations grow | Adds $50 or $97 per enabled sub-account | No per-connected-account fee; scales on job flows, messages, seats |
| 10 client locations | $500–$970/month in AI fees alone | Covered by a single business or agency subscription |
| Very low volume | Pay-per-use can be cheapest available option | $64/month floor once you're past the free tier |
| Message costs | Token-based under pay-per-use; included on the subscription tiers | Included on paid business plans up to the ceiling; rebillable per-message usage on agency |
| Voice | Included in Growth allowances and Unlimited; pay-per-use components otherwise | Text-focused; not a voice product |
| Rebilling | AI Employee rebilling requires the $497 Agency Pro plan | Built into the $397 Agency plan |

The pattern: HighLevel's native AI wins on cost at very low volume, especially if you're a single business with one location and no plans to resell anything. Its pay-per-use tier genuinely can be cheaper than a CloseBot subscription when you're handling a few hundred messages a month.

Flip the volume up and the comparison inverts. CloseBot's own cost breakdown for a 102-location account put the total around $809/month including base plan, message costs, storage and provider tokens, against $9,894 for the same footprint on HighLevel's AI Employee Unlimited. CloseBot published that comparison itself, and the GHL suite does more than appointment setting, so it isn't a like-for-like feature count — but the $97-per-location math is HighLevel's own published rate, and it does compound the way the table above suggests.

For a single high-volume business rather than an agency, the crossover is less dramatic. The question becomes whether the appointment-setting quality gap justifies a $64–$397 subscription on top of the platform you already pay for.

CloseBot's G2 listing shows a 4.8 rating, and its own site cites 175+ reviews. Its platform stats include over 1M booked appointments, roughly 150,000 daily messages, and 1,000+ agencies — all vendor-reported figures, so treat them as marketing until you've tested it yourself. On the minus side, reviewers consistently flag the learning curve and the fact that conversation quality depends heavily on how well you build and maintain the knowledge base. One G2 reviewer summed up the risk plainly: sloppy follow-up logic just gets scaled faster.

## Charges that stack on both

Whoever runs your chatbot, these don't disappear:

1. **Your CRM platform.** HighLevel at $97, $297 or $497, or HubSpot on its own pricing.
2. **Phone numbers and call minutes.** Billed separately through LC Phone or Twilio, even when Voice AI itself is "unlimited."
3. **SMS and messaging delivery.** Conversation AI generating a reply doesn't mean the text is free.
4. **WhatsApp.** HighLevel currently lists the integration at $10 per month per enabled sub-account, plus usage.
5. **A2P 10DLC registration** for US business messaging.
6. **Agent Studio** on HighLevel, pay-per-use on every plan.
7. **Setup and maintenance labour** — the line nobody quotes, and usually the biggest one in month one. One published review of CloseBot estimates 5 to 10 hours of initial configuration to build knowledge bases and connect webhooks.

## How to estimate your own number in 10 minutes

Work through it in this order and you'll land within spitting distance of your real bill.

1. **Count enabled locations, not clients.** Only sub-accounts with AI switched on count for HighLevel's AI fee.
2. **Estimate monthly messages per location.** Most lead volumes are trackable in your CRM in about two minutes. This is the number that decides everything else.
3. **Divide messages into likely conversations.** Roughly, conversations ≈ messages ÷ 4 or 5 for a booking-oriented agent. Booked appointments tend to run longer.
4. **Pick a model, then multiply.** Input and output tokens are priced separately, and output costs several times more than input. HighLevel publishes the per-million rates; use them.
5. **Add the per-minute voice floor** if anyone's calling in. $0.06 per minute is a reasonable starting base before tokens.
6. **Add telephony, SMS and WhatsApp** from your usage reports rather than guessing.
7. **Compare two configurations side by side** — platform plus native AI at current volume, versus platform plus a third-party layer. Run it at your volume today and at double your volume, because that's the version of this decision you'll actually be living with in six months.

## Frequently asked questions

**Does GoHighLevel's AI chatbot cost extra on top of the subscription?**
Yes. The platform subscription and the AI fee are separate. AI is either pay-per-use with no monthly fee, $50/month for AI Employee Growth, or $97/month for AI Employee Unlimited, charged per enabled location.

**Is pay-per-use actually cheaper?**
At low volume, often yes — sometimes cheaper than a third-party subscription too. At scale, token costs climb and the predictability of a flat per-location fee starts to look attractive again. There's no universal answer; it depends on your conversation count and which model you run.

**How much does one AI agent cost on GoHighLevel?**
Conversation AI and Voice AI fall inside Growth or Unlimited allowances. Agent Studio doesn't — it's pay-per-use on every plan, including Unlimited.

**Can I rebill AI costs to clients?**
Yes, but HighLevel's documentation says AI Employee rebilling requires the $497/month Agency Pro plan. On CloseBot's Agency plan, rebilling is part of the $397/month package.

**What's the cheapest way to test an AI chatbot on GoHighLevel?**
HighLevel's pay-per-use tier costs nothing monthly, so you only pay for what runs. CloseBot's free plan gives you 100 messages a month, one agent and unlimited account connections, which covers basic testing without a card. Both are genuine no-cost entry points — the difference is that CloseBot's paid tiers have no per-location fee attached, and HighLevel's do.
