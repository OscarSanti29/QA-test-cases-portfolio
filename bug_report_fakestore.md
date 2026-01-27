# BUG-001: Products card flip animation does not run on mobile size(390px)

**Environment:** Windows 11, Chrome (latest)  
**Severity:** Medium  
**Priority:** P2  
**Component:** Responive layout  
**Description:**  
When Resizing browser to mobile width (390px), products on main page do not flip when clicked on and details button cant be clicked to navigate to details page

## Steps to Reproduce
1. Open the FakeStore app
2. Log in as a user
3. Resize browser to 390px
4. Click on product to run animation and flip to reveal details button
5. Click details button to navigate to that specific product's detail page

## Actual Result
- Product card does not run animation and details button can not be clicked

## Expected Result
- Product card is flipped when clicked, revealing details button, and details button is clicked to navigate to details page

## Notes
- Possible cause: "Hover-Only" behavior used for flip, Hover only doesn't reliable trigger on tap/mobile sized layouts.
