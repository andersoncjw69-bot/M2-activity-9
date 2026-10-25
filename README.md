# Activity 09 — Health Data Reader

> **🛠️ Stack for this lesson** — Expo SDK 57 / React Native 0.86 + native platform APIs · runs in a development build on a real phone (native modules do not run in Expo Go).
> 📥 Template: [/learn/m2/template/activity-09-health-reader](/learn/m2/template/activity-09-health-reader)

A screen with an explanation card, a status line and a list slot. A manual-entry path is ready for iPhones, where Health Connect does not exist. You check availability, ask for permission, read the last 24 hours and show the records.

**Time:** ~45 min · **Concept:** Concept 10 — Health Connect Integration

---

## What You'll Build

| # | TODO | File |
|---|------|------|
| 1 | Check Health Connect; if it is missing, send the user to its Play Store page | `lib/healthConnect.js` |
| 2 | Ask for Steps and HeartRate access after the explanation | `App.js` |
| 3 | Read the last 24 hours of one record type | `lib/healthConnect.js` |
| 4 | Show each record in a list with its date and count | `components/StepsList.js` |

There are no commented-out solutions in the code. Each TODO states an outcome, a way to check it and a question to answer in your Notes doc. Read what is already there, work out what each TODO asks for, and write it.

**Already in the starter:** `App.js` (flow and explanation card); `lib/manualLog.js` and `components/ManualEntry.js` (the iPhone path).

## Run It

```bash
npm install --legacy-peer-deps
npx expo start --dev-client
```

Open your **development build** (the app from Activity 19) on a phone that is on the same Wi-Fi as your computer. It finds the running server and loads your code. Native modules do not run in Expo Go.

Android only. Install Health Connect, open it once and let a watch or fitness app write some steps. Add the Health Connect plugin and read permissions to `app.json` as Concept 10 shows, then rebuild your development build. On an iPhone the app uses the manual-entry form instead.

## Verify

Your activity is done when, on a real device:

- [ ] If Health Connect is missing, the app deep-links to the Play Store install.
- [ ] Your explanation shows before the system permission dialog.
- [ ] After granting, the list fills with the past 24 hours of step records.
- [ ] Heart-rate data appears, or the screen says there is none if your watch does not sync it.

## Stretch

Optional. Pick one and write a short note in your Notes doc about what you tried:

- **Your theme.** Read a record type that fits what you track, such as `Distance` or `TotalCaloriesBurned`, and show it in the same list.
- Add a 24 hour, 7 day and 30 day switch that re-queries.
- Show the sum at the top of the list.

## 🪞 Reflect on Your Work

Answer in 2-3 sentences each, in your Notes doc. Your tutor reads these as part of grading.

1. **What did you learn that you didn't know before?** Name the most surprising thing — a permission quirk, a platform difference, a debugging story.
2. **How did you collaborate with AI?** If you used Claude / ChatGPT / Cursor / Copilot, what part of the work did *you* contribute — the prompt, the verification, the design decision, the bug-fix? If you didn't use AI, what was the hardest thing to figure out alone?
3. **How do you know your code works?** Describe one specific thing you did to confirm — the device test you ran, the screenshot you took, the behavior you watched.

> AI is a great collaborator. Owning your thinking, verifying the output, and explaining your design choices is what *learning* looks like in this course.

## 📱 Device Evidence (required, 30% of grade)

Full marks need a real device, not a simulator or Expo's web preview. Link these in your Notes doc (`Activity 09 write-up`), under a heading **Device Notes**:

1. **`screenshot-portrait.png`** — one full-screen portrait screenshot from your device showing the list of step records, with the status bar visible (the clock and battery prove it is a real device).
2. **`recording.mp4`** — a 30–60 second screen recording of your real device showing the permission sheet, then the list filling.
3. **Device Notes** (80–150 words): the phone model and OS, what worked first try, the exact text of anything that broke, and what only the real phone showed you.

Grading: 70% feature works in code, 30% device evidence. "I tested in Expo Go web" is not device evidence.

## Submit

When the Verify checklist is green, submit the link to your Notes doc, then press **Mark as Complete**.

<!-- claude-template-fix: readme-v3 -->

<!-- claude-template-fix: notes-migration-v1 -->
