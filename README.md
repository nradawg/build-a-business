# Build A Business

**One hour. By the end, the machine is standing: a real product or service on a live URL, able to take a card, a place to track a buyer, and the legal setup correct enough to collect. The yes comes later. When it comes, nothing is improvised.**

Paste this into any AI chat:

```
Read https://raw.githubusercontent.com/nradawg/build-a-business/main/README.md
and run it on me. I have an hour.
```

## What this night is and is not

It is not a race to a customer. Nobody expects a yes by 9pm, and anyone promising a room of thirty students otherwise is selling a feeling.

It is operational readiness. At minute 60 you have:

- a real product, service, or small piece of software that exists
- it is live at a public URL anyone can open
- a payment link that charges a card
- one place where a buyer gets written down
- a one page agreement, a refund policy, and a privacy policy on the site
- a written answer to the two questions that can legally stop you

So the second somebody says "yes, I want this, I need it now," you are not scrambling. You are collecting.

---

## PRE-STAGE. Do this before the night, not during it

Three things in this stack involve a human or a machine approving you, and approval cannot be scheduled inside an hour. Do these first.

**At least a week before**

1. Apply for the GitHub Student Developer Pack at https://education.github.com/pack. You need proof of enrollment: a photo of a school ID showing a current date, a class schedule, a transcript, or an enrollment letter. If your school requires an academic email, add and verify it on your GitHub account before you apply. (docs.github.com apply page, checked 2026-10-19) **How long approval takes is UNKNOWN.** GitHub publishes no timeframe anywhere official. Check https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-education-for-students/apply-to-github-education-as-a-student

   The night works without it. GitHub Free already gives unlimited public and private repos and 2,000 Actions minutes per month (github.com/pricing, checked 2026-10-19), which is everything you need to ship.

2. Claim your free ChatGPT Plus as a student at https://chatgpt.com/students. Four months free with a verified school email. Do this before the night so Codex is working when you sit down. US and Canadian students can also claim $100 in Codex credits at https://developers.openai.com/community/students, one per student.

