# OTC Clean Up

Browser tool for the Soldiers' Angels **One Time Care Packages Available** Salesforce export.

Drop the export in and it flags:

- **Over 45 days**: any record whose `Program Engagement: Created Date` is more than 45 days before the "As of" date (both adjustable on the page).
- **Duplicates**: the same client (First + Last Name, case and punctuation ignored) or the same Program Engagement ID appearing more than once. Each pair is grouped (Dup 1, Dup 2...) and the newest record is marked (Created Date, then Start Date, then Last Modified).

Download gives an Excel file with four tabs: All Rows Flagged, Over 45 Days, Duplicates, Clean. Flagged rows are color coded.

Everything runs in the browser. The file is never uploaded anywhere.

## Deploy

Static site on Render. No build command, publish directory `.`
