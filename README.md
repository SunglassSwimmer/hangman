# Hangman

A game of words, peasants & suspicious cows.

Pick a secret word, turn it into a link, and text it to a friend. While they guess,
Sergeant Klaus, Gerard, Margot and Pip heckle from the crowd, curious cows wander up to the gallows,
a growing audience of villagers and animals gathers with every wrong guess,
and Olivia the snail tries to get across the grass without being snatched by Gary the eagle.

## Playing

Open `index.html` in any web browser, or play the online version (see the link on this
project's GitHub page once GitHub Pages is turned on).

## Where things are

Everything lives in one file: `index.html`.

- **Look and colors**: the `<style>` section at the top
- **Drawings** (gallows, blob, crowd, bird, sun, Olivia, Gary): the `<svg>` inside the game screen
- **What the characters say**: `CAST`, `SNATCH_LINES` and `RETURN_LINES` in the `<script>` section
- **Spectators** (who shows up, where they stand, what they say): `SPECTATORS` and `SPECTATOR_SLOTS`
- **Sound effects**: `SFX` (all made with the browser's synthesizer, no sound files)
- **Crowd reactions** to letters, streaks and chats: `LETTER_LINES`, `STREAK_LINES`, `CHATS`
- **Rare rescues** and how often they happen: `RESCUES`, `RESCUE_CHANCE`
- **Endings**: `winEnding`, `loseEnding`; **bribing Klaus**: `canBribe`
- **Difficulty modes** (and what gets drawn on each wrong guess): `MODES`
- **Characters** (who's on the rope, and how the crowd teases them): `CHARACTERS`, plus the
  `char-...` groups in the drawing
- **Dress-up options** (faces, extras, shirt colors): `FACES`, `EXTRAS`, `SHIRTS`, plus the
  `face-...` and `opt-...` groups in the drawing
- **Random words**: `SOLO_WORDS`. Words in Big Kid Words have a picture, a clue, a kid-friendly
  meaning and a sentence; Prison Mode words have a crossword-style clue, a definition and an origin.
- **Kind crowd lines for kids**: `KIND_LINES`, `KID_GREETINGS`, `KID_ENTRANCE`
- **Big Kid Words balloons and mud**: one balloon pops per wrong guess and the puddle grows (`updateBalloons`,
  `BALLOON_SPOTS`); losing is a SPLOOSH into the mud (`kidLoseEnding`), winning sends the balloons
  floating away (`releaseBalloons`)
- **Gags**: the pooping cow (Big Kid Words) is `cowPoop`; the princess who charms the swing with flowers
  (Big Kid Words) is `princessVisit` and `charmSwing`; Pip throwing a frisbee for Biscuit the dog (Big Kid Words)
  is `frisbeeFetch`; Sir Reginald tripping over the gallows is `reginaldVisit` (and his rare success is `reginaldRescue`);
  Klaus's performance review and Olivia's promotions are `reviewVisit` and `applyRank`; Pierre the drunk is `drunkVisit`;  the bird's stunts (balloon, beret, baguette, Klaus's spike) are `birdMischief`; Pierre's wife is
  `wifeFetchesPierre`; Olivia making Gary crash is `updateMiss`; the late executioner is `executionerVisit`;
  the wave is `doWave`; the ice cream truck is `iceCreamTruck`; the rain shower is `rainShower`;
  Henri the painter is `painterVisit`; the acorn-throwing squirrel is `squirrelVisit`;
  Brigitte napping (and Pierre fetching her) is `pierreFetchesBrigitte`; the flying saucer is `ufoVisit`;
  the golden cow is in `addSpectator`; Klaus getting zapped is in `loseEnding`

## Things that keep you coming back

All of this lives in the "The story so far" section of the `<script>`, and is remembered in each
player's own browser.

- **Daily puzzle** (three words a day, the same for everyone, with a winning streak): `dailyEntry`,
  `startDaily`, `recordDaily`, `renderDaily`. Daily #1 is October 28, 2026 (`DAILY_START`).
- **Sticker book** (every gag is a sticker; rare ones glow gold): `STICKERS`, `discover`. Gags you
  haven't seen yet turn up a bit more often: `odds`.
- **Unlockable extras** (Viking helmet, Wizard hat, Hero mask, unlocked by winning): `UNLOCKS`
- **Rivalries** (your history with each friend, and their best taunt): `logRival`, `renderRivals`
- **A world that remembers** (`world`, `applyWorld`, `pickCallback`): Klaus wears a bandage for a few
  games after the squirrel, the bird keeps its trophies in its nest (and Gerard and Pip get a new beret
  and balloon), a sign keeps score between Gary and Olivia, Henri's paintings hang in a gallery on the
  home screen, Klaus gets his umbrella fixed, the executioner's excuses get worse, and the crowd brings
  up what happened last time.
- **Quick mode** (the ⏩ button skips the cart entrance): `quickMode`

## Working on it together

We use GitHub Desktop to share changes.

1. **Before you start**: click **Fetch origin**, then **Pull origin**, to get your friend's latest changes.
2. **Make your changes** (for example, by asking Claude).
3. **When you're done**: in GitHub Desktop, write a short summary of what you changed
   (like "Gary now wears sunglasses"), click **Commit to main**, then **Push origin**.

Take turns if you can. If you both change the same part at the same time, GitHub Desktop
will ask you to pick which version to keep.
