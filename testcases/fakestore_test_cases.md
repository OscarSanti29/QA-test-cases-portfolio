# FakeStore - Manual Test Cases

**App:** FakeStore (E-commerce demo)  
**Type:** Web App  
**Focus Areas:** Login, product browsing, search/filter, cart, UI validation  
**Environment:** Chrome (latest), Windows 10/11

## Test Suite: Authentication

### TC-AUTH-001: Login with valid credentials
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

### TC-AUTH-002: Login with invalid password
**Steps:**
1. Navigate to Login page
2. Enter valid username
3. Enter invalid password
4. Click "Login"
**Expected Result:**
- Login fails
- Error message is displayed
- User remains on login page

## Test Suite: Product Search & Filter

### TC-PROD-001: Search by product name (exact match)
**Steps:**
1. Navigate to Products page
2. Enter a valid product name in search bar
3. Submit search
**Expected Result:**
- Relevant product(s) displayed
- No unrelated products shown

### TC-PROD-002: Search with no results
**Steps:**
1. Navigate to Products page
2. Search for a random string (e.g., "zzzz123")
**Expected Result:**
- "No results" state is shown (or empty state)
- App does not crash

### TC-PROD-003: Filter by category
**Steps:**
1. Navigate to Products page
2. Select a category filter
**Expected Result:**
- Only products from selected category appear
- Filter label updates correctly (if applicable)

## UI / UX Checks

### TC-UI-001: Responsive layout (mobile width)
**Steps:**
1. Resize browser to ~390px width (mobile)
2. Navigate through main pages
**Expected Result:**
- Layout remains readable
- Buttons and input fields remain usable
- No overlapping elements
