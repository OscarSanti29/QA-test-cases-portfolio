# FakeStore - Manual Test Cases

**App:** FakeStore (E-commerce demo)  
**Type:** Web App  
**Focus Areas:** Login, product browsing, search/filter, UI validation  
**Environment:** Chrome (latest), Windows 10/11

### TC-001: Login with valid credentials
**Priority:** High
**Type:** Functional
**Preconditions:** User account exists  
**Steps:**
1. Navigate to Login page
2. Enter valid username (should be to the left of the screen on the log in page, just press the dropdown on the names)
3. Enter valid password (should be to the left of the screen on the log in page, just press the dropdown on the names)
4. Click "Login"

**Expected Result:**
- User is logged in successfully
- User is redirected to the main/home page
- No error message displayed

### TC-002: Login with invalid password
**Priority:** High
**Type:** Functional
**Preconditions:** App is loaded, user is on home/search page
**Steps:**
1. Navigate to Login page
2. Enter valid username
3. Enter invalid password
4. Click "Login"

**Expected Result:**
- Login fails
- Error message is displayed
- User remains on login page

### TC-003: Search by product name (exact match)
**Priority:** Medium
**Type:** Functional/UI
**Preconditions:** App is loaded, user is on home/search page
**Steps:**
1. Navigate to Products page
2. Enter a valid product name in search bar
3. Submit search

**Expected Result:**
- Relevant product(s) displayed
- No unrelated products shown

### TC-004: Search with no results
**Priority:** Medium
**Type:** Functional/UI
**Preconditions:** App is loaded, user is on home/search page
**Steps:**
1. Navigate to Products page
2. Search for a random string (e.g., "zzzz123")

**Expected Result:**
- "No results" state is shown (or empty state)
- App does not crash

### TC-005: Filter by category
**Priority:** Medium
**Type:** Functional/UI
**Preconditions:** App is loaded, user is on home/search page
**Steps:**
1. Navigate to Products page
2. Select a category filter

**Expected Result:**
- Only products from selected category appear
- Filter label updates correctly (if applicable)


### TC-006: Responsive layout (mobile width)
**Priority:** High
**Type:** UI
**Preconditions:** App is loaded, user is on home/search page
**Steps:**
1. Resize browser to ~390px width (mobile)
2. Navigate through main pages

**Expected Result:**
- Layout remains readable
- Buttons and input fields remain usable
- No overlapping elements
