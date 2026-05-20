# Old MVP Evidence Folder

## Purpose

This folder is the home for old Orisen MVP evidence.

It contains the historical prototype description, pilot/test tables, bypass/failure notes, and qualitative tester feedback from the old physical MVP.

## Why this folder exists

The old MVP is important enough that it should not stay as loose files directly under `product/`.

It is one of the strongest current evidence sources for Orisen's first wedge:

- presence-based wake completion
- anti-snooze behavior
- return-to-bed detection
- unplug/battery backup as anti-bypass behavior
- real pilot behavior from early testers

At the same time, it is not proof of:

- broad production reliability
- paid demand
- reduced grogginess
- reduced sleep inertia
- sleep-stage detection
- artificial sleep phase transitioning
- clinical efficacy

## Contents

The old-MVP evidence set is:

- `old-mvp.md`
- `old-mvp-test-row-labels.md`
- `old-mvp-bypass-and-failure-notes.md`
- `old-mvp-user-feedback.md`

## How downstream docs should use this folder

`product/claims-and-evidence.md` should use this folder as the old-MVP evidence source.

Safe use:

- Old MVP supports early prototype/pilot evidence for wake completion.
- Old MVP supports the need for anti-bypass behavior.
- Old MVP supports product lessons such as pre-alarm lockout, volume escalation, battery backup, and event logging.

Unsafe use:

- Do not claim the old MVP proved Orisen reduces grogginess.
- Do not claim it proved artificial sleep phase transitioning.
- Do not claim broad product-market fit.
- Do not claim production reliability.
