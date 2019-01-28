# The KSoft.Si API is primarily for discord bots, therefore most examples will use Vixio (discord integration for Skript)

## Random Meme (Example uses Vixio 2!)

```
discord command !meme:
	trigger:
		get random meme and store it in {_meme::} # <-- Fetches a random meme from the API #
		if {_meme::nsfw} is true: # Simple section to prevent NSFW memes in non-NSFW channels #
			if nsfw state of event-channel is false:
				reply with "This image has been marked as NSFW and this channel is not marked as NSFW so I cannot send the meme"
				stop # Stops the code from executing after telling the user the meme is NSFW #
		make embed:
			set the author info of the embed to author named "%event-user%" with icon "%avatar of event-user%"
			set title of embed to title with text "Did someone order a spicy meme?" and link "%{_meme::url}%"
			add field named "Title" with value "%{_meme::title}%" to fields of embed
			add field named "Subreddit" with value "[%{_meme::subreddit}%](https://reddit.com/%{_meme::subreddit}%)" to fields of embed
			add field named "Votes" with value "Upvotes: %{_meme::upvotes}% | Downvotes: %{_meme::downvotes}%" to fields of embed
			set the image of embed to "%{_meme::img}%"
			set the timestamp of embed to now
		reply with last created embed
```

* Vixio - https://github.com/iBlitzkriegi/Vixio

This example is using Vixio 2, it will display an embed with a title, the subreddits, votes and the image.

Thanks to GamingGeek for this example.

## Search for Lyrics (Example uses Vixio 2!)

```
discord command !lyrics <string>:
	trigger:
		search lyrics for arg-1 and store it in {_lyrics::*} using options text only false
		make embed:
			set the author info of the embed to author named "I found lyrics for: %{_lyrics::tracktitle::1}%" with icon "%avatar of event-user%"
			set the description of embed to "%{_lyrics::tracklyrics::1}%"
			add field named "Artist" with value "%{_lyrics::artist::1}%" to fields of embed
			add field named "Album" with value "%{_lyrics::album::1}%" to fields of embed
			add field named "Track Released" with value "%{_lyrics::album_year::1}%" to fields of embed
			set the timestamp of embed to now
		reply with last created embed
```

* Vixio - https://github.com/iBlitzkriegi/Vixio

This example is using Vixio 2. It searches for argument one, or whatever you type after !lyrics. In this case, it could be: Never Gonna Give you up. Text only will search only inside the lyrics if set to true, we don't want that so it's only searching titles and artists.

Thanks to Ender for this example.

 ## If you wish to submit a example, please add it and create a pull request and we will take a look at it!
