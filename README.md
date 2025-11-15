# **Snapshot Repository**

The **snapshot** repository is a dedicated home for all “snapshot-style” websites—self-contained HTML apps that follow the `is-*` naming convention. These pages present structured topics using collapsible sections, filterable hubs, dynamic grids, and a consistent dark-first design system.

This repo exists to collect, refine, and evolve these patterns in a clean environment separate from the experimental workflows of *pocket-deploy*. It focuses on clarity, quality, and maintainability.

---

## **🎯 Purpose**

The goal of this repository is to:

* Host all “is-*” snapshot sites in one coherent ecosystem
* Provide a stable foundation for future snapshot-based applications
* Preserve the patterns and structures that work best
* Make it easy for AI-assisted tools (Claude Code, ChatGPT) to build, update, and extend snapshot apps
* Serve as a production-grade home for polished content

If *pocket-deploy* is the workshop, **snapshot** is the gallery of completed patterns.

---

## **📦 What This Repo Contains**

### **1. Hubs**

Central index pages that display snapshots using searchable, filterable card grids:

* `is-gospel-hub/`
* `is-real-analysis-hub/`
* `is-ww2-hub/`
* `is-revwar-hub/`
* `is-war-hub/` (hub of hubs)

### **2. Snapshot Pages**

Individual pages built on a standard seven-section collapsible layout. Examples include:

* Theology pages (`is-biblical-faith/`, `is-cruciform-god/`, etc.)
* Real analysis theorem pages (`is-real-analysis-heine-borel/`, etc.)
* WW2 battle cards (`is-ww2-battle-of-midway-1942/`)
* Revolutionary War battles (`is-revwar-lexington-and-concord-1775/`)

Each snapshot page is fully self-contained: HTML, CSS, and JavaScript are all embedded in the page.

### **3. Pattern Pages**

Reference examples that define the canonical structure:

* `is-instructor-snapshot/` — the reference implementation for snapshot pages
* Any pattern files needed for consistent development

### **4. Documentation**

Instruction files that define how snapshot systems should be built, extended, and maintained:

* Battle card instructions
* Real analysis theorem card instructions
* Gospel snapshot instructions (if applicable)
* Any new instruction sets this repo adopts

---

## **🎨 Design Philosophy**

Snapshot websites follow a set of principles:

* **Flat structure:** Each page lives in its own directory at the root
* **Self-contained:** No external dependencies except optional scripts (e.g., Blue Letter Bible Tagger)
* **Consistency:** Shared design tokens for all color palettes and layout patterns
* **Responsiveness:** Mobile-first design with smooth behavior across devices
* **Minimal friction:** Easy for both humans and AI tools to create, update, and maintain

This ensures reliability, portability, and predictable patterns for automated creation.

---

## **🧩 Core Components**

### **1. Collapsible Sections**

Each snapshot page contains seven structured collapsible sections.
Sections use a single-accordion behavior: only one open at a time.

### **2. Hubs & Filterable Grids**

Hub pages provide:

* Search by title, tags, or keywords
* Tag-based filtering
* Dynamic card rendering using lightweight JavaScript

### **3. Navigation**

Each snapshot page links back to its hub.
All links use absolute paths based on the repository name for GitHub Pages deployment.

### **4. Universal Color Tokens**

Standardized CSS variables (dark-first) ensure visual consistency across all apps.

---

## **🚀 Deployment**

This repo is designed for direct deployment via **GitHub Pages**.

### **URL Format:**

```
https://ewallt.github.io/snapshot/<directory-name>/
```

After enabling Pages in repository settings (deploy from `main`), each folder’s `index.html` becomes publicly accessible.

---

## **🛠 AI Development Workflow**

This repo is optimized for AI agents such as Claude Code and ChatGPT:

* Predictable folder structure
* Clear naming conventions
* Consistent UI patterns
* Embedded, self-contained HTML pages
* Explicit instructions for hub updates
* Minimal noise in the repo

AI agents can reliably:

* Add new snapshot pages
* Update hubs
* Fix internal links
* Validate structure
* Expand existing systems

---

## **📘 Adding New Snapshot Content**

1. Create a directory named `is-{topic-slug}/`
2. Add a fully self-contained `index.html`
3. Use the standard snapshot seven-section layout
4. Update the corresponding hub’s JavaScript array with:

   * id
   * title
   * blurb
   * tags
   * view URL
5. Commit and push

All new content must follow slugging rules: lowercase, hyphens, no spaces, no punctuation.

---

## **📂 Repository Structure Example**

```
snapshot/
├── is-gospel-hub/
├── is-biblical-faith/
├── is-cruciform-god/
├── is-real-analysis-hub/
├── is-real-analysis-heine-borel/
├── is-ww2-hub/
├── is-ww2-battle-of-midway-1942/
├── is-revwar-hub/
├── is-revwar-lexington-and-concord-1775/
└── is-instructor-snapshot/
```

---

## **📝 Notes**

* This repo represents the clean, production-ready version of snapshot-style apps.
* Experimental or incomplete snapshot work should remain in `pocket-deploy`.
* When a snapshot app feels polished, you can “promote” it into this repo.
