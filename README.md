# Time is Money

**Spend Your Time Wisely**

A pixel platformer where the clock is also your wallet. Complete the level before your time runs out! But to reach the flag, you must spend time in the shop.

And I do not mean that figuratively.

> Do you risk using your time to buy a power up? And what upgrades do you really need?

Made for the **IIT Hyd Milan Game Jam 2026**.

**[Play it on itch.io](https://sumanto.itch.io/time-is-money)**

---

## How it works

- **Time is your health, your money and your score.** It is one number, and everything costs it.
- **Apples add 8 seconds.** Spikes and saws take 10.
- **Spend seconds in the shop** on upgrades that change how a level plays.
- **Changed your mind?** Hold Shift and select a one-shot upgrade to sell it back for a partial refund.
- **Careful when you are low.** Below 20 seconds the shop prices go up. This is scarcity pricing in action.

## Game modes

- **Continuous:** all ten levels back to back on one shared clock. Run out of time and you start again from the first level. Beat it and you see your total time left, plus how long every level took you.
- **Level Select:** pick any single level and play just that one. Fail it and you can retry straight away. Clear it and you see the time you had left.

## Controls

| Key | Action |
|---|---|
| A / D or Left / Right | Move |
| W / Up / Space | Jump |
| S / Down | Ground pound (once bought) |
| Shift | Dash (once bought) |
| 1 to 7 or click | Buy from the shop (hold Shift to sell) |

## The shop

| Upgrade | Cost | What it does |
|---|---|---|
| Double Jump | 15s | A second jump in mid-air |
| Dash | 5s | A short burst of horizontal speed |
| Platform | 5s | Place a platform during a level |
| Trampoline | 8s | Place a trampoline, about 1.5x jump height |
| Wall Jump | 12s | Kick away from climbable walls |
| Ground Pound | 8s | Slam down and smash brick blocks |
| Apple Magnet | 12s | Pulls apples in from about six tiles away |

## Running it locally

The whole game is a single `index.html` plus an `assets/` folder, with no build step.

You need to serve it over HTTP, because browsers block loading the game's sounds and images when you just double-click the file.

```bash
# from the project folder
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

You also need an internet connection, since the game loads Kaplay and the font from CDNs.

## Tweaking it

Everything lives in `index.html`:

- **Level timers:** `LEVEL_TIMERS` sets how many seconds each level starts with.
- **Continuous mode time:** `CONTINUOUS_TIME_REDUCTION` is subtracted from the sum of all the level timers to get the shared clock.
- **Moving platforms and saws:** `MOVER_CONFIG` sets the range, speed and direction of each one, keyed by its row and column in the level map.
- **Levels:** the maps are written as grids of characters in the `LEVELS` array, so you can edit or add levels as text.

## Credits

- Made by Some Anto
- Built with [Kaplay](https://kaplayjs.com)
- Font: Press Start 2P (Google Fonts)
- Assets: [Pixel Adventures by Pixel Frog](https://pixelfrog-assets.itch.io/pixel-adventure-1)
- Music: [8-bit Driftveil City Remix by Bulby](https://www.youtube.com/watch?v=AzRe1PRG-k8)
- Sound effects: [Pixabay](https://pixabay.com/sound-effects/search/8%20bit/)
- Made for the [IIT Hyd Milan Game Jam 2026](https://itch.io/jam/glitch-milan-game-jam-26)

## License

The art, music and sound effects above belong to their creators and keep their own licenses.
