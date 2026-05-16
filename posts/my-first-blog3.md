---
title: Thirty
date: 2026-04-25
author: Boris Lo
summary: In this post, I start organising the platform structure through user flow and sitemap development to understand how users move through memorial spaces and interaction systems.
tags:
  - ideation phase 
  - interactive application 
  - endless possibilities 
---
Here I will write about all of the yhings.....

this is a markdown, so i can **use markdown**

# User flow

The user flow focuses on the main task users complete inside the platform: entering a memorial space, understanding the person’s story, and leaving a respectful interaction. Instead of creating a fast browsing experience like mainstream social media, the flow is intentionally simple and slower-paced so users can move through the platform without feeling overwhelmed.

The main experience of the platform is designed around emotional interaction and reflection rather than endless content consumption. Because of this, the navigation structure remains minimal and focused.

## Main user task

Browse memorial spaces → open a grave page → read memories → leave an interaction → continue exploring.

                              Home page
                                  ↓
                        Browse cemetery spaces
                                  ↓
                        Select memorial / grave
                                  ↓
                           View grave page
                                  ↓
                  Read stories, images, and memories
                                  ↓
                           Choose interaction
                                  ↓
                       Leave flower / short message......
                                  ↓
               Return to cemetery page or continue exploring

# System Structure

According to our user flow, we started organising the overall structure of the platform and identifying the core systems users would interact with.

## Sitemap

```
Home page
├── Browse cemetery spaces
│   ├── Search memorial / user
│   ├── Memorial pages
│       ├── Memorial content
│       │   ├── Stories and memories
│       │   ├── Images
│       │   └── Personal information
│       ├── Leave flower interaction
│       └── Short text interaction
│
├── Cemetery management
│   ├── Personal burial ground
│   ├── Manage memorial pages
│   ├── Uploaded memories and interactions
│   └── Cremation furnace system
│
└── User profile
    ├── Account settings
    ├── Saved interactions
    └── Personal information
```

During the structuring process, we prioritised memorial browsing and cemetery management as the core experience of the platform. Large public discussion systems and “nearby” recommendation features were intentionally removed because we wanted the platform to focus more on emotional resonance and one-on-one interaction rather than large-scale social communication or geographical relationships. Separating cemetery management into its own major section also helped emphasise the importance of memorial and content management within the overall experience.


# Identifying unknowns and risks

One important uncertainty we identified is whether reducing so many traditional online community functions will negatively affect long-term engagement and interaction within the platform. Compared to mainstream social media platforms, we intentionally removed features such as large discussion systems, recommendation feeds, and complex communication functions in order to maintain a calmer and more emotionally focused experience. However, this may also reduce user activity and limit the ways people interact within the community.

This created an important trade-off during the design process. While simplifying the platform helps reinforce emotional reflection and memorial atmosphere, it may also make the platform feel less socially active compared to conventional online communities. As the project develops further, we will need to evaluate whether the current interaction systems are emotionally meaningful enough to sustain user participation without relying on traditional engagement-driven features.

```test 
code blocks and all that 
```
You might want to revisit [https://www.
markdownlang.com/cheatsheet/](https://www. markdownlang.com/cheatsheet/)to refresh
yourself on Markdown syntax.