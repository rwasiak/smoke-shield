# SmokeShield

**Version:** 0.0.1

SmokeShield is a mobile-first Progressive Web App designed to provide instant, empathetic, and personalized AI-driven interventions based on Cognitive Behavioral Therapy (CBT) techniques to help users quit smoking (traditional and e-cigarettes).

## Table of Contents

- [Project Description](#project-description)
- [Tech Stack](#tech-stack)
- [Getting Started Locally](#getting-started-locally)
- [Available Scripts](#available-scripts)
- [Project Scope](#project-scope)
- [Project Status](#project-status)
- [License](#license)

## Project Description

When users experience sudden cravings during their quit-smoking journey, they often lack immediate, personalized support. SmokeShield aims to interrupt the automatic reach for a cigarette by offering a one-click AI-powered chat intervention tailored to each user’s profile and triggers.

Key features include:

- Onboarding with user profile data (gender, age, type of smoking habit, main triggers, motivations).
- Ultraminimalist main screen with a central intervention button.
- AI conversation based on predefined CBT scenarios.
- Feedback loop to record success (Yes/No) and add or select triggers.

## Tech Stack

- **Frontend:** Astro 5, React 19, TypeScript 5
- **Styling:** Tailwind CSS 4, Shadcn/ui components
- **Backend-as-a-Service:** Supabase (PostgreSQL, Authentication)
- **AI integration:** Openrouter.ai (supporting various LLM providers)
- **PWA:** Optimized as a Progressive Web App
- **CI/CD:** GitHub Actions
- **Hosting:** Docker image on DigitalOcean

## Getting Started Locally

### Prerequisites

- Node.js v22.14.0 (see `.nvmrc`)
- pnpm or npm

### Installation

```bash
# Clone the repository
git clone git@github.com:rwasiak/smoke-shield.git
cd smoke-shield

# Install dependencies
pnpm install    # or npm install
```

### Running in Development

```bash
pnpm dev         # or npm run dev
# Open http://localhost:3000 in your browser
```

## Available Scripts

In the project directory, you can run:

| Script          | Description                             |
| --------------- | --------------------------------------- |
| `pnpm dev`      | Starts Astro development server         |
| `pnpm build`    | Builds the production-ready application |
| `pnpm preview`  | Previews the production build locally   |
| `pnpm astro`    | Runs the Astro CLI                      |
| `pnpm lint`     | Runs ESLint across the project          |
| `pnpm lint:fix` | Runs ESLint with `--fix`                |
| `pnpm format`   | Formats code with Prettier              |

_Replace `pnpm` with `npm run` if using npm._

## Project Scope

### Phase 1: Proof of Concept (POC)

- Onboarding screen collecting user details
- Ultraminimalist interface with a single intervention button
- AI chat interaction based on 10–15 CBT scenarios
- Feedback loop (success logging, trigger selection/creation)
- User authentication & data protection (signup, login, secure data storage, account and history deletion)

### Phase 2: Minimum Viable Product (MVP)

- All POC features
- Dynamic personalization using user history
- Milestone tracking (24h, 3 days, 1 week, etc.)
- Event-based notifications (milestone achievements, inactivity reminders)
- Home screen widget for one-click intervention
- Multilingual support (Polish, English, Spanish)

## Project Status

Currently in **Phase 1 (POC)** development aiming to validate immediate AI-driven intervention effectiveness.

## License

_No license specified. Please add a LICENSE file to choose an open-source license._
