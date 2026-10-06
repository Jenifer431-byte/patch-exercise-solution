\# Notes



\## Summary of changes

\- Status filter: SQL AND/OR precedence bug in TaskRepository.java. Added brackets so the status condition applies to all results.

\- Page reset: App.jsx now resets to page 1 when search or status changes.

\- Stale responses: added a cancelled flag in useTasks.js so old API responses do not overwrite newer ones.

\- Controller: invalid status now returns 400 instead of 500. Removed Thread.sleep and replaced System.out with a logger.



\## What I chose not to change

\- Sorting UX and input validation on task creation. I only fixed bugs I could reproduce in the time available.



\## Assumptions

\- Search is a substring match on title and description, so "rate" also matches "Migrate". I treated this as expected.

\- Page reset was verified by reading the code, not tested manually on page 3.

\- Ran on Java 26 and Node 24 without any changes.



\## Biggest remaining risk

\- Task creation accepts blank titles and negative priority values, and there are no automated tests, so regressions are hard to catch.



\## Tools/AI used

\- I used Claude to help find the bugs and draft the fixes. I tested the status filter and the invalid status case in the browser, and wrote the handwritten explanations myself.

