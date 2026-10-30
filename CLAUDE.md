# Context

Read this first in every new chat or Claude Code session.

## What we're building
A website for Plant Parenthood, a plant-sitting service in Berlin (fictional): we take care of people's houseplants while they're away.

- **Services:** plant daycare, holiday care and emergency plant rescue.
- **Who it's for:** plant lovers living in Berlin apartments, especially busy professionals, frequent travellers, and people going on holiday with no one to look after their plants. Individual households across Berlin, not businesses for now.
- **What makes us different:** a boutique hotel for houseplants. Every plant gets personalised care based on its species and needs, with photo updates so its humans can enjoy their holiday without worrying. Emergency plant rescue for dramatic situations: yellow leaves, mysterious spots, or a plant that looks like it's given up on life.
- **Personality:** playful, warm and a little cheeky. We take plant care seriously, but not ourselves.

(The pages still carry the kit's sample content for Linden & Hart. Replace it page by page with Plant Parenthood content as each page goes through the loop.)

## Our Git
- Design system: github.com/cRistringss/cris-design-system
  Tokens (`assets/tokens.css`), components (`assets/components.css`), the storybook (`storybook.html`), the design skill (`SKILL.md`), and page designs in `prototypes/`.
- Website: github.com/cRistringss/cris-website
  The pages Claude Code builds. `main` is the live site, `staging` is the rehearsal, every change goes through a pull request.
- The design system repository is the source of truth. The website only uses what is in it.

## Stack
Plain HTML, CSS and a little JavaScript. No build step. Hosted on Netlify, connected to the website repository. The contact form uses Netlify Forms.

## Pages
`index.html` (home) · `pricing.html` · `about.html` · `contact.html` · `thanks.html` (after the form)

## How we work: the loop
1. Design in Claude chat: prototype the page, try versions, check phone and desktop.
2. Update the design system: anything reused or a rule goes into tokens, components, storybook and SKILL.md. The page goes into `prototypes/`.
3. Push the design system repository to GitHub.
4. Claude Code, in the website repository: get the latest design system, update tokens and components to match, build the page from its prototype, on a new branch.
5. Test on localhost: phone and desktop, every link, Lighthouse. Not OK? The report goes back to Claude chat.
6. Pull request, check the Netlify preview link, merge. The site goes live.

## Rules for Claude Code
- Never make a design decision. Colours, fonts, spacing, layout, copy, motion and imagery are decided in Claude chat and live in the design system or the prototype.
- If something isn't defined there, stop and ask. Offer two or three options with a short reason for each. Don't pick one yourself.
- Use only tokens from `assets/tokens.css` and components from `assets/components.css`. Never hard-code a value.
- Work on a branch, never directly on `main`.
- After building, run the site locally, test phone and desktop, and report what you built, what you tested and every open question, before opening a pull request.

## Current state
Business context defined (Plant Parenthood). Design system: based on starter-paper, still named "Paper". Kept the burnt orange accent and Fraunces + Inter. Corners changed from square to slightly rounded (6px buttons, inputs and small elements; 8px cards), no shadows. Tokens synced to cris-website.
Next: define the brand (name of the design system, whether the look still fits Plant Parenthood, favicon), then design the home page in Claude chat and save it as `prototypes/home.html`.
