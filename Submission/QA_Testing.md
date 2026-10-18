# Path of Ascension — QA Testing Report

**Course:** CSC 4370 — Web Programming  
**Project:** Path of Ascension (Quest Explorer + Adventure Pack)  
**Team members:** Trajuan Smith and Hien Dao  
**Testing date:** October 18, 2026

## 1. Testing approach

The website was manually tested in Chrome and with Chrome DevTools at desktop, tablet, and mobile viewport sizes. Navigation, mission interactions, and keyboard access were checked manually. HTML files were checked with the W3C HTML Validator, and CSS stylesheets were checked with the W3C CSS Validator.

## 2. Responsive design testing

| Viewport | Observed result | Status |
| --- | --- | --- |
| Desktop | Content displayed correctly, without overlapping elements or unwanted horizontal scrolling. | Pass |
| Tablet | Responsive layouts adapted without overlapping elements or unwanted horizontal scrolling. | Pass |
| Mobile | Content remained readable; region cards adapted to the narrow layout, without overlapping elements or unwanted horizontal scrolling. | Pass |

The World page uses a two-column CSS Grid layout on larger screens and switches to one column at viewport widths of 768px or less.

## 3. Navigation and functionality testing

| Test case | Observed result | Status |
| --- | --- | --- |
| Main navigation | Links correctly connected Home, World, Mission, and Team pages. | Pass |
| View Mission links | Selecting an available region opened its corresponding mission. | Pass |
| Mission selection | Visitors could switch between available missions. | Pass |
| Mission progression | **Take Mission** changed the status to **Ongoing**; **Complete Mission** changed it to **Completed**. | Pass |
| Locked content | Locked regions and missions could not be selected. | Pass |
| Home Journey Tracker | Selecting different regions updated the tracker. | Pass |

**Result:** All six manually checked functionality tests passed.

## 4. Keyboard accessibility testing

| Test case | Observed result | Status |
| --- | --- | --- |
| Forward keyboard navigation | Tab navigation worked across interactive elements. | Pass |
| Reverse keyboard navigation | Shift+Tab navigation worked. | Pass |
| Keyboard activation | Available links and controls responded to Enter. | Pass |
| Locked regions | Locked items were not selectable via keyboard; non-interactive `<span>` elements were used instead of unavailable links. | Pass |

Additional accessibility-related implementation includes semantic HTML landmarks and a `prefers-reduced-motion` media query. These implementation details are not substitutes for a comprehensive automated accessibility audit.

## 5. HTML and CSS validation

| Validation | Method | Result | Status |
| --- | --- | --- | --- |
| HTML files | W3C HTML Validator | All HTML files checked with no remaining errors. | Pass |
| CSS stylesheets | W3C CSS Validator | All CSS files checked successfully. | Pass |

### Defect identified and corrected

During HTML validation of `index.html`, the validator flagged four instances of `<p>` elements nested inside Journey Tracker `<label>` elements. These were replaced with `<span>` elements, preserving the label associations while making the markup valid. The HTML was validated again, and no errors remained.

## 6. Testing scope and follow-up

The confirmed results above reflect the tests performed and reported by the team. Separate Firefox/Safari cross-browser results, automated contrast measurements, and peer usability feedback are **not documented here** because results have not been confirmed for this report. These can be added if completed.

## 7. Overall result

Responsive behavior, core navigation and mission interactions, keyboard navigation, and W3C HTML/CSS validation passed the documented checks. The HTML validation defect was corrected and rechecked successfully.
