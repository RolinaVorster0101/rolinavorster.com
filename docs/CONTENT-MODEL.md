# Content Model

This document is conceptual. Exact Astro schemas will be implemented when the project is scaffolded.

## Project

Required/core fields:

```text
title
slug
summary
year
status
types[]
context
tags[]
technologies[]
role
featuredImage
featured
content
```

Optional fields:

```text
organisation
collaborators[]
gallery[]
videos[]
repositoryUrl
liveUrl
externalLinks[]
demo
downloads[]
changelog[]
publishedDate
updatedDate
```

### Project types

- Software
- Design
- Hardware
- Other

`Other` is supported but should not appear as a public filter/category until at least one real project requires it. Hardware follows the same UI rule: do not display empty categories.

Projects may have multiple types.

Websites are classified by the disciplines actually represented. Examples:

- designed + developed website: `Design`, `Software`
- UI-only website concept: `Design`
- web application: usually `Software`, plus `Design` if the design contribution is material

Web-specific detail belongs in tags/technologies.

### Context

- Professional
- Independent
- Academic
- Experimental

Context describes why/where the project exists; type describes what kind of work it is.

### Tags

Tags carry detailed, cross-cutting classification such as `C#`, `ASP.NET`, `UI`, `Accessibility`, `IoT`, `Web Development`, `Frontend`, `Robotics`, `Machine Learning` or `Design Systems`.

Maintain a controlled vocabulary to avoid near-duplicates such as `CSharp` vs `C#`.

### External links

Every external link must have a human-readable label.

```text
externalLinks:
  - label: "View the Figma prototype"
    url: "..."
    type: "figma"       # optional hint for icon/presentation
```

### Gallery

```text
gallery:
  - image: "..."
    alt: "..."
    caption: "..."      # optional
```

Alt text is required unless an image is explicitly decorative.

### Video

Support local video and external embeds.

```text
videos:
  - type: "local"
    src: "..."
    poster: "..."
    caption: "..."

  - type: "youtube"
    url: "..."
    caption: "..."
```

External video players should be lazy-loaded / click-to-load where practical to reduce unnecessary third-party requests and page weight.

### Rich body

Project content must support media/components inline. Galleries and video are not restricted to a fixed block at the bottom of the page.

## Note

Core fields:

```text
title
slug
description
publishedDate
tags[]
content
```

Optional fields:

```text
updatedDate
featuredImage
gallery[]
videos[]
externalLinks[]
```

Notes use the same reusable media concepts as Projects and can place rich media inside the content body.

## Related content

Projects and Notes should be structurally capable of linking to related content. Initial related-content logic can use shared tags/types and may be added to the UI only when there is enough content to make recommendations useful.
