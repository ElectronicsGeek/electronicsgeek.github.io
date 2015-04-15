---
layout: post
title: Quick Hack&#58; Spotify on Ubuntu 14.04
---

**NOTE:** Whilst this article specifically targets Ubuntu, I reckon you would probably have success on other distros, too. Keep me posted in the comments.

I recently installed Ubuntu on my laptop and I'm very pleased with it, so pleased, in fact, I haven't booted into windows for a good few weeks. I did however run into one small problem when setting up - Spotify was not installed.

Having used and been thoroughly disappointed by the Spotify Linux client (which Spotify themselves admit is "experimental") in the past, I decided I needed to access Spotify in an alternative way.

### You Will Need:

- Google Chrome

The Spotify web client was the way forward! To access the web client, obviously one must use a web browser.

If you close all instances of Chrome and type this into your terminal, you should notice that a Chrome window opens, albeit with no tabs and controls. This is perfect, because it "feels" more like a standalone application.

   google-chrome --app=https://play.spotify.com 

Easy :)

Now, we need to turn this into an actual "application" to run in the Unity launcher. Thankfully, this is also easy. Open a terminal and type:

    cd /usr/share/Applications
    
Then type:

    sudo nano spotify.desktop
    
It is *very important* that you type **"sudo"**    

    [Desktop Entry]
    Version=1.0
    Type=Application
    Name=Spotify
    GenericName=Web Music Streamer
    Comment=Listen to music using Spotify
    Icon=spotify
    categories=Audio;Player

    Exec=google-chrome --app=https://play.spotify.com

    Terminal=false

Once that's done, press "Ctrl + X" and hit "Y"

Now type "Spotify" into the searchbar and if all has gone to plan, it should be there. Click on it and a Spotify Chrome window should open.

You might even want to add it to your quick launch applications on the main Unity bar, as I have done.
