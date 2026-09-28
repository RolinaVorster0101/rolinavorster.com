# Architecture

## Public site

Planned V1 stack:

- Astro
- TypeScript
- HTML
- custom CSS (BEM)
- CSS custom properties/design tokens
- selective client-side JavaScript/TypeScript
- CSS / Web Animations API for most motion
- SVG where appropriate
- Astro content collections for Projects and Notes

Astro's default static output is a good fit for the initial public site. Static output reduces runtime complexity and allows the VPS web server to serve generated files directly. Add server-side rendering or a Node adapter only when a real feature requires server execution.

## Progressive enhancement

HTML provides the content and structure. CSS creates the visual system. JavaScript enhances interactions. Core content and navigation should not depend on unnecessary client-side JavaScript.

## CSS

Use custom CSS rather than a utility framework. BEM is the default naming methodology for component classes. Use native CSS capabilities (custom properties, Grid, Flexbox, `clamp()`, container queries, cascade layers where useful) rather than forcing every styling concern through BEM classes.

## Content

Projects and Notes are the two primary published content types. Now is a living snapshot; About and Contact are purpose-specific pages.

## Future split architecture

If customer accounts/licensing/subscriptions become real, do not force the public Astro site to become the customer application.

Possible future architecture:

```text
rolinavorster.com              Astro public/content site
account.rolinavorster.com      ASP.NET Core customer portal
```

The two systems can share branding and integrate through deliberately designed APIs/authentication/commerce services if and when required.

## Commerce

The site may present and sell digital products in future, but sensitive payment processing should be delegated to an established payment/commerce provider rather than implementing card processing directly.

## Media

- Images should be responsive and optimized.
- Local video is appropriate for short UI demonstrations/loops.
- External video is appropriate for longer walkthroughs.
- External players should be lazy/click-to-load where practical.
- Large binary media should not casually be committed to Git; decide hosting/storage strategy when media volume warrants it.
