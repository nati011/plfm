## PLFM

`plfm` is a personal finance project for collecting transaction data and turning it into useful tools for understanding spending.

## Why it exists

PLFM is meant to bridge the gap between financial data and personal analytics. Banks, mobile money providers, and payment services already send useful transaction data to your phone, but that data often stays trapped in SMS messages.

PLFM collects that data locally, turns it into structured records, and makes it available for deeper personal finance and accounting workflows.

## Local-First

PLFM does not need a cloud-hosted server. The phone agent can sync with a server running on your PC over a local network, which works well when the phone and computer are usually close to each other. Let's be real: your phone is probably near your desk anyway.

That keeps the project personal and private:

- financial data stays on devices you control;
- your machine can act as the main storage and analysis hub;
- sync can happen automatically when your phone can reach the local server;
- the same data can support more serious accounting and analytics tools over time.

## Storage

PLFM stores data in simple plain text files, keeping the records visible, inspectable, and easy to move. The goal is to avoid opaque databases where possible and make it clear what data exists and how it is structured.

If configured, PLFM can also back up those files to GitHub automatically. That makes GitHub an optional storage and backup layer, not a required cloud dependency.

## Extensible

PLFM should be easy to adapt to whatever personal finance workflow you actually use. It gives you a simple base for collecting, storing, and exposing transaction data, then lets you build your own extensions on top of it.

Examples of plugins and extensions:

- **Custom reports** for purchase prep, monthly reviews, category breakdowns, cash-flow summaries, or account-specific audits.
- **AI tools** that answer questions about your finances, explain spending patterns, summarize a month, suggest categories, or help write new rules from your own data.
- **Exporters** that turn PLFM records into CSV, spreadsheets, plain text accounting files, dashboard inputs, or long-term backup formats.
- **Notifications** for unusual spending, low balances, duplicate charges, large transactions, upcoming bills, or recurring payments that did not happen.
- **Integrations** with local scripts, GitHub backups, note-taking systems, personal dashboards, accounting tools, or any other workflow you want PLFM to feed.

## Components

- `agent`: runs on-device, reads financial transaction SMS messages, and exports parsed records.
- `server`: receives, stores, and aggregates transaction data from trusted agents.
- `client`: provides personal finance tools built on top of the collected data.

## Motivation

From my observation, personal finance tools tend to fall into one of two camps: polished products and mobile apps that keep your financial data on someone else's server, or serious CLI tools like [ledger-cli](https://ledger-cli.org/) that are powerful but can feel rigid and difficult to extend around your own needs.

PLFM tries to bridge that gap. It aims to keep the privacy and control of local-first tooling while still leaving room for a friendlier client, automatic data capture, extensibility, and more serious personal accounting.

It is not trying to be a polished product first. It is a personal system for owning the data, understanding it better, and experimenting with finance tools that can grow beyond simple spending charts.
