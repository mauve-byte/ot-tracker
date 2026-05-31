# OT Tracker 🗂️

A lightweight Progressive Web App (PWA) for Philippine government employees to quickly compute **Overtime Pay** and **Night Differential Pay** — and keep a monthly record of their earnings.

---

## Features

- **Overtime calculator** — supports both Regular Day and Day Off OT rates
- **Night Differential calculator** — computed separately from OT
- **My Position / Others mode** — check your own OT or simulate for other salary grades
- **Monthly notepad** — saves your computed totals per month, automatically
- **Works offline** — installable on any Android phone via Chrome, no Play Store needed
- **Data stays on your device** — nothing is sent to any server

---

## Formulas Used

These follow standard government compensation rules with 25% tax withholding applied:

```
Hourly Rate        = Base Monthly Salary ÷ 22 days ÷ 8 hours

Regular Day OT     = Hourly Rate × 1.25 × OT hours × 0.75
Day Off OT         = Hourly Rate × 1.50 × OT hours × 0.75
Night Differential = Hourly Rate × 0.20 × ND hours × 0.75
```

> The `× 0.75` factor reflects the 25% tax deduction applied to OT and ND earnings.

---

## How to Install on Android

1. Host the files using [GitHub Pages](https://pages.github.com/) (free)
2. Open the hosted URL in **Chrome** on your Android phone
3. Tap the **three-dot menu (⋮)** → **"Add to Home screen"**
4. Tap **Add** — the app installs with its own icon

It will work fully offline after the first load.

---

## How to Use

### Settings
Set your position label and base monthly salary once. This is used for all your personal computations.

### Calculator
- Choose **My Position** to compute your own OT/ND
- Choose **Others** to type in any salary and check — results won't be saved
- Enter Regular Day OT hours, Day Off OT hours, and Night Differential hours
- Results are computed instantly

### Save to Notepad
- Tap **Save to Notepad** to record the current month's total
- Each save **replaces** that month's entry (not cumulative)
- Only available in **My Position** mode

### Notepad
- View your monthly OT and ND totals
- Delete any entry using the × button

---

## Files

| File | Description |
|------|-------------|
| `index.html` | Main app — all UI and logic |
| `manifest.json` | PWA manifest for installability |
| `sw.js` | Service worker for offline support |
| `icon-192.png` | App icon (192×192) |
| `icon-512.png` | App icon (512×512) |

---

## Tech Stack

Plain HTML, CSS, and JavaScript — no frameworks, no dependencies. Data is stored in `localStorage` on the device.

---

## Contributing

Feel free to fork and adapt for your agency's specific salary grades or computation rules. Pull requests are welcome.

---

## Disclaimer

This app is a personal productivity tool and is not affiliated with or endorsed by any government agency. Always verify your computations against your official payslip.
