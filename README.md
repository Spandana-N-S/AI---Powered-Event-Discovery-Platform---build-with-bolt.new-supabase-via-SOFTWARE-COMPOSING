# AI---Powered-Event-Discovery-Platform---build-with-bolt.new-supabase-via-SOFTWARE-COMPOSING
A full-stack web app for music lovers to browse, create, manage, and RSVP to events (concerts, festivals). Users get personalized profiles showing created/attending events. ## How I Built It (Prompts, Iterations, Debugging) Everything via natural language in Bolt.new—no manual code.

# Event Discovery Platform – AI-Built Music Events App

**Live Demo:** https://youtu.be/SeybVD0NMQI?si=iUqY07FEa5BzQ-ME
**Built with:** Bolt.new (AI prompt-to-app builder), Supabase (backend/database/auth), Netlify (deployment)  
**Role:** Solo "software composer" – no traditional coding; directed AI via natural language prompts  
**Time to MVP:** ~Hours (vs. months manually)  
**Tech Stack Summary:** React-style frontend (AI-generated), Supabase (PostgreSQL + RLS), email/password auth, real-time updates

## Project Overview
A full-stack web app for music lovers to browse, create, manage, and RSVP to events (concerts, festivals). Users get personalized profiles showing created/attending events.

**Core Features:**
- Browse/search events with cards, filters, hero section
- Create/edit/delete your own events (title, date, location, image upload, description)
- "Attend/Leave" button → adds to personal attending list (many-to-many via junction table)
- Secure user profiles: tabs for "Created Events" + "Attending Events"
- Responsive UI (mobile-first), modals for details/edit
- Real-time persistence & updates

## Why "Software Composing" Instead of Scratch Coding?
Coding from scratch is slow, error-prone, and expensive—especially for prototypes/MVPs. AI tools like Bolt.new + Supabase let non-coders (or fast prototypers) ship 10–100x faster:
- Focus on vision/logic → AI handles boilerplate, structure, refactoring
- 98% fewer errors via auto-testing/iteration (Bolt.new claim)
- Instant full-stack (frontend + backend + DB) without setup
- Affordable/accessible → perfect for indie hackers, agencies, small biz solutions
In 2026, speed + iteration wins over handwriting everything.

## Tools Used in Software Composing Process

This project was built using a modern AI-first workflow—no manual coding from scratch. Here's the key stack:

- **Bolt.new** (primary builder)  
  Browser-based AI app builder that turns natural language prompts into full-stack apps (frontend + backend + integrations). Generated the entire Event Discovery Platform: UI, logic, Supabase connection, auth, and features. Ideal for rapid prototyping and beginners—chat to build, iterate, debug, and deploy.

- **Supabase** (backend/database)  
  Modern BaaS (Backend-as-a-Service) for PostgreSQL database, authentication (email/password), row-level security (RLS), and storage (e.g., event images). Bolt.new integrates seamlessly—handles persistent data, user accounts, and secure access without manual server setup.

- **Netlify** (deployment)  
  One-click hosting platform integrated with Bolt.new. Publishes the app live instantly with global CDN, auto-builds on changes, previews, and free tier—zero DevOps needed for production-ready URLs.

- **Figma** (UI/UX planning)  
  Used for initial wireframing and visual breakdown of screens (hero, event cards, modals, profiles). Provided a clear design reference to make prompts more precise and effective.

- **Relevance UI Designer Tool** (AI-assisted design planning)  
  Custom AI tool to refine UI/UX ideas: describe the app → it asks guiding questions → outputs detailed design specs. Translated high-level vision into actionable prompts for Bolt.new.

- **ChatGPT / Claude** (supplemental LLM)  
  General-purpose AI for brainstorming, clarifying web concepts (front-end/back-end/databases/APIs/auth), refining prompts, or debugging ideas outside Bolt.new.

- **Cursor / Windsurf / Replit Agent** (advanced/optional)  
  Mentioned for future scaling: AI code editors or agents for devs wanting more control over generated code, debugging existing repos, or incremental enhancements.

This workflow emphasizes **prompt engineering + iteration** over traditional dev—focusing on vision, clear descriptions, testing small changes, and using AI chat/console for fixes. Result: functional app shipped in hours.

## How I Built It (Prompts, Iterations, Debugging)
Everything via natural language in Bolt.new—no manual code.

**Prompts** (granular & iterative):
- Started broad: "Build a live music event discovery app with modern UI, event cards, search, and user auth"
- Got specific: "In the event details modal, bottom left: add Edit & Delete buttons only for the creator"
- Added logic: "When user clicks Attend, add them to event_attendees table and refresh profile tab"

**Iterations** ("incremental is best"):
- Built/tested one feature at a time (e.g., auth first → events CRUD → attending)
- Used "discuss mode" for back-and-forth: explain issue → AI suggests plan → "attempt fix"
- Reverted to prior version on "error loops" → rephrased prompt fresh

**Debugging** (combo of tools):
- **AI Chat/Discuss Mode:** "Not seeing sign-in modal on navbar click" → AI diagnoses, proposes fix, applies
- **Browser Console:** Opened dev tools → cleared logs → recreated bug → read errors (e.g., "event ID undefined on delete") → fed details back to AI ("Add console.log(eventId) here")
- **Supabase Dashboard:** Verified DB rows (e.g., delete didn't persist? Checked table directly)
This loop taught real debugging: observe → reproduce → diagnose → prompt fix

## Web Fundamentals (Why They Matter for AI Directing)
Understanding these gave me precise "vocabulary" to prompt AI effectively.

- **Front End** — The "dining room": UI/UX users see/interact with (event cards, modals, responsive layout, buttons, forms). Captures clicks → displays data.
- **Back End** — The "kitchen": Hidden logic/server (processes requests, auth checks, business rules like "only creator edits").
- **Databases** — Software's "memory/filing cabinet": Tables (events, users, event_attendees) store persistent data. Supabase = modern BaaS with row-level security (RLS) → users only access own rows.
- **APIs** — "Waiters/messengers": Front ↔ back communication (GET events, POST new event). Also external (e.g., future Google Maps/Stripe).
- **Authentication & Authorization** — Auth: "Prove who you are" (email/password login). Authz: "What you're allowed" (RLS ensures edit/delete only for creator; profiles private).

## Deployment with Netlify
Bolt.new → one-click publish to Netlify:
- Instant live URL, auto-builds on changes
- Free tier + custom domains, analytics, previews
- Advantages: Zero server config, global CDN (fast everywhere), easy rollbacks, scales automatically
From idea → live in minutes—no DevOps hassle.

## Why This Project Matters (Career Angle)
- Shows AI fluency: prompt engineering, rapid iteration, debugging without deep code
- Proves speed: Hours to functional SaaS vs. months
- Monetization path: Land $5k–$15k client projects (custom tools for small biz) or start AI agency
- Community boost: Share on X/LinkedIn/Reddit → feedback, collabs, visibility → accelerates career in AI era
- Crucial skill: In 2026, the person with ideas + AI-directing ability builds the future fastest.

Built as part of Liam Ottley's "Software Composing" guide.  
Questions? Reach out—happy to demo or discuss prompts/debug flow!
