# Runway Tracker Case Study

## Overview

Runway Tracker is a local-first planning tool for people living with unstable income. It helps users understand how long their bank balance can cover rent, bills, and living expenses without connecting bank accounts.

The project started from a broad personal finance dashboard idea and was narrowed into one core user question:

```text
How long will my bank balance last if my income and expenses stay the same?
```

## Scenario

The clearest use case is someone living alone in Berlin after leaving a full-time job.

In May 2026, they have:

- €5,000 in their bank account
- €400 freelance income this month
- €800 rent
- €800 living expenses
- €1,600 total monthly costs

The monthly shortfall is:

```text
€1,600 costs - €400 income = €1,200 shortfall
```

The runway estimate is:

```text
€5,000 bank balance / €1,200 monthly shortfall = 4.2 months
```

The product includes a Berlin demo that extends this scenario from May to September 2026, so a visitor can immediately see the chart and history working. The first month turns into a plain-English result:

```text
Your bank balance lasts about 4.2 months.
At this pace, it may reach zero around September 2026.
```

## Problem

People with uncertain income often need a fast answer during stressful periods:

- A freelancer has fewer projects than expected.
- A job seeker is living from savings while applying.
- A recent graduate is living independently and trying to manage rent.
- A solo builder is deciding how long they can keep working before income becomes urgent.

Most finance apps answer too many questions at once. They ask users to set up accounts, budgets, categories, goals, or bank connections before showing a useful number.

Runway Tracker keeps the first version focused on one useful answer: how long the current bank balance can cover a monthly shortfall.

## MVP Scope

The MVP includes:

- Bank balance input
- Monthly income input
- Monthly costs input
- Optional investment balance input
- Snapshot month input
- Berlin example button
- Multi-month Berlin demo data
- Monthly shortfall calculation
- Top Runway Answer with status
- Months remaining calculation
- Estimated zero date
- Monthly snapshot history
- Edit and delete actions
- Reset all local data
- Export saved snapshots as JSON
- Light and dark mode toggle
- Simple bank balance history chart
- Local browser persistence
- Responsive layout

The MVP does not include:

- Login
- Backend
- Bank integrations
- Broker integrations
- Budget categories
- Cloud sync
- Mortgage planning
- Apartment affordability
- Net-worth dashboard features

## Product Decisions

### Focus On Unstable Income

The strongest use case is not general wealth tracking. It is survival-time planning for someone with uncertain income and fixed monthly costs.

### Use Bank Balance As The Main Number

Rent and living expenses are paid from available money. Investments can be useful context, but they should not make the user feel safer unless they plan to sell them.

### Keep The Formula Visible

The app explains the calculation in plain language:

```text
Monthly shortfall = monthly costs - income
Balance lasts = bank balance / monthly shortfall
```

### Make The Chart Historical

The chart shows bank balance over saved months. It does not project the future because projection lines made the first version harder to understand.

### Avoid Overbuilding

Apartment buying and long-term investing are valid financial questions, but they are different products. Keeping them out makes Runway Tracker easier to understand and stronger as a portfolio MVP.

## User Flow

1. The user opens `index.html`.
2. The top Runway Answer explains the unstable-income result in plain language.
3. The user can load the Berlin demo or enter their own snapshot.
4. The app calculates monthly shortfall, months remaining, and estimated zero date.
5. The user saves the month to local history.
6. After two or more months, the chart shows bank balance over time.
7. The user can edit, delete, reset, or refresh without losing local data.

## Success Criteria

- A visitor understands the purpose without knowing finance terms.
- A user can test the Berlin example quickly.
- The app clearly explains why investments are optional context.
- The first visible result is the runway answer, not a dense table or chart.
- The chart does not look meaningful until there are at least two months.
- Data persists locally across refreshes.
- The project is clear enough to present on GitHub as a public portfolio MVP.

## Technical Implementation

The app is a static frontend:

- `index.html` contains the semantic HTML structure.
- CSS defines the responsive dashboard layout and visual system.
- JavaScript handles state, calculations, rendering, editing, deletion, reset, example filling, local persistence, and the trend chart.
- The trend chart uses the browser Canvas API.
- Data is stored in `localStorage`.

No build step, backend, database, account system, or API integration is required.

## Portfolio Value

Runway Tracker demonstrates product scoping, frontend implementation, UX thinking, and the ability to turn a vague finance problem into a focused MVP.

The key product decision is constraint: instead of building a generic finance dashboard, the project focuses on one practical question for a real user situation.
