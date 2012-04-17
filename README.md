scrollAppend Appends results as you scroll
===============================

This will automatically append the next page of results as you continue to scroll down a page. You can pause the appending and display a "Show More" button to continue so the user can stop to see the bottom of the page.  This also uses localStorage to cache the appended results so when a user clicks away and returns they'll come back to the place they left off.

Usage:
---
```
$(window).scrollAppend({
	url: 'newsfeed.php',
	params: { type: "image", who: "friends" }
	appendTo: "#newsfeed"
});
```

You can style the loading and show more divs with the following tags:
 
```
.scroll_append_more { width: 100%; text-align: center; }
.scroll_append_loading { width: 100%; }
.scroll_append_loading img { display: block; margin-left: auto; margin-right: auto; }
```

When you've reached the last page of results simply have your server-side script return the word "false" in plain text.