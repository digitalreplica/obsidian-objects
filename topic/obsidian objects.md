---
tags: a/topic
---
in:: [[topics]]
```breadcrumbs
type: tree
dir: down
depth: -1
from: -"_templates"
```

# Introduction
Obsidian Objects is a folder structure for sharing repositories of knowledge inspired by REST APIs, with a topic-based linking system to connect notes together. It solves the problem of sharing notes between our personal and work lives, and also allows sharing of notes with other people or the world. 

It's built with three basic tenants:

* Notes are **objects**, stored by what type of note it is and who can see it.
* A common object format allows notes to be **shared**.
* A common linking method allows knowledge to **scale** efficiently.

## Overview
- Read the [[obsidian objects overview |Overview]] for the reasoning behind the approach
- Create a [[obsidian objects basic moc |Basic MOC]] (map of content) using objects
- Look at [[obsidian objects additional principles |additional principles]] for how everything is laid out
- See the full [[obsidian objects shareable folder structure |shareable folder structure]]
- Learn about [[obsidian objects frontmatter tags and links |front matter, tags, and links]]
- See the list of [[obsidian objects common objects |common objects]]

## Getting started
- Download the starter kit
- Configure [[obsidian objects configuration and plugins |obsidian and plugins]]
- Add templates for common objects
- Link in a shared repository

## Using Obsidian Objects
- Navigating the knowledge structure
- Creating new types of objects
- Adding fields to objects
- Creating a shared repository
- Explore different linking methods
- Explore note naming methods

## Task objects
- What is a task object
- Creating a lightweight tracking system

## Getting help

# Implementation
Implementation of this structure is very much a work-in-progress to extend the type of objects, find the best ways to link and query them, and share them.

## Tagging
Tags denote objects for notes, and actions for tasks. Obsidian Objects uses only two tags to minimize conflicts with existing tag structures. Each tag nests to fully describe it.

Tag | Applies to | Description | Examples
--- | --- | --- | ---
a | notes | Object type or shape | `a/note`, `a/topic`, `a/recipe`, `a/project`, `a/person`
do | tasks | Tasks type or shape | `do/read/book`, `do/drink/beer`

This allows even tasks to become a "lightweight object" for a simple database or tracking system.

## Front matter
Every object has [YAML front matter](https://help.obsidian.md/Advanced+topics/YAML+front+matter) describing what type of object it is, and where it links to. Obsidian doesn't like wikilinks in front matter, so a dataview inline field is used just below the frontmatter. Here's the front matter for a note and a topic

Notes and topics can be related through breadcrumbs `same` links.

## Starter Kit
TODO: link to starter kit

## Templates
TODO: link to templates

## Fields
More complex objects can use dataview fields to add structure. Here are some examples.

**project**
```
---
tags: a/project
active: false
due: 2022-12-31
---
```

**person**
```
---
tags: a/person
birthday: 2000-01-01
---
```

# Common objects

## Linking objects
For many objects, a simple topic for that type of object is easiest. Here an example for things, showing object type and how things are linked.

**iphone (a/thing) -> my things (a/topic) -> index**

Some objects can vary based on personal preference. Here are two ways a journal could be linked.

**2022-01-01 (journal) -> journals (topic) -> index**
**2022-01-01 (journal) -> 2022 (year) -> years (topic) -> index**

While the second seems longer, the year approach is more useful. I'm linking events and journals to a year, and using the year to summarize what I want to remember about it. Other date-based things like trips can easily be added in. And it's just as easy to navigate with `Quick switcher` -> `22` and year/2022 is the first item, or linking years with breadcrumbs `prev` and `next` links.

Other objects need more organization. People is a great example, with an `all people` topic fairly useless. But home and work people could use structures like:

**Mom (person) -> family (community) -> communities (topic) -> index**
**Brad (person) -> hr (team) -> my company (company) -> index**

## Nested Topics
Topics can eventually grow large enough to break into subtopics. A large collection of recipes might become:

**butter chicken (recipe) -> indian cooking (topic) -> cooking (topic) -> index**

## Flexible linking
There are many ways to link between objects, topics and the index. There's not a "best" way that will work for everyone. It's really a bit of experimentation to find a combination to fit they way you think and remember things. It's not that hard to relink something if it doesn't work out, simply change the `in` wikilinks in each note or topic. You don't even have to move the file to a new place.

# Share-friendly file structure
One of the goals is sharing knowledge, both sharing your own out to others, and pulling in knowledge from others. Not everything will be shared though, or some stuff will only be shared with a few people, so the structure has to take that into account.

Thankfully, there are many ways to share files, synchronize them across devices, and manage access control. What's needed is a way to organize the files and folders to support multiple ways of sharing.

## Private notes
At the heart is a set of private notes that will never be shared. Inside is the object-based file structure shown above. A small structure might look like:

```
index
private/note/note1
private/note/note2
private/topic/topicA
```

## Repositories
This structure follows the conventions for git [repositories](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories). There is a folder for each user or organization you're sharing with. Within that is a folder for each shared repository. And each repository is its own set of Obsidian Objects. So the folder structure looks like

**{owner}/{repository}/{object-type}/{object-name}**

Let's redo the shared recipes from above with this structure.

```
index
private/topic/recipes
private/topic/cooking
private/recipe/butter chicken
private/note/braising chicken
markbittman/recipes/recipe/stuffed flank steak
michaelruhlman/recipes/recipe/east carolina barbecue
```

# TODO
- howto share
- lightweight objects and tasks
- Useful tidbits
	- General Knowledge topic in default note template.
- Sections
	- Types of sections: Note, Thoughts, Research, List, Howto, Preferences, Questions. Other potential sections: argument?
	- Can a section become an object too?
	- Callouts as light objects: person
-

