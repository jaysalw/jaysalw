---
title: Down with Streaming!
date: 2026-02-20
summary: A view on my hatred for streaming companies - and how to fix it!
tags: music
---

![Banner](https://raw.githubusercontent.com/jaysalw/jaysalw/refs/heads/main/blog-assets/2026/down_with_spotify.png)

Earlier today, along with creating the **music page** on my website (and a styling update!!) I decided to add the above banner showcasing how terrible streaming services are. Bit graphic with the dripping blood maybe? Oh well...

For years now I have preferred self-hosting my media collection however I could. For example, my music server is currently hosted on a Raspberry Pi 5, though you can use whatever you like with a media server!

Some media servers are more lightweight than others, however I personally use Jellyfin.

## So, what's the issue with streaming?

**You don't own your media**. If the platform decides to remove it, censor it, or if your local authority doesn't like your music tastes (looking at you trump) then it has effectively gone forever (almost).

Issues with Streaming Services such licenses expiring so that they can't play that music anymore, or content gets replaced. AI slop covering up the decent music and real artists too.

Albums vanish overnight, tracks get silently swapped - your library isn't really yours, only rented.

Adding onto the topic of **owning nothing**, streaming services use the cloud. If their platform goes down, so does your music. Let's take into account how Google Play Music shut down and people lost their whole libraries. If you forgot to move your music to YouTube Music within a specific period of time then all your purchases went "poof".

You also have to pay for **offline independence**. You can't control metadata, and you of course have no file access. So that brings us to the solutions!

## Solutions to the Streaming BS

There are many ***open-source*** (and free!) software out there for streaming media (not just music).

* Jellyfin (I use this one.) https://jellyfin.org - Easy to set up. You can just use docker! Allows for video, books, photos and more importantly ***MUSIC!!***
* Subsonic https://subsonic.org
* mStream https://mstream.io/ - Music only

Personally I have gone with Jellyfin. Not just because of the user-friendly UI/UX, but for syncing my tunes with last.fm (or musicbrainz if you prefer that). So for setting up a media server I will show you Jellyfin.

### Small note about the world of Self-hosting
Self Hosting requires a computer, of course, so when it comes to picking your poison it is recommended to look into hardware too. You can find cheap old mini computers such as the Lenovo ThinkCentre Mini, or even use a Raspberry Pi 3+.

It all depends on what you want to run! If you're looking for music only, a raspberry pi (with at least 4-8GB of ram) will do perfectly!

I am running my media server on a Raspberry Pi 5 with 16GB of ram, along with 512GB of NVMe SSD Storage. (Look into the Argon Fourty Neo 5 case - comes with passive cooling and a NVMe M.2 slot: https://thepihut.com/products/argon-neo-5-m-2-nvme-case-for-raspberry-pi-5 and https://thepihut.com/products/raspberry-pi-5?variant=42531604955331)

The project as a whole is overall cheaper than using spotify for one year alone (at £11.99/mo).

Oh and, if you're planning on ripping CDs, make sure you have a CD player which can connect to your computer.

***FYI***, A Raspberry Pi 5 with 16gb of ram will cost around £1-1.50 in electricity per month at FULL LOAD (which you shouldn't reach if you limit to a few users - around 20?).

### Installing Jellyfin

There are many ways to install jellyfin, such as installing the **Binary** (which is the bare application), however for this guide we will be using Docker. Once you have flashed an OS such as Debian or Raspberry Pi OS (Lite NO gui!!), then we can get started.

Run these commands to update your OS:
```
sudo apt-get update && sudo apt-get upgrade
```
By running these two commands in ONE terminal line with &&, you tell the terminal to execute one and then the other.

You'll need to install two packages once this has been completed:

```
sudo apt-get install docker docker-compose
```

This will install docker so that we can get jellyfin up and running! There are **TWO** ways to get docker up and running:

Then follow this guide to get Jellyfin setup using docker: https://jellyfin.org/docs/general/installation/container/ (this will show the latest version of jellyfin.)

**REMEMBER** If you want to use your media server outside your home network NEVER port-forward (this can cause lots of issues down the road) - instead use cloudflare tunnels. See https://www.youtube.com/watch?v=R2yERDD77jg

Once you have installed jellyfin installed see https://jellyfin.org/docs/general/post-install/setup-wizard - This will guide you through setting up your server. Make sure to connect to cloudflare tunnels if you want to access your server outside your network!

Simply add your music to the selected mount point (folder) which will show up in ``/opt/Jellyfin/data/``.

## My Setup

![My Small CD Collection](https://raw.githubusercontent.com/jaysalw/jaysalw/refs/heads/main/blog-assets/2026/my_cds_feb.jpg)

I know I don't have tons of CDs in the image above (many of them are stacked on my table), however I have ripped each one in WAV or FLAC (the best formats for music) and plopped them onto Jellyfin.

![My Jellyfin Setup](https://raw.githubusercontent.com/jaysalw/jaysalw/refs/heads/main/blog-assets/2026/jellyfin_preview.jpg)

Here is a picture of my jellyfin server. I use **finamp** (https://github.com/UnicornsOnLSD/finamp) on my phone, and I use a custom theme on the webclient. I use the client **feishin** on my desktop (looks similar to spotify) (https://github.com/jeffvli/feishin)

There are loads of clients for Jellyfin so take your pick!

If you can't find a song, or a track in CD format try looking on https://discogs.com, ebay or head to Bandcamp and pay for a digital download of that track.

Still no luck? Try piracy! (shhhh 🦜)

On a day-to-day basis, I personally enjoy **no advertisements** from companies I couldn't care less about, and I support the artists which I enjoy buy directly purchasing content rather than listening to them from crappy streaming services.

Allthough Jellyfin behaves like any commercial streaming service, you are in control and **you** decide what goes on it. Not only that **you own your music**!

It doesn't matter if Jellyfin disappears, if an API shuts down or if some company decides to remove a bunch of albums or access. 

My music is mine. forever.

Streaming services may have solved convinence, but at the cost of ownership and what it should actually feel like to choose, select and listen to music. Listening to music should NOT be an endeless activity, but something to enjoy.

Self-hosting solves both issues of portability, and ownership of music. No more subscriptions, no more media going poof, no restrictions.