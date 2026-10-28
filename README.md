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
- **Kind crowd lines for little kids**: `KIND_LINES`, `KID_GREETINGS`, `KID_ENTRANCE`
- **Gags**: the pooping cow (Big Kid Words) is `cowPoop`; Pierre the drunk is `drunkVisit`; Bernard the streaker is `streak`;
  the bird's stunts (balloon, beret, baguette, Klaus's spike) are `birdMischief`; Pierre's wife is
  `wifeFetchesPierre`; Olivia making Gary crash is `updateMiss`; the late executioner is `executionerVisit`;
  the wave is `doWave`; the ice cream truck is `iceCreamTruck`; the rain shower is `rainShower`

## Working on it together

We use GitHub Desktop to share changes.

1. **Before you start**: click **Fetch origin**, then **Pull origin**, to get your friend's latest changes.
2. **Make your changes** (for example, by asking Claude).
3. **When you're done**: in GitHub Desktop, write a short summary of what you changed
   (like "Gary now wears sunglasses"), click **Commit to main**, then **Push origin**.

Take turns if you can. If you both change the same part at the same time, GitHub Desktop
will ask you to pick which version to keep.
