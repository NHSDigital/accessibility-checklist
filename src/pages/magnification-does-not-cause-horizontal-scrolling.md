---
layout: page.njk
tags: pages
title: Magnification software users do not have to unnecessarily scroll horizontal to find content

conformanceLevel:
  - Best practice
description:
  - Magnification software users do not have to unnecessarily scroll horizontal to find content
filters:
  - Best practice
interaction:
  - Magnification
knowledgeToTest:
  - Easy
principal:
priority:
responsibility:
  - Designer
severity:
  - Minor
  - Moderate
successCriteria:
  - 1.4.10 Reflow
testProcedure:
  - Manual
  - Visual inspection
timeToTest:
  - Quick
topic:
  - Layout
understandingScURL:
  - https://www.w3.org/WAI/WCAG22/Understanding/reflow
userImpact:
order:
  - 64
---

# {{ title }}

## Design Notes

### Ensure users of magnification software do not have to unnecessarily scroll horizontally to find content (Best practice)

Design interfaces that consider users of screen magnification software.

Consider setting a maximum width for the main body content of pages and favour a single column, vertical arrangement of important information over the horizontal.

Position feedback close to the control which triggered the response. For example, position error messages immediately next to (ideally above) the form input field in error.

#### More information

- [Form Field Usability: Avoid Multi-Column Layouts](https://baymard.com/blog/avoid-multi-column-forms)

### Ensure your designs are responsive

For people with moderate visual impairment, it's important to be able to resize content using browser zoom functions. When users do this on desktop-style browsers they eventually reach mobile size for media queries. Consider how content works in a single column layout and ensure priority content and functionality is operable on smaller screens.

Consider the landscape orientation usage of the small-screen view, and take care with fixed-position elements — do they overlap, obscure or otherwise interfere with using the interface.

For optimal designs across device sizes and orientations it may be that fixed elements such as headers/footers are un-fixed at a certain zoom percentage (e.g. using CSS breakpoints).

#### More information

- [Interaction Design Foundation: Responsive Design](https://www.interaction-design.org/literature/topics/responsive-design)
- [NNGroup: Responsive Design](https://www.nngroup.com/articles/responsive-web-design-definition/)

## Developer Notes

Although heavily reliant on design, ensure horizontal scrolling is not prompted by a change of magnification.

### Ensure the interface is usable when viewport size is changed

Allow the browser zoom function to increase the size of content to 400% without requiring scrolling in more than one direction (horizontal and vertical). This helps people with low vision. Information and functionality must not be lost for users who are zoomed in.

When using zoom users should be able to view and use all content at an equivalent of 320px wide (e.g. with a 1280px window at 400% zoom).

#### Some key considerations

- Fixed height containers of text often break when text spacing is changed. Use min-height instead
- Sticky elements, or containers that prevent scrolling, are often unusable at higher levels of zoom in landscape orientation. Use vertical media-queries to make sure there is enough space
- Large data tables are allowed to scroll horizontally, but you should wrap them in an element that contains the scrolling to the table, rather than making the whole page scroll.

#### Common mistakes

The text and calls-to-action in website hero (aka Jumbotron) sections at certain zoom percentage due to fixed height container being used.

#### Information and tools

- [Responsive web design basics - web.dev](https://web.dev/responsive-web-design-basics/)
- [A Dao of Web Design -  A List Apart](https://alistapart.com/article/dao/)

## Testing Notes

By zooming or using magnification methods within a browser, check that the user is not forced to scroll horizontally to reach content. If there is any content that requires scrolling in two dimensions, evaluate if the two-dimensional layout is essential.

**WCAG Reference:** [Understanding Success Criterion {{ successCriteria}}]({{ understandingScURL }})
