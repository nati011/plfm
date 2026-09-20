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

- **SMS parsers** for different banks, mobile money providers, or payment services.
- **Categorization rules** that tag transactions by merchant, sender, amount, or message pattern.
- **Budgeting rules** for limits, envelopes, recurring expenses, and savings goals.
- **AI tools** built on top of your own financial data.

## Components

- `agent`: runs on-device, reads financial transaction SMS messages, and exports parsed records.
- `server`: receives, stores, and aggregates transaction data from trusted agents.
- `client`: provides personal finance tools built on top of the collected data.

## Motivation

Similar tools often make two tradeoffs that PLFM tries to avoid: they store sensitive financial data on someone else's server, and they stop at lightweight budgeting instead of becoming powerful enough for serious personal accounting.

PLFM is not trying to be a polished product first. It is a personal system for owning the data, understanding it better, and experimenting with finance tools that can grow beyond simple spending charts.
# plfm
