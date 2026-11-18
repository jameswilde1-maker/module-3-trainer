MODULE 03 — ELECTRICAL FUNDAMENTALS OFFLINE TRAINER
Prototype v0.1 · 13 November 2026

WHAT THIS VERSION INCLUDES
- Apple-inspired responsive dashboard, suitable for iPad Mini portrait/landscape, iPhone and desktop.
- Demonstration exam with 12 questions (NOT a full mock, NOT a validated full bank).
- Study mode, calculation practice, immediate feedback, score review and topic reports.
- Short offline formula sheet, topic overview and day-of-exam checklist (drafts only).
- Dark mode, browser-local saved history, export and restore backups.
- JSON question-pack import with structural checks.
- PWA manifest and service worker for installation when hosted via HTTPS.

WINDOWS, WITHOUT INTERNET
Double-click index.html. A browser opens the app locally without any network connection. The PWA install button may not appear when opened from the file system.

IPAD MINI / IPHONE INSTALLATION
Publish the contents of this folder (not the ZIP alone) to an HTTPS web host, e.g. GitHub Pages. While online, open its index.html in Safari, Share > Add to Home Screen, launch it and allow it to load. Then test it in aeroplane mode. The service worker caches the app shell. Downloading just the ZIP onto iPad does not automatically provide a reliable installable PWA.

QUESTION PACK FORMAT
A JSON document containing title, kind ('full-mock' or 'practice'), qaApproved (true only after external source, calculation, knowledge-level, layout and duplicate review), and questions.
Each question must include: id, topic (e.g. '3.6'), objective, level (1 or 2), type ('definition','technical','scenario','calculation'), source, page, q, options (exactly 3), answer (0,1,2), explanation. Calculations also require working.

QA LIMITATIONS
The app checks structure, exact duplicate stems and IDs, but DOES NOT validate technical facts, option correctness, exam topic weighting or semantic paraphrases. No imported exam should be called QA-approved without completing the standards checklist and checking the external master question register. Do not reuse questions across newly published full mocks.

SOURCE MATERIAL
The 105 MB Resource Group PDF is not bundled. Demonstration questions and early guide facts cite selected pages in the uploaded notes. This starter build does not yet achieve full syllabus coverage.

DATA
Saved in the specific browser/device (localStorage). Regularly export a backup via Settings. Avoid clearing site data. Updating a hosted version requires care to preserve the same origin for user data.

VERSION 0.2 — SIDEBAR ICON UPDATE
The navigation now uses locally embedded, recognisable line icons for Home (house), Mock Exams (clipboard), Calculations (calculator), Study (open book), Progress (bar chart), Guides (document) and Settings (gear). The home dashboard and mobile navigation have matching icons. No external icon library or Wi-Fi required.

GITHUB PAGES UPDATE
Replace index.html and sw.js in the repository root with the files from this folder. Do not replace your manifest or icons. After commit and successful Pages deployment, open the site online and refresh or relaunch once to activate the updated offline cache. Offline data should remain in local storage; export a backup before updating as a precaution.

VERSION 0.3 - SAFE MOCK IMPORT
Export a backup before updating. Replace index.html and sw.js at the SAME existing HTTPS origin/path. Do not clear Safari data or delete the Home Screen app. Open online, refresh/relaunch, then test offline. Existing history, bookmarks and topic packs are retained. Approved full mocks may reuse topic-pack IDs while maintaining their own question order and answer positions. Draft full mocks are blocked; question repeats across full mocks are blocked. Full mocks require exact blueprint counts and knowledge levels. Full mock timer: 65 minutes, auto-submit at expiry while running, pass mark 39/52. Topic practice remains untimed. Timer is not persisted if you close/leave a session.
