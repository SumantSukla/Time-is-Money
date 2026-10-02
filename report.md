# Report

## 1. Game concept, core loop and intended experience

**Time is Money** is a 2D browser platformer built with Kaplay (JavaScript). You play a Ninja Frog and have to reach the flag at the end of each level before the countdown hits zero. There are 10 playable levels (shown on screen as 0 to 9), from "The Meadow Walk" to "Possible Impossible".

The one idea the whole game runs on: **the timer is also your money.**

- Collecting apples gives you time (+8s).
- Spikes and saws take time away (-10s) and knock you back.
- During a level, you can buy upgrades by using your time as currency: Double Jump (15s), Dash (5s), Platform (5s), Trampoline (8s), Wall Jump (12s), Ground Pound (8s) and Apple Magnet (12s). Most can be sold back for a partial refund.
- When time is low (under 20s), prices go up by as much as 80%.

So the player has to make decisions on whether it's worth it to sacrifice their time on power ups and on what powers they should spend their time on

**Core loop:** look at the level, decide which upgrades are worth their seconds, run and jump through the traps, grab apples to refill the clock, reach the flag. Whatever time is left is your result.

**Modes**

- **Continuous:** all levels back to back on one shared clock. Dying sends you back to the first level. The victory screen shows total time left and the time taken in each level.
- **Level Select:** pick one level and play only that. If you die you retry the same level. Clearing it shows a victory screen with the time left for that level.

**Intended experience:** quick and tense. Every purchase and every mistake has a visible price in seconds, so players keep making small risk/reward calls, and the short levels make it easy to retry and play faster.

## 2. How the game uses the theme

The game takes "time" literally and makes it the currency, the health bar and the score at once. Spending time on a power-up is a trade-off against having less time to finish the level.

## 3. Key design decisions

After the theme came out, I asked around in my friend circle for some ideas, and in the end I settled on this one because it seemed the easiest to implement and is also pretty on-theme.

I used a JavaScript engine because that's what I'm familiar with - most of my previous (smaller-scale) games were made using JavaScript. I plan to learn Unity or Godot very soon, but I decided I won't be able to learn a new game engine and make a game during this 3 day window of the game jam.

I settled on a platformer, because I like platformers, and I hadn't made one yet. I searched around on itch for assets packs, and used that as a reference for how my game would look like.

Initially the plan was to make a more traditional platformer game, with victory screens at the end of each level, slow paced, etc. But during development, I had the game switch levels immediately after completion as I was too lazy to make the end screen. Eventually I decided to keept it as it gave a more fast-paced and speedrunny vibe, which I liked. I added a seperate level selector mode for players who may not like that.

My friend suggested the background music. I initially didn't want to use any well-known music, but my friends liked it, and it is a bop, so I kept it.

## 4. Cut, simplified or incomplete

- Wasn't able to add enemies
- Could have made more puzzle like levels instead of skill-based levels
- Could have added more unique power ups
- Level design could have been tuned better. Some players found them hard, others easy.
- Did not add high scores, etc
- Could not add particle affects to run/jump/pound.

## 5. Who worked on what

Team -> Me, myself and I.
I did all the game designing and programming, using 3rd party assets.

## 6. Resources and references

**Engine and libraries**

- Kaplay `3001.0.0-alpha.20` (open source JavaScript game library), loaded from unpkg.
- Google Fonts: Press Start 2P (UI font).

**Art and Audio**

Assets were taken from (itch.io)[https://pixelfrog-assets.itch.io/pixel-adventure-1]

Music was taken from Driftveil City 8-bit Remix (YouTube)[https://www.youtube.com/watch?v=AzRe1PRG-k8]

And other sound effects were taken from (Pixabay)[https://pixabay.com/sound-effects/search/8%20bit/]

Used a few Canva assets

**References**

- I used this (itch.io)[https://pixelfrog-assets.itch.io/pixel-adventure-1] page as a reference to how my platformer would look and feel.
- Changed speed and jump height to my own liking
