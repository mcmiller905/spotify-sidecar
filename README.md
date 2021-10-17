# spotify-sidecar

This repo contains the code for a node.js web app that connects to Spotify and displays the currently playing song.
It was designed for a Raspberry Pi Zero W and an Adafruit 2.8 inch screen

This project started with Spotify's tutorial for authentication, and then I tweaked it to focus on playback information.

The screen displays:
- The song name
- The artist name
- The album art
- The album name

It also has 4 buttons:
- Play/Pause
- Previous song
- Next song
- Save song (to specified playlist)

User info is contained in a config.js file. You need a client_id, client_secret, and a redirect_uri, all of which are created when you register your app in Spotify. You also will need the playlist_id of the playlist you want to save your songs to.
**Note:** You'll need to copy the *config-template.js* file and rename it *config.js* and fill it with the needed info

If you notice two syntax errors in *index.html*, it's due to using Handlebars syntax in a style tag. The compiler doesn't like {{token}} annotation in css, but it gets compiled away when token replacement happens.