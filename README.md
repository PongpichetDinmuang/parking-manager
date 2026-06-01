# Parking Manager

A lightweight, privacy-first monthly parking fee management system that runs entirely in the browser — no installation, no account required.

---

## Overview

Parking Manager is a single-file web application (`parking_manager.html`) built with vanilla HTML, CSS, and JavaScript. All data is stored locally in the browser via `localStorage`. No data is ever transmitted to a server.

---

## Usage

### Via GitHub Pages (recommended)

Open the following URL in any browser:

```
https://pongpichetdinmuang.github.io/parking-manager/parking_manager.html
```

Bookmark it for quick access. Data persists in `localStorage` as long as the browser's site data is not cleared.

### Via local file

Download `parking_manager.html` and open it directly in a browser. Note that `localStorage` is scoped to the origin, so data saved when running from `file://` is separate from data saved via GitHub Pages.

---

## Features

### Customer Management
- Add, edit, and delete customer records
- Fields: license plate, name, phone number, start date, monthly price, and notes
- Mark a customer as inactive (moved out) without deleting their record

### Monthly Billing
- Add billing months per customer; deadline is calculated automatically from the start date
- Mark months as paid or unpaid with a single checkbox
- Each month stores its own price, allowing price changes without affecting past records
- First month cannot be deleted to preserve billing history

### Status Classification

Status is derived automatically from each month's deadline.

| Status   | Condition                              |
|----------|----------------------------------------|
| Paid     | Marked as paid                         |
| Pending  | Deadline has not passed, not yet paid  |
| Overdue  | Deadline has passed, not yet paid      |

### Views
- **Overview** — summary stats (total active, overdue, fully paid) and a financial summary (collected vs pending)
- **Customer detail** — full edit view with monthly billing list
- **Calendar** — monthly view with license plates shown on their deadline dates, color-coded by status

### Data Management

| Action | Behavior |
|--------|----------|
| Save | Writes current state to `localStorage` |
| Open file | Loads a previously exported `.json` file into memory; press Save to commit to `localStorage` |
| Export JSON | Downloads `parking_data.json` to the device for backup or transfer to another browser/device |

---

## Data & Privacy

- All data is stored in `localStorage` on the user's device only
- No cookies, analytics, tracking, or external requests of any kind
- The exported `parking_data.json` is a plain JSON file the user owns and controls

---

## Browser Support

| Browser | Desktop | Mobile |
|---------|---------|--------|
| Chrome  | Yes     | Yes    |
| Safari  | Yes     | Yes    |
| Edge    | Yes     | Yes    |
| Firefox | Yes     | Yes    |

---

## Tech Stack

- HTML / CSS / JavaScript (no frameworks, no build step)
- [Tabler Icons](https://tabler.io/icons) (loaded via CDN)

---

## File Structure

```
parking-manager/
├── parking_manager.html    # Application entry point
└── README.md
```

---

## License

MIT
