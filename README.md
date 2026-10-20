# Build A Business

**One hour. By the end the machine is standing: a real product or service on a
live URL, able to take a card, a place to track a buyer, and the paperwork
ready. The yes comes later. When it comes, nothing is improvised.**

Paste this into any AI chat:

```
Read https://raw.githubusercontent.com/nradawg/build-a-business/main/README.md
and run it on me. I have an hour.
```

## The stack, all free

| what | tool | why |
|---|---|---|
| Build it | Codex | writes the code, you do not need to know how |
| Code lives | GitHub | free, and Cloudflare reads from it |
| Website | Cloudflare Pages | free, and it allows commercial use |
| Payments | Stripe | no monthly fee, 2.9% plus 30 cents per card |
| Track buyers | Notion | free, and it is where a name goes the second someone is interested |

Total to start: zero. You pay nothing until someone pays you.

**Do not host this on Vercel Hobby or GitHub Pages.** Both forbid commercial
use in their own terms, and both are what an AI will suggest first. Vercel
counts any method of requesting payment from visitors as commercial. Cloudflare
Pages free does not have that restriction, which is why it is here.

## This is not a race to a customer

Nobody expects a sale by the end of the hour. The point is that everything
exists and works, so the moment someone says "yes, I want this, I need it
now," you are collecting instead of scrambling.

At minute 60 you have:

- a real product, service, or small piece of software that exists
- it is live at a public URL anyone can open
- a payment link that charges a card
- one place where a buyer gets written down
- terms, a refund policy, and a simple agreement ready to sign

## One thing to do before you sit down

Stripe will not take live charges from an account you create mid session. It
needs a public website whose content matches what you say you sell, plus
dashboard verification.

So a few days ahead: put up a bare page with the real name, what it is, and
the price, then start Stripe activation pointing at that URL. If activation
has not cleared by the night, you still build everything and your link runs in
test mode. Switch it live when Stripe clears.

Also check Stripe's prohibited and restricted business list against your idea
first. Sixty seconds, and a prohibited category kills the plan.

## The hour

**0 to 5. Name it and check for a wall.**
Operating under your own legal name makes you a sole proprietor automatically
in the US. No filing, no fee, no liability protection either. A separate
business name usually needs a trade name filing, and a local business license
is its own separate thing. Note it as a task, do not solve it tonight.

**5 to 10. The CRM.**
A CRM is one list of everyone who might buy from you and what you owe them
next. That is all it is. In Notion, one database, five columns: Name, Contact,
What they want, Price, Stage.

Add a second small database called Tasks. Put two things in it right now: look
up whether your city needs a business license, and set aside money for taxes on
anything you earn.

**10 to 20. The offer.**
One sentence. One thing, one price, one delivery date. Not a company, not a
vision. The thing someone can say yes to.

Go deeper with [offer-build](https://raw.githubusercontent.com/nradawg/offer-build/main/README.md)
and sanity check the number with [price-floor](https://raw.githubusercontent.com/nradawg/price-floor/main/README.md).

**20 to 38. Build it with Codex.**
Plain HTML and CSS, no framework, no build step. A single page: what it is, who
it is for, the price, and a button. Put `PAYMENT_LINK_HERE` where the button
goes.

Stripe wants a few things visible on the page before it will go live: a clear
description of what you sell, a way to contact you, and your refund policy. Put
them on now so you are not fixing it later.

**38 to 46. Ship it.**
Make the GitHub repo with a README in it, since a completely empty repo breaks
Cloudflare's branch picker. Then in the Cloudflare dashboard, Workers and
Pages, connect the repo, leave the build command blank for plain HTML, deploy.

You get a free `yourproject.pages.dev` URL. Use it. Do not touch custom domains
tonight, DNS can take a while and it is not what tonight is for.

**46 to 54. Wire up money.**
In Stripe, business type Individual. Paste your live URL and the matching
product description. You will need the last four of your SSN and bank details
for payouts. Create a Payment Link for your offer.

Replace `PAYMENT_LINK_HERE` with it, push, and Cloudflare redeploys. Open it on
your phone and confirm the address bar switches to a Stripe domain when you tap
the button. Cards get typed on Stripe, never on your page.

First payout on a new account takes a few days. After that it settles into a
rhythm.

**54 to 60. The paperwork and the first name.**
Second page on the site with terms, refund and cancellation policy, and a
privacy policy. Stripe Shop's terms and 37signals' policies are published under
CC BY 4.0, so you can adapt them with attribution instead of inventing legal
text.

Save a one page agreement with six fields: who, who, what exactly, how much,
when it is due, when it is delivered. Common Paper publishes a services
agreement under CC BY 4.0 you can base it on.

Then put one real name in the CRM and send one message using
[first-touch](https://raw.githubusercontent.com/nradawg/first-touch/main/README.md).

## The Yes Runbook

This is why tonight mattered. Someone says yes. In order:

1. **Reply in under an hour.** Speed is most of it.
2. **Confirm the scope in writing.** One message: here is exactly what you
   get, here is what you do not, here is the date. Their reply is your record.
3. **Send the agreement**, if the job is big enough to need one. Under a
   hundred dollars, the written scope is usually enough.
4. **Send the payment link.** Deposit or full, decided before you send it, not
   negotiated live.
5. **Write it in the CRM** the same minute. Name, what they bought, what they
   paid, delivery date, next action.
6. **Set aside the tax portion** immediately, before the money feels like
   yours.
7. **Start the work**, and send one unprompted update before the deadline.

What goes wrong for people who skipped tonight: no way to invoice, no written
scope so the job grows, money mixed into a personal account they cannot
untangle, and no record of what was promised.

If they say no, run
[objection-drill](https://raw.githubusercontent.com/nradawg/objection-drill/main/README.md)
on what they actually said. A no with a reason is worth more than a maybe.

## Keep in mind

Taking money does not mean you have a business and it does not exempt you from
anything. Income is taxable whether or not any payment app ever sends you a
form. A business name other than your own usually needs a filing, and a local
license is separate from that. Look up your own city, nobody can do that part
for you.

For anything involving food, childcare, health, or a licensed trade, find out
what permit it needs before you sell it, not after.

This is not legal or tax advice. For a real contract, an entity, or a tax
question with money on the line, pay a professional once rather than guessing
for a year.

## Limits

This gets the machine standing. It does not get you a customer, and it cannot
tell you whether your idea is good. For that, run
[idea-kill](https://raw.githubusercontent.com/nradawg/idea-kill/main/README.md)
before you build, and accept the answer.

One hour is enough for a single page and a payment link. It is not enough for
an app. Scope accordingly, and ship something real rather than half of
something impressive.

One of 48 skills: [assume-nothing](https://github.com/nradawg/assume-nothing)

MIT.
