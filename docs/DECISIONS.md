# Architectural Decisions

This document records important project decisions and why they were made.

---

## Use Expo

Reason:

- Faster development
- Easier maintenance
- Excellent AI support
- Sufficient for MVP

---

## iPhone Only

Reason:

- Better focus
- Better user experience
- Faster development

Android support may be considered later.

---

## One Screen Only

Reason:

- Minimize complexity
- Faster interaction
- Easier maintenance

---

## Apple-like Design

Reason:

- Timeless appearance
- Familiar interaction patterns
- Better readability

---

## No Notifications

Reason:

Notifications are not essential for the first version.

The user should be able to understand the fasting status simply by opening the app.

Notifications may be reconsidered in future versions.

---

## No History in MVP

Reason:

The first goal is validating the core fasting timer experience.

History will be implemented only after the core experience is stable.

---

## No Weight Tracking in MVP

Reason:

Weight tracking is valuable but not required to validate the core product.

It is planned for v1.2.

---

## Keep Dependencies Minimal

Reason:

- Smaller bundle
- Easier maintenance
- Fewer bugs
- Better AI-generated code quality

Prefer native Expo APIs whenever possible.

---

## One Feature at a Time

Reason:

Every implementation step should leave the application in a working state.

Avoid implementing multiple major features in a single change.
