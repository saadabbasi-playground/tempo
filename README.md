# Tempo — Deep Work Focus Timer

A focus timer built around the ideas in Cal Newport's *Deep Work*: protect a daily block, work towards a concrete goal each session, know how much of your time is actually deep, and build your focus stamina gradually.

It combines:

- **Time-blocking (anchors)** — fixed daily blocks like deep work or gym
- **Goal-based focus sessions** — every session starts with what "done" looks like and ends with an honest check
- **Deep vs shallow tracking** — see what share of your focus time is real deep work
- **A deep work ladder** — train from 30 to 60 to 90-minute sessions
- **Eisenhower matrix** — sort tasks by what actually matters

It runs entirely in your browser. No account, no server — your data stays on your device.

---

## Getting started (deploy to GitHub Pages)

1. In your GitHub repository, upload these files to the **root** of the repo (not a subfolder):
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `README.md`
2. Go to **Settings → Pages**. Under **Source**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
3. After a minute, the app is live at `https://<your-username>.github.io/tempo/`.

> `manifest.json`, `sw.js` and the icons must sit next to `index.html`. If they're in a subfolder, the app still loads but can't be installed properly or work offline.

**Install it like an app:** open the link on your phone or desktop, then choose **Add to Home Screen** (iPhone: Share → Add to Home Screen) or click the install icon in the address bar (desktop). It works offline after the first load.

**Updating later:** when you change `index.html`, also bump the version in `sw.js` (`tempo-v2` → `tempo-v3`) so installed copies pick up the new version.

---

## How to use it

The app has three tabs: **Focus**, **Plan**, and **Stats**.

### 1. Plan your day (Plan tab)

**Set your anchors.** Anchors are the fixed blocks that structure your day. Give each one a name, a start time and an end time, then press **Add anchor**. They appear as orange arcs on the 24-hour dial in the Focus tab.

Make one of them your **deep work block**: a window you protect like a meeting with your most important client. Most people find one daily block is the most realistic approach — the first 1–3 hours of the morning works well for many.

**Add your tasks.** Type a task, pick a quadrant, choose **Deep** or **Shallow**, then press **Add task**.

| Quadrant | Meaning | What to do |
|---|---|---|
| Do first | Urgent + important | Focus on these today |
| Schedule | Important, not urgent | Plan time for these — this is where real progress happens |
| Delegate / batch | Urgent, not important | Hand off or batch into one block |
| Drop | Neither | Question why it's on the list at all |

**Deep or shallow?** Ask yourself: *how long would it take to train a smart, motivated person to do this task?*

- **Weeks or months → Deep.** Writing, designing, building, solving hard problems.
- **A day or two → Shallow.** Email, messages, admin, updating spreadsheets, most meetings.

Tap a task's **deep / shallow** tag to switch it. Tick ✓ to mark a task done, or × to delete it.

### 2. Run a focus session (Focus tab)

1. **Pick a task** from **Next up** (optional). Its deep/shallow tag sets the session type automatically.
2. **Write what "done" looks like.** Something concrete you can check at the end, like *"First draft of section 2 written"* — not *"work on the report"*. You can't start a focus session without one.
3. **Choose Deep or Shallow** if you didn't pick a task.
4. **Choose a length:** `25` (classic Pomodoro), `30`, `60` or `90` minutes. Each preset sets a matching break (5, 5, 10, 15). You can also type custom lengths.
5. Press **Start focus**. Put your phone in another room — even face down on the desk it still pulls on your attention.
6. When the timer ends, Tempo asks **Did you hit your goal?** Answer **Hit it**, **Partly** or **Missed**. Be honest — this is what makes your stats useful.
7. A break is queued. Press **Start break**, step away from the screen, then repeat.

Once a session starts, the goal, type and length are locked until it ends or you press **Reset**. Resetting discards the session.

**Reading the dial:**
- **Outer ring** = your whole day (24 hours). Orange arcs are your anchors; the thin hand shows the time right now.
- **Inner ring** = the current session counting down. Blue for deep, grey-green for shallow and breaks.

### 3. Build your deep work muscle

**Deep work today meter.** Shows today's deep minutes against a **240-minute (~4 hour) ceiling**. Research on elite performers suggests about four hours of real deep work a day is the practical limit; past that, quality drops. When you cross it, the meter turns orange — switch to shallow work or rest.

**Deep level ladder.** Focus is a muscle, so Tempo starts you at **30 minutes** and builds up:

- Complete **5 deep sessions** at your current level (or longer) and Tempo offers to move you up: **30 → 60 → 90 minutes**.
- Shorter deep sessions don't count towards the level but don't hurt it either.
- A **Missed** goal resets the count — it's a signal to consolidate before stepping up.
- Press **Not yet** to stay at your current level; Tempo asks again after your next session.

The first week of protected deep work usually feels restless and uncomfortable. That's normal — it typically gets easier within a couple of weeks.

### 4. Review your progress (Stats tab)

| Card | What it tells you |
|---|---|
| Focus min · 14 days | Total focus time |
| Sessions · 14 days | Completed sessions |
| Day streak | Days in a row with at least one completed session |
| **Deep ratio** | Deep minutes ÷ (deep + shallow minutes). Most people are surprised how low this is at first |
| **Goals hit** | Share of sessions where you hit your goal, plus the hit / partly / missed split |
| **Deep level** | Your current ladder level and progress to the next |

The bar chart stacks each day's **deep** (blue), **shallow** (grey-green) and **untagged** minutes. Untagged minutes come from sessions logged before this version.

---

## Tips for getting the most out of it

- **Audit before you change anything.** Tag a normal week honestly and look at your deep ratio. Seeing the real number is the first step.
- **Protect one block a day.** Put it in your anchors and treat it as non-negotiable.
- **Make goals small and concrete.** A session with a clear finish line becomes a game you can win.
- **Remove distractions, don't manage them.** Phone in another room, notifications off, same place each time so your brain links that spot with focus.
- **Practise being bored.** Resist reaching for your phone in queues and small gaps. Constant stimulation in the gaps makes it harder to stay with one hard task later.
- **Live in "Schedule".** If most of your work sits in Urgent + Important, you're firefighting.
- **Don't break the chain.** One completed session a day keeps the streak alive.

---

## Notes

- Data is stored in your browser (localStorage). Clearing site data resets the app, and data doesn't sync between devices.
- Sessions and tasks from earlier versions still work. Older tasks show a **tag** button so you can mark them deep or shallow; older sessions count as **untagged** in stats.
- Works in any modern browser; no build step or dependencies.
