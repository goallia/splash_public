# Starter project board

How to set up a GitHub Project board for this repo. It takes about 5 minutes.

## 1. Create the board

1. Open https://github.com/goallia/splash_public and click the **Projects** tab.
2. Click **Link a project** → **New project** (or **New project** directly).
3. Choose the **Board** template and name it **Product Roadmap**.

## 2. Set up the columns (Status field)

Rename or add the columns so they read:

| Column | Meaning |
|---|---|
| **Inbox** | New ideas and bugs, not yet looked at |
| **Discovery** | Researching the problem, writing a spec |
| **Ready** | Spec approved, ready for engineering |
| **In progress** | Being built |
| **Shipped** | Released to users |

## 3. Add custom fields

In the board, click **+** next to the field headers (or open **Settings → Fields**):

| Field | Type | Options |
|---|---|---|
| **Priority** | Single select | P0, P1, P2, P3 |
| **Impact** | Single select | High, Medium, Low |
| **Quarter** | Iteration or single select | e.g. Q4 2026, Q1 2027 |
| **Spec** | Text | Link to the spec in `specs/` |

## 4. Add useful views

- **Board** (default) — grouped by Status.
- **Roadmap** — click **New view → Roadmap**, group by Quarter.
- **Triage** — a Table view filtered to `status:Inbox`, sorted by Impact.

## 5. Turn on automation

Open the board's **⋯ menu → Workflows** and enable:

- **Auto-add to project** — filter `repo:goallia/splash_public is:issue`, so every new issue lands in **Inbox**.
- **Item closed** → set Status to **Shipped**.
- **Pull request merged** → set Status to **Shipped**.

## 6. Create the labels

The issue templates use these labels. Create them under **Issues → Labels → New label**:

| Label | Suggested colour |
|---|---|
| `type:feature` | `#1D76DB` |
| `type:bug` | `#D73A4A` |
| `status:triage` | `#FBCA04` |
