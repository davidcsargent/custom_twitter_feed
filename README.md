# custom_twitter_feed
Custom Twitter Feed for Websites


Make A Custom Twitter Widget Without A Plugin
---------------------------------------------

### Step 1

First, place the following code where you want the list to show up:

```
<ul id="twitter_update_list"><li>Twitter feed loading</li></ul>
```

Note: The `<li>Twitter feed loading</li>` is not a part of the original code Twitter provided, but it’s required to make the HTML validate. It can also provide a useful message while the feed is loading, as it could take a few seconds on a slow day.

### Step 2

Second, you’ll need to place the following lines of Javascript as close to the `</body>` tag as possible.

```
<script type="text/javascript" src="http://twitter.com/javascripts/blogger.js"></script>
<script type="text/javascript" src="http://twitter.com/statuses/user_timeline/USERNAME.json?callback=twitterCallback2&count=3"></script>
```

You should keep these lines of Javascript as low as possible on the page because in the event that Twitter doesn’t load, everything below that code will hang (which isn’t a big deal if it’s already at the bottom).

### Step 3

Here’s the code I use for the list:
```
#twitter_update_list {
	font-size: 13px;
	line-height: 21px;
	list-style: none;
	}
#twitter_update_list li {
	background: url('images/twitter-divider.gif') bottom left repeat-x;
	padding-bottom: 7px;
	margin-bottom: 9px;
	}
#twitter_update_list span, #twitter_update_list span a {
	color: #ababab;
	text-decoration: none;
	}
#twitter_update_list a {
	color: #6f7276;
	}
```

1. The first line selects the entire list. It sets the font size, line height, and makes sure no bullet points show up.
2. The second line makes a small 2×1 image repeat below each list item as a sort of divider. The padding sets the space between the tweet and the top edge of the divider. The margin sets the space between the bottom edge of the divider and the next tweet.
3. The third line sets the color of the tweet, including links, and makes sure no lines show up below links.
4. The last line sets the color of the “time ago” link.

*Initial source and credit to [IsItWp](http://www.isitwp.com/custom-twitter-widget-tutorial/)*
