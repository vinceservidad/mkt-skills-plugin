# Tracking guide

## Source of truth

Orders and revenue: the store or billing system. Leads and deals: the CRM. Platform conversions are that platform's view under its own rules.

## Defect versus attribution

| Symptom | Likely |
| --- | --- |
| Platform conversions exceed total orders | Collection defect (double firing, wrong page, renewals counted) |
| Platform credits more than last click | Attribution difference (windows, view-through, model) |
| Both move together with orders | Real change |

Fix defects first, then read attribution.

## Events

One name format (for example object_action), fire once, include order or lead ID for deduplication across browser and server.

## UTMs

source (where), medium (type), campaign (initiative), content (variant). Lowercase, allowed-value list, required on email, podcast, partner and social links.

## Server-side

A conversions API or server-side tag sends events from the server; deduplicate with the browser event by event ID. Setup and requirements change: cite current platform docs with URL and date.

## Consent

Tags that need consent vary by place (for example the EU and UK, some US states); verify or mark *to confirm*.
