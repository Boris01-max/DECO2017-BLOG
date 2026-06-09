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

This made me realise that accessibility cannot only be checked visually. A page can look clear to me but still have semantic problems in the HTML. If I continued development, I would add proper label elements or aria-label attributes to all form controls, especially dropdowns and icon-only buttons.

![Accessibility Warning](/DECO2017-BLOG/assets/image/accessibility-warning.png)

*Figure 3. Lighthouse accessibility warning showing missing labels on select elements.*

## Responsive Layout Testing

Responsive behaviour was manually tested using Chrome Developer Tools across tablet and mobile viewports.

Testing was conducted using:

* iPad Air (820 × 1180)
* iPhone SE (375 × 667)

The Community page adapted successfully from a multi-column desktop layout into a single-column layout on smaller devices. Memorial cards remained readable and interactive elements such as search filters and friend controls remained accessible.

The Garden page also remained functional on tablet and mobile devices. Memorial cards stacked vertically and maintained readability. However, the navigation bar became increasingly crowded on smaller screens, suggesting that a dedicated mobile navigation menu would improve usability.

The Inbox page performed particularly well during responsive testing. Content blocks resized correctly and all controls remained accessible without horizontal scrolling.

The Profile page required the most responsive adjustments due to its custom circuit-board layout. Although the page remained usable on both tablet and mobile devices, significant scaling was required to fit all interactive elements within smaller viewports. Future versions could benefit from a simplified mobile-specific layout.


![Community Tablet](/DECO2017-BLOG/assets/image/community-tablet.png)

*Figure 4. Community page displayed on an iPad Air viewport.*

![Garden Tablet](/DECO2017-BLOG/assets/image/garden-tablet.png)

*Figure 5. Garden page displayed on an iPad Air viewport.*

![Community Mobile](/DECO2017-BLOG/assets/image/community-mobile.png)

*Figure 8. Community page displayed on an iPhone SE viewport.*

![Profile Mobile](/DECO2017-BLOG/assets/image/profile-mobile.png)

*Figure 11. Profile page displayed on an iPhone SE viewport.*

# Lessons Learned

Looking back on the project, the biggest lesson for me was learning how difficult it is to move beyond familiar design patterns. Throughout development, I was heavily influenced by the idea of an online community. Because of this, I kept thinking that the platform needed features commonly found in community-based websites. As a result, we continued adding functions and interactions that felt familiar rather than questioning whether they were truly necessary for the experience we wanted to create.

Over time, I realised that adding more features does not automatically make a website more meaningful. In some cases, additional functions increased complexity without strengthening the core idea of remembrance and reflection. If I were to continue developing Silent Archive, I would spend more time identifying the essential experience first and only include features that directly support that goal.

I also learned that innovation is not only about functionality but also about presentation and visual identity. While the final design is functional and visually consistent, many aspects of the interface still resemble conventional websites. The layouts, navigation structure, and colour palette were largely based on safe design decisions. Rather than exploring more experimental directions, I often chose options that felt reliable and familiar. This helped reduce design risk, but it also limited the uniqueness of the final experience.

In hindsight, I believe I was too focused on making the platform work and not focused enough on creating a distinctive visual language that would give users a strong reason to remember the website. The project challenged me to think about how interaction design, atmosphere, and visual storytelling can work together to create a stronger emotional impact.

Perhaps the most important lesson from this project is that good design is not about how many features are included. Instead, it is about making deliberate decisions and ensuring that every element contributes to the overall experience. Moving forward, I want to become more confident in removing unnecessary features, taking creative risks, and exploring ideas beyond familiar design conventions.
