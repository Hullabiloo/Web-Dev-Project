# SDG 12 Requirements Study Guide

This guide is ordered to match your rubric list and points to exactly where each feature lives.

## 1. Professional single-page interactive UI
- What to study:
  - Main single-page layout, controls, forms, cards/table, and modals.
- Where:
  - `WEBDEVPROJECT/html/index.html:17` (`<main class="main-content">`)
  - `WEBDEVPROJECT/html/index.html:47` (`<section class="controls">`)
  - `WEBDEVPROJECT/html/index.html:100` (`#addSection`)
  - `WEBDEVPROJECT/html/index.html:191` (`#editSection`)

## 2. Use `fetch()` to read JSON and display data in table
- What to study:
  - Fetch from JSON file, parse data, then render.
- Where:
  - `WEBDEVPROJECT/html/index.html:488` (`loadData`)
  - `WEBDEVPROJECT/html/index.html:491` (`fetch(JSON_PATH)`)
  - `WEBDEVPROJECT/html/index.html:804` (`renderTable`)

## 3. Add random `favorite` yes/no when data is fetched
- What to study:
  - Random favorite helper and assignment in load.
- Where:
  - `WEBDEVPROJECT/html/index.html:401` (`getDefaultFavorite`)
  - `WEBDEVPROJECT/html/index.html:505` (`favorite: getDefaultFavorite()`)

## 4. Add random `rating` 0-5 when data is fetched
- What to study:
  - Random rating helper and assignment in load.
- Where:
  - `WEBDEVPROJECT/html/index.html:406` (`getDefaultRating`)
  - `WEBDEVPROJECT/html/index.html:506` (`rating: getDefaultRating()`)

## 5. Responsive behavior for phone/tablet/computer
- What to study:
  - Breakpoint behavior and view switching logic.
- Where:
  - `WEBDEVPROJECT/static/css/stylesheet.css` (media queries)
  - `WEBDEVPROJECT/html/index.html:724` (`checkIsDesktop`)
  - `WEBDEVPROJECT/html/index.html:1519` (resize listener)

## 6. Hamburger menu on mobile, horizontal filter on larger screens
- Current status:
  - You changed this to always use a hamburger menu (as requested), so it no longer switches to horizontal on larger screens.
- Where:
  - `WEBDEVPROJECT/html/index.html:14` (`#hamburgerMenu`)
  - `WEBDEVPROJECT/html/index.html:30` (`#targetSidebar`)
  - `WEBDEVPROJECT/html/index.html:1472` and `WEBDEVPROJECT/html/index.html:1476` (open/close sidebar listeners)

## 7. Cards on phone/tablet and table on computer
- What to study:
  - `updateDisplay()` decides card vs table.
- Where:
  - `WEBDEVPROJECT/html/index.html:714` (`updateDisplay`)
  - `WEBDEVPROJECT/html/index.html:735` (`renderCards`)
  - `WEBDEVPROJECT/html/index.html:804` (`renderTable`)

## 8. Table row click opens row details modal
- What to study:
  - Row click binding and details modal rendering.
- Where:
  - `WEBDEVPROJECT/html/index.html:829` (row click listener)
  - `WEBDEVPROJECT/html/index.html:847` (`renderDetailsModal`)
  - `WEBDEVPROJECT/html/index.html:873` (`openDetailsModal`)
  - `WEBDEVPROJECT/html/index.html:274` (`#detailsModal` markup)

## 9. Sort against columns ascending/descending
- What to study:
  - Sort options and sort logic switch.
- Where:
  - `WEBDEVPROJECT/html/index.html:74` (`#sortBy` dropdown options)
  - `WEBDEVPROJECT/html/index.html:623` (`getFilteredAndSorted`)
  - `WEBDEVPROJECT/html/index.html:1467` (sort change listener)

## 10. Add data: only show add form (hide table/other details)
- What to study:
  - Add form toggle and submit behavior.
- Where:
  - `WEBDEVPROJECT/html/index.html:1044` (`addExample`)
  - `WEBDEVPROJECT/html/index.html:1386` (`toggleAddBtn` logic)
  - `WEBDEVPROJECT/html/index.html:1416` (`cancelAddBtn` logic)

## 11. Add one or more image URLs during add, with previews
- What to study:
  - Add image URL to preview area before submit.
- Where:
  - `WEBDEVPROJECT/html/index.html:175` (`#newImagePreview`)
  - `WEBDEVPROJECT/html/index.html:1176` (`addNewImage`)

## 12. Modify data: only show modify form (hide table/other details)
- What to study:
  - Edit flow and screen visibility switching.
- Where:
  - `WEBDEVPROJECT/html/index.html:1076` (`editExample`)
  - `WEBDEVPROJECT/html/index.html:1116` (`saveEdit`)
  - `WEBDEVPROJECT/html/index.html:1424` (`cancelEditBtn` logic)

## 13. Modify images/URLs in edit form and show originals
- What to study:
  - Existing images + editable URL inputs in edit form.
- Where:
  - `WEBDEVPROJECT/html/index.html:225` (`#editImagePreview`)
  - `WEBDEVPROJECT/html/index.html:1089` (render original images + URL inputs)
  - `WEBDEVPROJECT/html/index.html:1200` (`addNewEditImage`)

## 14. Delete from table with confirmation modal
- What to study:
  - Delete button in table rows + confirm modal flow.
- Where:
  - `WEBDEVPROJECT/html/index.html:817` (Delete button in table rows)
  - `WEBDEVPROJECT/html/index.html:291` (`#deleteModal`)
  - `WEBDEVPROJECT/html/index.html:888` (`openDeleteModal`)
  - `WEBDEVPROJECT/html/index.html:1141` (`deleteExample`)

## 15. Validation and good feedback on add/modify
- What to study:
  - Validation helpers and user-visible error text.
- Where:
  - `WEBDEVPROJECT/html/index.html:443` (`showError`)
  - `WEBDEVPROJECT/html/index.html:452` (`clearAllErrors`)
  - `WEBDEVPROJECT/html/index.html:963` (`validateAddForm`)
  - `WEBDEVPROJECT/html/index.html:1002` (`validateEditForm`)

## 16. Added/modified tags must match current tags list
- What to study:
  - Central tag validation using `allTags`.
- Where:
  - `WEBDEVPROJECT/html/index.html:905` (`validateTagsField`)

## 17. Tag manager: add, delete, modify tags
- What to study:
  - Tag manager modal and operations.
- Where:
  - `WEBDEVPROJECT/html/index.html:311` (`#tagManagerModal`)
  - `WEBDEVPROJECT/html/index.html:1228` (`openTagManagerModal`)
  - `WEBDEVPROJECT/html/index.html:1239` (`renderTagManager`)
  - `WEBDEVPROJECT/html/index.html:1256` (`renameTag`)
  - `WEBDEVPROJECT/html/index.html:1305` (`addNewTag`)
  - `WEBDEVPROJECT/html/index.html:1340` (`deleteTag`)

---

## Extra simplifications already applied
- Removed `Restore Original` button and its function.
- Removed click-to-open-image-in-new-tab behavior.
- Removed rating/favorite edit interactions (kept random values and sorting support).
- Added requirement-labeled section notes directly inside script for faster study.
