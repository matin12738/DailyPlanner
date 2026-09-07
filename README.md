# 📓 Daftarche — Smart Life Planner

<div align="center">

**An all-in-one productivity system for managing goals, projects, habits, routines, daily tasks, and a focus timer**  
With Persian (Jalali) calendar, persistent storage, and a fully responsive UI

[![Version](https://img.shields.io/badge/version-12.0-blue)](https://github.com/your-username/daftarche)
[![Built with](https://img.shields.io/badge/built_with-Vanilla_JS-orange)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

</div>

---

## ✨ Overview

**Daftarche** (دفترچه) is a personalized productivity tool that helps you:

- Manage daily tasks with priority levels and categories.
- Track long‑term goals and projects with progress indicators.
- Build positive habits and visualize your streaks.
- Control daily routines with a single click.
- Stay focused using a Pomodoro timer.
- Keep a journal and capture quick notes.
- Analyze your performance with daily, weekly, and monthly charts.
- Use the Jalali (Persian) calendar for date selection.
- Automatically save your data in the browser and create backup copies.

---

## 🚀 Key Features

| Feature | Description |
|---------|-------------|
| 📋 **Task Management** | Add, edit, delete, search, and filter tasks by category, priority, and status. Drag‑and‑drop to reorder. |
| 🎯 **Goals & Projects** | Define goals and projects, link tasks to them, and see completion percentages. |
| 🔥 **Habits** | Log habits daily, track your streak, and link them to goals. |
| 🔄 **Routines** | Manage recurring daily routines with one click. |
| ⏱️ **Focus Timer (Pomodoro)** | Work, short break, and long break modes with customizable durations. Circular progress display and session counter. |
| 📅 **Jalali Calendar** | Monthly view with activity indicators (tasks, habits, pomodoros). Quick date picker. |
| 📊 **Performance Analytics** | Stats for task completion, habits, and pomodoros over 1‑day, 7‑day, and 30‑day periods. Bar charts included. |
| 📝 **Journal & Brain Dump** | Record achievements, challenges, and tomorrow's priorities. Quick, untitled notes for fleeting ideas. |
| 🌓 **Light/Dark Theme** | Instant theme switching with user preference persistence. |
| 💾 **Persistent Storage** | Uses IndexedDB with a localStorage fallback. Automatic saving after every change. |
| ⏪⏩ **Undo/Redo** | Go back and forward through your data history (up to 30 steps). |
| 📦 **Import/Export** | Export all data as a JSON file and re‑import it anytime. |
| 🔔 **Browser Notifications** | Alerts when a Pomodoro or break session ends (with user permission). |
| 📱 **Responsive Design** | Optimized for desktop, tablet, and mobile with a bottom tab bar and floating action button for adding tasks. |

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| **HTML5** | Page structure |
| **CSS3** | Styling and responsiveness (CSS variables for theming) |
| **JavaScript (ES6+)** | Application logic, data management, interactions |
| **IndexedDB** | Primary data storage |
| **localStorage** | Fallback and backup storage |
| **Sortable.js** | Drag‑and‑drop task reordering |
| **Font Awesome 6** | Icons |
| **Vazirmatn** | Beautiful Persian font |
| **Web Notifications API** | Desktop notifications |

---

## 📥 Installation & Setup

**Daftarche** is a single‑page application (SPA) – no installation required.

1. Download the `index.html` file from the repository.
2. Open it in your browser (Chrome, Firefox, Edge, Safari).
3. All your data is stored locally in your browser.

> 💡 **Tip**: For the best experience, use the latest version of a Chromium‑based browser or Firefox.

---

## 🧭 User Guide

### 1. Today View (Default)
- **Daily Tasks**: Shows tasks for the selected date. Click the `+` button to add a new task.
- **Pomodoro Timer**: Hit the play button to start. Switch modes using the tabs.
- **Date Navigation**: Use the previous/next week buttons, the Jalali date picker, or the Today button to change the date.

### 2. Growth Section (Goals, Projects, Habits, Routines)
- **Goals**: Define goals and link tasks to them.
- **Projects**: Similar to goals, but project‑oriented.
- **Habits**: Log them daily; streaks are calculated automatically.
- **Routines**: Recurring daily tasks that you can tick off with one click.

### 3. Mind Section (Journal & Brain Dump)
- **Journal**: Three fields to record today's achievement, today's challenge, and tomorrow's most important task.
- **Brain Dump**: Untitled notes for quick ideas, accessible anytime.

### 4. Analytics Section
- **Monthly View**: Jalali calendar with activity indicators.
- **Stats**: Today's task completion percentage, habit streaks, pomodoro count.
- **Charts**: Completed tasks over the last 7 and 30 days.

### 5. Settings & Tools
- **Theme Toggle**: Moon/sun button in the header.
- **Import/Export**: For backup or data migration.
- **Reset**: Clears all data (with confirmation).
- **Keyboard Shortcuts**:
  - `Ctrl+Z` / `Cmd+Z`: Undo
  - `Ctrl+Y` / `Cmd+Y`: Redo
  - `Ctrl+N` / `Cmd+N`: Add a new task
  - `Esc`: Close modals and popovers

---

## 🗄️ Data Structure

Data is stored in a JavaScript object with the following keys:

```json
{
  "selectedDate": "2026-09-07",
  "tasks": [
    {
      "id": "unique-id",
      "text": "Task title",
      "done": false,
      "date": "2026-09-07",
      "tag": "personal",
      "priority": "high",
      "recurrence": "daily",
      "goalId": "",
      "projectId": "",
      "note": "Additional note"
    }
  ],
  "goals": [
    { "id": "goal-id", "title": "Goal" }
  ],
  "projects": [
    { "id": "project-id", "title": "Project" }
  ],
  "habits": [
    {
      "id": "habit-id",
      "title": "Habit",
      "dates": { "2026-09-07": true },
      "goalId": ""
    }
  ],
  "routines": [
    {
      "id": "routine-id",
      "title": "Routine",
      "dates": { "2026-09-07": true }
    }
  ],
  "brainDump": [
    { "id": "brain-id", "text": "Quick note" }
  ],
  "journal": {
    "2026-09-07": {
      "success": "Today's achievement",
      "challenge": "Today's challenge",
      "next": "Tomorrow's priority"
    }
  },
  "pomodoroLog": { "2026-09-07": 5 },
  "timerSessionsCompleted": 10,
  "timerMode": "work",
  "timerSettings": {
    "workDuration": 25,
    "shortBreakDuration": 5,
    "longBreakDuration": 15,
    "longBreakInterval": 4
  },
  "uiPrefs": { "activeMobileTab": "today" }
}
```

---

## 🤝 Contributing

If you have ideas or improvements, we’d love your help:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Make your changes and test thoroughly.
4. Submit a Pull Request with a clear description of what you’ve done.

> 📌 **Note**: This project was built for learning and personal use, but any contributions to make it better are warmly welcomed.

---

## 🌟 Support

If you like this project, please give it a ⭐ and share it with others.

---

<div align="center">

**Built with ❤️ for better productivity**

</div>