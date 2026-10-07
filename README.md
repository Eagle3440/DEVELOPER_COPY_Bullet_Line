# Bullet Line: Scripture Pursuit (KJV)

**Bullet Line: Scripture Pursuit** is an engaging, high-speed King James Version (KJV) Bible trivia game built as a self-contained web application. Test your knowledge of the Old and New Testaments, build your silver treasury, and outrace the rival Train X!

---

## 🚀 Core Features

* **KJV Scripture Integration:** Every trivia question is paired with a direct King James Bible reference and scripture quote to deepen your study and understanding of the Word.
* **The Shekel Builder Round:** A fast-paced 60-second opening round where consecutive correct answers pay a rising combo ladder -- 1,000 -> 1,250 -> 1,500 -> 1,750 -> 2,000 Shekels of Silver. Five in a row banks 1 AUTO STALL + 1 AUTO ADVANCE and restarts the ladder; a miss resets it to 1,000.
* **Choose Your Opponent:** After START GAME, pick your rival's smarts -- **Scribe** (68% accuracy, x1 win bonus), **Scholar** (76% accuracy, x1.25 win bonus), or **Prophet** (84% accuracy, x1.5 win bonus). Sharper mind, richer win. Your choice is remembered between visits.
* **Head-to-Head Race Mechanics:** A 7-step sprint against the rival Train X -- you board at Step 5, 6, or 7 depending on the line you choose, and the first to reach the station (Step 0) wins. Correct answers advance your Bullet Line; Train X advances on its own hidden accuracy roll each round.
* **Hazard Events:** Up to one Bible-themed track hazard per race (round 4 or later, never in sudden death) -- Bridge Out, the Red Sea, Daniel's Lions, the Fiery Furnace, and 10 more, drawn from a shuffled no-repeat deck. The race question doubles as your dodge test: answer correctly to dodge it, miss and you're knocked back a step.
* **Rivalry Record:** Your lifetime win-loss record against each opponent is tracked and shown as a badge on their card (FIRST MEETING, gold when you're leading, red when trailing) and as a W-L card on every game summary.
* **Learning Library:** Every question you miss is saved as a KJV verse flashcard. Review them from the summary screen -- tap to flip, mark MASTERED to remove, and resize the verse text with the -/+ buttons.
* **The Ticket Store:** Spend your lifetime Total Treasury on five themed question packs -- each unlocking hundreds of additional KJV questions and a matching category-only way to play. See below for details.
* **Procedural Web Audio API Sound Effects:** Sound effects and train ambient audio generated programmatically via JavaScript -- no audio assets required for gameplay. The title-screen weather music is embedded in the page.
* **The Jerusalem Herald News Ticker:** A two-line LED marquee on the title screen delivers scrolling live weather from the Holy Land and a rotating feed of KJV-inspired "breaking news" headlines -- see below for details.
* **Title Videos:** Three cinematic clips play over the title-train picture on a five-minute rotation -- `title-intro.mp4` on page load, then `time-tunnel.mp4`, then `jerusalem-entry.mp4`, looping. Each launch is announced with an amber ticker warning ("WARNING: BULLET LINE DEPARTING ON ANOTHER ADVENTURE") plus a 3-2-1 countdown (desktop only), and the ↻ button replays the intro anytime. See below for details.
* **Responsive & Immersive UI:** Features a custom neon train CSS layout, animated fog background, mobile-optimized scripture viewing drawers, and dynamic game statistics tracking.

---

## 🎮 How to Play

1. **Start the Game:** Click the **START GAME** button on the main screen, then **choose your opponent** -- Scribe, Scholar, or Prophet. Tapping a card starts the race.
2. **The Builder Round:** Answer as many KJV Bible questions as you can within 60 seconds to stack up your starting Shekels of Silver. Streaks pay extra: 5 correct in a row banks 1 AUTO STALL and 1 AUTO ADVANCE together (max 1 each), and the streak resets.
3. **Choose Your Line:** Pick how you enter the race -- each line races for a different share of your bank:
 * **Express Line** -- boards at Step 5, keeps the AUTO ADVANCE (forfeits the AUTO STALL), races for **half** your bank.
 * **Brake Line** -- boards at Step 6, keeps the AUTO STALL (forfeits the AUTO ADVANCE), races for your **full** bank.
 * **Engineer Line** -- boards at Step 7 and races for **triple** your bank -- "Triple or nothing." No builder bonuses.
 
 AUTO STALL is emergency-only and Brake-only: it fires automatically only when Train X is one step from the station and about to take it. AUTO ADVANCE is emergency-only and Express-only: it fires automatically only when Train X is one step from the station and about to take it while you are one step away -- the Express surges to the station, turning defeat into a sudden-death tiebreak. The player is told what happened via an on-screen banner in both cases.
4. **Mystery Ticket Bonus:** each Ticket Store pack purchased secretly banks one random Shekel bonus (1st ticket: 1-20,000, 2nd: 1-30,000, 3rd: 1-40,000, +10k per ticket -- one amount per ticket). Nothing is revealed at purchase. At race start each bonus arms a secret trigger (a random correct-answer number, 1-8); answering that race question correctly fires a gold " TICKET BONUS!" banner (stays 8 seconds) adding the Shekels to the race bank -- win the race to keep it, and the win summary itemizes the bonus so you can see what you got. Unfired bonuses stay armed for future races.
5. **The Race:** Answer questions to advance your Bullet Line to the station (Step 0) before Train X gets there. Train X runs at the accuracy of the opponent you picked (Scribe 68%, Scholar 76%, Prophet 84%, adjusted slightly by question difficulty each round). Watch for ** hazard events** -- at most one per race, never before round 4 and never in sudden death: a hazard card appears with a thunder-rumble warning, and the race question becomes your dodge test. Answer correctly to dodge it (green DODGED flash); miss and the hazard knocks you back one step (red HIT flash). Win the race to bank your Builder total multiplied by your opponent's win bonus (x1 / x1.25 / x1.5). If both trains cross together, a sudden-death question decides it!
6. **End of Race:** When the race ends, the steps collapse one by one (7->1, then the TRAIN STATION bar -- 8 clacks total), then a cinematic plays: `win.mp4` on victory, `lose.mp4` on defeat (a placeholder panel with 3-second auto-continue appears if the video file is missing). After the video, the Game Summary Report slides up over the emptied board.

If you've bought one or more question packs from the Ticket Store (see below), the title screen also offers a **category-only play** option, drawing questions solely from that pack's books of the Bible instead of the full mixed deck.

---

## 🎬 Title Videos

Three cinematic clips play over the title-train picture on the title screen:

* `title-intro.mp4` -- Plays automatically on page load.
* `time-tunnel.mp4` -- A train ride through a time vortex.
* `jerusalem-entry.mp4` -- A lightning train arriving over the city.

They run on a rotation: the intro plays on load, then the title picture returns; five minutes later `time-tunnel.mp4` plays, five minutes after that `jerusalem-entry.mp4` plays, then the loop starts over from the intro. The rotation runs the same on phone and desktop.

* The videos fill the title picture exactly, playing above it but below the treasury HUD, so your Shekels stay visible.
* Video sound follows the sound switch -- the clips stay muted until you turn sound on.
* Before each automatic video (except the first page-load intro), a **3-2-1 countdown** appears in a small circle in the bottom-left corner of the picture -- desktop only, since the phone's bottom-left corner holds the TREASURY marker.
* **Ticker launch warning:** every video launch is announced on the news ticker -- line 1 clears and an amber warning appears, fading in and pulsing like a warning beacon until the video ends: `⚠ WARNING: BULLET LINE DEPARTING ON ANOTHER ADVENTURE ⚠` on desktop, or the shorter `BULLET LINE DEPARTING` on phone. A single two-tone warning alarm sounds once when the warning appears (it follows the sound switch), and the weather music cuts out for the duration of the video, returning on its own afterward. When the video ends, the warning fades out and line 1 goes back to its normal welcome messages. The full launch sequence is: five-minute timer → warning + music cut → 3 seconds → 3-2-1 countdown → video.
* The **↻ replay button** (bottom-right of the picture on desktop, top-right on phone) replays the intro at any time, which also restarts the rotation from the beginning.
* Starting a game stops the rotation; returning to the title screen restarts the five-minute countdown.
* Deployment note: all three `.mp4` files must sit in the same folder as `index.html`. If one is missing, the rotation skips it and moves on to the next.

---

## 💰 Treasury Management System

The game tracks your biblical wealth across three distinct metrics:

**Starting over:** If you clear your browser's data (or localStorage) for this site, everything resets -- treasuries, owned ticket packs, rivalry records, Learning Library cards -- as if you'd never played. There is no account and no backup, so cleared data cannot be recovered.

### **TREASURY** (Current Game Bank)
* **What it is:** The amount of Shekels you've earned in the current game session.
* **When it updates:** Increases per correct answer during the Builder Round on the combo ladder -- 1,000 -> 1,250 -> 1,500 -> 1,750 -> 2,000 Shekels for consecutive correct answers (a miss resets it to 1,000).
* **When it resets:** Resets to 0 Shekels when you start a new game or finish the current one.
* **Display:** Shows at the top-left of the screen during gameplay.

### **TOTAL TREASURY** (Running Tally)
* **What it is:** The cumulative total of all Shekels earned across every won game, ever.
* **When it updates:** Only increases when you **win** a game (reach the Train Station). Your Builder total is multiplied by your chosen opponent's win bonus -- x1 (Scribe), x1.25 (Scholar), or x1.5 (Prophet) -- before it's banked. Losses don't add to this total. It also **decreases** when you spend it on a question pack in the Ticket Store.
* **When it resets:** Never resets automatically -- it's a persistent running tally saved in browser localStorage under the key `totalTreasuryAccount`, and it carries forward across page reloads and browser sessions (and is shared with the Ticket Store -- see below). You can manually clear it only by clearing your browser's localStorage.
* **Display:** Shows at the top-right of the screen during gameplay.
* **Purpose:** Tracks your all-time success across every game you've ever played on this device/browser, and doubles as your spending balance in the Ticket Store.

### **🏆 HIGH SCORE TREASURY** (Persistent Record)
* **What it is:** The single highest TREASURY amount you've ever earned in a game.
* **When it updates:** Automatically updates whenever you complete a game with more Shekels than your previous high score.
* **When it resets:** Never resets automatically--persists forever until you beat it. You can manually clear it only by clearing your browser's localStorage.
* **Storage:** Saved in browser localStorage under the key `treasuryHighScore`.
* **Display:** Shows above the train board during the Race (only during active gameplay, not on the title screen).
* **Purpose:** Gives you a challenge to beat across sessions--a personal record to surpass.

### **Example Scenario**
```
Starting Point (from previous play):
  - HIGH SCORE: 5,000 Shekels
  - TOTAL TREASURY: 12,000 Shekels

Game 1 (Win with 3,000):
  - TREASURY: 3,000 Shekels  game ends, resets to 0
  - TOTAL TREASURY: 15,000 Shekels (12,000 + 3,000, saved to localStorage)
  - HIGH SCORE: Still 5,000 (didn't beat it)

Game 2 (Win with 6,000):
  - TREASURY: 6,000 Shekels  game ends, resets to 0
  - TOTAL TREASURY: 21,000 Shekels (15,000 + 6,000)
  - HIGH SCORE: 6,000 Shekels 🎉 (NEW HIGH SCORE!)

Game 3 (Lose, earn 0):
  - TREASURY: 0 Shekels (crashed before banking)
  - TOTAL TREASURY: 21,000 Shekels (losses don't add)
  - HIGH SCORE: Still 6,000 Shekels

Page reload/new browser session:
  - TOTAL TREASURY: Still 21,000 Shekels (persists, does not reset)
```

---

## 🎟️ The Ticket Store

`store.html` is a standalone page, styled to match the main game, where you spend your **TOTAL TREASURY** on five themed "Bullet Train Ticket" question packs. It shares the `totalTreasuryAccount` localStorage balance directly with the game -- so Shekels you've banked from winning games are exactly what you spend here, and the balance updates live in both places.

| Pack | Covers | Questions | Price |
|---|---|---|---|
| **Torah** | Genesis - Deuteronomy | 194 | 50,000 Shekels |
| **Kings & History** | Joshua - Esther | 168 | 250,000 Shekels |
| **Prophets & Wisdom** | Psalms - Malachi | 128 | 500,000 Shekels |
| **Gospels** | Matthew - John | 234 | 125,000 Shekels |
| **Epistles & Revelation** | Acts - Revelation | 177 | 1,000,000 Shekels |

* **Free questions:** 100 questions are always available at no cost, regardless of which packs you own.
* **Total question bank:** 100 free + 901 across the five packs = **1,001 questions**.
* **What buying unlocks:** Owned packs are saved to localStorage (`bulletline_owned_packs`) and read directly by the main game -- their questions are added to the mixed deck immediately, and a category-only play option appears on the title screen for each owned pack.
* **BUY TICKET prompt:** A glowing "BUY TICKET" link appears once your Total Treasury is enough to afford the next-cheapest pack you don't yet own, nudging you toward the store. It stops glowing once dismissed, and won't reappear until your treasury grows further.
* **The ARRIVALS/DEPARTURES board explains itself:** The split-flap board on the title screen lists a "train line" for each of the five packs. A line shows a normal running status (ON TIME, BOARDING NOW, or a DELAY) if you own that pack, or **LOCKED** if you don't. A caption under the board header explains what LOCKED means, and clicking a LOCKED row takes you straight to the Ticket Store to buy it.
* **Note:** Spending Shekels in the store permanently reduces your Total Treasury balance -- there's no separate in-store currency.

---

## 📊 Game Summary Report

After each game concludes (win or loss), a detailed **Game Summary Report** is displayed showing:

* **Question-by-Question Breakdown:** Every question you answered during the game, listed in order with:
 * Your choice vs. the correct answer
 * Result badge (✓ CORRECT or ✗ INCORRECT)
 * The KJV scripture reference paired with each question
 * The full scripture text for deeper study
* **High Score Banner:**
 * If you set a **new high score** (win only): An Electric Blue **NEW HIGH SCORE** banner appears at the very top of the summary, showing your record Shekel total.
 * If you won without a new record: A panel shows your final score, the high score to beat, and how many Shekels away you were.
 * If you lost: An Electric Blue **OUTRUN** banner appears at the very top, showing your 0-Shekel score and the high score to beat.
* **Rivalry Record:** A blue W-L card shows your lifetime record against the opponent you just faced (e.g. RIVALRY / vs the Scribe -- 1-0). Records persist in localStorage (`bulletline_rivalry`) and also appear as badges on the opponent-select cards: FIRST MEETING for a fresh matchup, gold when you're leading or tied, red when you're trailing.
* **Ticket Bonus Breakdown:** On a win where a Mystery Ticket Bonus fired, a gold " TICKET BONUS: +X Shekels" line shows exactly how much of your total came from your mystery ticket reward.
* **Opponent Bounty:** On a win against Scholar or Prophet, a line names the opponent you beat and the win bonus applied (x1.25 / x1.5).
* **Game Statistics:** A running total at the bottom tracks total games played, games won, and games lost for the current browser session (these counters are in-memory only and reset on page reload -- unlike TOTAL TREASURY and HIGH SCORE, they are not saved to localStorage).
* **Print Report:** Click the **🖨️ Print** button next to the report title to open a print-friendly popup window with all questions, answers, scripture references, and formatting -- perfect for saving as a PDF or printing a physical copy for personal record-keeping.
* **Restart:** Start a fresh game immediately from the summary screen.

Separately, a **SHARE** link in the top navigation (available any time, not just after a game) opens a Facebook share dialog for the game's own URL -- it shares the game itself, not your individual results.

This report helps reinforce biblical knowledge, track your progress over multiple play sessions, see how close you came to beating your personal high score, and generate a printable record of your gameplay.

---

## 📚 Learning Library

Every question you miss -- in the Shekel Builder, the race, or sudden death -- is saved as a KJV verse flashcard in your **Learning Library** (stored in localStorage as `bulletline_learning_library`, one card per verse, deduplicated by reference). The cards say nothing about the game, your wrong answer, or the right one -- just the verse.

* **Opening it:** After a game where you missed questions, the summary shows a **LEARNING LIBRARY** button ("N new verses waiting for you ->") with a gold NEW badge while you have unreviewed verses.
* **Flip cards:** The front shows the scripture reference with a KJV badge; tap to flip to the verse text on the back.
* **MASTERED** removes the card from your library; **NEXT ->** keeps it and moves on. A counter shows your place (N of M).
* **Text size:** **-** and **+** buttons above the card resize the verse text (0.8-2.5rem) -- your size is remembered and applies to every card.
* **Honor system:** There is no quiz or test mode -- review is on your conscience.

---

## ⚠️ Hazard Events

The race isn't just you versus Train X -- the track itself fights back. A 14-card hazard deck (Bridge Out, the Red Sea, Jonah's Storm, Jericho Walls, Daniel's Lions, the Fiery Furnace, Elijah's Whirlwind, Locust Swarm, Earth Quakes, Jordan Overflows, Hornets, Frogs, Thunder on Mount Sinai, Earth Opens) is shuffled once per session with no repeats until every card has been seen.

