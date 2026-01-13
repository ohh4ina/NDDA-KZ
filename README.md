Project Overview
This project presents a comprehensive Quality Assurance audit of ndda.kz, the official web resource of the National Center for Expertise of Medicines and Medical Devices in Kazakhstan. The portal serves as a critical gateway for healthcare professionals and the public to access medicine registries and online services.




The primary goal was to ensure the website operates reliably, safely, and provides uninterrupted access to pharmaceutical data.

🛠 Tech Stack & Tools

Browsers: Google Chrome, Yandex Browser.


OS: Windows 11, Android 11.

Testing Tools:


Chrome DevTools: For UI inspection and network request monitoring.




Fake Filler: Automated form validation testing.


EqualWeb: Accessibility (WCAG/ADA) compliance auditing.


Dead Link Checker: Identification of broken links and 404 errors.


PageSpeed Insights: Core Web Vitals and performance analysis.


🔍 Testing Scope
The audit covered both functional and non-functional aspects:


Functional Testing: End-to-end user flows, search filters, and medicine registration forms.


UI/UX Testing: Visual consistency, responsive behavior on mobile/desktop, and navigation logic.


Localization: Verification of Kazakh and Russian language versions.


Performance: Measuring LCP and page loading times.


🚩 Key Findings
During the audit, 23 test cases were executed, revealing significant defects:



Critical Logic Flaws: Found a CDbException (SQL error) when interacting with breadcrumbs, indicating server-side issues.


Data Integrity Issues: The system fails to "trim" spaces in search queries, leading to "No results found" for valid medicines.


State Management: Changing the language during registration resets the form, causing users to lose all entered data.


Broken Navigation: The "Back" button on certain pages redirects users to the news archive instead of the previous logical screen.


Technical Debt: Identified 120 dead links and the presence of "Lorem Ipsum" / test content on the production site.


💡 Recommendations

High Priority: Fix SQL exceptions and restore predictable navigation (Back button/breadcrumbs).


UX Improvement: Implement input trimming and fix age-restriction validation during registration.


Performance: Optimize Core Web Vitals (specifically LCP) to improve user retention and SEO.


Accessibility: Address contrast and navigation issues identified by the EqualWeb audit (current score: 0/100).

📂 Project Structure

Test_Cases/ - Detailed steps and expected vs actual results.


Bug_Reports/ - Documented defects with reproduction steps and severity levels.


Screenshots/ - Visual evidence of UI overlaps and system errors.

Contact: Shyngys Lesbaev – LinkedIn: ohh4ina – lesbaevsh05@gmail.com
