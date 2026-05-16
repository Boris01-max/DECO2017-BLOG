---
title: Forty
date: 2026-05-02
author: Boris Lo
summary: The first blog post where I go over the brief and consider a few potential concept.
tags:
  - ideation phase 
  - interactive application 
  - endless possibilities 
---
Here I will write about all of the yhings.....

this is a markdown, so i can **use markdown**

# DDD

Memorial pages were identified as the central entity of the platform rather than user profiles. Most interactions, uploaded content, and management systems connect back to memorial pages instead of individual users.

At first, some attributes looked simple inside the wireframe, but later revealed hidden entities during the DDD process. For example, “memorial content” initially appeared as a single section, but it actually contains stories, uploaded images, personal information, and interactions. Similarly, temporary grave posts and cremation furnace records also required their own data structures rather than existing as simple attributes inside memorial pages.

## Memorial page

| attribute | description | example value |
|---|---|---|
| memorial_id | Memorial ID | 001 |
| name | Deceased name | John Smith |
| biography | Personal story | “Loved travelling and photography.” |
| birth_date | Birth date | 1945 |
| death_date | Death date | 2021 |
| cover_image | Memorial image | memorial_01.png |


<br><br>


## Story / Memory

| attribute | description | example value |
|---|---|---|
| story_id | Story ID | 102 |
| memorial_id | Connected memorial | 001 |
| title | Story title | “Family camping trip” |
| content | Story content | “He always carried a camera…” |
| upload_date | Upload date | 2026-05-14 |


<br><br>


## Interaction

| attribute | description | example value |
|---|---|---|
| interaction_id | Interaction ID | 301 |
| memorial_id | Connected memorial | 001 |
| interaction_type | Interaction type | Flower |
| content | Interaction message | “Rest in peace.” |
| created_at | Creation time | 2026-05-14 18:30 |


<br><br>


## Temporary grave post

| attribute | description | example value |
|---|---|---|
| post_id | Temporary post ID | 501 |
| memorial_id | Connected memorial | 001 |
| content | Emotional message | “I still miss you.” |
| created_at | Creation time | 2026-05-14 20:00 |
| expires_at | Deletion time | 2026-05-21 20:00 |

# ERD

```test 
code blocks and all that 
```
You might want to revisit [https://www.
markdownlang.com/cheatsheet/](https://www. markdownlang.com/cheatsheet/)to refresh
yourself on Markdown syntax.