---
title: "Database fields and queries"
note_type: "documentation"
tags: ["runes/index", "sofia-pereswetoff-morath"]
---

# Using the database

The notes work in plain Obsidian. The properties at the top hold Sofia's catalogue number, signature, date, findplace, object type, material, and reading status. You do not need a plugin to browse them.

## If you use Dataview

This lists the plates Sofia marks as interpreted:

```dataview
TABLE catalogue_number AS "No.", country, plate_type, material, dating
FROM "Files/Sofia - Viking-Age Runic Plates/Plates"
WHERE interpreted = true
SORT catalogue_number ASC
```

This finds plates linked to balanced runes:

```dataview
TABLE catalogue_number AS "No.", place_of_find, dating
FROM "Files/Sofia - Viking-Age Runic Plates/Plates"
WHERE contains(file.outlinks, [[Concepts/Balanced runes]])
SORT catalogue_number ASC
```

## Where the information comes from

The plate details come from Appendix 1 of [Sofia's book](<Sofia Pereswetoff-Morath - Viking-Age Runic Plates - Source.md>). The short rune notes summarize the sections linked at the bottom of each note. The original PDF has not been changed.
