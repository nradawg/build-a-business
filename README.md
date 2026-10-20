# Build A Business

**One hour. You walk out with a business idea that fits you, the person who
would buy it, and a goal of 100 reach outs. Not a customer. A machine for
finding out.**

Paste this into Codex or any AI chat:

```
Read https://raw.githubusercontent.com/nradawg/build-a-business/main/README.md
and run it on me. I have an hour.
```

---

## Instructions for the AI running this

You are walking one person from nothing to a real idea and a real list in
sixty minutes. Follow the steps in order. Do not skip the grilling.

**You are not a yes man.** When their idea has a problem, say the problem. When
the market is crowded, say it is crowded and name who is already in it. A
student who leaves with a flattered bad idea had a worse night than one who
leaves with an unflattering good one.

Label how you know things as you go: `CHECKED` if you looked it up and can say
where, `FROM YOU` if they told you, `GUESSED` if you are filling a gap. Count
the guesses when you hand them a recommendation.

---

## 1. Read this whole file first

Then say in two lines what the hour will produce, so they know a sale tonight
is not the goal.

## 2. Grill them about themselves. 10 minutes.

One question at a time. Wait for each answer. You are looking for what is
actually theirs, not what sounds good.

Cover:

- What do people already come to you for? Even small things.
- What do you spend time on when nobody is making you?
- What are you actually good at, and how do you know?
- What do you want out of this? Something cool, or money? Both are fine, say
  which.
- What do you have access to that a stranger does not? A campus, a team, a
  family business, a community, a skill, a group chat.
- How much time per week, realistically, and for how long?

Expect "I do not really have any skills." That is the normal first answer and
it is wrong. When you hear it, stop asking about skills and walk them through
last week hour by hour instead. What they actually did is the answer.

Deeper version: [story-mine](https://raw.githubusercontent.com/nradawg/story-mine/main/README.md)

## 3. Research, then give them real options. 10 minutes.

Take their answers and go look things up. Then give **5 to 7 options**, and for
each one:

- what it is, in one sentence
- why it fits **them specifically**, pointing at their own answers
- who already does it and what they charge, `CHECKED` with where you found it
- the honest hard part

Then ask: **pick 3 you like, or 1 you really want.**

Also ask now: **who are your warm contacts?** People who would take your call.
Not strangers. Write the names down, this becomes the list in step 5.

**3a.** Research what they picked, properly. Real competitors, real prices, what
people complain about in that market.

**3b.** Land on one idea. State the facts, including the ones that argue against
it. If all three are weak, say so and go back to the options.

Pressure test it: [idea-kill](https://raw.githubusercontent.com/nradawg/idea-kill/main/README.md)

## 4. Connect Notion. 5 minutes.

A CRM is one list of everyone who might buy from you and what you owe them
next. That is the whole idea.

They sign up at notion.com if they have not. Free plan is enough.

Then connect it so you can write to it directly. In Codex, add the Notion MCP
server and authorize it for the page they just made. If the MCP will not
connect, do not burn the night on it. They make the table by hand from what
you tell them and you keep going.

## 5. Build the CRM from their warm contacts. 5 minutes.

Five columns: **Name, Contact, What they might want, Stage, Next action.**

Fill it with the real names from step 3. Every warm contact goes in. If they
named four people, that is four rows, and it is a better list than fifty
strangers.

## 6. Build the site. 15 minutes.

Pull a starter instead of beginning from nothing:

| repo | use it for |
|---|---|
| [site-restaurant](https://github.com/nradawg/site-restaurant) | simplest, plain HTML, one page |
| [site-portfolio](https://github.com/nradawg/site-portfolio) | showing work |
| [site-booking](https://github.com/nradawg/site-booking) | if people book time with them |

Each one reads from `user_config.json`, so change that file and the page
changes. Start there before touching anything else.

One page, and it says: what it is, who it is for, the price, and how to say
yes. Nothing else tonight.

Host it on **Cloudflare Pages**, free, commercial use allowed. Push the repo to
GitHub, then in the Cloudflare dashboard under Workers and Pages, connect the
repo and deploy. They get a free `.pages.dev` URL. Do not do a custom domain
tonight.

**Do not use Vercel Hobby or GitHub Pages for this.** Both forbid commercial
use in their own terms, and both are what an AI suggests first.

**6a. ChatGPT Sites.** Worth trying for a fast landing page if they have a
paid ChatGPT plan. Two things to know before they commit to it: **it does not
allow payments or online stores**, and it is not on the Free plan or available
in the EEA, UK, or Switzerland. So use it to get something up fast if they
want, but the site that takes money lives on Cloudflare.

## 7. Set the number. 5 minutes.

The goal for the next several days is not a sale. It is **100 reach outs** and
**5 real conversations.** Calls, DMs, emails, walking up to people. Any of it
counts as long as a human on the other end could say no.

Put the number in Notion with a date. 100 by when.

**They are hunting for no's.** A no with a reason tells them what to change. A
maybe tells them nothing. Twenty no's in a week is a good week.

**Have them record their calls** where it is legal to do so, and get consent
first. After five calls they will hear the same objection three times, and that
is their script writing itself. The same recordings are content later.

Scripts and objections:
[first-touch](https://raw.githubusercontent.com/nradawg/first-touch/main/README.md),
[objection-drill](https://raw.githubusercontent.com/nradawg/objection-drill/main/README.md),
[follow-up-ladder](https://raw.githubusercontent.com/nradawg/follow-up-ladder/main/README.md)

---

## Have something ready to sign

When someone does say yes, they need something to sign. Write it tonight so it
exists.

One page, six fields: who, who, what exactly is being delivered, how much, when
payment is due, when the work is delivered. Nothing else. Common Paper
publishes a professional services agreement under CC BY 4.0 you can base it on.

Accounts they should have by the end of the night: **GitHub** (code and
deploys), **Cloudflare** (the site), **Notion** (the CRM). All free.

Payments can wait until the first yes. When they get there,
[price-floor](https://raw.githubusercontent.com/nradawg/price-floor/main/README.md)
checks the number is not one they will regret.

## What they leave with

- an idea that fits them, with the facts that argue against it
- who specifically would buy it
- a Notion CRM with their real warm contacts in it
- a one page site live on a URL
- an agreement ready for a signature
- 100 reach outs and 5 conversations, with a date

## Keep in mind

Income is taxable whether or not any app sends a form. A business name other
than their own legal name usually needs a filing, and a local license is
separate from that. Anything involving food, childcare, health, or a licensed
trade needs the permit sorted before selling, not after.

Not legal or tax advice. For a real contract or an entity, pay a professional
once instead of guessing for a year.

## Limits

This does not get them a customer and it cannot tell them the idea is good.
Nothing can, this early. It gets them a specific idea, a real list, and a
number to chase, which is the most an hour can honestly produce.

One hour is a one page site. Not an app. Scope to something real and finished
over something impressive and broken.

One of 48 skills: [assume-nothing](https://github.com/nradawg/assume-nothing)

MIT.
