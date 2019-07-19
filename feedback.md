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

## UX

- [✓] Basic styling added
- [✗] Responsive design
- [✓] Items aligned
- [✓] Content legible (not too wide, obstructed, etc)
- [✓] Refreshing doesn’t cause an issue on sub-pages
- [✓] No errors in the console
- [✓] Votes / Posts / Deletions happen instantly _OR_ give user indication of loading

* Content is very clear and most aligned except on some mobile devices where the article cards are squashed and the content is overflowing
* Pretty responsive overall - buttons get a bit squashed when viewport width gets really narrow
* Consider a colour scheme with a tad less vividity - at the moment the colours are all very intense !
* Consider using pseudo-classes for the buttons - like background colour shifts when hovering over certain button elements
* 


## Functionality

### Login

- [✗] Some indication of who is logged in

### Articles

- [ ] Serves all articles / top articles
- [ ] Can vote on articles
- [ ] Can vote a maximum of once in either direction per page load
- [ ] Votes are persistent when page is refreshed
- [ ] Topic pages load only relevant articles (especially when navigating from one topic page to another)
- [ ] Can sort articles by date created / comment_count / votes

### Individual Article / Comments

- [ ] Individual articles are served with comments
- [ ] Can vote on comments
- [ ] Can vote a maximum of once in either direction per page load
- [ ] Votes are persistent when page is refreshed
- [ ] Can post new comments, which are persistent
- [ ] Can only delete comments of logged in user
- [ ] Deleted comments don’t re-appear on re-render/refresh

### Additional functionality:

- [ ] navigate over pages of articles (if implemented in back-end)
- [ ] navigate over pages of comments (if implemented in back-end)
- [ ] filter / display articles by specific user
- [ ] post new article
- [ ] delete logged in user's articles

## Error Handling

- [ ] Bad url
- [ ] Bad topic slug in url
- [ ] Bad article id in url
- [ ] Bad username in url
- [ ] Post comment: (No text in comment body / Can you post without logging in?)

## Code

- [ ] Well named components
- [ ] Functional components used where possible
- [ ] `node_modules` git ignored
- [ ] Components reused where possible (`Articles` / `Voter`...)
- [ ] Functions are DRY (`handleChange` for controlled components / api calls)
- [ ] Use object destructuring where possible
- [ ] No `console.log`s / comments
- [ ] Tidy? If not: ESLint / Prettier

## MAKE SURE ALL TESTS ARE STILL PASSING IN BACK END

## Once everything else is complete, here are some extra challenges:

- [ ] Use `aXe` extension to check for a11y issues
- [ ] Make sure any pure functions are extracted and tested with `Jest`
- [ ] Add integration tests with `cypress`
- [ ] Use Context API for sharing logged in user amongst components
