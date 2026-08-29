# Multi-Source Lead Aggregator

Normalizes leads from any source into one schema and de-duplicates against Airtable before logging.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![Airtable](https://img.shields.io/badge/-Airtable-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

## Table of Contents

- [Problem](#problem)
- [Solution](#solution)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Configuration](#configuration)
- [Error Handling & Resilience](#error-handling--resilience)
- [Use Cases](#use-cases)
- [Demo](#demo)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Problem

Leads land from a dozen different forms and tools, but never in one deduplicated place.

## Solution

**Trigger:** Webhook (generic lead payload from any source)

Normalizes leads from any source into one schema and de-duplicates against Airtable before logging. The workflow runs as a single n8n automation with 8 functional nodes (trigger, logic, and integration steps combined).
