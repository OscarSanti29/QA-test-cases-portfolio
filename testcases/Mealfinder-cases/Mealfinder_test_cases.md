# Mealfinder - Manual Test Cases

**App:** Mealfinder  
**Type:** Web App  
**Focus Areas:** local storage, product browsing, search/filter, UI validation  
**Environment:** Chrome (latest), Windows 10/11

## TC-001: Search meal by valid name returns results
**Priority:** High  
**Type:** Functional  
**Preconditions:** App is loaded, user is on home/search page  

**Steps:**
1. In the search input, enter `chicken`
2. Click the **Search** button (or press Enter)

**Expected Results:**
- A results list/grid is displayed
- Each result shows a meal name and thumbnail (if available)
- No error message is shown


## TC-002: Search with no matching results shows empty state
**Priority:** High  
**Type:** Functional / UI  
**Preconditions:** App is loaded, user is on home/search page  

**Steps:**
1. Enter `zzzzzzzzzz` in the search input
2. Click **Search**

**Expected Results:**
- A “No results found” (or similar) message is displayed
- No broken UI elements appear
- Previous search results (if any) are cleared or clearly replaced


## TC-003: Search input validation for empty input
**Priority:** Medium  
**Type:** Functional / UI  
**Preconditions:** App is loaded, user is on home/search page  

**Steps:**
1. Ensure the search input is empty
2. Click **Search**

**Expected Results (choose what matches your app):**
- Option A: Search button is disabled when input is empty
- Option B: An inline validation message appears (“Please enter a search term”)
- App does not crash and does not call the API unnecessarily


## TC-004: Navigate to meal details from results
**Priority:** High  
**Type:** Functional  
**Preconditions:** Results are displayed for a valid search (ex: `chicken`)  

**Steps:**
1. Click on a meal card (or “View Details” button) in the results list

**Expected Results:**
- User is navigated to the meal details page/view
- Details page shows:
  - Meal name
  - Instructions (or section for instructions)
  - Ingredients list (or section for ingredients)
- No console/UI errors displayed


## TC-005: Handle meal with missing image gracefully
**Priority:** Medium  
**Type:** UI / Data Handling  
**Preconditions:** A meal result exists with a missing/invalid thumbnail (or simulate by blocking image URL / using a known missing image case)  

**Steps:**
1. Search for meals (any term that returns multiple results)
2. Identify a result with a missing/broken thumbnail OR simulate broken image loading
3. Observe the meal card UI

**Expected Results:**
- UI layout does not break
- A placeholder image or fallback UI is shown (or image area stays clean)
- Meal name remains visible and clickable
