# Canonical trip record and change handling

Use an existing maintained plan/ledger as the source of truth. If none exists and the task is substantial, establish a compact record in the user's chosen workspace/document. This is a guide, not a requirement to build a database or expose implementation details in the family itinerary.

| Record | Useful fields |
|---|---|
| Trip | Dates/year, time zones, origin/return deadline, travelers/ages, vehicle configuration, comfort constraints, priorities, currency, cancellation preference |
| Day | Date, overnight, departure/arrival windows, driving versus elapsed time, breaks, core outing, optional/substitute stops, meals |
| Stop | Stable ID, exact name/branch, address/coordinates, official source, duration/walking effort, hours/season, tickets, parking/transit, status |
| Stay | Dates/nights, exact room/beds/occupancy, channel/link, access confirmation, parking, cash/points, due-property fees, payment status, cancellation terms |
| Reservation | Linked stop/stay, quoted/prepared/booked/canceled status, private confirmation evidence, refund status, checked date |
| Cost | Category, retained/removed item, actual/quote/estimate, cash/points, paid/due, included fees, optional/included, source/date |
| Uncertainty | Question, consequence, pending evidence, fallback and recheck date |
| Artifact | Existing map/doc/plan links, language, access level, last verified update |

Keep contact details, confirmation numbers and payment evidence private. Shared versions should offer useful logistics without account-specific links or sensitive health details.

## Source/status rules

- Current booking confirmations and written property replies outrank general summaries but apply only to the dates, unit and vehicle described.
- Latest explicit user decisions supersede older plans; optional suggestions do not automatically replace booked stops.
- A quote is not booked; approval is not checkout success; a room request is not guaranteed; a cancellation request is not completed cancellation.
- Connect uncertainty to a useful fallback: surface lot for unknown garage fit, shorter walk when tired, picnic for unconfirmed cafe hours.
- Record validity/check date for operational information. Keep transient prices, schedules and loyalty balances out of the reusable skill itself.

## Change sequence

1. Recover the latest plan and requested change. Identify affected dates, nights, reservations, routes, parking, meals, tickets, return time and cost.
2. Research affected choices without reopening settled decisions unnecessarily.
3. Carry out authorized actions in a recoverable order. Preserve old bookings until replacements are confirmed when appropriate; resolve ambiguous checkout before retries.
4. Update the canonical record, requested shared artifacts and translated versions. If an artifact is inaccessible, state what remains stale.
5. Read back the saved changes. Check dates, route order, occupancy, budget arithmetic, links, removed items and sharing. Return useful links and unresolved details.

## Full-plan completion check

- Every overnight has enough beds, current status, parking and cancellation terms.
- Driving days fit the family's pace and return deadline; timed activities allow travel, check-in, breaks and meals.
- Map contains outbound/return legs, final stays, parking and chosen outings; alternatives are clearly optional.
- Food matches real branches/hours and does not hide costly detours.
- Budget matches retained itinerary and distinguishes cash, points, credits, actuals and estimates.
- Shared itinerary, translations, map and private booking checklist agree; uncertainties have fallbacks or recheck tasks.
