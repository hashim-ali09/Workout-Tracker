# Workout Tracker

A browser-based workout tracker for logging training sessions, managing weekly splits, reviewing exercise history, and keeping all data local to your device.

## Overview

This app is a single-file HTML application built with HTML, CSS, and JavaScript. It is designed to help you:

- Track workouts by date
- Organize push, pull, legs, cardio, or custom splits
- Log normal sets, drop sets, and supersets with different data structures
- View complete exercise history and exact last-week comparisons
- Manage a weekly split planner with temporary one-week overrides when life gets busy
- Keep all data in localStorage with backup export/import support

## Main Features

- Workout logging by day
- Day-level save status (saved or not saved)
- Split planner by weekday
- Temporary weekly split shifts for busy days
- Normal, drop set, and superset logging modes
- Cardio set logging
- Calendar view with saved-workout month list
- Dedicated History tab for full exercise session history
- Exercise recommendation chips when building splits
- Holiday/rest-day support
- Local backup and restore through JSON export/import

## How To Use

1. Open `workout_tracker.html` in a modern browser.
2. Go to the Splits tab to create and organize your splits.
3. Assign a split to each weekday in the weekly planner.
4. Open Today to select a date, choose a split, and log your workout.
5. Pick a logging mode for each exercise:
   - Normal: weight and reps
   - Drop Set: top set and drop set fields
   - Superset: A and B exercise fields
6. Press Save Workout to mark the day as saved (partial completion is allowed).
7. Use History to inspect complete logs for any exercise.

## Data Storage

All information is stored locally in the browser using `localStorage`. The app does not require an account or backend.

Storage keys used:

- `workoutTracker_v1` (primary)
- `workoutTracker_v1_backup` (fallback backup)

Stored data includes:

- Splits and exercises
- Weekly schedule
- Temporary weekly overrides
- Workout sessions
- Notes and settings
- Holidays and rest days

Use the Data tab to export or import a JSON backup.

## File

- `workout_tracker.html`: the full application

## Notes

- The app is fully client-side.
- You can open it directly from disk or host it on any static web server.
- If browser site data is cleared, localStorage is cleared too. Export your data regularly if you care about long-term retention.
- localStorage is origin-specific. Data on `file://` and data on a hosted URL are different stores.

## License

Free to use, modify, and share.

