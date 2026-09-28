# Decision Log

Record decisions that materially affect the site's identity, content model, architecture or long-term maintainability. This is not a diary; it preserves rationale that would otherwise be lost.

## D001 — Stable identity rather than job-title branding

**Decision:** The site is Rolina's long-lived home on the internet rather than a site branded around a current job title.

**Why:** Roles and interests change. The stable pattern is understanding how things work, improving them and building useful solutions.

## D002 — Public identity line

**Decision:** Use `Developer · Designer · Problem Solver` with `Understand. Improve. Build.` as the primary public shorthand.

## D003 — Astro for the public site

**Decision:** Start the public site with Astro + TypeScript + HTML + custom CSS.

**Why:** The site is primarily content-led, visual and static with selective interaction. Astro allows static output by default while leaving room for interactive components and future server rendering if genuinely needed.

## D004 — Custom CSS + BEM

**Decision:** Use custom CSS and BEM as the default component naming methodology.

**Why:** It keeps the implementation explicit, maintainable and aligned with a bespoke visual identity without adopting a utility framework's design conventions.

## D005 — Projects, not Work, as the main portfolio concept

**Decision:** Use `Projects` publicly rather than `Work` as the umbrella.

**Why:** Projects naturally include professional, independent, academic and experimental work without implying that everything was paid/client work.

## D006 — Project taxonomy

**Decision:** Project types are `Software`, `Design`, `Hardware`, and optionally `Other`. Hardware and Other remain hidden from public filters until they contain content. Context is separately `Professional`, `Independent`, `Academic` or `Experimental`.

**Why:** Type and context answer different questions. Tags carry detailed subject/technology information. Websites are classified by their actual disciplines rather than creating a mixed-dimension `Web` category.

## D007 — Notes, not Blog or Journal

**Decision:** Use `Notes`.

**Why:** Notes allow short/long, technical/personal and visual/textual content without implying diary-writing or a publishing schedule.

## D008 — Rich media in Projects and Notes

**Decision:** Both content types support inline rich media, optional galleries and local/external video. Projects additionally support repository/live links, named external links, demos, downloads and changelogs.

## D009 — Related content

**Decision:** Structure Projects and Notes so related content can be surfaced later, primarily from shared metadata. Do not show it until there is enough content for it to be useful.

## D010 — Search/tags timing

**Decision:** Store tags from V1. Do not add site search or elaborate public tag browsing until content volume warrants them.

## D011 — Follow a rabbit hole

**Decision:** Reserve `Follow a rabbit hole` as a future homepage discovery section based on tags/related content. Keep it hidden until the site has enough content to make it meaningful.

## D012 — Future commerce/accounts

**Decision:** Leave room for digital products and a customer portal without building them in V1. A future ASP.NET Core app on a separate subdomain is a strong candidate for accounts, purchases, licences, subscriptions and billing.

## D013 — Security from the beginning

**Decision:** Security is reviewed throughout implementation and deployment, not bolted on at launch. Prefer the smallest runtime surface that satisfies current requirements.

## D014 — Git from first implementation commit

**Decision:** Initialize Git before building and commit incrementally from the start.

**Why:** Preserve reasoning/history, make experimentation safer and avoid the common failure mode of adding version control only after substantial work already exists.
