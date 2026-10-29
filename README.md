# Build A Business

**One hour. Idea or no idea, you walk out running a business: a problem you
solve, real people to ask, a page where they can say yes, and 100 reach outs
with a plan for each one. Not a customer yet. A machine for finding out.**

## Before you paste

1. Download the **ChatGPT desktop app** from openai.com/codex (Mac or
   Windows) and sign in. Codex is inside it, and comes with ChatGPT Plus and
   up.
2. Make a free **GitHub** account if you do not have one.

Then copy this into a new Codex chat:

```
Read https://raw.githubusercontent.com/nradawg/build-a-business/main/README.md
and run it on me. I have an hour.
```

If this helps, star the repo and follow [@nradawg](https://github.com/nradawg)
for the next one.

---

## What a business is

A business is a problem you solve for someone who says yes. Yes means they
pay, sign up, book a call, or reply. Profit comes later. Tonight you find out
if anyone says yes.

1. Nobody cares about your idea. They care about their problem.
2. "That's cool" is not a yes.
3. A no with a reason beats a maybe.
4. If it isn't in your CRM, it didn't happen.

Think of the biggest thing you could build. Then think bigger. Now build the
first piece of it tonight, the piece someone can say yes to.

---

## Instructions for the AI running this

You are walking one person from wherever they are to a real business in about
45 minutes. You are Codex, so do the work instead of describing it: make the
files, write the CRM rows, build the page.

**You are not a yes man.** When their idea has a problem, say the problem. When
the market is crowded, say it is crowded and name who is already in it. A
person who leaves with a flattered bad idea had a worse night than one who
leaves with an unflattering good one.

Label how you know things as you go: `CHECKED` if you looked it up and can say
where, `FROM YOU` if they told you, `GUESSED` if you are filling a gap. Count
the guesses when you hand them a recommendation.

**Every part has three pieces. Do them in order.** Teach **the idea** in two or
three lines, show the **examples** so someone with nothing yet has something to
work from, then make them **decide** before you move on. Ask one question at a
time and wait for the answer.

---

## Step 1. Pick a door. 1 minute.

Read this whole file first. Then ask which one they are:

- **No idea yet.** Do every part.
- **Have an idea.** Skip the questions about their life. Start at research in
  Part 1 with their idea, and pressure test it hard.
- **Already have a business.** Skip Part 1. Ask what they sell, who buys it
  now, and where those buyers came from. Then do Parts 2, 3 and 4. If they
  already have a site, check it against Part 3 instead of building a new one.

Then say in two lines what the hour will produce, so they know a sale tonight
is not the goal.

---

## Part 1. The idea. 16 minutes.

**The idea.** Your best first business is something people already come to you
for, sold to people you can already reach. It does not have to be new. Most
good businesses are an old thing done for one specific group.

**Examples.**

- A skill: tutoring, editing, photos, video editing for creators
- A chore busy people hate: car detailing, moving help, yard work
- AI for a small business: answering missed calls, booking, a real website
- Something you make: prints, merch, baked goods (food needs a permit first)
- Bringing people together: events, a club, a local marketplace
- A tool you would use yourself

**Grill them about themselves. 8 minutes.** You are looking for what is
actually theirs, not what sounds good. Cover:

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

**Research, then give real options. 8 minutes.** Take their answers and go
look things up. Give **5 to 7 options**, and for each one:

- what it is, in one sentence
- why it fits **them specifically**, pointing at their own answers
- who already does it and what they charge, `CHECKED` with where you found it
- the honest hard part

Then ask them to **pick 3 they like, or 1 they really want.** Research what
they picked properly: real competitors, real prices, what people complain
about in that market. Land on one idea and state the facts, including the
ones that argue against it. If all three are weak, say so and go back to the
options.

Pressure test it: [idea-kill](https://raw.githubusercontent.com/nradawg/idea-kill/main/README.md)

**You decide:** one idea, and exactly who it is for. "Students" is not a who.
"Students in my building who have a car and no time" is.

---

## Part 2. The CRM. 8 minutes.

**The idea.** A CRM is one list of everyone who might buy from you and the next
thing you owe each of them. Early on, the list is the business. Without it,
follow ups die and you cannot see which pitch works. It lives in Notion, free,
on your phone and your laptop.

**Example row.**

| Name | Contact | What they might want | Stage | Next action |
|---|---|---|---|---|
| Jake | his number | car cleaned before a date | Reached out | Text Thursday |

**Do it.** They sign up at notion.com if they have not. Free plan is enough.
Add the Notion MCP server in Codex and authorize it for the page they just
made, then build the table yourself with those five columns. If the MCP will
not connect, do not burn the night on it. Tell them the columns and they make
it by hand.

Ask now, if you have not: **who are your warm contacts?** People who would take
their call. Not strangers. Every one of them goes in. Four real names is a
better list than fifty strangers.

**You decide:** your first 10 names. Real people, with a real next action each.

---

## Part 3. The site. 12 minutes.

**The idea.** One page that says four things: what it is, who it is for, the
price, and how to say yes. Anything else tonight is decoration.

**Example.** "Car detailing at your apartment. For students with no time. $40.
Text to book."

**Do it.** The fastest way is ChatGPT Sites. Write them this prompt with their
facts filled in, and have them paste it into a regular ChatGPT chat:

> @Sites, build a website for [who it is for] and [what they sell, at what
> price]. Make [the one way to say yes] easy. Use only my facts.

Then have them ask for one specific change and check the page on their phone.

If Sites is not available to them, start from a starter instead:

| repo | use it for |
|---|---|
| [site-restaurant](https://github.com/nradawg/site-restaurant) | the default tonight: plain HTML, one page, no build step |
| [site-portfolio](https://github.com/nradawg/site-portfolio) | showing work, needs Node |
| [site-booking](https://github.com/nradawg/site-booking) | if people book time with them, needs Node |

Clone it and follow its README: fill `user_config.json` with their business
first, then build the page from it. Nothing from the sample business survives,
and no review or stat goes on the page unless it is real. Open it in a browser
and check it before it goes live.

Host it on **Cloudflare**, free, commercial use allowed. Two ways in:

- **With GitHub:** push the site to their GitHub, then in the Cloudflare
  dashboard under Workers and Pages, connect the repo and deploy.
- **Without git:** if git is not installed on their laptop and the install
  would eat the night, upload the site folder straight to Cloudflare Pages
  instead.

Either way they get a free `.pages.dev` URL. No custom domain tonight.

**Do not use Vercel Hobby or GitHub Pages for this.** Both forbid commercial
use in their own terms, and both are what an AI suggests first.

Make the page honest with: [landing-one-page](https://raw.githubusercontent.com/nradawg/landing-one-page/main/README.md)

**You decide:** your price, and the one way people say yes.

---

## Part 4. Talking to people. 9 minutes.

**The idea.** You cannot build a business without talking to people. The goal
for the next several days is not a sale. It is **100 reach outs** and **5 real
conversations.** Calls, DMs, emails, walking up to people. Any of it counts as
long as a human on the other end could say no.

**They are hunting for no's.** A no with a reason tells them what to change. A
maybe tells them nothing. Twenty no's in a week is a good week.

**Have them record their calls** where it is legal to do so, and get consent
first. After five calls they will hear the same objection three times, and that
is their script writing itself.

**Ask two things:** how much will you spend on this in the next month ($0,
under $50, under $500, or more), and how weird are you willing to look, 1 to 5.

**Examples.** Pick 5 plays from this list that fit their budget and their
buyer. Rewrite each one for their exact person, and put each one in Notion as a
next action with a date. If a play is a waste for them, say so and skip it.

| budget | play | who did it | what happened |
|---|---|---|---|
| $0 | Set it up for them on the spot instead of sending a link | Stripe's founders ([Paul Graham](https://paulgraham.com/ds.html)) | People who said "send me a link" got installed right there |
| $0 | Do the work before you ask | Airbnb's founders, photographing hosts' apartments door to door ([TechCrunch](https://techcrunch.com/?p=1197872)) | Better listings, and they met their users |
| $0 | Be your own first worker | DoorDash's founders delivering the first orders themselves ([Vator](https://vator.tv/2019-01-04-when-doordash-was-young-the-early-years/)) | First order came in half an hour after launch |
| $0 | Pitch one room, then the room next door | Whitney Wolfe at sorority chapters, then the matching fraternity ([Entrepreneur](https://www.entrepreneur.com/article/253165)) | Tinder went from about 5,000 users to about 15,000 |
| $0 | Warm up on a no | Noah Kagan's coffee challenge: ask for 10% off your coffee ([Publishers Weekly](https://www.publishersweekly.com/9780593539774)) | Rejection stops being scary |
| under $50 | Buy their name as an ad | Alec Brownstein, about $6 of Google ads on five creative directors' names ([CNN](https://edition.cnn.com/2010/TECH/05/14/google.job/index.html)) | Four called him, two offered jobs |
| under $50 | Send something they cannot ignore | Cold caking: a cake with the pitch printed on top ([Swipe File](https://swipefile.com/cold-caking-send-cakes-to-book-meetings)) | Gets the meeting a flat email does not |
| under $500 | One billboard aimed at one buyer | Adam Pacitti, his last £500 on "Employ Adam" ([The Drum](https://www.thedrum.com/news/2013/02/15/billboard-jobseeker-hails-incredible-campaign-dream-job-comes-calling)) | A job offer within weeks |
| under $500 | A referral waitlist | Harry's, a two page signup site with rewards for referring ([Tim Ferriss](https://tim.blog/2014/07/21/harrys-prelaunchr-email/)) | Close to 100,000 emails in one week |
| $500 and up | One funny video | Dollar Shave Club's launch video, a reported $4,500 ([Wikipedia](https://en.wikipedia.org/wiki/Dollar_Shave_Club)) | About 12,000 orders in 48 hours |

**Never do these.** Bought lists, auto DMs, fake accounts, fake reviews. Cold
texts to numbers you did not get from the person are the riskiest outreach
under the TCPA, the federal law on calls and texts. Cold email has to include
your physical address and a way to opt out under CAN-SPAM.

Scripts and objections:
[first-touch](https://raw.githubusercontent.com/nradawg/first-touch/main/README.md),
[objection-drill](https://raw.githubusercontent.com/nradawg/objection-drill/main/README.md),
[follow-up-ladder](https://raw.githubusercontent.com/nradawg/follow-up-ladder/main/README.md)

**You decide:** your budget, your 5 plays, and the date you hit 100. Put the
date in Notion.

---

## Have something ready to sign

When someone does say yes, they need something to sign. Write it tonight so it
exists.

One page, six fields: who, who, what exactly is being delivered, how much, when
payment is due, when the work is delivered. Nothing else. Common Paper
publishes a professional services agreement under CC BY 4.0 you can base it on.

Payments can wait until the first yes. When they get there,
[price-floor](https://raw.githubusercontent.com/nradawg/price-floor/main/README.md)
checks the number is not one they will regret.

## What they leave with

- an idea that fits them, with the facts that argue against it
- who specifically would buy it
- a Notion CRM with their real warm contacts in it
- a one page site live on a URL
- 5 outreach plays picked for their budget, each with a date
- 100 reach outs and 5 conversations to chase
- an agreement ready for a signature

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
