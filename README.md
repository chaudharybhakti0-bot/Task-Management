Here's the README for the Focusly app:

---

# ✦ Focusly — Student OS

> A beautiful, dark-mode student task manager. Built with zero dependencies — just HTML, CSS, and vanilla JS.

---

## 🚀 Getting Started

No install. No build step. No npm.



---

## ✨ Features

- **Smart Greeting** — Greets you by name, shows today's date, and cycles through motivational quotes every 6 seconds
- **Progress Rings** — Animated SVG rings tracking Weekly Tasks, Assignments, and Exam Prep
- **Kanban Board** — Three columns (To Do / In Progress / Done) with real task cards. Click the circle to mark done
- **Deadline Timeline** — Right sidebar with live countdowns: `2d 4h left`, color-coded red/amber/green
- **Add Task Modal** — Floating `+` button opens a slide-up form. Fill in subject, priority, due date, and status
- **Reminder Ticker** — Scrolling bar at the bottom showing urgent reminders. Pauses on hover
- **Notification Bell** — Click to open a dropdown of alerts
- **Streak Counter** — Shows your current study streak in the navbar

---

## 🎨 Design

| Token | Value |
|---|---|
| Background | `#0a0a0f` |
| Primary | `#6366f1` (Indigo) |
| Accent | `#a3e635` (Lime) |
| Danger | `#f87171` (Red) |
| Warning | `#fbbf24` (Amber) |
| Success | `#4ade80` (Green) |
| Heading font | Syne 700/800 |
| Body font | DM Sans 400/500 |

---

## 📁 Structure

Everything lives in a single file:

```
focusly.html
├── <style>        → All CSS, variables, animations
├── <body>         → Navbar, sidebar, kanban, modal, ticker
└── <script>       → Task data, render logic, animations
```

---

## 🗂️ Task Data

Tasks are stored as a plain JS array at the top of the script. Each task looks like:

```js
{
  id: 1,
  title: "Solve Calculus Problem Set 4",
  subject: "Mathematics",
  priority: "high",      // "high" | "medium" | "low"
  due: "2025-04-17",
  status: "inprog"       // "todo" | "inprog" | "done"
}
```

To add your own default tasks, just push objects into the `tasks` array.

---

## ⚙️ Customization

**Change the student name** — Search for `Alex` in the HTML and replace it.

**Add a subject** — Add an `<option>` to the subject dropdown in the modal, add an emoji to `subjectEmoji`, and a color to `subjectColor`.

**Change streak count** — Find `🔥 14 days` in the navbar and edit the number.

**Adjust ring targets** — At the bottom of the script, change the percentages in:
```js
animateRing('ring1', 'ring1txt', 61);  // Weekly Tasks
animateRing('ring2', 'ring2txt', 63);  // Assignments
animateRing('ring3', 'ring3txt', 43);  // Exam Prep
```

---

## 🌐 Browser Support

Works in all modern browsers — Chrome, Firefox, Safari, Edge. No polyfills needed.

---

## 📄 License

Free to use, fork, and build on. Just don't ship it as your own product without changes. Give credit where it's due. 🙏