* **Trigger rules:** At most one hazard per race, never before round 4, never in sudden death -- roughly a 30% chance on each eligible round.
* **The dodge:** When a hazard triggers, its card appears alone with a thunder-rumble warning and an explicit red CONTINUE button. Tap through, and the race question becomes your dodge test -- answer correctly to advance normally (green **DODGED!** flash), miss and the hazard knocks you back one step (red **HIT!** flash, never below your boarding step range cap of step 7). Train X is unaffected.
* **Bounty cards:** Two hazards pay a Shekel bounty for a successful dodge -- Daniel's Lions (10,000 Shekels) and the Fiery Furnace (5,000 Shekels). The card tells you the bounty up front; dodging adds it to your race bank (win the race to keep it) with a "BOUNTY!" banner, and the win summary itemizes it.
* **The summary** marks hazard rounds so you can see where the track bit you.

---

## 🔄 Question Deck Shuffle Logic

The game uses a **smart deck shuffling system** to ensure a fresh experience while preventing question fatigue:

* **Session Persistence:** Used question IDs are tracked in browser localStorage (`bulletline_used_questions`), preventing the same question from appearing twice in a single session.
* **Automatic Reshuffling:** When all available questions have been asked (accounting for which category, if any, and which paid packs you own), a shuffle modal appears notifying you that the deck is being reset. The used question log is cleared, and every available question becomes eligible again.
* **Graceful Fallback:** If localStorage is unavailable (e.g., private browsing mode or embedded browsers), the question deck still tracks usage in-memory for that session only--you won't replay questions until you reload the page.
* **Randomized Draw:** Active questions are randomly shuffled on each reset to ensure varied game experiences.
* **No manual reset control:** A previous version of the game had a manual "Reshuffle Deck" button on the title screen. It has since been intentionally removed -- deck shuffling is now handled entirely by the automatic system above, and there is no manual override on the title screen.

