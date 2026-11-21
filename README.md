<p align="center">
  <img src="assets/VireoIcon.svg" alt="Vireo icon" width="140" height="140">
</p>

<h1 align="center">Vireo</h1>

<p align="center">
  <strong>The private AI agent that does real work on your Mac.</strong><br>
  Hand it a job, not just a question. It works through your files, plans the steps,<br>
  checks its work and asks before it changes anything.<br>
  Open models like Gemma 4 and Qwen 3.5, on Vireo's own engine, Syrinx. Nothing leaves your Mac.
</p>

<p align="center">
  <a href="../../releases/latest"><img src="https://img.shields.io/github/v/release/InvurseStudio/Vireo-app?label=latest&color=5B4FD6&style=flat-square" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/macOS-14%2B-17171C?logo=apple&logoColor=white&style=flat-square" alt="macOS 14 or later">
  <img src="https://img.shields.io/badge/Apple%20Silicon-M1%20or%20later-17171C?logo=apple&logoColor=white&style=flat-square" alt="Apple Silicon">
  <a href="https://github.com/InvurseStudio/Syrinx"><img src="https://img.shields.io/badge/engine-Syrinx-5B4FD6?style=flat-square" alt="Engine: Syrinx"></a>
  <img src="https://img.shields.io/badge/made%20in-Canada%20%F0%9F%8D%81-C9C1FF?style=flat-square" alt="Made in Canada">
</p>

<p align="center">
  <a href="../../releases/latest"><img src="https://img.shields.io/badge/Download%20for%20Mac-5B4FD6?logo=apple&logoColor=white&style=for-the-badge" alt="Download for Mac"></a>
</p>

---

## New in 0.9.3: a faster Inkling 2 Mini

- **About twice as fast at reading, and quicker to write.** On an M5 Max, Inkling 2 Mini
  now reads about 2,950 tokens a second and writes about 65 with 8K of context.
- **A drafter for faster replies.** Inkling's small DSpark drafter (400 MB) downloads with
  it and guesses ahead for Inkling to check: code and copied text are written about
  25–40% faster, and every word is still Inkling's own.
- **Chats pick up where they left off.** Inkling chats are now saved, so going back to one
  loads it in a fraction of a second, and new chats start sooner.
- **A smaller version for 32 GB Macs.** Inkling 2 Mini (smaller) is the 4-bit IQ4_NL
  version, a 17.6 GB download that scores almost the same in our tests.

The full list is in the [0.9.3 release notes](../../releases/tag/v0.9.3).

## New in 0.9.2: Inkling 2 Mini

- **A new model.** Thinking Machines' **Inkling 2 Mini** is in Settings › Models for Macs
  with 48 GB of memory or more: a mixture-of-experts model (26B in all, 3.4B working on
  each token) that thinks before it answers and uses Vireo's tools. On an M5 Max it reads
  about 1,450 tokens a second and writes about 50, and it got all 14 of our agent and
  coding test tasks right.
- **A more careful model picker.** Versions of a model that Syrinx can't run (such as
  IQ4_NL, Q2_K and Q3_K) are no longer offered, so Vireo can't suggest a download that
  won't load.
- **Less memory held between replies.** At most 4 GB of recent chats stay ready in
  memory, and older ones already saved to disk are let go when Vireo is idle.

The full list is in the [0.9.2 release notes](../../releases/tag/v0.9.2).

## New in 0.9.1: Vireo's own engine

