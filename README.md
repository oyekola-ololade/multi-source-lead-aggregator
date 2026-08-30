# Multi-Source Lead Aggregator

Normalizes leads from any source into one schema and de-duplicates against Airtable before logging.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![Airtable](https://img.shields.io/badge/-Airtable-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

**[Open the visual project page →](./index.html)**

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Demo status](#demo-status)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Overview

**Trigger:** Webhook (generic lead payload from any source)

Normalizes leads from any source into one schema and de-duplicates against Airtable before logging.

### Key Features

- Source-agnostic lead normalization
- Email-based de-duplication
- Single master lead table across channels

## Architecture

Open the [visual project page](./index.html#architecture) for the flow derived from the sanitized export.


## Workflow

1. Multi-source webhook receives a lead from any channel
2. Normalize into a common schema (source, name, email, phone, raw data)
3. Query Airtable for an existing record with the same email
4. Duplicate: skip and tag as skipped
5. New: create a master lead record and post a daily summary to Slack

## Tech Stack

- n8n
- Airtable

## Demo status

A configured live-run recording is not included yet. Credentials and service identifiers remain placeholders.


## Setup

1. Import `workflow/T7_Multi_Source_Lead_Aggregator.json` into your n8n instance (**Workflows → Import from File**).
2. Replace every placeholder credential/URL in the workflow (e.g. `YOUR_..._API_KEY`, `YOUR_..._URL`) with your own service credentials.
3. Activate the workflow and point the relevant integration (webhook source, scheduled trigger, etc.) at the generated webhook URL.
4. Test with a sample payload before going live.

## Repository Structure

```text
.
├── index.html
├── README.md
├── LICENSE
├── .gitignore
└── workflow/
    └── T7_Multi_Source_Lead_Aggregator.json
```


## Disclaimer

This workflow was built as a portfolio/template project to demonstrate n8n workflow automation and AI integration. API credentials and sensitive configuration have been removed before publication — replace all `YOUR_..._KEY` / `YOUR_..._URL` placeholders with your own before use.

---

Designed and engineered by

**Oyekola Ololade**

AI Systems & Integration Engineer

- LinkedIn: <http://linkedin.com/in/ololade-oyekola-5b1797397>
- Email: <oyekolaololade69@gmail.com>
