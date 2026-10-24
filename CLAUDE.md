# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Personal web page for Ravi Rangachari (SAP Functional Consultant and South Indian Astrologer). Ravi is new to coding and this is Ravi's first project, so it doubles as a learning exercise.

## Structure

A plain static site with no build step, dependencies or tests:
- `index.html`: all page content (initials avatar, name, tagline, "About me", "What I care about")
- `style.css`: all styling, linked from `index.html`

## Running it

Open `index.html` in a browser. To check a change visually in a cloud session, take a screenshot with the pre-installed Playwright:

```bash
node -e "const {chromium}=require('playwright');(async()=>{const b=await chromium.launch();const p=await b.newPage({viewport:{width:800,height:950}});await p.goto('file://'+process.cwd()+'/index.html');await p.screenshot({path:'preview.png'});await b.close();})()"
```

## Conventions

- Keep it beginner-friendly: plain HTML and CSS only, no frameworks, JavaScript or build tools unless Ravi asks for them.
- Both files are full of plain-English comments explaining each part. Keep that style in anything you add, and explain changes in simple terms.
- Color scheme is green: background gradient `#a8e6a1` → `#d4f5c9`, accent `#2e8b57`.
- Don't load images or assets from other websites (an external avatar failed to load before). Keep assets in this folder.
- Never write `-->` inside an HTML comment: it ends the comment early and the rest of the text shows up on the page.