---

## 📰 The Jerusalem Herald News Ticker

The title screen features a two-line scrolling LED ticker themed as a fictional news network, "The Jerusalem Herald":

* **Line 1** cycles through welcome and promotional messages.
* **Line 2** alternates between a live Holy Land weather readout ("YOUR LOCAL WEATHER IN THE HOLY LAND" -- real current conditions fetched from a weather API for Jerusalem, Bethlehem, Nazareth, the Sea of Galilee, and other biblical locations) and batches of KJV-inspired news headlines, each labeled with the "JERUSALEM HERALD" masthead (styled gold) and a status tag (styled red -- normally "BREAKING NEWS," see below).

**Randomized playback:** Every time Line 2 finishes a pass -- including each time it loops -- the news headlines are freshly shuffled into a new random order, and are broken into randomly-sized batches of 1 to 5 stories between each weather segment (rather than a fixed count), so the sequence and grouping is different every time.

**Weather audio:** Background weather music fades out automatically the moment a news headline begins, whenever that headline appears in the rotation.

**Headline library:** Line 2 currently draws from 41 headlines spanning both Old and New Testament events (Creation, the Flood, the Exodus, the judges and kings, the exile, the life and ministry of Jesus, and the early church), written in a tabloid "breaking news" voice. A number of headlines involving Jesus explicitly proclaim His identity -- as the Christ, the Son of God, and the Savior of the world who came to save mankind from sin -- in addition to reporting the event itself.

