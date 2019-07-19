## FE - feedback

# Checklist for Northcoders News - Front End
✓
✗
## README

- [✗] provide general info about app
- [✗] clear instructions on how to run locally
- [✗] link to API & back end repo
- [✗] specify minimum versions
- [✓] deploy
- [✗] link to deployed version

* Need to get the README done with info about cloning the repo, getting it started and with a link to the deployd version

## UX

- [✓] Basic styling added
- [✗] Responsive design
- [✓] Items aligned
- [✓] Content legible (not too wide, obstructed, etc)
- [✓] Refreshing doesn’t cause an issue on sub-pages
- [✓] No errors in the console
- [✓] Votes / Posts / Deletions happen instantly _OR_ give user indication of loading

* Content is very clear and most aligned except on some mobile devices where the article cards are squashed and the content is overflowing
* Pretty responsive overall - comment cards get a bit squashed when viewport width gets really narrow - minor issue here though
* Consider a colour scheme with a tad less vividity - at the moment the colours are all very intense !
* Consider using pseudo-classes for the buttons - like background colour shifts when hovering over certain button elements
* Lovely clear icons with clear symbols - this looks great!
* Play around with the format of the dates more ... consider using an npm package to get a more user-friendly format


## Functionality

### Login

- [✗] Some indication of who is logged in

* Needs to be clearer who is currently logged in
* Ensure login changing is at the top of the page


### Articles

- [✓] Serves all articles / top articles
- [✓] Can vote on articles
- [✓] Can vote a maximum of once in either direction per page load
- [✓] Votes are persistent when page is refreshed
- [✓] Topic pages load only relevant articles (especially when navigating from one topic page to another)
- [✓] Can sort articles by date created / comment_count / votes

### Individual Article / Comments

- [✓] Individual articles are served with comments
- [✓] Can vote on comments
- [✓] Can vote a maximum of once in either direction per page load
- [✓] Votes are persistent when page is refreshed
- [✓] Can post new comments, which are persistent
- [✓] Can only delete comments of logged in user
- [✓] Deleted comments don’t re-appear on re-render/refresh

### Additional functionality:

- [✓] navigate over pages of articles (if implemented in back-end)
- [✓] navigate over pages of comments (if implemented in back-end)
- [✗] filter / display articles by specific user
- [✗] post new article
- [✗] delete logged in user's articles

* Page navigation could be a bit clearer - next page maybe and previous page could be clearer options for a user
* No POST article functionality the moment
* Consider pages for specific users if you have time


## Error Handling

- [✓] Bad url
- [✗] Bad topic slug in url
- [✗] Bad article id in url
- [?] Bad username in url
- [✓] Post comment: (No text in comment body / Can you post without logging in?)

* Bad article id in the url should result in a 400 message - you are sending back 404 regardless at the moment
* Topic doesn't exist should be 404 so this is fine at the moment
* What happens in the case when topic does exist but there are no articles for the given topic ?


## Code

- [✓] Well named components
- [✓] Functional components used where possible
- [✓] `node_modules` git ignored
- [✓] Components reused where possible (`Articles` / `Voter`...)
- [✓] Functions are DRY (`handleChange` for controlled components / api calls)
- [✓] Use object destructuring where possible
- [✓] No `console.log`s / comments
- [✓] Tidy? If not: ESLint / Prettier

* A default warning from React when navigating to a page with an non-existent article id
* `setOrder` , `setPage` functions could be made more DRY - consider ways in which you can re-use the functionality, they are essentially doing the same sort of thing
* `Header` not dynamically producing list of options - what happens if more icons are addded at a later point
* Lots of `if` statements when inside the `componentDidMount` lifecycle method in the `Articles` component - how could you make this check cleaner and more DRY ?


## MAKE SURE ALL TESTS ARE STILL PASSING IN BACK END

## Once everything else is complete, here are some extra challenges:

- [ ] Use `aXe` extension to check for a11y issues
- [ ] Make sure any pure functions are extracted and tested with `Jest`
- [ ] Add integration tests with `cypress`
- [ ] Use Context API for sharing logged in user amongst components
