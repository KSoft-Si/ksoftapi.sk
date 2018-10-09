# Random Meme (Example uses Vixio 2 pre-2!)

```
discord command !meme:
	trigger:
		get random meme # <-- Fetches a random meme from the API #
		make embed:
			set the author info of the embed to author named "%event-user%" with icon "%avatar of event-user%"
			set title of embed to title with text "Did someone order a spicy meme?" and link "%last randmeme url%"
			add field named "Title" with value "%last randmeme title%" to fields of embed # <-- This expression grabs the last random meme title. This will fetch from where ever your "get random meme" code is #
			add field named "Subreddit" with value "[%last randmeme subreddit%](https://reddit.com/%last randmeme subreddit%)" to fields of embed
			add field named "Votes" with value "Upvotes: %last randmeme upvotes% | Downvotes: %last randmeme downvotes%" to fields of embed
			set the image of embed to "%last randmeme img%"
			set the timestamp of embed to now
		reply with last created embed
```

* Vixio - https://github.com/iBlitzkriegi/Vixio

This example is using Vixio 2 pre release 2, it will display an embed with a title, the subreddits, votes and the image.

Thanks to GamingGeek for this example.

# Search for Lyrics (Example uses Vixio 2 pre-2!)

```
discord command !lyrics <string>:
	trigger:
		search lyrics for arg-1 with text only false
		make embed:
			set the author info of the embed to author named "I found this for: %last lyric title%" with icon "%avatar of event-user%"
			set the description of embed to "%last lyrics%"
			add field named "Artist" with value "%last lyric artist%" to fields of embed
			add field named "Album" with value "%last lyric album%" to fields of embed
			add field named "Track Released" with value "%last lyric album year%" to fields of embed
			set the timestamp of embed to now
		reply with last created embed
```

* Vixio - https://github.com/iBlitzkriegi/Vixio

This example is using Vixio 2 pre release 2. It searches for argument one, or whatever you type after !lyrics. In this case, it could be: Never Gonna Give you up. Text only will search only inside the lyrics if set to true, we don't want that so it's only searching titles and artists.

Thanks to Ender for this example.

 ## If you wish to submit a example, please add it and create a pull request and we will take a look at it!
