# Birthdays next calendar month

Demo reference date: October 26, 2026. “Next month” means November, not the next 30 days. The query compares the month, so birth year does not affect the result.

```dataview
TABLE birthday AS "Birthday", address AS "Send a card to"
FROM "People"
WHERE birthday AND birthday.month = (date(2026-10-26) + dur(1 month)).month
SORT birthday.day ASC
```

Expected: Maya on November 8, then Alex on November 23. Sam is excluded.

## Live version

This version follows today's date, so results may differ when you rehearse.

```dataview
TABLE birthday AS "Birthday", address AS "Send a card to"
FROM "People"
WHERE birthday AND birthday.month = (date(today) + dur(1 month)).month
SORT birthday.day ASC
```

Use proper date properties, not ambiguous date strings. This month-based filter also handles December to January; February 29 remains a February birthday and the person decides when to send the card in other years.
