# Profile README Revamp Design

- **Date:** 2026-09-16
- **Status:** Approved by User
- **Target Repository:** NathanaelGracedo/NathanaelGracedo

## 1. Objective & Scope

Revamp and stabilize GitHub profile `README.md` by eliminating broken third-party widgets, removing redundant profile metadata, deferring project showcases to GitHub native Pinned Repositories, and halting unneeded CI workflows.

### Out of Scope
- Creating new custom GitHub Action workflows or self-hosted metrics server.
- Modifying repository configuration outside `README.md` and `.github/workflows/`.

---

## 2. Proposed Changes

### A. Navigation & Header
- **Typing SVG & Header Badges:** Retain current Tokyo Night typing SVG banner and Shields badges (Followers & Profile Views).
- **Navigation Bar:** Update anchor links to match retained sections:
  ```html
  <p align="center">
    <a href="#-about-me">About Me</a> •
    <a href="#%EF%B8%8F-tech-stack">Tech Stack</a> •
    <a href="#-github-streak">Streak</a> •
    <a href="#-connect-with-me">Connect</a>
  </p>
  ```

### B. About Me Section
- **YAML Block Removal:** Delete redundant YAML block (`Name`, `Status`, `Campus`, `Focus`, `Interests`, `Location`) as these details are native to GitHub profile sidebar.
- **Bullet Points:** Preserve clean descriptive bullet list (education, focus, interests, collaboration, and location).

### C. Tech Stack Section
- **Icons & Breakdown:** Retain `skillicons.dev` dark-theme icon line and collapsible `<details>` table breakdown.

### D. Activity & Stats Section
- **Broken Widget Cleanup:**
  - Remove `github-readme-stats-sigma-five.vercel.app` (API PAT rate limit exceeded).
  - Remove `github-readme-stats-sigma-five.vercel.app/api/top-langs/`.
  - Remove `github-readme-activity-graph.vercel.app` (HTTP 402 payment required on Vercel host).
- **GitHub Streak Display:**
  - Retain functional `github-readme-streak-stats.herokuapp.com` with `theme=tokyonight` and centered layout.
  - Section header updated to `## 🔥 GitHub Streak`.

### E. Removals
- **Featured Projects Section:** Fully removed. Project showcases will rely on GitHub native Pinned Repositories.
- **Contribution Snake Section:** Fully removed from `README.md`.
- **Workflow Cleanup:** Delete `.github/workflows/snake.yml` to prevent runner quota consumption on deleted snake artifact.

### F. Connect & Footer
- Retain social badges (LinkedIn, GitHub, Instagram, Gmail).
- Retain footer quote: `⚡ "Stay curious, keep learning, and build things that matter."`.

---

## 3. Verification & Validation Plan
1. **Link Verification:** Ensure all anchor links in navigation match section headers.
2. **Asset Validation:** Ensure remaining SVGs/badges render without HTTP error responses.
3. **Git Cleanliness:** Ensure `.github/workflows/snake.yml` is removed and git tree is consistent.
