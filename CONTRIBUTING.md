# Contributing Guidelines

Thank you for helping improve Diep.io! Because the game is closed-source,
contributing here means writing **clear, actionable issue reports**. Please
read these rules carefully — they exist so developers can actually find, fix,
and close what you report.

> GitHub automatically links to this file when you open a new issue.

---

## 1. One Issue = One Problem

This is the single most important rule.

Open a **separate** issue for each bug, visual problem, AI issue, balance
concern, or suggestion. Do **not** bundle unrelated problems together.

A report like "here are 90 things that are broken" is impossible to triage,
assign, or close. **Mega-list issues will be closed** and you will be asked to
resubmit them as individual reports.

### Bad

> **Title:** visual feedback/bugs and a few gameplay bugs
>
> - Destroyer recoil doesn't work when stunned
> - Necromancer drones have no outlined asset
> - Sprayer's bullet spread grows way too wide
> - Trapper's traps seem broken
> - Stalker invisibility can be seen by all players
> - *(…80 more unrelated items)*

This was [an actual issue in a sibling repo](https://github.com/MopeIOTeam/mope-issues/issues/23). Don't do this.

### Good

> **Title:** [Bug] Stalker invisibility visible to all players in Domination mode
>
> Stalker's invisibility when stationary does not function correctly in
> Domination mode. All players can see the Stalker regardless of whether it
> is moving. Expected: Stalker fades to invisible after standing still.

---

## When Multiple Bugs ARE Related

If several bugs clearly affect the **same tank class AND the same system**
(ability, rendering, stat interaction), they **can** go in one issue.

### Acceptable as one issue

> **Title:** [Visual] Overlord — multiple issues during drone repel
>
> When using drone repel:
> - Drone sprites flicker and disappear momentarily
> - Overlord body briefly renders behind the score bar
>
> Both occur during the same repel action and likely share a root cause.

### Also acceptable

> **Title:** [Bug] Auto Gunner — auto-turret targeting + missing barrel animation
>
> - Auto Gunner's auto-turret targets invulnerable players on spawn
> - Auto Gunner's secondary barrel has no recoil animation
>
> Both relate to the Auto Gunner's auto-turret behavior.

### NOT acceptable

> Auto Gunner has no recoil animation, also Overlord is too fast, also
> Destroyer bullet knockback is wrong.

These are three completely unrelated tank classes. File them separately.

**Rule of thumb:** same tank class + same system = okay to group.
Different tank classes or different systems = separate issues.

---

## When a Bug Is Systemic

Some bugs affect many tank classes because of shared underlying logic — for
example, "all drone-class tanks lose drones on tab-out" or "all invisible
tanks are revealed on the minimap."

In these cases, file **one** issue describing the **systemic pattern**, list
the affected tank classes as examples, and title it after the shared mechanic
rather than a single tank:

> **Title:** [Bug] Drone desync on browser tab-out affects multiple drone classes
>
> Affected: Overlord, Necromancer, Factory, Manager.
> All drone-class tanks lose control of existing drones when the browser
> tab loses focus and regains it.
> Expected: drones should remain under player control on refocus.

This is acceptable because the root cause is clearly one shared system, not
four unrelated bugs.

---

## 2. Search Before Posting

Before opening a new issue:

1. Search [open issues](../../issues)
2. Search [closed issues](../../issues?q=is%3Aissue+is%3Aclosed)
3. If the same problem exists, add new evidence or a 👍 there instead

Duplicates will be closed and linked to the original.

---

## 3. Write Clear Titles

Use this format:

```
[Type] Tank class or feature — short description
```

### Types

| Type | Use when… |
|---|---|
| `Bug` | Something doesn't work as intended |
| `Visual` | Wrong asset, missing animation, rendering glitch, transparency |
| `AI` | NPC / bot behavior is wrong |
| `Balance` | Works as coded but feels too strong, weak, fast, or slow |
| `Regression` | Used to work, now broken after an update |
| `Suggestion` | New idea or design change |

### Examples

- ✅ `[Bug] Trapper traps disappear instantly when placed near base`
- ✅ `[Visual] Necromancer drone outlines not rendering correctly`
- ✅ `[AI] Crasher AI ignores players below level 15`
- ✅ `[Regression] Stalker can no longer turn invisible after latest update`
- ❌ `bugs`
- ❌ `lots of issues`
- ❌ `BUGGGG PLZ FIX`

---

## 4. Include Enough Detail

A useful report contains:

| Field | Example |
|---|---|
| **Tank class / feature** | Overlord |
| **Context** | FFA mode, near Pentagon Nest |
| **Steps to reproduce** | 1. Pick Overlord → 2. Send drones to max range → 3. Right-click to repel → 4. Tab out and back in |
| **Expected result** | Drones return to normal control |
| **Actual result** | Drones freeze in place and become unresponsive |
| **Frequency** | Always / Often / Sometimes / Rarely / Once |
| **Game version or date** | Noticed after the May 2025 update *(if known)* |
| **Browser / device** | Chrome, desktop *(if relevant)* |
| **Evidence** | Screenshot, GIF, or video link |

> **Game version:** If you know which update introduced or changed the
> behavior, mention it. This helps narrow down regressions enormously. Even
> a rough date ("started after the last patch") is useful.

---

## 5. Bugs vs. Feedback

Use the correct template:

- **Bug Report** — something does not work as intended (broken ability,
  wrong rendering, AI misbehavior, collision issue)
- **Feature / Balance Request** — something works but feels wrong, or you
  want something new

Do not mix categories in one issue.

---

## 6. Exploits and Sensitive Issues

Do **not** post detailed exploit or cheat instructions publicly. If the issue
can be abused, report it privately via the
[Discord server](https://discord.gg/P64PZaaMtv) instead of filing a
public issue.

---

## 7. Account, Payment, and Ban Issues

This repository is **not** for account support. For account, payment, or ban
issues, submit a ticket at:

🔗 **https://support.vexxusarts.com/submit-ticket/3-diepio**

Issues filed here for account support will be closed immediately.

---

## 8. Language

Issues should be written in **English**. If English is not your first
language, do your best — we appreciate the effort. You may include a
description in your native language *in addition to* an English summary if
that helps communicate the problem more clearly.

---

## What Will Get Your Issue Closed

| Reason | Policy |
|---|---|
| Mega-list of unrelated bugs | Closed; resubmit individually |
| Duplicate | Closed with link to original |
| No useful information / too vague | Labeled `needs-info`; closed after 14 days if no response |
| Not a bug (intentional behavior) | Closed with explanation |
| Account / ban / payment support | Closed; use [Support Tickets](https://support.vexxusarts.com/submit-ticket/3-diepio) |
| Hostile or disrespectful tone | Closed; repeated offenses may result in a repo ban |

---

## Moderation

Maintainers are developers assigned to Diep.io by 3AM Experiences LLC. They
are responsible for labeling, confirming, prioritizing, and closing issues.
Only maintainers create umbrella or tracking issues.

If you disagree with a closure, reply politely on the closed issue with new
evidence. Do not open a new issue to argue about a closed one.

---

## Summary Cheat Sheet

| ✅ Do | ❌ Don't |
|---|---|
| One bug per issue | Dump 50 bugs in one issue |
| Search for duplicates first | Assume nobody reported it |
| Include the tank class name in the title | Use vague titles |
| Describe expected vs. actual behavior | Just say "it's broken" |
| Group related bugs for the **same tank class + system** | Group bugs just because you found them at the same time |
| Include reproduction steps | Assume we know what you mean |
| Attach screenshots or video | Leave a text-only report for visual bugs |
| Use [Support Tickets](https://support.vexxusarts.com/submit-ticket/3-diepio) for account issues | File account/ban issues here |
| Report exploits privately on [Discord](https://discord.gg/P64PZaaMtv) | Post exploit details publicly |
| Mention the game version or date | Omit when the bug started |

Thank you for helping make Diep.io better!