* **Status tags:** Most headlines run under the default **"BREAKING NEWS"** tag. A headline can instead carry a custom tag when "breaking news" wouldn't make sense for it -- for example, the Noah's Ark headline is framed as a retrospective, first-person recollection from an aged Noah rather than same-day coverage (since only his family of eight would have survived to report it), and runs under a **"SPECIAL REPORT"** tag instead.

---

## 💬 Feedback

A **FEEDBACK** link in the top navigation opens an in-page form for sending questions, comments, or suggestions about the game directly to the developer's email.

---

## 📂 Project Structure

The project is organized into a handful of files rather than a single monolithic one, separating the question data and styling from the application logic:

* `index.html` -- The core application: HTML structure, SVG graphics, audio synthesis logic, and game logic.
* `styles.css` -- All CSS styling, including the neon train layout, animated fog background, mobile-optimized scripture drawers, and news ticker styling.
* `questions.json` -- The KJV question bank (100 free questions plus 901 across the five Ticket Store packs -- 1,001 total), including scripture references, quotes, and answer choices.
* `store.html` -- The standalone Ticket Store page described above, sharing the game's branding, fog background, and visual style.
* `logo.png` -- The game's logo image.
* `title-intro.mp4`, `time-tunnel.mp4`, `jerusalem-entry.mp4` -- The three title-screen videos (see Title Videos above). They must sit next to `index.html`.
* `LICENSE` -- Project license terms (plain text).
* `license.html` -- The same license terms as a styled web page.

---

## 📜 License

(c) 2026 William Monti. All rights reserved.

This game is proprietary software. See the LICENSE file for the full terms: no copying, modifying, distributing, or selling any part of the game without written permission.
