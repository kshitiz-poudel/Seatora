# Seatora — Exam Seat Allocation Portal

A responsive browser-based portal prototype based on the entities, sample data, and allocation rules in the supplied Seatora Java project.

## Run it
1. Extract the ZIP file.
2. Open `index.html` in Chrome, Safari, Firefox, or Edge. No build tools or server are required.
3. The portal starts with the supplied student and room sample data and four sample exams. Use **Reset demo** to restore the original demo data.

## Included features
- Student seat lookup by roll number.
- Student management (add, delete, search, and CSV import).
- Exam creation with date/session and branch/semester enrolment matching.
- Room management with capacity computed as rows × seats per row.
- Automatic seat allocation for a date/session, with room-capacity validation and attempts to separate same-course neighbours.
- Seating plan table, session filter, search, and CSV export.
- Dashboard summaries and browser-local persistence via `localStorage`.
- Responsive layout and Seatora branding/logo.

## Important limitations
This is a **front-end demo**, not a production multi-user deployment. Data is stored in the current browser only; administrators and students do not share a live database, and there is no login/authentication or server-side access control. To deploy for real students, connect the UI to a backend/API and shared database, add authenticated student/admin roles, validate allocations on the server, and publish it using HTTPS. The browser demo's allocator is a practical approximation of the Java service, not a direct execution of the Java code.

## CSV formats
Student import accepts headers `roll_no,name,branch,semester` (also accepts `roll` instead of `roll_no`). Exported seating plan columns: `Date,Session,Course,Student name,Roll number,Room,Row,Seat`.
