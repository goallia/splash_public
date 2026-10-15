# Spec: Personalised match notifications

> **Example spec** — shows how the [template](_TEMPLATE.md) looks when filled in. The content is illustrative.

| | |
|---|---|
| **Status** | Draft |
| **Owner** | @goallia |
| **Reviewers** | @eng-lead, @design-lead |
| **Last updated** | 2026-10-15 |
| **Related issues** | — |

## 1. Problem

Fans miss key moments (kick-off, goals, final whistle) for the teams they follow. Today we only send generic notifications, so many users mute them entirely.

## 2. Goals and non-goals

**Goals**
- Let users choose which teams and which events they get notified about.
- Reduce notification opt-outs.

**Non-goals**
- Live video in notifications.
- Notifications for betting odds.

## 3. Success metrics

| Metric | Today | Target | How we measure |
|---|---|---|---|
| Notification opt-out rate | 38% | < 25% | Push settings analytics |
| Weekly active users (followers of 1+ team) | baseline | +10% | Product analytics |

## 4. Users and use cases

- **Primary user:** Fans who follow one or two clubs closely.
- **Key use cases:**
  1. As a fan, I want a notification when my team scores, so that I don't miss it.
  2. As a fan, I want to turn off everything except kick-off reminders, so that I'm not overwhelmed.

## 5. Proposed solution

A "Notifications" section on each team page with toggles for kick-off, goals, red cards, half-time and full-time. Sensible defaults: kick-off + goals + full-time.

## 6. Requirements

| # | Requirement | Priority |
|---|---|---|
| R1 | Per-team toggles for each event type | Must |
| R2 | Notifications arrive within 30 s of the event | Must |
| R3 | "Mute all for 24 h" quick action | Should |
| R4 | Player-level notifications | Could |

## 7. Open questions

- [ ] Do we need different defaults per market?
- [ ] Which data provider gives us the lowest latency?

## 8. Risks and dependencies

- Depends on live-data provider latency.
- Risk of notification fatigue if defaults are too broad.

## 9. Rollout plan

- Phase 1: 10% of users in one market, A/B test against current notifications.
- Launch criteria: opt-out rate below control, no latency regressions.

## Changelog

- 2026-10-15 — First draft
