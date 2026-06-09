---
title: A3 Evaluation and Reflection – Silent Archive
date: 2026-06-08
author: Boris Lo
summary: Short description
tags:
  - tag1
  - tag2
  - tag3
---
Write your content here.
# Introduction

Silent Archive is a digital memorial platform that I developed to explore how digital spaces can support remembrance and emotional reflection. Unlike traditional social media platforms that focus on constant engagement, this project aims to create a calmer environment where users can preserve memories, express emotions, and interact with others in a more meaningful way.

The final prototype consists of four main sections: Garden, Community, Inbox, and Profile. Each section was designed to support a different part of the user journey, from private reflection to public remembrance and communication.

For this evaluation, I wanted to understand not only whether the website worked technically, but also whether users could understand the experience without needing instructions. To assess this, I conducted Lighthouse performance testing, WCAG-style accessibility checks, responsive layout testing across different devices, and informal user testing. The findings from these evaluations helped me reflect on the strengths of the project, identify areas for improvement, and consider what I would do differently if development continued.

# Performance and Technical Behaviour

## Lighthouse Testing Results

To evaluate the technical performance of the application, Lighthouse audits were conducted on the four main pages of the website. The tests assessed performance, accessibility, best practices, and search engine optimisation (SEO).

| Page      | Performance | Accessibility | Best Practices | SEO |
| --------- | ----------- | ------------- | -------------- | --- |
| Garden    | 100         | 93            | 100            | 90  |
| Community | 96          | 93            | 100            | 90  |
| Inbox     | 100         | 100           | 100            | 90  |
| Profile   | 100         | 98            | 100            | 91  |

*Figure X. Lighthouse audit results across all major pages.*

## Reflection on Performance

Before conducting the Lighthouse audits, I expected the visual design of the project to create performance challenges. Silent Archive includes animated backgrounds, multiple interactive components, database-driven content, and several interconnected pages. Throughout development, I was concerned that these elements could reduce responsiveness or increase loading times, particularly on pages with more visual effects.

However, the Lighthouse results were much stronger than expected. Performance scores ranged from 96 to 100 across all major pages, indicating that the application remained responsive despite the visual atmosphere and interactive features. The Garden, Inbox, and Profile pages achieved perfect performance scores, while the Community page achieved a score of 96. These results suggest that the overall structure of the website remained efficient and did not significantly impact user experience.

One possible reason for these results is that the application uses a relatively simple page structure and avoids unnecessary third-party libraries. Most interactions are lightweight, and database content is displayed in a straightforward manner. This helped maintain smooth navigation between pages while still supporting the intended emotional atmosphere of the platform.

The testing also highlighted several areas for improvement. While performance scores were high, accessibility scores were slightly lower due to issues such as missing labels on some form elements. These issues did not prevent users from completing tasks, but they demonstrate the importance of considering accessibility alongside functionality and aesthetics.

Another limitation of the project relates to the animated video backgrounds used on the Community and Profile pages. Due to time constraints, these assets were sourced from existing visual references rather than being created and optimised specifically for the project. As a result, I was unable to fully investigate how alternative video formats, compression methods, or custom-built animations might affect performance. During development, I observed that large media assets and complex visual effects can sometimes cause delays in loading or reduce responsiveness. Although the current implementation still achieved high Lighthouse scores, future iterations would benefit from creating custom animations and conducting additional optimisation testing. This would provide greater control over file size, visual consistency, and performance across different devices and network conditions.

Looking back, one of the most surprising outcomes of the evaluation was how little the visual effects affected overall performance. I initially assumed that creating a strong atmosphere would require sacrificing efficiency. Instead, the testing demonstrated that it is possible to balance visual storytelling and technical performance when design decisions are carefully considered. This reinforced the importance of testing assumptions rather than relying solely on expectations during development.

![Community Lighthouse](/DECO2017-BLOG/assets/image/lighthouse-community.png)

*Figure 1. Lighthouse audit results for the Community page.*

![Garden Lighthouse](/DECO2017-BLOG/assets/image/lighthouse-garden.png)

*Figure 2. Lighthouse audit results for the Garden page.*


# Accessibility and Responsive Testing

## WCAG-style Testing Evidence

To evaluate accessibility, I combined Lighthouse accessibility results with manual WCAG-style checks. I tested keyboard navigation, focus visibility, colour contrast, form labels, and responsive behaviour across desktop, tablet, and mobile layouts.

| Test | Result | Observation |
|------|--------|-------------|
| Keyboard navigation | Pass | Main navigation, buttons, dropdowns, and inputs could be reached using the keyboard. |
| Focus visibility | Pass | Interactive elements showed visible focus states when tabbing through the page. |
| Colour contrast | Pass | Lighthouse did not identify contrast issues across the tested pages. |
| Form labels | Minor issue | Lighthouse identified that some select elements did not have associated label elements. |
| Responsive layout | Pass with minor issues | Pages remained usable on tablet and mobile, but navigation became crowded on smaller screens. |

The most useful accessibility finding was the missing label issue on select elements. Visually, users could still understand the dropdowns because they were placed near relevant content, such as visibility settings and filters. However, this is still a weakness because screen reader users may not receive enough context about what the dropdown is for.

This made me realise that accessibility cannot only be checked visually. A page can look clear to me but still have semantic problems in the HTML. If I continued development, I would add proper `label` elements or `aria-label` attributes to all form controls, especially dropdowns and icon-only buttons.

