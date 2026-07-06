# Architecture

## Overview

Fast16 follows a simple layered architecture.

```

UI
↓
Components
↓
Hooks
↓
Storage / Utilities

```

---

# Folder Structure

```

app/
components/
hooks/
storage/
utils/
types/
assets/

```

---

# Responsibilities

## app/

Application entry point and screen definitions.

---

## components/

Reusable UI components.

Examples:

- Header
- Countdown
- MealButton
- StatusCard
- MealInfo

Components should remain small and focused.

---

## hooks/

Business logic.

Examples:

- useCountdown()

Hooks should not contain UI.

---

## storage/

Reading and writing local data.

Responsibilities:

- Save last meal time
- Load last meal time

Uses AsyncStorage.

---

## utils/

Pure helper functions.

Examples:

- Calculate remaining time
- Calculate next meal time
- Date formatting

Utility functions should not access storage.

---

# Data Flow

```

User taps Meal Button
↓

Current Date
↓

Save to AsyncStorage
↓

Update State
↓

Countdown recalculates
↓

UI refreshes

```

---

# State

MVP stores only:

```

lastMealTime

```

No global state management library is required.

React state is sufficient.

---

# Component Tree

```

HomeScreen

├── Header
├── StatusCard
├── Countdown
├── MealInfo
└── MealButton

```

---

# Design Principles

- Single responsibility
- Small components
- Functional components
- TypeScript only
- No duplicated logic
- Readability over cleverness

---

# Future Extensions

Architecture should allow future addition of:

- Meal history
- Weight tracking
- Widgets
- HealthKit
- Apple Watch
- Charts

These features are NOT implemented in MVP.
