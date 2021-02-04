### fedi-spotify
A simple (kinda) way to post what you are listening to on Twitter and Mastodon

**Setup**
Visit https://zapier.com/apps/spotify/integrations/twitter and configure these however. You'll want to create a **dedicated** account for the music posting.

Make note of the username, then clone this repository and init setup:
```
git clone https://github.com/qd-w/fedi-spotify
cd fedi-spotify
npm install
nano spotify.edn
```
Fill in the tokens for Spotify and Mastodon. You'll need to create them first, then you can finish the next steps.
```
shadow-cljs compile spotify
shadow-cljs release app
chmod a+x mastodon-bot.js
```

You are ready! Now, run the script...

```
node mastodon-bot.js
```

Your account will now post however you configured it in Zapier.
