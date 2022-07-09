---
tags: a/note
---
in:: [[obsidian objects]]

# Overview of Obsidian Objects
This dives deeper into the reasoning behind Obsidian Objects.

## Brains like things
We don't just take notes, we take notes about things: people, books, projects, meetings, concepts, and ideas. Think about a recipe collection. It holds all the knowledge for making food. It has recipes, and each recipe follows the same format with a list of ingredients and a set of directions. It might include a set of notes, like what braising is and how to do it. Our brains work really well with this type of structure, so let's abstract it to work with any type of note.

Modern web applications are increasing built using a [REST API](https://medium.com/garri-hov/rest-api-guideline-resource-modeling-48e63807a1b3), where the application is simply the interface to read and manipulate **resources**, like posts, songs, products, or orders. This approach adapts the REST API naming structure to notes, by requiring all notes to have an object type. Here's some examples:
- This is a **recipe** note named Butter Chicken
- This is a **person** note named Alice
- This is a **topic** note named Animals

Don't worry, you can have a **note** note too. It may sound redundant, but should make sense shortly.

It's natural to group collections of things into containers, like the recipe collection. That's the approach we're striving for, to create containers of knowledge with common formats. By grouping and linking containers of notes, you can create large knowledge structures that are still easy to navigate.

So Obsidian Objects is a essentially a library of basic objects and containers, and a process for fitting them together. It's a starting point to explore how your brain likes to store and remember the things important to you.

## Sharing knowledge
The current ways of sharing knowledge is linking to other's content, or manually copy and pasting it into your own note format. A common set of objects allows embedding someone else's knowledge directly into your knowledge system. Like with recipes, you should be able to share yours, or download someone else's, and both should seemlessly auto-link into the right container.

## Scaling knowledge
This approach can scale in multiple directions. A recipe collection can have ten recipes, or a thousand. As you add more types of knowledge, you can add more containers to put them in, then create containers of containers. But tying all of these together, particularly notes from different people, requires a common linking structure. 

This follows the container structure. Every note must be **in** a container, and every container must be **in** another container or the index or all containers. Then backlinks or a breadcrumbs heirarchy can be followed from the index to any note.

