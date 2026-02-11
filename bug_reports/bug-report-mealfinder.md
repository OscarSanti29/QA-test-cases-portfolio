# BUG-001: Search input validation for empty input does nothing after pressing search

**Environment:** Windows 11, Chrome (latest)  
**Severity:** Low
**Priority:** Low 
**Component:** Search Bar 
**Description:**  
When pressing the search button and the input box is empty nothing happens 

## Steps to Reproduce
1. Open the Mealfinder app
2. Leave the search box empty
3. Press Search button

## Actual Result
- Nothing happens

## Expected Result
-An inline validation message appears (“Please enter a search term”)

## Notes
- Possible cause: Alert is not set up correctly in the code or no error catching
