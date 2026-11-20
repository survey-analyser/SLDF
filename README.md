# SLDF complete browser demonstration

Open `index.html` in a proper browser or host the folder on a static host (GitHub Pages, Netlify, etc.). The certificate artwork is included as `certificate-reference.png`. The app generates personalised, printable landscape certificates as scalable SVG that match the reference artwork (banner, laurels, seal, QR, certificate ID). The QR code is generated from the verification address in Admin > Settings and needs internet access to load its library (cdnjs). Signature images are optional uploads in Settings. Print / Save as PDF works from the certificate page.

## Demo login
Create an account with `nithish2577@gmail.com` to access the local admin preview. This is **not secure**: any person can claim that email and data are kept in browser localStorage. Do not use a real password, real personal information or public competitions.

## Features
- Admin create/edit/unpublish competitions, select eligibility, judging criteria, quiz duration/start, essay submission email, plagiarism limit
- Manual quiz question authoring and PDF question import (text-based PDF with one line per question: `Question | A | B | C | D | 1`, where final digit is correct answer position 1–4). PDF import loads pdf.js from a CDN and needs an internet connection.
- Participant registration, timed multiple-choice quizzes, auto score, immediate participation certificates
- Admin participant score table, first-place tie random draw among highest scorers, local draw log, manual positions, result publishing
- Essay plagiarism review and admin-approved certificates, certificate registry/revocation, certificate verification
- Landscape printable certificate and reference artwork, policy pages

## Important limitations before going live
This is a **single-browser demo**, not a production service. Authentication is insecure (demo passwords are stored locally), quiz answer keys are exposed to the browser, timing can be manipulated, scores/results are not shared across devices, certificate IDs are not centrally verifiable, and random draws are not server-audited. Payment processing, real email sending, file uploads, automatic similarity checking, secure administrator roles, privacy compliance and a server/database are not implemented. Paid competition publishing is disabled. Build a server-backed version with proper security and audit logging before accepting real participants.

The certificate reference image contains fictional sample details, signatures and QR code and is not an actual certificate or a working verification code. The generated certificate omits those fabricated details and uses the actual locally recorded certificate ID. The text policies are draft summaries, not a substitute for a legal review.
