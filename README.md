# mattata

mattata is a powerful, plugin-based Telegram bot similar to [topkecleon's](https://github.com/topkecleon/otouto). mattata boasts many nifty features such as a fully-fledged administration plugin, AI (native Cleverbot implementation, which utilises my [mattata-ai](https://github.com/wrxck/mattata-ai) library) and much more.

## Setup

Installing & configuring mattata is very simple.

Clone the repository using:

```Bash
git clone https://github.com/wrxck/mattata
```

in Terminal. Then, run the following:

```Bash
cd mattata/
chmod +x ./install.sh
./install.sh
chmod +x ./launch.sh
```

You'll need sudo access to be able to install the dependencies required. Then, you need to fill in the values in `configuration.lua`. After you've done that, use:

```Bash
./launch.sh
```

to run your bot.

## Plugins

mattata features an extensive, robust plugin system, similar to [topkecleon's](https://github.com/topkecleon/otouto). Below is a table containing a list of currently-documented plugins and their corresponding usage information.

| Command                         | Plugin                | Arguments                                                     | Description                                                                                                                                                                                                                                                                                                                                                   | Aliases         |
|---------------------------------|-----------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| /administration                 | `administration.lua`  | -                                                             | Configure the administration settings for your chat through an interactive menu sent via private message.                                                                                                                                                                                                                                                     | /antispam       |
| /apod                           | `apod.lua`            | [dd/mm/yyyy]                                                  | Sends the Astronomy Picture of the Day via NASA's API. If a date is given, the Astronomy Picture for that date is returned.                                                                                                                                                                                                                                   | -               |
| /appstore                       | `appstore.lua`        | \<query\>                                                     | Displays information about the first app returned by iTunes for the given search query.                                                                                                                                                                                                                                                                       | /app            |
| /avatar                         | `avatar.lua`          | \<user\> [offset]                                             | Sends the profile photos of the given user, of which can be specified by username or numerical ID. If an offset is given after the username (which must be a numerical value), then the nth profile photo is sent (if available).                                                                                                                             | -               |
| /base64                         | `base64.lua`          | \<text\>                                                      | Converts a string of text into base64-encoded text.                                                                                                                                                                                                                                                                                                           | /b64            |
| /binary                         | `binary.lua`          | \<text\>                                                      | Converts a numerical value into binary.                                                                                                                                                                                                                                                                                                                       | /bin            |
| /bing                           | `bing.lua`            | \<query\>                                                     | Searches Bing for the given search query and returns the top results.                                                                                                                                                                                                                                                                                         | -               |
| /blacklist                      | `administration.lua`  | [user]                                                        | Prevents a user from using the bot in the chat. The user must be specified by username/ID, or by reply.                                                                                                                                                                                                                                                       | -               |
| /bugreport                      | `bugreport.lua`       | \<text\>                                                      | Reports a bug to the configured developer.                                                                                                                                                                                                                                                                                                                    | /bug, /br       |
| /calc                           | `calc.lua`            | \<expression\>                                                | Solves the given mathematical expression using mathjs.org.                                                                                                                                                                                                                                                                                                    | -               |
| /canitrust                      | `canitrust.lua`       | \<url\>                                                       | Reveals any known security issues with a website.                                                                                                                                                                                                                                                                                                             | -               |
| /catfact                        | `catfact.lua`         | -                                                             | Sends a random, cat-themed fact.                                                                                                                                                                                                                                                                                                                              | -               |
| /cat                            | `cats.lua`            | -                                                             | Sends a random photo of a cat.                                                                                                                                                                                                                                                                                                                                | /sarah          |
| /channel                        | `channel.lua`         | \<channel\> \<message\>                                       | Sends a message to a Telegram channel/group. The channel/group can be specified via ID or username. Messages can be formatted with Markdown. Users can only send messages to channels/groups they own and/or administrate.                                                                                                                                    | /ch             |
| /chuck                          | `chuck.lua`           | -                                                             | Sends a random Chuck Norris joke.                                                                                                                                                                                                                                                                                                                             | -               |
| /coinflip                       | `coinflip.lua`        | [guess]                                                       | Flips a coin and returns the result! If a guess is given, the result is tested against it and reveals the accuracy accordingly.                                                                                                                                                                                                                               | /cf             |
| /copypasta                      | `copypasta.lua`       | -                                                             | Riddles the replied-to message with cancerous emoji.                                                                                                                                                                                                                                                                                                          | /😂             |
| /currency                       | `currency.lua`        | \<amount\> \<from\> TO \<to\>                                 | Converts exchange rates for various currencies via Google Finance.                                                                                                                                                                                                                                                                                            | /convert, /cash |
| /demod                          | `administration.lua`  | [user]                                                        | Strip a user of their moderator status, revoking their ability to use administrative commands such as /ban, /kick and /unban. The user must be specified by username/ID, or by reply.                                                                                                                                                                         | /demote         |
| /dice                           | `dice.lua`            | \<number\> \<range\>                                          | Rolls a die - returning random numbers between 1 and the given range the given number of times.                                                                                                                                                                                                                                                               | -               |
| /dictionary                     | `dictionary.lua`      | \<word\>                                                      | Looks up the given word in the Oxford Dictionary and returns the relevant definition(s).                                                                                                                                                                                                                                                                      | /define         |
| /dns                            | `dns.lua`             | \<url\> \<record type\>                                       | Sends the given URL's DNS records of the given type. The record types currently supported are AAAA, A, CERT, CNAME, DLV, IPSECKEY, MX, NS, PTR, SIG, SRV and TXT.                                                                                                                                                                                             | -               |
| /doggo                          | `doggo.lua`           | -                                                             | Sends a random photo of a dog.                                                                                                                                                                                                                                                                                                                                | -               |
| /echo                           | `echo.lua`            | \<text\>                                                      | Repeats the given string of text.                                                                                                                                                                                                                                                                                                                             | -               |
| /eightball                      | `eightball.lua`       | -                                                             | Makes a decision for you using the (virtual) magic 8 ball!                                                                                                                                                                                                                                                                                                    | /8ball          |
| /emoji                          | `emoji.lua`           | \<emoji\>                                                     | Sends information about the given emoji.                                                                                                                                                                                                                                                                                                                      | -               |
| /facebook                       | `facebook.lua`        | \<Facebook username\>                                         | Sends the given Facebook user's profile picture.                                                                                                                                                                                                                                                                                                              | /fb             |
| /fact                           | `fact.lua`            | -                                                             | Returns a random (yet somewhat-untrue) fact!                                                                                                                                                                                                                                                                                                                  | -               |
| /flickr                         | `flickr.lua`          | \<query\>                                                     | Searches Flickr for a photo matching the given search query and returns the most relevant result.                                                                                                                                                                                                                                                             | -               |
| /fortune                        | `fortune.lua`         | -                                                             | Sends your fortune (featuring a seasonally-adjusting ASCII animal!).                                                                                                                                                                                                                                                                                          | -               |
| /game                           | `game.lua`            | [stats]                                                       | Play a game of Tic-Tac-Toe. Use /game stats to view your current game statistics.                                                                                                                                                                                                                                                                             | -               |
| /gif                            | `giphy.lua`           | \<query\>                                                     | Searches GIPHY for the given search query and returns a random, relevant result.                                                                                                                                                                                                                                                                              | /giphy          |
| /github                         | `github.lua`          | \<GitHub username\> \<GitHub repository name\>                | Returns information about the specified GitHub repository.                                                                                                                                                                                                                                                                                                    | -               |
| /githubfeed                     | `githubfeed.lua`      | \<sub \| del\> \<GitHub username\> \<GitHub repository name\> | Manage your subscriptions to updates from GitHub repositories.                                                                                                                                                                                                                                                                                                | /gh             |
| /google                         | `gsearch.lua`         | \<query\>                                                     | Searches Google for the given search query and returns the most relevant result(s).                                                                                                                                                                                                                                                                           | -               |
| /hackernews                     | `hackernews.lua`      | -                                                             | Sends the top stories from Hacker News.                                                                                                                                                                                                                                                                                                                       | /hn             |
| /help                           | `help.lua`            | [plugin]                                                      | A help-orientated menu is sent if no arguments are given. If arguments are given, usage information for the given plugin is sent instead.                                                                                                                                                                                                                     | /start          |
| /hexadecimal                    | `hexadecimal.lua`     | \<text\>                                                      | Converts the given string of text into hexadecimal.                                                                                                                                                                                                                                                                                                           | /hex            |
| /hextorgb                       | `hextorgb.lua`        | \<hex code\>                                                  | Converts the given hex colour code into its RGB format.                                                                                                                                                                                                                                                                                                       | -               |
| /id                             | `id.lua`              | [chat]                                                        | Sends information about the given chat. Input is also accepted via reply.                                                                                                                                                                                                                                                                                     | -               |
| /identicon                      | `identicon.lua`       | \<text\>                                                      | Generates an identicon from the given string of text.                                                                                                                                                                                                                                                                                                         | -               |
| /imdb                           | `imdb.lua`            | \<query\>                                                     | Searches IMDb for the given search query and returns the most relevant result(s).                                                                                                                                                                                                                                                                             | -               |
| /instagram                      | `instagram.lua`       | \<Instagram username\>                                        | Sends the given Instagram user's profile picture.                                                                                                                                                                                                                                                                                                             | /ig             |
| /insult                         | `insult.lua`          | -                                                             | Generates a random insult.                                                                                                                                                                                                                                                                                                                                    | -               |
| /isp                            | `isp.lua`             | \<url\>                                                       | Sends information about the given URL's Internet Service Provider (ISP).                                                                                                                                                                                                                                                                                      | -               |
| /ispwned                        | `ispwned.lua`         | \<account\>                                                   | Returns the existence of the given account in any major data leaks.                                                                                                                                                                                                                                                                                           | -               |
| /isup                           | `isup.lua`            | \<url\>                                                       | Checks to see if the given URL is down for everyone or just you.                                                                                                                                                                                                                                                                                              | -               |
| /itunes                         | `itunes.lua`          | \<query\>                                                     | Searches iTunes for the given search query and returns the most relevant result.                                                                                                                                                                                                                                                                              | -               |
| /jsondump                       | `jsondump.lua`        | -                                                             | Returns the raw JSON of your message.                                                                                                                                                                                                                                                                                                                         | -               |
| /kick                           | `kick.lua`            | [user]                                                        | Bans, then unbans, a user from the chat (also known as a "soft-ban"). The user must be specified by username/ID, or by reply.                                                                                                                                                                                                                                 | -               |
| /lastfm                         | `lastfm.lua`          | [Last.fm username]                                            | Returns what you, or the given Last.fm user, last listened to on Last.fm.                                                                                                                                                                                                                                                                                     | /np             |
| /link                           | `administration.lua`  | -                                                             | Sends the group link.                                                                                                                                                                                                                                                                                                                                         | -               |
| /lmgtfy                         | `lmgtfy.lua`          | \<query\>                                                     | Sends a LMGTFY link for the given search query.                                                                                                                                                                                                                                                                                                               | -               |
| /location                       | `location.lua`        | [query]                                                       | Sends your location, or a location from Google Maps.                                                                                                                                                                                                                                                                                                          | /loc            |
| /loremipsum                     | `loremipsum.lua`      | -                                                             | Generates a paragraph of Lorem Ipsum text.                                                                                                                                                                                                                                                                                                                    | -               |
| /lyrics                         | `lyrics.lua`          | \<query\>                                                     | Finds the lyrics to the given track.                                                                                                                                                                                                                                                                                                                          | -               |
| /me                             | `me.lua`              | \<emote message\>                                             | Allows you to emote, Minecraft-style.                                                                                                                                                                                                                                                                                                                         | -               |
| /minecraft                      | `minecraft.lua`       | \<Minecraft username\>                                        | Sends information about the given Minecraft user.                                                                                                                                                                                                                                                                                                             | /mc             |
| /mod                            | `administration.lua`  | [user]                                                        | Promote the given user to moderator status, allowing them use of administrative commands such as /ban, /kick and /unban. The user must be specified by username/ID, or by reply.                                                                                                                                                                              | /promote        |
| /msglink                        | `msglink.lua`         | -                                                             | Gets the link to the replied-to message.                                                                                                                                                                                                                                                                                                                      | -               |
| /name                           | `name.lua`            | \<text\>                                                      | Changes the name that the bot's AI responds to.                                                                                                                                                                                                                                                                                                               | -               |
| /netflix                        | `netflix.lua`         | \<query\>                                                     | Searches Netflix for the given search query and returns the most relevant result.                                                                                                                                                                                                                                                                             | /nf             |
| /news                           | `news.lua`            | \<news source\>                                               | Sends the current top story from the given news source.                                                                                                                                                                                                                                                                                                       | -               |
| /ninegag                        | `ninegag.lua`         | -                                                             | Returns a random image from the latest 9gag posts.                                                                                                                                                                                                                                                                                                            | /9gag           |
| /nsources                       | `news.lua`            | [query]                                                       | Returns a list of available sources that can be used with /news. If a query is given as a command argument, a Lua pattern match for the given query is made and a list of matching news sources is returned.                                                                                                                                                  | -               |
| /paste                          | `paste.lua`           | \<text\>                                                      | Uploads the given text to a pasting service and returns the result URL.                                                                                                                                                                                                                                                                                       | -               |
| /pay                            | `pay.lua`             | \<amount\>                                                    | Sends the replied-to user the given amount of mattacoins.                                                                                                                                                                                                                                                                                                     | -               |
| /plugins                        | `plugins.lua`         | -                                                             | Toggle the plugins you want to use in your chat with a slick inline keyboard, paginated and neatly formatted.                                                                                                                                                                                                                                                 | -               |
| /pokedex                        | `pokedex.lua`         | \<query\>                                                     | /pokedex \<query\> - Returns a Pokedex entry from pokeapi.co. Alias: /dex.                                                                                                                                                                                                                                                                                    |                 |
| /prime                          | `prime.lua`           | \<number\>                                                    | /prime \<number\> - Tells you if a number is prime or not.                                                                                                                                                                                                                                                                                                    |                 |
| /pun                            | `pun.lua`             | -                                                             | Generates a random pun.                                                                                                                                                                                                                                                                                                                                       | -               |
| /qr                             | `qr.lua`              | \<text\>                                                      | Converts the given string of text to a QR code.                                                                                                                                                                                                                                                                                                               | /qrcode         |
| /randomword                     | `randomword.lua`      | -                                                             | Generates a random word.                                                                                                                                                                                                                                                                                                                                      | /rw             |
| /r/subreddit                    | `reddit.lua`          | -                                                             | Returns the latest posts from the given subreddit.                                                                                                                                                                                                                                                                                                            | -               |
| /rimg                           | `rimg.lua`            | \<width\> [height] [-g \| -b]                                 | Sends a random image which matches the dimensions provided, in pixels. If only 1 dimension is given, the other is assumed to be the same. Append -g to the end of your message to return a grayscale photo, or append -b to the end of your message to return a blurred photo. The maximum value for each dimension is 5000, and the minimum for each is 250. | -               |
| /s/\<pattern\>/\<substitution\> | `sed.lua`             | -                                                             | s/\<pattern\>/\<substitution\> - Replaces all occurences, of text matching a given Lua pattern, with the given substitution.                                                                                                                                                                                                                                  | -               |
| /setlang                        | `setlang.lua`         | -                                                             | Allows you to select your language.                                                                                                                                                                                                                                                                                                                           | -               |
| /setloc                         | `setloc.lua`          | \<location\>                                                  | Sets your location to the given value.                                                                                                                                                                                                                                                                                                                        | -               |
| /setsteam                       | `steam.lua`           | \<text\>                                                      | Sets your Steam username to the given text                                                                                                                                                                                                                                                                                                                    | -               |
| /setwelcome                     | `administration.lua`  | \<text\>                                                      | Sets the group's welcome message to the given text. Markdown formatting is supported.                                                                                                                                                                                                                                                                         | -               |
| /shorten                        | `shorten.lua`         | \<url\>                                                       | Shortens the given URL using one of the given URL shorteners.                                                                                                                                                                                                                                                                                                 | -               |
| /shout                          | `shout.lua`           | \<text\>                                                      | Shouts the given text in multiple directions!                                                                                                                                                                                                                                                                                                                 | -               |
| /slap                           | `slap.lua`            | [target]                                                      | Slaps someone, or something.                                                                                                                                                                                                                                                                                                                                  | -               |
| /snapchat                       | `snapchat.lua`        | \<Snapchat username\>                                         | Sends the "Snap" code for the given Snapchat username.                                                                                                                                                                                                                                                                                                        | /sc             |
| /spotify                        | `spotify.lua`         | \<query\>                                                     | Searches Spotify for a track matching the given search query and returns the most relevant result.                                                                                                                                                                                                                                                            | -               |
| /statistics                     | `statistics.lua`      | -                                                             | Shows statistical information about the current chat's top ten users (ordered by message count).                                                                                                                                                                                                                                                              | /stats          |
| /steam                          | `steam.lua`           | [username]                                                    | Displays information about the given Steam user. If no username is specified then information about your Steam account (if applicable) is sent.                                                                                                                                                                                                               | -               |
| /synonym                        | `synonym.lua`         | \<word\>                                                      | Sends a word similar to the word given.                                                                                                                                                                                                                                                                                                                       | -               |
| /time                           | `time.lua`            | [location]                                                    | If no arguments are given; the current time, date, and timezone for your location are sent (if applicable). Otherwise, the current time, date and timezone for the given location is returned. The returned location is the first relevant result on Google Maps for the given search query.                                                                  | -               |
| /translate                      | `translate.lua`       | [locale] \<text\>                                             | If a locale is given, the given text is translated into the said locale's language. If no locale is given then the given text is translated into the bot's configured language. If the command is used in reply to a message containing text, then the replied-to text is translated and the translation is returned.                                         | /tl             |
| /twitch                         | `twitch.lua`          | \<query\>                                                     | Searches Twitch for the given search query and returns the most relevant result(s).                                                                                                                                                                                                                                                                           | -               |
| /unicode                        | `unicode.lua`         | \<text\>                                                      | Returns the given text as a JSON-encoded table of Unicode (UTF-32) values.                                                                                                                                                                                                                                                                                    | -               |
| /urbandictionary                | `urbandictionary.lua` | \<query\>                                                     | Searches the Urban Dictionary for the given search query and returns the most relevant result(s).                                                                                                                                                                                                                                                             | /urban, /ud     |
| /uuid                           | `uuid.lua`            | -                                                             | Generates a random UUID.                                                                                                                                                                                                                                                                                                                                      | /guid           |
| /weather                        | `weather.lua`         | [location]                                                    | If no arguments are given, the weather forecast for your known location is given. If a location is given, then the weather forecast for that location is given instead.                                                                                                                                                                                       | -               |
| /whitelist                      | `administration.lua`  | [user]                                                        | Allows a previously-blacklisted user to use the bot in the chat again. The user must be specified by username/ID, or by reply.                                                                                                                                                                                                                                | -               |
| /whois                          | `whois.lua`           | \<IP address\>                                                | Performs a WHOIS lookup for the given IP address and returns the result.                                                                                                                                                                                                                                                                                      | -               |
| /wikipedia                      | `wikipedia.lua`       | \<query\>                                                     | Searches Wikipedia for the given search query and returns the most relevant article.                                                                                                                                                                                                                                                                          | /wiki, /w       |
| /xkcd                           | `xkcd.lua`            | [n | query]                                                   | Returns the latest xkcd strip and its alt text. If a number is given, returns that number strip. If 'r' is passed in place of a number, returns a random strip. Any other text passed as the command argument will search Google for a relevant strip and, if applicable, return it.                                                                          | -               |
| /yify                           | `yify.lua`            | \<query\>                                                     | Searches Yify Torrents for the given search query and returns the most relevant result(s).                                                                                                                                                                                                                                                                    | -               |
| /yomama                         | `yomama.lua`          | -                                                             | Tells a Yo' Mama joke!                                                                                                                                                                                                                                                                                                                                        | -               |
| /youtube                        | `youtube.lua`         | \<query\>                                                     | Searches YouTube for the given search query and returns the most relevant result(s).                                                                                                                                                                                                                                                                          | /yt             |

Arguments enclosed in [square brackets] are optional, and arguments enclosed in <angle brackets> are required.

## Telegram API

Below you will find each currently-documented method and its corresponding function and information.

### sendMessage

Use this function to send text messages using Telegram's `sendMessage` method.

```Lua
mattata.send_message(
    chat_id,
    text,
    parse_mode,
    disable_web_page_preview,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters                  | Type                                                                             | Required | Description                                                                                                                                                                    |
|-----------------------------|----------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id                    | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                       |
| text                        | String                                                                           | Yes      | Text of the message to be sent                                                                                                                                                 |
| parse\_mode                 | String                                                                           | Optional | Send `Markdown` or `HTML`, if you want Telegram apps to show bold, italic, fixed-width text or inline URLs in your bot's message.                                              |
| disable\_web\_page\_preview | Boolean                                                                          | Optional | Disables link previews for links in this message                                                                                                                               |
| disable\_notification       | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                |
| reply\_to\_message\_id      | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                          |
| reply\_markup               | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user. |

### forwardMessage

Use this function to forward messages of any kind using Telegram's `forwardMessage` method.

```Lua
mattata.forward_message(
    chat_id,
    from_chat_id,
    disable_notification,
    message_id
)
```

| Parameters            | Type              | Required | Description                                                                                                                     |
|-----------------------|-------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| chat\_id              | Integer or String | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                        |
| from\_chat\_id        | Integer or String | Yes      | Unique identifier for the chat where the original message was sent (or channel username in the format @channelusername)         |
| disable\_notification | Boolean           | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound. |
| message\_id           | Integer           | Yes      | Message identifier in the chat specified in *from\_chat\_id*                                                                    |

### sendPhoto

Use this function to send photos using Telegram's `sendPhoto` method.

```Lua
mattata.send_photo(
    chat_id,
    photo,
    caption,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters             | Type                                                                             | Required | Description                                                                                                                                                                                                                              |
|------------------------|----------------------------------------------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id               | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                                                                                 |
| photo                  | InputFile or String                                                              | Yes      | Photo to send. Pass a file\_id as String to send a photo that exists on the Telegram servers (recommended), pass an HTTP URL as a String for Telegram to get a photo from the Internet, or upload a new photo using multipart/form-data. |
| caption                | String                                                                           | Optional | Photo caption (may also be used when resending photos by *file\_id*), 0-200 characters                                                                                                                                                   |
| disable\_notification  | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                                                                          |
| reply\_to\_message\_id | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                                                                                    |
| reply\_markup          | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.                                                           |

### sendAudio

Use this function to send audio files using Telegram's `sendAudio` method, if you want Telegram clients to display them in the music player. Your audio must be in the `.mp3` format. Bots can currently send audio files of up to 50 MB in size, this limit may be changed in the future.

```Lua
mattata.send_audio(
    chat_id,
    audio,
    caption,
    duration,
    performer,
    title,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters             | Type                                                                             | Required | Description                                                                                                                                                                                                                                             |
|------------------------|----------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id               | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                                                                                                |
| audio                  | InputFile or String                                                              | Yes      | Audio file to send. Pass a file\_id as String to send an audio file that exists on the Telegram servers (recommended), pass an HTTP URL as a String for Telegram to get an audio file from the Internet, or upload a new one using multipart/form-data. |
| caption                | String                                                                           | Optional | Audio caption, 0-200 characters                                                                                                                                                                                                                         |
| duration               | Integer                                                                          | Optional | Duration of the audio in seconds                                                                                                                                                                                                                        |
| performer              | String                                                                           | Optional | Performer                                                                                                                                                                                                                                               |
| title                  | String                                                                           | Optional | Track name                                                                                                                                                                                                                                              |
| disable\_notification  | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                                                                                         |
| reply\_to\_message\_id | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                                                                                                   |
| reply\_markup          | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.                                                                          |                                                                        |

### sendDocument

Use this function to send general files using Telegram's `sendDocument` method. Bots can currently send files of any type of up to 50 MB in size, this limit may be changed in the future.

```Lua
mattata.send_document(
    chat_id,
    document,
    caption,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters             | Type                                                                             | Required | Description                                                                                                                                                                                                                         |
|------------------------|----------------------------------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id               | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                                                                            |
| document               | InputFile or String                                                              | Yes      | File to send. Pass a file\_id as String to send a file that exists on the Telegram servers (recommended), pass an HTTP URL as a String for Telegram to get a file from the Internet, or upload a new one using multipart/form-data. |
| caption                | String                                                                           | Optional | Document caption (may also be used when resending documents by *file\_id*), 0-200 characters                                                                                                                                        |
| disable\_notification  | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                                                                     |
| reply\_to\_message\_id | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                                                                               |
| reply\_markup          | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.                                                      |

### sendSticker

Use this function to send `.webp` stickers using Telegram's `sendSticker` method.

```Lua
mattata.send_sticker(
    chat_id,
    sticker,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters             | Type                                                                             | Required | Description                                                                                                                                                                                                                                    |
|------------------------|----------------------------------------------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id               | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                                                                                       |
| sticker                | InputFile or String                                                              | Yes      | Sticker to send. Pass a file\_id as String to send a file that exists on the Telegram servers (recommended), pass an HTTP URL as a String for Telegram to get a `.webp` file from the Internet, or upload a new one using multipart/form-data. |
| disable\_notification  | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                                                                                |
| reply\_to\_message\_id | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                                                                                          |
| reply\_markup          | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.                                                                 |

### sendVideo

Use this function to send video files using Telegram's `sendVideo` method. Telegram clients support `.mp4` videos (other formats may be sent using `sendDocument`). Bots can currently send video files of up to 50 MB in size, this limit may be changed in the future.

```Lua
mattata.send_video(
    chat_id,
    video,
    duration,
    width,
    height,
    caption,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters             | Type                                                                             | Required | Description                                                                                                                                                                                                                              |
|------------------------|----------------------------------------------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id               | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                                                                                 |
| video                  | InputFile or String                                                              | Yes      | Video to send. Pass a file\_id as String to send a video that exists on the Telegram servers (recommended), pass an HTTP URL as a String for Telegram to get a video from the Internet, or upload a new video using multipart/form-data. |
| duration               | Integer                                                                          | Optional | Duration of sent video in seconds                                                                                                                                                                                                        |
| width                  | Integer                                                                          | Optional | Video width                                                                                                                                                                                                                              |
| height                 | Integer                                                                          | Optional | Video height                                                                                                                                                                                                                             |
| caption                | String                                                                           | Optional | Video caption (may also be used when resending videos by *file\_id*), 0-200 characters                                                                                                                                                   |
| disable\_notification  | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                                                                          |
| reply\_to\_message\_id | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                                                                                    |
| reply\_markup          | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.                                                           |

### sendVoice

Use this function to send audio files using Telegram's `sendVoice` method, if you want Telegram clients to display the file as a playable voice message. For this to work, your audio must be in an `.ogg` file encoded with `OPUS` (other formats may be sent as Audio or Document). Bots can currently send voice messages of up to 50 MB in size, this limit may be changed in the future.

```Lua
mattata.send_voice(
    chat_id,
    voice,
    caption,
    duration,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters             | Type                                                                             | Required | Description                                                                                                                                                                                                                               |
|------------------------|----------------------------------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id               | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                                                                                  |
| voice                  | InputFile or String                                                              | Yes      | Audio file to send. Pass a file\_id as String to send a file that exists on the Telegram servers (recommended), pass an HTTP URL as a String for Telegram to get a file from the Internet, or upload a new one using multipart/form-data. |
| caption                | String                                                                           | Optional | Voice message caption, 0-200 characters                                                                                                                                                                                                   |
| duration               | Integer                                                                          | Optional | Duration of the voice message in seconds                                                                                                                                                                                                  |
| disable\_notification  | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                                                                           |
| reply\_to\_message\_id | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                                                                                     |
| reply\_markup          | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.                                                            |

### sendLocation

Use this function to send a location on a map using Telegram's `sendLocation` method.

```Lua
mattata.send_location(
    chat_id,
    latitude,
    longitude,
    disable_notification,
    reply_to_message_id,
    reply_markup
)
```

| Parameters             | Type                                                                             | Required | Description                                                                                                                                                                    |
|------------------------|----------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chat\_id               | Integer or String                                                                | Yes      | Unique identifier for the target chat or username of the target channel (in the format @channelusername)                                                                       |
| latitude               | Float number                                                                     | Yes      | Latitude of location                                                                                                                                                           |
| longitude              | Float number                                                                     | Yes      | Longitude of location                                                                                                                                                          |
| disable\_notification  | Boolean                                                                          | Optional | Sends the message silently. iOS users will not receive a notification, Android users will receive a notification with no sound.                                                |
| reply\_to\_message\_id | Integer                                                                          | Optional | If the message is a reply, ID of the original message                                                                                                                          |
| reply\_markup          | InlineKeyboardMarkup or ReplyKeyboardMarkup or ReplyKeyboardRemove or ForceReply | Optional | Additional interface options. A JSON-serialized object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user. |

## External Usage

You can use the mattata API without initialising the entire library (i.e. no plugin system etc.) by referencing the library in your code. This can be done in the following way:

```Lua
local mattata = require('mattata')
-- Blah, blah; your code goes here
```

Now, if you wish to make a request to the Telegram API, you need to use the `mattata.request()` function; which takes 4 parameters. Below is a table containing each parameter, the type of value it takes and a brief description of what it's for.

| Parameters | Type                | Required | Description                                                                                                                                                                                                               |
|------------|---------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| endpoint   | String              | Yes      | The API URL (with the token and method) which you'd like to make the request to (e.g. `https://api.telegram.org/bot123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11/sendMessage`)                                                |
| parameters | Table               | Yes      | A key-value table of parameters and their respective values (if you're using the official Telegram bot API, check out the documented examples above)                                                                      |
| file       | InputFile or String | Optional | A table of a single key/value pair, where the key is the name of the parameter and the value is the filename (if these are included in parameters instead, mattata will attempt to send the filename as a file ID or URL) |
| timeout    | Boolean             | Optional | If set to true, the request will timeout after 1 second                                                                                                                                                                   |

Here's an example script which, when executed, will send the message `Hello, World!` to the chat ID `-100123456789` using the `sendMessage` method via the default API endpoint, `https://api.telegram.org/bot`, using the token `123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11`:

```Lua
local mattata = require('mattata') -- Load the library

local request, code =  mattata.request( -- Make the request to the Telegram bot API
    'https://api.telegram.org/bot123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11/sendMessage',
    {
        ['chat_id'] = -100123456789,
        ['text'] = 'Hello, World!'
    }
)

if not request then
    print('The Telegram bot API returned the following error: ' .. code)
    return false
end

return true
```

It is easier to make requests if you're using mattata for its intended purpose (a plugin-based bot), however it really is that easy to make a request to the bot API - in any snippet of Lua!

Here's an example bot which uses long-polling to get updates, and responds to `/ping` with `PONG`:

```Lua
api = require('mattata')
token = '' -- Enter your token here
last = last or 0
while true do
    local request = api.get_updates(
        5,
        last + 1,
        token
    )
    if request then
        for _, update in ipairs(request.result) do
            last = update.update_id
            if update.message and update.message.text and update.message.text == '/ping' then
                api.request(
                    string.format(
                        'https://api.telegram.org/bot%s/sendMessage',
                        token
                    ),
                    {
                        ['chat_id'] = update.message.chat.id,
                        ['text'] = 'PONG'
                    }
                )
            end
        end
    else
        print('Error')
    end
end
```

## Contribute

As well as feedback and suggestions, you can contribute to the mattata project in the form of a monetary donation. This makes the biggest impact since it helps pay for things such as server hosting and domain registration. A donation of any sum is appreciated and, if you so wish, you can donate [here](https://paypal.me/wrxck).

I'd like to take a moment to thank the following people for their donation:

* j0shu4
* para949
* aRandomStranger
* mochicon
* xenial
* fizdog
* caidens
