# Dr. Alireza Jalali — Interactive Design Studio / Version 07

An independent, editable Jekyll website for Dr. Alireza Jalali (University of Tehran), created to let the professor select the visual direction for a final academic website.

## What makes Version 07 different?

The **Design Studio** controls on the upper left of the desktop interface give live control over:

- **8 complete design presets**, each changing several visual dimensions together
- **17 palettes**: 14 light, 3 dark
- **8 typography pairings** for headings and body copy
- **4 homepage Hero layouts** and **4 complete design languages**
- **3 navigation treatments**, **3 spacing scales**, **3 corner styles**, **3 card styles**
- **4 photo treatments**, **4 background textures**, **3 text scales**, and motion preferences

These choices update the shared site-wide style system. On phones, use the **Customize** icon at top left to open the same Design Studio.

The Save tab supports two named slots (**A/B**), copying a shareable URL, downloading a JSON design specification, copying a text summary, and a mobile-device preview on supported browsers. Browser choices persist with `localStorage`. When another person receives a share link, the URL imports those settings. All functionality runs client-side: no server, tracking, account or paid service.

**Important**: Browser-local selections are personal previews; they are not public repository changes. To make a chosen design the site's default for new visitors, edit `_data/design.yml`, or choose **Design Defaults** in Pages CMS. You can also send the exported JSON file to the developer to reproduce the selected design exactly.

## Publish on GitHub Pages

1. Create a **public** repository called `alirezajalaliut7` in the `AlirezaJalaliUT` GitHub account.
2. Extract the ZIP. Upload its **contents** (not an outer folder) to the repository root. Keep hidden `.pages.yml` in the upload.
3. In GitHub, visit **Settings → Pages → Build and deployment**; use **Deploy from a branch**, select **main** and **/(root)**, then save.
4. Once GitHub Pages finishes its build, open `https://alirezajalaliut.github.io/alirezajalaliut7/`.
5. Edit content using [Pages CMS](https://app.pagescms.org/), after authorizing access to the repository.

`baseurl: /alirezajalaliut7` is set for GitHub Pages project hosting. All local links use `relative_url`. Robots directives have `noindex` and `/alirezajalaliut7/` is excluded from crawling during design selection.

## Content architecture

`_data/site.yml` — professor info, contact, photos and homepage text.

`_data/about.yml` — professor biography.

`_data/design.yml` — published design defaults, accessible through Pages CMS.

`_areas`, `_projects`, `_publications`, `_people`, `_positions`, `_news`, `_teaching`, `_awards`, `_talks` — GitHub Pages compatible collections. Alumni is a filtered view of `_people`. The 12 top-level pages include About, Research, Projects, Publications, Team, Alumni, Teaching, Awards, Talks, Positions, News and Contact.

`assets/css/studio.css`, `assets/js/studio.js` — design system and interactive editor. No npm dependencies or frontend build step.

## Content verification

The supplied earlier site archive provided the professor's portrait, academic profile data, research areas and selected publication records. The design avoids inventing projects, awards, team members or news. Empty sections show clearly marked verification notices. Review `SOURCES_AND_FACT_CHECK.md` prior to publication.

## Testing and limitations

A structural test validates YAML/front matter, 12 section pages, missing includes/layouts, media paths and CMS collection paths. Chromium browser testing uses a static approximation of the Jekyll rendering and verifies the interactive controls and desktop/tablet/mobile layouts. **The complete Jekyll build has not been run** in this environment because the Jekyll gem is not installed. Always verify GitHub Pages' Actions/Pages build status after deployment.

Browsers must permit JavaScript for the Design Studio. External Google Fonts are optional, with local fallbacks. Configurations may also be exported as JSON. This test version deliberately contains `noindex`.
