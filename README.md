# Rolina Vorster — Personal Website

Personal website and evolving home on the internet for Rolina Vorster.

**Developer · Designer · Problem Solver**

**Understand. Improve. Build.**

> I explore ideas, learn how things work and turn what I discover into useful, beautiful and robust solutions.

## Purpose

This is not intended to be a conventional portfolio template. It is a long-lived personal site that can contain professional work, independent projects, notes, current interests and learning, while remaining stable as Rolina's career and interests change.

The site's underlying pattern is:

**Reality → Understand → Improve → Build**

The public shorthand is:

**Understand. Improve. Build.**

The recurring informal line is:

**Building things · Learning things · Figuring things out**

## V1 technology

- Astro
- TypeScript
- HTML
- Custom CSS using BEM naming
- CSS custom properties/design tokens
- Selective JavaScript/TypeScript only where interaction requires it
- CSS animations / Web Animations API where appropriate
- SVG for identity marks, diagrams and lightweight visual elements
- Astro content collections for Projects and Notes

The public site should remain predominantly static and progressively enhanced. Complexity should be introduced only where it provides a real benefit.

## V1 site structure

Primary navigation:

- Projects
- Notes
- Now
- About
- Contact

The site mark/name returns to Home. The CV is available from appropriate professional contexts (especially About) rather than occupying primary navigation.

Not in V1 unless real content creates a reason: Search, public tag browsing, Shop, customer accounts, newsletter, comments, speaking section, product documentation.

## Core content types

### Projects

A Project is something Rolina made or materially contributed to.

Primary project types:

- Software
- Design
- Hardware
- Other (supported, but hidden from public filtering until it has real content)

A project may have multiple types. Websites are not a separate type: their actual disciplines determine classification, while tags provide web-specific detail. For example, a designed-and-developed website may be `Design + Software` with tags such as `Web Development`, `Frontend`, `UI`, `HTML`, `CSS` and `JavaScript`.

Project context is separate from type:

- Professional
- Independent
- Academic
- Experimental

Tags provide the detailed cross-cutting taxonomy.

Project entries can support repository links, live links, named external links, local or externally embedded video, galleries, demos, downloads and changelogs. These are optional and should appear only when meaningful.

### Notes

Notes are things Rolina wants to record, explain, explore or share. They are deliberately not framed as a journal or a conventional blogging obligation.

Notes may be short or long, technical or personal, text-led or visual. Their bodies can contain images, galleries, video, diagrams and other rich media at meaningful points in the content rather than forcing all media into a gallery at the end.

### Now

A living snapshot rather than an archive. Possible headings include Building, Learning, Figuring out, Playing and Exploring. Only use headings that reflect reality at the time.

## Homepage direction

Current planned sequence:

1. Hero — identity: `Understand. Improve. Build.`
2. Selected Projects — evidence early
3. Now — what is happening currently
4. Recent Notes — thinking and discoveries
5. Personal/visual interruption — warmth and personality without forcing a lesson
6. Short About introduction
7. `Follow a rabbit hole` — future discovery section, only once enough connected content exists
8. Contact invitation and footer

The experience should move roughly through **Identity → Evidence → Present → Thinking → Person → Story → Connection**.

## Voice

The site should sound like Rolina, not like a polished thought-leadership persona.

Preferred qualities: curious, intelligent, warm, precise, grounded, occasionally playful, willing to say when something is not yet understood.

Natural openings include:

- “I've been thinking about this…”
- “I don't understand this yet…”
- “I thought X, but…”
- “I tried this…”
- “Something about this doesn't make sense…”
- “I found this fascinating…”
- “I built this because…”

Avoid manufactured authority, engagement bait, generic inspiration, forced business lessons from hobbies, productivity-cult language, and pretending every interest needs symbolic meaning.

A useful reminder: **Sometimes you can just really like a bloody daisy.**

See `docs/CONTENT-AND-VOICE.md` for the operational content rules.

## Design direction

**Bright. Intelligent. Warm. Curious. Precise. Calm. Modern. Human.**

The visual system deliberately combines contrasts such as ballet pink with raw steel, precise grids with organic wildflowers, clean typography with handwritten notes, and digital interfaces with pen-and-paper details.

The existing visual brand/style guide remains the visual source of truth while the repository documentation records implementation and content decisions.

## Documentation

- `docs/CONTENT-AND-VOICE.md` — voice, Notes guidance and content behaviour
- `docs/CONTENT-MODEL.md` — Project and Note schemas and taxonomy
- `docs/ROADMAP.md` — V1 vs architect-for vs later features
- `docs/ARCHITECTURE.md` — technical architecture and future customer portal
- `docs/SECURITY-AND-DEPLOYMENT.md` — security principles and VPS deployment planning
- `docs/DECISIONS.md` — important decisions and why they were made

These documents should evolve with the site. Significant decisions should be recorded rather than left only in conversation history.

## Git

Initialize Git before implementation begins and commit from the start.

```bash
git init -b main
git add .
git commit -m "chore: initialise personal website project"
```

A repository-level `.gitignore` should be committed from the beginning. Never commit secrets, `.env` files containing credentials, private keys, deployment credentials, build output or dependency directories.

## Repository name

Recommended: **`rolinavorster.com`**

It says exactly what the repository contains and distinguishes it from future repositories that may also be called Rolina Vorster projects.

Alternative: `rolina-vorster-site`.

Suggested GitHub description:

> Personal website and evolving portfolio — projects, notes and things I'm building, learning and figuring out.

## Security

Security is a project-wide concern, not a deployment checklist added at the end. It should be considered during design, implementation, dependency selection, forms, external embeds, deployment and ongoing VPS maintenance.

The first release can remain a static Astro site where possible, which keeps the public runtime surface small. VPS hardening, HTTPS, web-server configuration, deployment user/permissions, firewalling, updates, backups, security headers, logging and the contact-form architecture must be explicitly reviewed before launch.

See `docs/SECURITY-AND-DEPLOYMENT.md`.

## Status

Planning / pre-build.

Next design task: define the homepage hero composition, content, interactions and responsive behaviour.
