# Case study — Building and operating CoachNoChill AI

## The challenge

A 32-team Madden NFL franchise league involves frequent schedule advances, owner-to-owner coordination, rule questions, changing rosters and standings, award selection, and commissioner decisions. Performing these tasks manually creates inconsistent records, repetitive messaging, and delays.

## My role

I independently developed and operate CoachNoChill AI, an AI-assisted Discord application used by a real online gaming community. The work combines product requirements, Python and asynchronous workflows, API integration, cloud deployment, database operations, debugging, and user support.

## The approach

### 1. Make useful information accessible

I built Discord-native interfaces that answer routine questions about league schedules and rules, help owners find the right workflow, and provide commissioners with operational context.

**Engineering lesson:** User-friendly conversational answers must be grounded in approved rules or verified live data; they should not invent the league's current state.

### 2. Automate recurring work

The platform includes advance countdowns, game reminders, scheduling coordination, weekly recognition features such as POTW/GOTW, and commissioner-facing management tools.

**Engineering lesson:** Automation needs explicit state handling and idempotency, especially when a league progresses into a new week or season.

### 3. Integrate structured league data

I integrated read-only league information from NeonSportz/Madden, including schedules, teams, players, standings, and available historical records. SQLite is used for persistent application records and workflow state.

**Engineering lesson:** Cached data, incomplete API responses, and season changes require validation and reconciliation before publishing definitive results.

### 4. Support production operations

I deployed the Python application with Railway, Docker, GitHub, and GitHub Actions, and added validation, health diagnostics, integrity checks, backups, and release testing.

**Engineering lesson:** Building a feature is only part of the job. Reliable deployment, recoverability, and incident diagnosis are equally important.

### 5. Troubleshoot real incidents

I investigated a production database path misconfiguration that produced an empty ownership view and recovered the correct state. I also addressed Discord API command-synchronization throttling with more controlled startup and retry behavior.

**Engineering lesson:** Good incident response starts by finding the root cause, understanding impact, limiting risk, testing the fix, and verifying the service after deployment.

### 6. Design for safe growth

I extended the design toward a separate multi-server Hosted Edition with guild-isolated storage, approved knowledge, feature gates, AI usage budgets, and restricted administrative actions.

**Engineering lesson:** Multi-tenant features demand more than reusing commands: data separation, permission checks, and privacy boundaries need their own tests.

## Outcomes

- Built and maintain a cloud-hosted application serving a live **32-team franchise league**.
- Implemented AI assistance, scheduling tools, weekly award workflows, and commissioner support.
- Gained hands-on experience with Python, REST APIs, SQLite, Docker, Railway, and GitHub Actions.
- Improved operational practices for debugging, database recovery, deployment checks, privacy, and data correctness.

This case study deliberately does **not** claim unverified productivity percentages, revenue, or user adoption numbers.

## Interview demonstration

I can walk through a sanitized question-and-answer flow, show an approval-gated commissioner action, explain the GitHub-to-Railway delivery process, and discuss troubleshooting steps from a real production issue. Demos are subject to member privacy and availability.

[Back to project overview](../README.md)
