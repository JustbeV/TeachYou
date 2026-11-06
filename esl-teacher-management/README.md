# TeachMate V2 — ESL Teacher Workspace

A free, local-first browser application for an ESL teacher handling 21–50 students, children and adults, one-on-one classes, and changing group rosters. Built with HTML, CSS, JavaScript, and IndexedDB. There is no paid database, backend, or cloud account.

## Included in V2

- Dashboard with student, class, workload, and task summaries
- Student directory with child/adult age groups, guardian details, English level, goals, and notes
- One-on-one and group class sessions
- **Changing group rosters:** choose the students separately for every group session; no permanent group membership is required
- Session roster history and individual attendance records
- Online and face-to-face session details
- Schedule overlap detection
- Reusable lesson library
- Attendance per student, including within group sessions
- Individual progress evaluations across speaking, listening, reading, writing, grammar, vocabulary, pronunciation, and overall skills
- Tasks and reminders
- Teaching activity reports and CSV export
- JSON backup and restore
- Responsive desktop, tablet, and mobile layout
- Basic PWA/offline app-shell support
- Upgrade path from the previous TeachMate v1 IndexedDB database

## Run locally

A local web server is recommended for IndexedDB and service-worker/PWA support.

### Option A — VS Code + Live Server
1. Extract the ZIP.
2. Open the `esl-teacher-management` folder in VS Code.
3. Install the **Live Server** extension if needed.
4. Right-click `index.html` and choose **Open with Live Server**.

### Option B — Python
1. Open a terminal in this folder.
2. Run `python -m http.server 8000`.
3. Visit `http://localhost:8000`.

## Existing v1 data

TeachMate V2 keeps the existing database name (`teachmate-esl`) and upgrades its IndexedDB schema from version 1 to version 2. Existing student, lesson, and session records are retained. Old one-student sessions are converted into one-on-one sessions with a one-student roster. **Before upgrading an existing installation, export a JSON backup from v1.**

## Important privacy and storage notes

All records are stored in the current browser profile on the current device. They do not automatically synchronize between a laptop and phone. Clearing browser data, using private browsing, or losing the device can make records unavailable. Export backups regularly and keep them somewhere safe.

This version assumes student billing is managed by the company, so student invoicing and payment collection are not part of the active workflow. Legacy finance records from v1 are preserved in the database but are not shown in the V2 navigation.

This is a prototype, not a hardened production system. It has no cloud login, server-side access control, encryption, or multi-device sync. Anyone with access to the same browser profile may be able to access the records. Follow the employer's student-data policies and avoid entering highly sensitive information without approval.

## Suggested next improvements

- Student profile detail pages with full lesson and progress timelines
- Calendar month/week/day views and recurring-session tools
- Homework assignment and completion workflow
- Printable student progress reports
- Optional encrypted backups and company-approved report templates
- Optional company-specific billing or payroll exports, if required
