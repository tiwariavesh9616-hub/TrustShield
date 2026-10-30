# TrustShield[span_1](start_span)[span_1](end_span)

**One trust score for calls, payments and links.** TrustShield is a working prototype of a mobile security app that protects everyday users in India from voice-clone calls, fake UPI requests and phishing messages, and explains every decision in their own language.[span_2](start_span)[span_2](end_span)

> Team **Quantum Quills** · Hackathon 2k26 · Security track[span_3](start_span)[span_3](end_span)

## Live demo[span_4](start_span)[span_4](end_span)

Open `index.html` in any browser, or use the hosted version[span_5](start_span)[span_5](end_span):

`https://<your-github-username>.github.io/<repo-name>/`[span_6](start_span)[span_6](end_span)

No build step, no dependencies. It is a single HTML file.[span_7](start_span)[span_7](end_span)

## The problem[span_8](start_span)[span_8](end_span)

Scams in India now arrive through three doors at once[span_9](start_span)[span_9](end_span):

- A cloned voice of a "bank manager" or a family member asks for an OTP or money[span_10](start_span)[span_10](end_span).
- A UPI **collect request** is disguised as a refund or cashback. Approving it takes money out of your account[span_11](start_span)[span_11](end_span).
- An SMS or WhatsApp link imitates a real bank and steals your login[span_12](start_span)[span_12](end_span).

Most tools handle only one of these, and their warnings are in English and hard to act on[span_13](start_span)[span_13](end_span).

## The solution[span_14](start_span)[span_14](end_span)

Three shields feed one **trust score from 0 to 100**. The score decides the action[span_15](start_span)[span_15](end_span):

| Score | Action |
|-------|--------|
| 0-40 | **Block** |
| 40-70 | **Warn** |
| 70-100 | **Allow** |

Every verdict comes with plain-language reasons, and alerts can be shown and spoken in **English, Hindi, Tamil and Telugu**[span_16](start_span)[span_16](end_span).

### The three shields[span_17](start_span)[span_17](end_span)

| Shield | What it checks | Signals in this prototype |
|--------|----------------|---------------------------|
| **Voice Shield** | Calls and voice notes | Synthetic-voice probability, urgency pressure |
| **UPI Risk Engine** | Payee and request, before you pay | Collect request, unknown payee, bait keywords (refund, prize, KYC), high amount, random-looking UPI ID |
| **Phishing Guard** | SMS and WhatsApp messages | URL shortener, look-alike bank or payment domain, no HTTPS, risky domain ending, urgency words, bait keywords |

### Pipeline[span_18](start_span)[span_18](end_span)