Vireo now runs on **[Syrinx](https://github.com/InvurseStudio/Syrinx)**, an engine
built for Vireo. It replaces the Python server and the separate MLX and llama.cpp
runtimes that 0.9 started.

- **One small download.** A 10 MB download (about 27 MB installed, down from about 850 MB), with nothing else to install. No bundled
  Python and no background services: Start Model loads the model, and quitting
  Vireo frees the memory.
- **Built for agent work.** Syrinx is tuned for the models Vireo recommends and for
  the way an agent works: long instructions, tool results and checking its work.
  Going back to a chat picks up where it left off instead of reading the whole
  conversation again.
- **Straight on your Mac's GPU,** with GGUF models: Gemma 4, Qwen 3.5, Inkling 2 Mini
  (from 0.9.2) and Llama.

Updating from 0.9 keeps your chats, memories, skills, approvals and API keys. A few
0.9 features are gone for now; see [Coming from Vireo 0.9](#coming-from-vireo-09).

## An agent, not just a chat window

Give Vireo a job and it gets on with it. It reads your files, uses tools on your Mac,
works through each step and comes back with the work done, not just an answer.

- *"Process the November invoices in Finance and log them in the tracker."*
- *"Sort these donation requests against our policy and draft the replies."*
- *"Fill the sponsorship template for Harbour Lane, then make a slide deck from it."*
- *"Check this trip against the travel policy and work out the per diems."*
- *"Every morning at 8, sum up yesterday's new files in Inbox."*

**How a job runs**

1. **It plans.** Longer jobs get a short checklist, and you can see the step it's on.
2. **It uses real tools.** It reads Word, Excel, PowerPoint, PDF, Pages, Numbers and
   Keynote files and writes Word, Excel, PowerPoint and PDF, searches your files,
   earlier chats and the web, checks your calendar and reminders, runs your
   Shortcuts, and does sums with an exact calculator.
3. **It follows your rules.** It reads the policy that applies, flags what doesn't
   fit, and marks things as pending until someone approves them.
4. **It doesn't bluff.** If a reply says it saved, sent or changed something it
   didn't, Vireo says so under the reply.
5. **You approve, and can undo.** Changes wait for your OK, and **Undo this run**
   puts back any files it changed.
6. **It learns.** Ask it to save how it did a job as a skill, and it remembers the
   people and facts that matter, once you approve.

It can also work on its own: on a schedule, when new files arrive in a folder, or
when a private link is opened on your Mac. Changes it wants to make still wait for you.

## Why Vireo

<table>
<tr>
<td width="50%" valign="top">

### 🔒 Private by design
The model runs on your Mac and your chats are saved there. No account, no cloud,
no analytics. Nothing to sign up for.

</td>
<td width="50%" valign="top">

### ⚡ Its own engine
Syrinx runs models straight on your Mac's GPU, tuned for the models Vireo
recommends. One small app, nothing else to install.

</td>
</tr>
<tr>
<td valign="top">

### 🔎 Pick your model
Gemma 4 and Qwen 3.5 are tested and tuned for agent work, and Inkling 2 Mini is there
for Macs with 32 GB or more. Search Hugging Face from
the app for other GGUF models, see at a glance whether one fits your Mac, or add a
folder of models you already have, such as an LM Studio library.

</td>
<td valign="top">

### 📎 Works with your files
Word, Excel, PowerPoint, Pages, Numbers, Keynote, PDFs and text. It reads them,
fills Word and Pages templates, updates spreadsheets, and creates documents, PDFs
and slide decks.

</td>
</tr>
<tr>
<td valign="top">

### ✅ You stay in control
Changing files, running commands and sending messages all wait for your approval.
You see each step as it works, and **Undo this run** puts back any files it changed.

</td>
<td valign="top">

### 🧩 Works with your other apps
Other apps on your Mac can use your model through an OpenAI-compatible API at
`http://localhost:3000/v1`, like they would OpenAI or LM Studio. It's off until
you turn it on in Settings › Developer.

</td>
</tr>
<tr>
<td valign="top">

### 🗓️ Keeps track of your day
Ask what's on today, find a free hour, or add, move and complete events and
reminders. Hand off routine jobs to run on a schedule or when new files arrive.

</td>
<td valign="top">

### ✨ Quick Ask, from any app
A small panel over whatever you're doing, plus the menu bar, Services and
Shortcuts actions.

</td>
</tr>
</table>

## Tested on real work

Vireo is tested on a month of made-up office work: 32 tasks covering invoices,
donations, events, travel, expenses and inventory, plus four safety traps. Each
answer is graded by hand. All test data is fictional.

**Vireo 0.9.1 on Syrinx**, Gemma 4 31B, the night it shipped:

| | Fully right (of 32) | Partly right | Wrong | Time |
| --- | --- | --- | --- | --- |
| Vireo 0.9 (after its fixes) | 25 | 7 | 0 | 52 min |
| **Vireo 0.9.1** | **21** | **11** | **0** | **32 min** |

0.9.1 finishes the same work about 40% faster with no wrong answers. It gets a few
more tasks only partly right; those are the next thing being worked on.

Before 0.9 shipped, three models ran the same test, and the problems found on
Vireo's side were fixed before it was run again:

| Model (Vireo 0.9) | Fully right (of 32) | Partly right | Wrong | Time |
| --- | --- | --- | --- | --- |
| Gemma 4 31B | 22 → **25** | 9 → 7 | 1 → **0** | 59 → **52** min |
| Muse Glimmer 30B | 16 → **24** | 15 → 8 | 1 → **0** | 86 → **79** min |
| Qwen 3.8 27B | 20 → **27** | 10 → 5 | 2 → **0** | 132 → **118** min |

The [0.9 before-and-after report](test-results/Vireo-0.9-Before-After.pdf) (PDF)
goes through every task in plain language.

## Download

Grab the latest version from the **[Releases page](../../releases/latest)**. Each
release is a single file: `Vireo-<version>-arm64.dmg`.

Vireo needs a Mac with Apple silicon (M1 or later) and macOS 14 or later.

### Which model?

The first time you open Vireo it looks at your Mac's memory and recommends a model.
These are the ones Vireo is tested and tuned on:

| Model | Download |
| --- | --- |
| Gemma 4 E2B | ~3.4 GB |
| Gemma 4 E4B | ~5.2 GB |
| Qwen 3.5 4B | ~2.7 GB |
| Qwen 3.5 9B | ~5.7 GB |

For agent jobs on your own files, larger models do noticeably better. Vireo also
runs Gemma 4 26B and 31B and Qwen 3.8 27B, which suit Macs with 48 GB of memory or
more.

## Getting started

1. Open the DMG and drag **Vireo** to **Applications**.
2. Open Vireo. Setup recommends a model for your Mac and downloads it.
3. Ask a question, or give it a job. Attach files with **+** or by dragging them in.

### Coming from Vireo 0.9

Vireo updates itself to 0.9.1 like any other update. The first time 0.9.1 opens, it
copies your chats, memories, skills, approvals and settings across, and doesn't
change anything in 0.9's folder. Your GGUF models stay in your model list. MLX
models aren't supported any more; download the GGUF version of the model from the
app instead.

When everything's there, **Settings › Advanced › Files from Vireo 0.9** moves your
GGUF models into Vireo's folder and puts the rest of 0.9's files in the Trash.

**Not in 0.9.1:**

- **Coming back in a later update:** attaching pictures (Syrinx can't see images yet),
  watched folders and document search, the daily briefing, and MCP servers.
- **Removed:** MLX models, Apple's on-device model, mail triage, the search-service API
  keys (web search works without one), the iPhone and iPad companion apps, using Vireo
  on this Mac from another device, the Compare window, and skill suggestions after
  long tasks.
- **Scheduled tasks** made in 0.9 aren't carried over. Ask Vireo to set them up again.

The full list is in the [0.9.1 release notes](../../releases/tag/v0.9.1).

## Updates

Vireo checks for new versions and installs them for you (you can turn this off in
Settings, or choose **Vireo › Check for Updates…** at any time). Every update is
signed, and checked before it's installed.

## FAQ

<details>
<summary><strong>What's the difference between an assistant and an agent?</strong></summary>

An assistant answers. An agent does the work. Ask Vireo about a folder of invoices
and it can read each one, check them against your policy, add up the totals, log
them in your spreadsheet and draft the emails, showing each step as it goes. It
still asks before it changes anything.

</details>

<details>
<summary><strong>What is Syrinx?</strong></summary>

Vireo's own engine: the part that runs the model on your Mac's GPU. It's written in
Rust and built for Vireo and its models, and it's
[on GitHub](https://github.com/InvurseStudio/Syrinx). A syrinx is a songbird's voice
box; a vireo is a songbird.

</details>

<details>
<summary><strong>Will it change my files without asking?</strong></summary>

No. Writing, moving and deleting files, running commands, changing your calendar and
sending messages all wait for your approval. You can choose "Don't ask again" for
some kinds of change, but deleting files, running commands and Shortcuts always ask.
**Undo this run** puts back any files a job changed, and deleted files go to the Trash.

</details>

<details>
<summary><strong>Does it work offline?</strong></summary>

Yes. Once a model is downloaded, chats and agent jobs work with no internet
connection. Only web searches, model downloads and update checks need to go online.

</details>

<details>
<summary><strong>Does it work on an Intel Mac?</strong></summary>

No. Running models locally needs Apple silicon (M1 or later).

</details>

<details>
<summary><strong>Can I use my own models?</strong></summary>

Yes, in GGUF format. Search Hugging Face from the app, or add a folder of models you
already have. Vireo runs Gemma 4, Qwen 3.5 and 3.8, and Llama models; others are
hidden from the model picker.

</details>

<details>
<summary><strong>What about Windows, iPhone and iPad?</strong></summary>

A new Windows app on Syrinx is on the way. The old Windows client (0.7.5) only works
with Vireo 0.9 and earlier. The iPhone and iPad companion apps were retired with 0.9.1.

</details>

## About

Vireo is my first major app. I started it to learn how local AI really works:
running models on a Mac, streaming replies, tools, and connecting other devices.
Along the way it grew into the app I wanted to use every day, then into an agent
that can take real work off my plate, and now it runs on an engine of its own.

It's made by one person at Invurse Studio in Canada, and it's still early. It's also
signed and notarized by Apple, updates itself safely, and never collects your data.
If something's rough or you have an idea, [let me know](#feedback). Feedback is how
it gets better.

I used Claude, Anthropic's AI, along the way to find bugs, review code, and implement
fixes and polish.

## Privacy

Vireo collects nothing: no accounts, analytics or tracking. Read the full
[privacy policy](PRIVACY.md).

## Feedback

Found a bug or have an idea? [Open an issue](../../issues/new) on GitHub, or email
[hello@invursestudio.com](mailto:hello@invursestudio.com) if you don't have a GitHub
account.

---

<p align="center">
  <img src="assets/VireoIcon.svg" alt="" width="28" height="28"><br>
  Developed in Canada 🍁 by <strong>Invurse Studio</strong>
</p>
