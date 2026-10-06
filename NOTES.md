\# Notes and Assumptions



\## Setup

\- Ran the app on Java 26 and Node 24. Both worked without any changes.

\- Backend needs a restart after Java changes. Frontend reloads automatically.



\## Assumptions

\- Search is a substring match on title and description (not whole-word), so "rate" also matches "Migrate". I treated this as expected behaviour.

\- The tasks shown in the list (e.g. "Add input validation", "Improve table sorting UX") are sample data, so I only fixed bugs I could reproduce myself.

\- Page reset on search/filter change was verified by reading the code only, not tested manually on page 3.



\## Scope

\- I fixed four issues: status filter (SQL AND/OR precedence), page reset, stale API responses, and controller validation (400 instead of 500).

\- Other possible improvements (sorting UX, input validation on task creation) were not done because of the timebox.

