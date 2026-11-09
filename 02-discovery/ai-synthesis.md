# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Assumption to validate #1:** Lena values a Riverty card for effort-saving, not rewards.
- **Assumption to validate #2:** “try first, pay later” works on a card without turning into revolving debt.
- **Assumption to validate #3:** The card strengthens merchant relationships instead of competing with them
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** N-06, consumer, test launch participant: “The card was declined at a bakery and the app did not say why. I went back to my debit card the same week.”
- **Moment of misery / red flag #2:** T-107, ticket: Participants ask whether using the card affects their credit score. No help article exists yet.
- **Moment of misery / red flag #3:** N-08: the enterprise merchant sees the card as a reason for customers to skip Riverty at checkout, and wants a visible benefit.
- **Product Health & Insights Summary (Claude's output):** # Product Health & Insights Summary

## Executive Summary

The card's core payment rails function, but the experience around them is failing at the moments that matter most: first use, in-store payment, and understanding what is owed. Technical defects (declines without explanation, wallet provisioning failures, delayed notifications) are directly eroding user trust and pushing participants back to their existing debit cards within days. Compounding this, the evidence base is skewed toward a colleague-heavy test group, and the value proposition is not yet compelling to consumers or merchants, so current stability and approval metrics should be read as optimistic.

## Thematic Synthesis

### 1. Technical Stability and Payment Reliability

The most acute issues sit at the point of payment. Declines occur without any reason surfaced to the user, wallet provisioning breaks after activation, and purchase notifications arrive late enough that users assume failure and pay a second time. These are individually fixable defects, but together they undermine the one behavior the product depends on: tap-and-forget payment. One participant reverted to a debit card within a week of a single unexplained decline, which suggests very low tolerance for early failures.

- **Wallet provisioning failure or abandonment (T-102):** 143 activated cards never reached the phone wallet, meaning a large share of activated users cannot use the card in-store. *Critical*
- **Unexplained in-store declines (T-101, N-06):** 48 declines in the test log, with no reason shown in the app; at least one confirmed reversion to debit. *Critical*
- **Delayed purchase notifications causing duplicate payments (T-108):** Users assume the payment failed and pay again with another card, creating double-spend and support exposure. *High*

### 2. Onboarding and Activation

Friction in identity verification and wallet setup is causing drop-off before users ever transact. The failed-upload loop in the identity check forces a repeat document submission, and some applicants abandon at that step. Combined with wallet provisioning failures, the funnel from application to first in-store use appears to leak at multiple points.

- **Repeated document photo request after failed upload (T-106):** Applicants abandon at this step. *High*
- **Activation-to-wallet drop-off (T-102):** Overlaps with the stability theme; it is also the largest measured activation gap. *High*

### 3. Trust, Clarity and Financial Comprehension

Users cannot form a clear mental model of what they owe or how the product behaves. Balances are split across two screens with no reconciled total, due dates and statement dates diverge, and the instalment option appears inconsistently. For a segment that already juggles multiple pay-later apps, this adds cognitive load rather than reducing it. Credit-card framing also triggers wariness among interest-averse users, and the absence of guidance on credit score impact leaves a common question unanswered.

- **Fragmented balance view across card and pay later (T-103, N-07):** Participants ask which total is real. *High*
- **Misaligned statement and due dates producing duplicate reminders (T-104):** Two reminders in the same week for different amounts. *High*
- **Inconsistent instalment availability post-purchase (T-105):** Perceived as random by users. *Medium*
- **Credit-card and interest perception among cautious users (N-05):** Instalment language raises anxiety. *Medium*
- **No guidance on credit score impact (T-107):** An unanswered, recurring question. *Medium*

### 4. Value Proposition and Market Fit

Interest is real but conditional. Heavy BNPL users value deferred payment and some would use the card daily for groceries, yet others see a third app as added burden or default to their bank card out of habit. Cashback is cited as a trial driver but not a retention driver. On the merchant side, enterprise merchants question what the card offers their checkout, and SMEs are interested only if it drives traffic to them rather than to large marketplaces.

- **Habit competition with debit and existing apps (N-02, N-03):** Low top-of-mind presence at the point of purchase. *High*
- **Unproven retention beyond incentive-led trial (N-12):** Cashback may drive trial without sustained use. *Medium*
- **Unclear merchant value proposition (N-08, N-09):** Enterprise merchants see no differentiator; SMEs are wary of marketplace-weighted benefits. *High*
- **Unmet demand for large-basket instalments at supermarkets (N-04):** Signals an opportunity but also an acceptance and product-fit gap. *Low*

### 5. Data Validity and Operational Constraints

The reliability of the evidence itself is a health concern. The test cohort is largely colleagues, so approval and repayment performance will likely overstate real-world results. Separately, any change to the proposition must pass pricing, credit policy and terms approval, which takes months and limits how quickly learning can be translated into product changes.

- **Test cohort bias inflating approval and repayment metrics (N-10):** Risks false confidence in credit performance. *High*
- **Lengthy proposition-change approval cycle (N-11):** Constrains iteration speed on anything touching pricing, policy or terms. *Medium*

### 6. Support Load

Several defects generate predictable inbound demand rather than silent failure: users cannot self-diagnose declines, reconcile balances, interpret dual reminders, or find an answer on credit score impact. Duplicate payments from late notifications add dispute and refund handling on top. Support demand is currently a symptom of the clarity and stability gaps rather than an independent problem.

- **Contacts driven by declines, balance confusion, reminder overlap and missing help content (T-101, T-103, T-104, T-107):** Avoidable volume tied to upstream issues. *Medium*
- **Duplicate-payment handling from delayed notifications (T-108):** Adds dispute and reconciliation effort. *Medium*

### Minor Technical Debt

Inconsistent in-app messaging and copy around instalment terminology, missing help-centre articles, and uneven category-level behavior in post-purchase flows.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** yes
- **Did it smooth over a critical frustration into a generic bullet point?:** no
- **Did the AI try to suggest features or a roadmap despite the constraints?:** no
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** _(not filled in)_
- **Logic leak / hallucination #2:** _(not filled in)_