3. If you are on an F-1 or J-1 visa, email your international student office and ask in writing whether you may earn money from this. Do not start until you have their written answer. DHS says "If you decide that you want to work, the first step is always to talk with your designated school official (DSO)," and that unauthorized work gets reported through SEVIS (https://studyinthestates.dhs.gov/students/work/working-in-the-united-states, checked 2026-10-19). This is the one item on the list that can end badly.

**At least three days before**

4. Read Stripe's prohibited and restricted businesses list against your idea before you build anything. A prohibited category means Stripe will never work for you (https://docs.stripe.com/get-started/account/checklist, checked 2026-10-19). Sixty seconds, and it can save the whole night.

5. Decide the offer, put up a bare one page site with the real product name, description, and price, then start Stripe activation using that live URL. You must do this in that order. Stripe requires a business URL that is "a valid, publicly accessible business website" and says "Website content should match your business name and product description" (https://docs.stripe.com/connect/required-verification-information, checked 2026-10-19). Live charges also require verifying your business in the dashboard first (https://docs.stripe.com/get-started/account/activate, checked 2026-10-19). An account created at minute 40 of the hour is a sandbox, and a sandbox link does not charge anyone. If you are walking in cold with nothing pre-staged, you still finish the night with the machine standing, except the payment link may sit in test mode until Stripe clears you. The Yes Runbook below covers that case.

6. Notion: if you already have an account made with a personal Gmail and you want the student plan, change your primary email to your school email first. Notion requires the school email to be the main email on the account, does not accept student IDs, and does not cover K-12 (https://www.notion.com/help/notion-for-education, checked 2026-10-19). Each school email can claim the offer once for one workspace, ever, so do not burn it on a throwaway. **How long Notion verification takes is UNKNOWN,** that page does not say. You do not need it. Notion Free gives unlimited pages and databases (https://www.notion.com/pricing, checked 2026-10-19), which is plenty for a CRM.

---

## The stack, and what is actually true about it

| Job | Tool | What you need to know |
|---|---|---|
| Track buyers | Notion | Free plan is enough. Student plan is an upgrade, not a gate. |
| Code host | GitHub | Free plan is enough. Student Pack is a bonus that arrives later. |
| Hosting | Cloudflare Pages | Free and allowed to be commercial. One hard rule below. |
| Payments | Stripe | 2.9% plus 30 cents per domestic card charge, no monthly fee. |
| Build | Codex | $100 credits, US and Canada students only. |
| Legal | Free CC BY documents | Real human written policies, no generator branding. |

**Why Cloudflare and not Vercel.** Vercel's own guidelines say Hobby teams are "restricted to non-commercial personal use only" and list "Any method of requesting or processing payment from site visitors" as commercial usage (https://vercel.com/docs/limits/fair-use-guidelines, checked 2026-10-19). A Stripe button on Vercel Hobby is exactly the banned case. Donations are carved out, so a free tool with a tip jar could stay there. Selling cannot.

**Why not GitHub Pages either.** GitHub's docs say "GitHub Pages is not intended for or allowed to be used as a free web-hosting service to run your online business," rule out a site "primarily directed at either facilitating commercial transactions" or "providing commercial software as a service (SaaS)," and say Pages sites "shouldn't be used for sensitive transactions like sending passwords or credit card numbers" (https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits, checked 2026-10-19). GitHub holds the code. Cloudflare serves the site.

**Cloudflare's own terms carry no commercial use restriction** anywhere in the Self-Serve Subscription Agreement (https://www.cloudflare.com/terms/, checked 2026-10-19). You may sell from a free Pages site.

### The one hard rule, and it is the most important line in this file

Clause 2.2.1(h) of that same agreement says you have no right to "process or collect personal or business credit card information on any web property" that is receiving Free Services. That sits in the agreement wide restrictions, not in any plan specific section (https://www.cloudflare.com/terms/, checked 2026-10-19).

So: **your site links or redirects to a Stripe Payment Link or Stripe hosted Checkout, where the card is typed on Stripe's own domain. Never embed Stripe Elements, embedded Checkout, or any card input field on your page.**

Say that sentence to your AI tool out loud when you ask it to build the checkout. Left unsaid, a coding agent asked for a checkout will embed Elements by default and put you in breach of your host's agreement on the exact thing tonight is about.

Two more Cloudflare facts. No single site asset over 25 MiB, and 500 builds per month on Pages Free (https://developers.cloudflare.com/pages/platform/limits/, checked 2026-10-19). Requests to static assets are free and unlimited (https://developers.cloudflare.com/workers/platform/pricing/, checked 2026-10-19), so going viral tonight costs you nothing. If the product itself is video or a big file bundle, keep the storefront on Pages and deliver the file from somewhere else.

Cloudflare's docs now show a banner saying "Start new projects with Workers." Ignore it tonight. The Workers path is documented only through a CLI and a config file (https://developers.cloudflare.com/workers/static-assets/get-started/, checked 2026-10-19). Pages connects a GitHub repo from the dashboard with no terminal at all.

---

## The hour

| Minutes | What happens |
|---|---|
| 0 to 4 | Name it. Confirm the two stoppers. |
| 4 to 8 | Notion CRM, five columns, done. |
| 8 to 18 | The offer: one sentence, one price, one delivery date. |
| 18 to 36 | Build the thing and the page with Codex. |
| 36 to 44 | GitHub repo, then Cloudflare Pages. Live URL exists. |
| 44 to 52 | Stripe: live URL in, Payment Link out. |
| 52 to 57 | Link into the page, redeploy, test on your phone. |
| 57 to 60 | Legal page live. Agreement saved. Three names in the CRM. |

### 0 to 4. Name it and clear the two stoppers

Default to your own legal name. The SBA says you are "automatically considered to be a sole proprietorship if you do business activities but don't register," and if you work under your own legal name "you won't need to register anywhere" (https://www.sba.gov/business-guide/launch-your-business/choose-business-structure, checked 2026-10-19). Zero paperwork. Also zero liability shield, which is the honest other half.

Want a brand name instead? Then most states require a DBA filing and the SBA says a DBA "doesn't provide legal protection by itself" (https://www.sba.gov/business-guide/launch-your-business/register-your-business, checked 2026-10-19). Tonight, use your name and put the brand name on the roadmap.

Stopper one: visa. See pre-stage item 3. Stopper two: Stripe's restricted list. See pre-stage item 4.

### 4 to 8. The CRM

A CRM is one list of the people who might buy from you, with a note on each about what they want and what you owe them next. That is all it is, and without it you will forget the person who said yes on a Tuesday.

Make one Notion database. Five columns, no more: Name, Contact, What they want, Price, Stage. Stage values: Talked, Wants it, Agreement sent, Paid, Delivered. Add one row right now for the first person you plan to tell.

Add a second database called Tasks with two rows:
- "Look up whether my city requires a business license." You will do this tomorrow, not tonight. Licensing is local. The SBA says "Local governments determine registration, licensing, and permitting requirements" (https://www.sba.gov/business-guide/launch-your-business/apply-licenses-permits, checked 2026-10-19). Nobody in this room can tell you the answer for your city, and anyone who does is guessing. Search your city name plus "business license" and your state Secretary of State site, then write what you found in that row.
- "Set aside part of the first payment for tax." See the legal section.

### 8 to 18. The offer

One sentence, one price, one delivery date. If you cannot say it in a sentence, the page will not sell it.

Run [`offer-build`](https://raw.githubusercontent.com/nradawg/offer-build/main/README.md) if the sentence will not come out, and [`price-floor`](https://raw.githubusercontent.com/nradawg/price-floor/main/README.md) to set the number instead of guessing it. If you suspect the idea is already dead, spend three minutes on [`idea-kill`](https://raw.githubusercontent.com/nradawg/idea-kill/main/README.md) now rather than forty minutes building it. Blank on what you are even good at? [`story-mine`](https://raw.githubusercontent.com/nradawg/story-mine/main/README.md).

Write the exact words down. You will paste the same words into Stripe later, and they have to match.

### 18 to 36. Build it

Hand your AI tool the offer sentence, the price, and this instruction set:

- plain HTML and CSS, single page, no framework, no build step
- the buy button is an anchor tag pointing at a Stripe Payment Link URL I will paste in later, leave it as PAYMENT_LINK_HERE
- never embed Stripe Elements or any card input field, card entry happens on Stripe's domain only
- no file over 25 MiB
- include these sections, because Stripe's own website checklist requires them

Stripe's checklist wants: a description of what you are selling, the purchase currency, customer service contact information "including direct communication channels, such as email addresses, phone numbers, and live chat (something besides contact forms)," your fulfillment policies, legal or export restrictions, a privacy policy, your business address, promotion terms, website and payment security including HTTPS, and the logos of the cards you accept (https://docs.stripe.com/get-started/checklist/website, checked 2026-10-19).

The two everyone misses: a real email or phone, not just a contact form, and the currency written next to the price. Stripe does carve out fulfillment policies for businesses with "no fulfillment process, such as those that only offer in-person services," so in person tutoring does not need a shipping policy. Write a refund and cancellation policy anyway. It prevents arguments.

### 36 to 44. Live URL

Create the GitHub repo **with a README checked**, or commit your index.html through the GitHub web interface first. Cloudflare's production branch dropdown only shows branches already pushed, so an empty repo looks like Cloudflare is broken when it is not (https://developers.cloudflare.com/pages/get-started/git-integration/, checked 2026-10-19).

Then in Cloudflare: Workers and Pages, Create application, Pages, Connect to Git, authenticate GitHub, Install and Authorize, Begin setup, project name, production branch, **leave the build command blank**, leave the output directory as the root, Save and Deploy.

Use the free yourproject.pages.dev URL. Do not touch custom domains tonight. An apex domain needs your nameservers pointed at Cloudflare (https://developers.cloudflare.com/pages/configuration/custom-domains/, checked 2026-10-19), and **how long activation, certificates, and propagation take is UNKNOWN** because that page does not say. Put the domain on tomorrow's list.

If the site does not load, that is normal for a minute. Cloudflare's own docs say to wait for DNS or try another device or network. Try your phone on cell data before you rebuild anything working.

Emergency only: Pages Direct Upload lets you drag a folder in with no repo, but a Direct Upload project can never be switched to Git later (https://developers.cloudflare.com/pages/get-started/direct-upload/, checked 2026-10-19). Use it if GitHub authorization stalls, and know you have chosen manual deploys forever.

### 44 to 52. Stripe

Choose business type **Individual**, not Company. For a US individual, Stripe's own requirements list asks for your name, date of birth, a street address with no PO box, email, phone, **SSN last 4**, your industry code, a product description of at least 10 characters, a support phone number, a statement descriptor, and the business URL. **No EIN, no company name, and no company tax ID appear anywhere in that list** (https://docs.stripe.com/connect/required-verification-information, checked 2026-10-19). No LLC, no state filing, no waiting.

Paste the live pages.dev URL. Use the same words for the product description that are on the page. Set the statement descriptor deliberately so the first charge is recognizable on a buyer's statement. Add your bank details, because Stripe says "Incorrect bank information is a common cause of payout delays."

Then create a Payment Link. Payment Links are no code, Stripe hosted, work without a website, share as a link or a QR code, and support refunds and automatic receipts (https://docs.stripe.com/payments/payment-links, checked 2026-10-19). Skip the $10 per month custom checkout domain (https://stripe.com/pricing, checked 2026-10-19). The default Stripe URL is free, and it is what keeps card entry off your free Cloudflare property.

**Know this before you sell anything.** The card clears instantly and the money appears in your Stripe balance. The first bank transfer is different: Stripe typically schedules a new account's first payout to complete within 7 to 14 days after the first successful live payment, then US payouts settle in 2 business days (https://docs.stripe.com/payouts, checked 2026-10-19). Nothing is broken. Do not refund and recharge your first customer because the cash has not landed.

### 52 to 57. Close the loop

Replace PAYMENT_LINK_HERE with the real link, commit, let Cloudflare redeploy, then open your own site on your phone and click the button. You are looking for one thing: the URL in the address bar becomes a Stripe domain. If a card field appears on your own site, stop and fix it.

### 57 to 60. The paperwork that makes a yes collectible

Add a second page with your terms, refund and cancellation policy, and privacy policy. Use documents written by humans and licensed for reuse, not a generator:

- Terms: Stripe publishes its own Stripe Shop Terms under CC BY 4.0 and says "feel free to use the Stripe Shop Terms as a starting point as you build your site" (https://stripe.com/stripe-shop/legal, checked 2026-10-19). It is written for a physical goods shop, so cut the shipping parts if you sell a service.
- Privacy, cancellation, refund: 37signals publishes its full policy set under CC BY 4.0 (https://github.com/basecamp/policies, checked 2026-10-19; the repo is archived, current set at 37signals.com/policies).
- Keep the attribution line. That is the whole price.

Save a one page letter of agreement with exactly six fields, modeled on Common Paper's Professional Services Agreement cover page, which is CC BY 4.0 (https://commonpaper.com/standards/professional-services-agreement/, checked 2026-10-19): both parties and addresses, the deliverable and scope, the price, how long they have to pay, the delivery date, and signatures. Long terms live at a URL. The signable page stays one page. Common Paper says plainly that its forms "are not a substitute for a lawyer."

Then put three real names in the CRM and send one message. Use [`first-touch`](https://raw.githubusercontent.com/nradawg/first-touch/main/README.md).

---

## THE YES RUNBOOK

Someone just said "yes, I want this." This is the whole point of the night. Run it in order and do not skip step 1.

1. **Write it down first.** Open the Notion CRM, set their Stage to "Wants it," and type what they actually asked for in their words. Thirty seconds. Memory is where deals die.
2. **Say the price and the delivery date back to them.** Out loud or in writing, as one sentence. If they flinch, do not discount on the spot. Run [`objection-drill`](https://raw.githubusercontent.com/nradawg/objection-drill/main/README.md) and answer the real objection instead.
3. **Fill in the agreement.** Six fields, their legal name, your legal name, the deliverable, the price, the payment window, the date. If their version of the deal is bigger than yours, run [`contract-risk`](https://raw.githubusercontent.com/nradawg/contract-risk/main/README.md) before you sign anything.
4. **If you sold them in person at their place, say the cancellation line.** The FTC cooling off rule gives a buyer three business days to cancel certain sales made "at your home, workplace, or dormitory" or "at a seller's temporary location." It does not apply under $25 for sales at the buyer's home, or under $130 at temporary locations, or to sales made entirely online or by phone. The seller must tell the buyer about the right at the time of sale and hand over "Two copies of a cancellation form" and "A copy of your contract or receipt" (https://consumer.ftc.gov/articles/buyers-remorse-ftcs-cooling-rule-may-help, checked 2026-10-19). An online Payment Link sale is outside this rule. A handshake in a dorm room is not.
5. **Send both at once.** The agreement and the Payment Link, same message. Stage moves to "Agreement sent."
6. **They pay. Confirm it in the Stripe dashboard, not in your inbox.** Stage moves to "Paid." Say thank you and restate the delivery date in the same message.
7. **Set aside tax money the same day.** Before you spend any of it. See the legal section and [`tax-set-aside`](https://raw.githubusercontent.com/nradawg/tax-set-aside/main/README.md).
8. **Start the work inside 24 hours and send something visible.** A rough draft, a screenshot, a schedule. The gap between payment and first contact is where refund requests are born.
9. **Deliver, then ask for the next thing.** Stage moves to "Delivered." Use [`follow-up-ladder`](https://raw.githubusercontent.com/nradawg/follow-up-ladder/main/README.md).

**If Stripe has not cleared you yet.** Do steps 1 through 3 exactly the same. Tell them the truth: "My payment setup clears in a few days, here is the signed agreement, I will send the payment link the moment it is live, and I am starting now." A signed agreement with a date on it is a real yes. Then finish Stripe activation that night.

---

## Legal, verified, with sources

Verified and true for a US individual:

- You are a sole proprietor automatically, with no filing, if you use your own legal name (SBA, checked 2026-10-19, link above). No liability shield.
- An EIN is optional. The IRS says you need one only if you have employees, owe employment or excise or alcohol, tobacco and firearms taxes, or withhold on income paid to a non-resident alien (https://www.irs.gov/businesses/small-businesses-self-employed/employer-identification-number, checked 2026-10-19). It is free, immediate, and "You never have to pay a fee for an EIN." The online tool has hours in Eastern Time: Monday to Friday 6am to 1am, Saturday 6am to 9pm, Sunday 6pm to midnight (https://www.irs.gov/businesses/small-businesses-self-employed/get-an-employer-identification-number, checked 2026-10-19). If your event is a Sunday afternoon, the tool is closed and this step does not belong in the hour. The one real reason to get one: you hand clients an EIN instead of your SSN on a W-9.
- Income is taxable even when nobody sends you a form. The IRS says "You have to file an income tax return if your net earnings from self-employment were $400 or more," and the self employed generally file annually and pay estimated taxes quarterly (https://www.irs.gov/businesses/small-businesses-self-employed/self-employed-individuals-tax-center, checked 2026-10-19). Set money aside the day it arrives.
- A privacy policy is not optional, and not because of the usual hand waving. Nevada NRS 603A.340 requires an operator of a commercial website collecting covered information to post a notice with the categories collected, the categories of third parties, the review process, how material changes are announced, whether third parties track users, and an effective date (https://www.leg.state.nv.us/NRS/NRS-603A.html, checked 2026-10-19). The only exemption needs all three of being located in Nevada, revenue mostly from non-online sources, and under 20,000 unique visitors a year, so selling online fails it. Delaware 6 Del. C. 1205C requires the same kind of notice "conspicuously available" plus a do not track line, and gives 30 days to cure after notice (https://delcode.delaware.gov/title6/c012c/index.html, checked 2026-10-19). Use the Nevada list as your checklist of what the policy must contain.
- CCPA almost certainly does not apply to you. The California AG lists thresholds of over $25 million gross annual revenue, or the personal information of 100,000 or more California residents or households, or 50 percent of revenue from selling it (https://oag.ca.gov/privacy/ccpa, checked 2026-10-19). Do not install rights language you cannot honor.

**Where you need a real professional, and no tool substitutes:**

- forming an LLC or corporation, if you want an actual liability shield
- anything licensed or regulated: health, legal advice, financial advice, food, childcare, contracting
- **sales tax**, including economic nexus across states. This is the real trap for anyone selling software or digital goods to buyers in other states. Ask an accountant before your second month, not your second year.
- paying a helper, which raises contractor versus employee classification
- any contract over a few thousand dollars, or with IP assignment, or with indemnities
- the tax return itself, once you have 1099 or Stripe reported income

---

## UNKNOWN, do not let anyone tell you otherwise

These were researched and could not be confirmed from a primary source. They appear here as open questions with the page to check, not as facts.

- GitHub Student Pack approval time. No published timeframe. Check the apply docs page linked in pre-stage item 1.
- Notion education verification duration. Not stated at https://www.notion.com/help/notion-for-education
- Cloudflare Pages custom domain activation, certificate, and propagation times. Not stated at https://developers.cloudflare.com/pages/configuration/custom-domains/

- Whether the Codex student credit has a deadline. The page states none as of 2026-10-19.
- CalOPPA's exact requirements. The California legislature's text could not be retrieved. The privacy policy guidance above rests on Nevada and Delaware instead.
- Whether CCPA's $25 million threshold has been inflation adjusted. Check https://oag.ca.gov/privacy/ccpa rather than quoting the number as law.

---

## Limits

- This is not legal, tax, or immigration advice. Every rule here is quoted from a primary source with the date it was checked, and primary sources change. Re-check anything before you rely on it.
- All US specific. Sole proprietor status, SSN last 4, EIN, the FTC rule, and the state privacy statutes do not transfer. If you are outside the US, the shape of the hour still works and the legal section does not.
- Prices and plan limits were checked on 2026-10-19 only. Do not quote them to anyone next semester without opening the pricing page.
- The hour gets the machine standing. It does not get you customers. Finding people to ask is a different night: see [`assume-nothing`](https://raw.githubusercontent.com/nradawg/assume-nothing/main/README.md) and [`first-touch`](https://raw.githubusercontent.com/nradawg/first-touch/main/README.md).
- There is no estimate here of how long a beginner takes to deploy for the first time, because no credible measurement of that exists. The minute budget is a scope limit, not a prediction. If you are behind, cut the product, not the live URL and not the payment link.
- Nothing here makes you safe from liability. You are personally on the hook as a sole proprietor, which is the trade for filing nothing.