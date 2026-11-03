LearnSkillX - Updated Project

RUN:
1. Extract the folder.
2. Open learnskilllx/login.html in a browser, OR serve the folder with a local web server.
3. The exact official logo supplied by the project owner is in assets/learnskillx-official-logo.jpg.

TEST FLOW:
Each of the 10 subjects has Easy, Medium, and Hard tests. Every level has 10 questions. A student must score 60% or more on Easy to unlock Medium, and 60% or more on Medium to unlock Hard.

CERTIFICATES:
80%+ Gold, 70-79% Silver, 60-69% Bronze, below 60% no certificate.

REGISTRATION:
Student registrations are pending until an Admin or Super Admin accepts them. Admin navigation includes Registration Requests with a live pending badge. Accept/Reject is available.

MANAGE ADMINS:
Add Member includes an assigned password field. New members are stored as approved accounts and can log in with the assigned credentials.

NOTE:
This version is a browser/localStorage demo. For multi-device production use, replace localStorage authentication with a real backend/database and hashed passwords.

NEW UPDATE — MEDALS, SUBJECT LOGOS & TEST GENERATOR
===================================================
- Certificates now show the official LearnSkill X logo plus a medal:
  Gold Medal = 80%+
  Silver Medal = 70–79%
  Bronze Medal = 60–69%
- Standard coding assessment contains 10 subjects × 3 levels × 10 questions = 30 tests / 300 questions.
- Student progression is Easy → Medium → Hard; 60%+ is required to unlock the next level.
- Admin > Generate Test includes 10 questions as the recommended/default option, plus 5/15/20.
- Generate Test shows the selected subject's logo and generated-test rows show subject logos.
- Subject logos are also shown on subject cards, certificates/results, and the test runner.
- The uploaded LearnSkill X official logo is stored at assets/learnskillx-official-logo.jpg.

DEFAULT ADMIN LOGIN
===================
Email: rohan@learnskillx.com
Password: 123456
The Super Admin login remains:
Username: s.admin@1
Password: 123456

PROFESSIONAL CERTIFICATE UPDATE
===============================
- Certificates now use an official print-ready certificate layout.
- Gold, Silver and Bronze certificates have matching professional medal treatments.
- Certificate includes LearnSkillX branding, official logo, score, certificate ID, issue date, verification seal and signature areas.
- Print / Save as PDF uses an A4 landscape certificate layout.
- Registration Requests now uses a clean white bell SVG icon matching the sidebar.

PROJECT STRUCTURE (SPLIT INTO SEPARATE FILES)
=============================================
The original app.js and style.css were cut into separate files by feature, with no code changed.
Scripts are plain (non-module) scripts loaded in the same order as before, so everything works exactly as it did.
Open login.html to start (same as before).

learnskilllx/
  login.html                      Login / register page
  index.html                      Main app shell (loads all css/ and js/ files below, in order)
  assets/                         Put learnskillx-official-logo.jpg here (see assets/README.txt)
  css/
    base.css                      Colours, fonts, reset, hexagon mark
    layout.css                    Sidebar, top bar, page shell
    components.css                Cards, buttons, tables, badges, subject cards
    modal.css                     Modal dialogs and form fields
    test-runner.css               Test taking screen
    result-certificate.css        Result hero, basic certificate, print base
    tiers-notifications.css       Registration badge, Gold/Silver/Bronze tiers
    logos.css                     LearnSkillX and official logo styles
    medals.css                    Medal discs and ribbons
    subject-logos.css             Subject logos and generate-test preview
    professional-certificate.css  Print-ready professional certificate
    icons-print.css               White bell icon, A4 print rules, mobile rules
    login.css                     Login page styles
  js/
    core/                         ui-helpers, storage, sync-and-seed, session, helpers
    data/database.js              Subjects, 300 questions and default data
    ui/shell.js                   Root render, navigation, sidebar and top bar
    views/superadmin/             overview, registration-requests, manage-admins, reports, backup, settings
    views/admin/                  overview-subjects, question-bank, generate-test, learners
    views/learner/                overview, levels, take-test, results-certificates
    views/shared/                 results-table
    test/test-runner.js           Start, answer, step and submit a test
    certificate/certificate.js    Professional certificate rendering
    modals/                       modals, question-generator, export-question-bank, question-and-user-forms
    actions/data-actions.js       Delete / toggle / generate-test actions
    init.js                       Starts the app
    login/                        login-storage, login-render, login-auth
