---
tags: a/note
---
in:: [[obsidian objects]]

# Let's start with a MOC
Maps of Content (MOC) organize a bunch of notes into a single topic, making it easier to remember and find things. It's a simple concept already using basic objects and containers. Let's look at it from an object perspective.

`note` -> `topic` -> `index`

This structure has three objects.

- **Index**: The starting point of all knowledge
- **Topic**: A collection of notes about something
- **Note**: A chunk of knowledge.

Let's create a basic recipe collection with objects and links.
- This is an **index** named Index
- This is a **topic** named Recipes **in** Index
- This is a **recipe** named Butter Chicken **in** Recipes.

Even a massive recipe collection doesn't need to be very complex to scale.
- This is an **index** named Index
- This is a **topic** named Recipes **in** Index
- This is a **topic** named Indian Recipes **in** Recipes
- This is a **topic** named Chicken Recipes **in** Recipes
- This is a **recipe** named Butter Chicken **in** Indian Recipes, Chicken Recipes

## Basic file and folder layout
With a topic-based knowledge structure, most navigation happens through links and backlinks. The folder and file structure **doesn't matter**. So Obsidian Objects uses it to convey other types of meaning, like the types of objects and how they're shared. Let's look at a basic (non-shareable) layout.

```
index
topic/topic one
topic/topic two
note/note one
note/note two
note/note three
note/note four
```

While it's easy to imagine how the notes are linked, it illustrates the point that the folder structure doesn't care how notes are linked, and the linking structure doesn't care how notes are stored.

## Basic Sharing
Having a common structure for allows for easier sharing. Let's look at sharing recipes.

**Me**
```
index
topic/recipes
recipe/butter chicken
```

**Mark Bittman**
```
index
topic/recipes
recipe/stuffed flank steak
```

**Michael Ruhlman**
```
index
topic/recipes
recipe/east carolina barbecue
```

If each person links their recipe to their recipes topic, then you can download anyone's recipes, and it auto-magically links to **your** recipes topic.
