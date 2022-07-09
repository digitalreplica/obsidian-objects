---
tags: a/note
---
in:: [[obsidian objects]]

# Shareable Folder Structure
Obsidian Objects uses four levels of folders for everything except the top-level index files. Each level conveys a specific meaning.

## Organization or community
The first level is who **owns** the notes. When combining knowledge from many sources, having a clear understanding of ownership is critical.

## Sharing level
The second level shows the expected level of **sharing**. This can be one of three choices:
- **Private**: Private notes that should not be shared with anyone
- **Shared**: Notes shared with a limited number of people are groups
- **Public**: Notes shared with everyone

## Repository
The name of the repository of notes. For shared repositories, this is generally related to the topics in the repository.

## Object
The type of notes in this folder.

# Default repository
While the default repository can have any name, within the Obsidian Objects template, it is named `my/private/notes`. This is the most clear and succinct way to describe them.

# Sharing methods
Any sharing method can be used. Most work at the folder level, so sharing individual repositories can easily be done. But sharing at higher level folders is equally possible.

## Symlinks
Obsidian seems to work well with repositories as symlinks to other parts of your file system. So if sharing is already set up, you can pull some of those folders directly in.

# Example
This example takes the recipe collection from before, and lays it out in a more shareable layout.

```
index
my/private/notes/topic/recipes
my/private/notes/recipe/grandmas biscuits
my/public/recipes/recipe/butter chicken
markbittman/public/recipes/recipe/stuffed flank steak
michaelruhlman/public/recipes/recipe/east carolina barbecue
```

All recipes still link up through the recipes topic, but it's far easier to tell where all the recipes came from 