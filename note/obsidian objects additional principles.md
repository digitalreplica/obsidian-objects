---
tags: a/note
---
in:: [[obsidian objects]]

### Principles
A few general principles build upon the framework.

## One vault
One vault to rule them all.

## Objects link upwards
Objects should link up to their topic or place in the structure, or out to related notes or topics. Backlinks, or breadcrumbs `down` and `same`, create the path from the index down through topics to notes. Embedding shared notes with the same topic structure will auto-link them into your structure.

## Object types are singular
REST API design hotly debates whether object types should be singular or plural. Having everything singular makes it consistent, easy to query, and keeps the focus on each object. "It is a `note`. It is a `topic`."

This doesn't apply to object **names**. A note called `elephants`, or a `recipes` topic, makes more grammatical sense.

## Objects are nouns, tasks are verbs
When naming things, try to find the shortest noun form for objects, or verb-form for tasks. For example, instead of the note:

**cutting hair**
```
blah blah
```

It becomes:

**hair**
```
# Cutting hair
blah blah
```

This may not always hold, but the reasoning will be explained later on.

## Uncluttered namespace
Similar to above, names should be as short and direct as possible. The most-used topics and notes should be easily accessible using just the keyboard and quick switcher.