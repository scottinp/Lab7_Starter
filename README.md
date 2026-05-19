# Lab 7 - Browser Testing

## 1) **Within a GitHub action that runs whenever code is pushed.**

Running automated tests in a GitHub Action on every push is the best fit because it catches errors the moment they're introduced. It won't let  broken code spread further into the project or get merged into the main branch. 

The tests runs in a clean environment so results aren't affected by whatever happens to be installed on a particular developer's machine. Tests are also automatic so developers won't forget to run them.


## 2) Would you use an end to end test to check if a function is returning the correct output?

No. End-to-end tests are slow and test the full user flow through the UI. A unit test better tool for checking a function's return value because it's faster and isolates the function, and tells you exactly the error is. End-to-end tests should be used for testing user-facing behavior.

## 3) What is the difference between navigation and snapshot mode?

Navigation mode audits a full page load from start to finish. It reloads the page and measures load-time performance metrics.

Snapshot mode analyzes the page in its current state without reloading. It does not include load-time performance metrics like Navigation mode. I's' useful for auditing a specific UI state or page.

## 4) Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.

1. Reduce Total Blocking Time (my Lighthouse reported 660 ms). Break up long JavaScript tasks, remove unimportant scripts, and use code splitting to keep the main thread free during load.

2. Improve Speed Index (my Lighthouse reported 9.8 s). Optimize images, lazy-load offscreen content, and reduce render-blocking resources so the visible page renders sooner.

3. Raise the Accessibility score (my Lighthouse reported 90). Add alt text to all images and add ARIA label so screen readers can describe the page.