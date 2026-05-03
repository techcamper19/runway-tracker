# Runway Tracker

Runway Tracker is a local-first financial planning tool that helps users understand how long their available cash can last based on income, expenses, and monthly burn.

I built it as a focused MVP to explore product scoping, financial UX, and simple frontend implementation without bank integrations or user accounts.

## Why It Was Built

Personal finance tools often become complex quickly: bank connections, budgeting categories, account sync, investments, goals, and dashboards. For a portfolio MVP, the goal was to narrow the problem to one useful question:

How long can my available cash last at my current monthly burn?

Runway Tracker is designed for freelancers, job seekers, solo builders, and anyone who wants a quick local snapshot of their cash runway without connecting financial accounts.

## Features

- Save monthly financial snapshots
- Track liquid cash, income, expenses, and optional investments
- Calculate net monthly burn
- Estimate remaining runway in months
- Estimate projected cash-out date
- Show total tracked balance
- Display a simple cash balance trend chart
- Show editable snapshot history
- Delete individual snapshots or reset all local data
- Persist data locally with `localStorage`
- Work as a static HTML/CSS/JavaScript app with no backend

## Product Decisions

- The MVP stays focused on runway, not full personal finance management.
- Data entry is manual because bank integrations would add scope, privacy concerns, and backend complexity.
- The app is local-first so users can try it immediately without login or setup.
- Investment balance is optional and included in tracked balance, but runway is based on liquid cash only.
- Snapshot history keeps the product useful over time while avoiding complex analytics.
- The interface prioritizes the main financial answer first: cash, burn, runway, and cash-out date.

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

## Portfolio Value

This project demonstrates product scoping, frontend implementation, UX thinking, and the ability to turn a vague finance problem into a focused MVP that can be shipped publicly on GitHub.
