# Runway Tracker Case Study

## Overview

Runway Tracker is a local-first cash runway tool for freelancers, job seekers, solo builders, and anyone who wants to understand how long their cash can last without connecting bank accounts.

The project started from a broad personal finance dashboard idea and was narrowed into a focused MVP around one core user question:

How many months can my available cash last at my current burn rate?

## Problem

People often need a fast answer about their financial runway during moments of uncertainty:

- A freelancer has uneven income and wants to know whether their cash buffer is healthy.
- A job seeker wants to understand how long they can search before cash becomes tight.
- A solo builder wants to plan product work without overcomplicating financial tracking.

Most finance apps try to solve too much at once. They often require account creation, bank connections, categories, budgets, or setup work before the user can see a useful answer.

Runway Tracker intentionally avoids that scope. It gives the user a simple, manual, privacy-friendly way to track cash, income, expenses, burn, and runway.

## Target Users

### Freelancer

Freelancers may have variable income and inconsistent monthly expenses. They need a quick way to understand whether their current cash can cover future months.

### Job Seeker

Job seekers may have savings but temporarily reduced income. They need a calm, clear estimate of how many months they can continue searching.

### Solo Builder

Solo builders may be funding their own work. They need a lightweight planning view without a full accounting system.

## MVP Scope

The MVP includes:

- Liquid cash input
- Monthly income input
- Monthly expenses input
- Optional investment balance input
- Snapshot month input
- Net monthly burn calculation
- Remaining runway calculation
- Estimated cash-out date
- Total tracked balance
- Monthly snapshot history
- Edit and delete actions
- Reset all local data
- Simple cash balance trend chart
- Local browser persistence
- Responsive layout

The MVP does not include:

- Login
- Backend
- Bank integrations
- Broker integrations
- Budget categories
- Cloud sync
- Complex investing features
- Tax planning

## Product Decisions

### Keep The Product Local-First

The app uses browser `localStorage` so users can try it immediately. This keeps the MVP simple, private, and easy to ship publicly.

### Base Runway On Liquid Cash

Investments are tracked as optional context, but runway is calculated from liquid cash. This reflects the practical question the app is answering: how long available cash can cover expenses.

### Use Manual Snapshots

Manual monthly snapshots avoid the complexity of financial APIs while still giving the user useful trend history.

### Show The Answer First

The dashboard opens with four key metrics: liquid cash, monthly burn, runway remaining, and cash-out date. The rest of the interface supports those numbers.

### Avoid Overbuilding

The project is meant to be a portfolio MVP, not a full finance platform. The goal is to show product judgment by choosing what not to build.

## User Flow

1. The user opens `index.html`.
2. The dashboard shows empty states and default zero values.
3. The user records a monthly snapshot with cash, income, expenses, optional investments, and month.
4. The dashboard updates immediately.
5. The user can see burn, runway, projected cash-out date, tracked balance, chart trend, and history.
6. The browser stores the data locally.
7. The user can return later, add another month, edit history, delete a snapshot, or reset all data.

## Success Criteria

- A user can understand their runway within one minute.
- A user can record a monthly snapshot without setup or login.
- The app persists data across refreshes.
- The interface works on desktop and mobile.
- The product story is clear enough for a public portfolio repository.

## Technical Implementation

The app is built as a static frontend:

- `index.html` contains the semantic HTML structure.
- CSS defines the layout, visual system, responsive behavior, and dashboard styling.
- JavaScript handles state, calculations, rendering, editing, deletion, reset, local persistence, and the trend chart.
- The trend chart uses the browser Canvas API.
- Data is stored in `localStorage`.

No build step, backend, database, account system, or API integration is required.

## Portfolio Value

Runway Tracker demonstrates product scoping, frontend implementation, UX thinking, and the ability to turn a vague finance problem into a focused MVP.

The strongest product decision is the constraint: instead of building a generic finance dashboard, the project focuses on a single practical outcome. That makes the app easier to understand, easier to use, and easier to present.

## Future Improvements

Possible next steps after the MVP:

- Export snapshots to CSV
- Add a 3-month average burn option
- Add light validation for unusual entries
- Add sample data for demo mode
- Add basic automated tests if the project grows beyond one file

These are optional. The current MVP is intentionally scoped for a small public portfolio project.
