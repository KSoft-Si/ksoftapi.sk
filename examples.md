# Random Meme (Example uses Vixio 2 pre-2!)

```
discord command !meme:
	trigger:
		get random meme
		make embed:
			set the author info of the embed to author named "%event-user%" with icon "%avatar of event-user%"
			set title of embed to title with text "Did someone order a spicy meme?" and link "%last randmeme url%"
			add field named "Title" with value "%last randmeme title%" to fields of embed
			add field named "Subreddit" with value "[%last randmeme subreddit%](https://reddit.com/%last randmeme subreddit%)" to fields of embed
			add field named "Votes" with value "Upvotes: %last randmeme upvotes% | Downvotes: %last randmeme downvotes%" to fields of embed
			set the image of embed to "%last randmeme img%"
			set the timestamp of embed to now
		reply with last created embed
```

* Vixio - https://github.com/iBlitzkriegi/Vixio

This example is using Vixio 2 pre release 2, it will display an embed with a title, the subreddits, votes and the image.

