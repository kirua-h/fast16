# Product Specification

## Overview

Fast16 is an iPhone application for managing 16-hour intermittent fasting.

The app is designed to be extremely simple.
The user only needs to press one button when starting a meal.

The app continuously displays the remaining fasting time and the next available eating time.

---

# Target Platform

- iPhone
- iOS only

---

# MVP Goals

The first version of the application must provide only the following features.

## Features

- Record meal start time
- Store the latest meal start time locally
- Calculate the end of a 16-hour fasting period
- Display remaining fasting time
- Display next available eating time
- Continue working after the app is restarted

No additional features should be implemented unless explicitly requested.

---

# Screens

## Home Screen

Displays:

- App title
- Fasting status
- Remaining fasting time
- Next available eating time
- Previous meal start time
- Meal Start button

There is only one screen in MVP.

---

# User Flow

User opens the app.

↓

Remaining fasting time is displayed.

↓

User starts eating.

↓

Presses "Start Meal".

↓

Current date and time are saved.

↓

16-hour fasting timer starts.

↓

Countdown updates automatically.

---

# Meal Button

When pressed:

- Save current date and time
- Restart fasting timer
- Refresh UI immediately

No confirmation dialog.

---

# Data Storage

Only one value is stored.

```

lastMealTime: Date

```

Storage:

- AsyncStorage

---

# UI Principles

The application should feel like a native Apple application.

Principles:

- Minimal
- Calm
- Large spacing
- Clear typography
- One primary action
- Countdown is the most important element

---

# Non Goals (MVP)

Do NOT implement:

- Authentication
- Cloud sync
- Social features
- Ads
- Notifications
- History
- Weight tracking
- Widget
- Apple Watch
