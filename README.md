# Runway Tracker

Runway Tracker is a local-first planning tool that helps people with unstable income understand how long their bank balance can cover rent, bills, and living expenses.

I built it as a focused portfolio MVP to show product scoping, financial UX, and simple frontend implementation without bank integrations, user accounts, or a backend.

## Example Scenario

Imagine you live alone in Berlin and start May 2026 without a full-time job. You are trying to find freelance projects, but income is uncertain.

```text
Bank balance: €5,000
Freelance income this month: €400
Rent: €800
Living expenses: €800
Monthly costs: €1,600
Monthly shortfall: €1,200
```

The built-in Berlin demo extends the story from May to September 2026 so the chart and history are meaningful. It turns the situation into a plain answer:

```text
Your €5,000 bank balance lasts about 4.2 months.
If nothing changes, it may reach zero around September 2026.
```

## Why It Was Built

Most personal finance tools quickly become broad dashboards: budgets, categories, bank sync, investments, net worth, goals, and reports.

This MVP focuses on one practical question:

```text
How long can my bank balance keep me going if my income is unstable?
```

That makes the app useful for freelancers, people between jobs, solo builders, recent graduates living independently, and anyone planning through a temporary income gap.

## Features

- Save monthly financial snapshots
- Load a Berlin freelance demo with multiple months of sample data
- Track bank balance, income, monthly costs, and optional investments
- Calculate monthly shortfall
- Estimate how many months the bank balance can last
- Estimate the month the balance may reach zero
- Show optional tracked balance with investments
- Display a simple bank balance history chart after two or more snapshots
- Show editable snapshot history
- Delete individual snapshots or reset all local data
- Export saved snapshots as JSON
- Switch between light and dark mode
- Persist data locally with `localStorage`
- Work as a static HTML/CSS/JavaScript app with no backend

## Product Decisions

- The app is a runway tool, not a full net-worth or budgeting dashboard.
- Bank balance is the main input because rent and living costs are paid from available money.
- Investments are optional context and are not used to calculate how long the bank balance lasts.
- The chart only shows saved history, not future projection, to keep the MVP understandable.
- Data entry is manual because bank integrations would add scope, privacy concerns, and backend complexity.
- Apartment buying, mortgage planning, and long-term wealth planning are intentionally out of scope.

## Tech Stack

- HTML
- CSS
- JavaScript
- Browser `localStorage`
- Canvas API for the trend chart
- Google Fonts for typography

## Run Locally

Open `index.html` directly in a browser.

No install, build step, server, login, or API key is required.

## Screenshots To Add

Screenshots are not required to run the project, but they will make the GitHub repo easier to understand.

Capture and add these images later:

- `docs/screenshots/empty-state.png`: app before entering data
- `docs/screenshots/berlin-example.png`: app after loading the Berlin demo
- `docs/screenshots/history-trend.png`: app after adding at least two months so the chart is visible
- `docs/screenshots/mobile.png`: app on a narrow/mobile viewport

Suggested README placement after adding screenshots:

```md
## Screenshots

![Empty state](docs/screenshots/empty-state.png)
![Berlin example](docs/screenshots/berlin-example.png)
![History trend](docs/screenshots/history-trend.png)
![Mobile view](docs/screenshots/mobile.png)
```

## Portfolio Value

This project demonstrates product scoping, frontend implementation, UX thinking, and the ability to turn a vague finance problem into a focused MVP that can be shipped publicly on GitHub.
