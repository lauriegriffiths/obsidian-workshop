# Contacts overview

```dataview
TABLE birthday AS "Birthday", address AS "Postal address"
FROM "People"
SORT file.name ASC
```

Expected: Alex, Maya and Sam. Open a person to read context; use backlinks for dated conversations.
