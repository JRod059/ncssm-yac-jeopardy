# Yakety Jeopardy — Planning

Living planning document. Updated as decisions are made.

**Status: building version one.** Jacob gave the go-ahead on 2026-10-11. The app is the single file `yac-jeopardy.html`.

Last updated: 2026-10-11

## The brief

Yakety hosts a Jeopardy-style trivia game with a board of categories and point values, where members pick a square, see the clue, and reveal the answer. The group fleshes out the categories, questions, and scoring.

Yakety stands at a big podium beside the board, reads each clue in a speech bubble, and does a happy hoof-stomp for right answers and a dramatic faint for wrong ones.

### Guiding questions from the brief

- **Design:** What colors and overall look do you want the app to have?
- **Fun:** What will make it fun, and how should Yakety bring it to life?
- **Features:** What are the top 1–3 things people will want to do in the app?

## Who it's for

The YAC is the Young Alumni Council of NCSSM, the North Carolina School of Science and Mathematics, covering both the Durham and Morganton campuses.

- It is a post-graduation council of recent graduates who bridge communication and outreach between the school and its young alumni.
- Its main work is outreach events on the campuses most NCSSM alumni attend, mostly in the Triangle: UNC Chapel Hill, NC State, and some at Duke. The aim is for alumni to know there is a community around them, and to meet older alumni.
- The app gives the council a trivia game it can always pull out at easier indoor events. The council has run this game before on a Jeopardy website and wants its own app instead.

"Yakety" is a stand-in name, not an established mascot.

## Decisions

| # | Decision | Detail |
|---|----------|--------|
| 1 | One shared screen | The game runs on a single laptop or TV. Players watch the screen; they never touch the app. |
| 2 | Facilitator-only controls | The only person operating the app is the facilitator. Every control is designed for them, not for players. |
| 3 | Saved boards plus an editor | On opening, the facilitator chooses a saved board or creates a new one. Boards can be edited. A clear Play action starts the game from a chosen board. |
| 4 | Starter board uses the council's existing questions | The first saved board is the game the council has already run, with the same questions. Jacob will supply them. |
| 5 | NCSSM brand, one palette throughout | The app uses the school-wide NCSSM colors everywhere. No campus-specific colors. |
| 6 | NCSSM fonts, friendly and fun tone | Stay within NCSSM's type system, styled to feel playful rather than corporate. |
| 7 | No on-screen host for now | A real person hosts the game, so the app needs no host character. Mascot characters may be added later, once the app is fully built. |
| 8 | Web app, shareable as an easy-access file | A web app is fine. It must be usable by anyone in the YAC, not only Jacob, without technical setup. |
| 9 | Streamlined scoring | Same point values as the existing game, but the facilitator records one outcome per clue instead of using plus and minus buttons: the team got it correct, another team stole it, or no one scored. |
| 10 | Answer timer with sound, started by hand | A visible countdown for each clue, with a timer sound. It does not start on its own: the facilitator lets teams read the clue, then clicks to start it. |
| 11 | Turn tracking | The app tracks whose turn it is, so "correct" applies to that team without picking it. |
| 12 | Wrong answers cost nothing | Points only move when a team gets a clue correct or steals it. |
| 13 | Steals | The facilitator taps the team that stole. With two teams it is automatic. |
| 14 | Scores can be corrected by hand | Clicking a team's score lets the facilitator type in a new number, to fix mistakes or take points away. |
| 15 | Bonuses deferred | No bonus squares or final round in version one. May be added later. |
| 16 | Model split | Planning and orchestration in Opus 5.5. Implementation (coding) in Haiku 5.5. |

## Brand research

Researched 2026-10-11. The official brand kit at brand.ncssm.edu sits behind an NCSSM Google sign-in, so the values below come from the kit's publicly indexed "Fonts and colors" page and from the live stylesheet of ncssm.edu.

### Colors

| Role | Name | Pantone | Brand kit hex | ncssm.edu web hex |
|------|------|---------|---------------|-------------------|
| Primary | NCSSM blue | 653 C | `#346094` | `#346094` |
| Primary | Gray | Cool Gray 8 C | `#8a8a8d` | — |
| Accent | Light blue | 291 C | `#99caea` | `#a2c9e8` |
| Accent | Plum | 512 C | `#853175` | `#7d3774` |
| Accent | Green | 363 C | `#4b8b2a` | `#4d7732` |
| Accent | Gold | 7406 C | `#f4c300` | `#ecc646` |
| Accent | Orange | 145 C | `#d57e00` | `#cb843c` |

The website also uses a near-black `#252525` for text and a darker blue `#27486e` for hover states.

### Fonts

- **Montserrat** — primary typeface. The website loads weights 500, 600 and 700. Free on Google Fonts, with heavier weights (800, 900) that suit big, friendly game-show headings.
- **Verdana** — the stated fallback when Montserrat is unavailable.
- **Georgia** — the complementary secondary (serif) typeface.

### Proposed use in the app

- Board, podium and chrome: NCSSM blue, with gold for point values and light blue for highlights.
- Plum, green and orange: reactions, team colors and celebrations.

### Sources

- https://brand.ncssm.edu/fonts-and-colors
- https://www.ncssm.edu/

## Starter board: "NCSSM Jeopardy!"

Taken from the council's existing JeopardyLabs game (`ncssm-jeopardy-5-3.html`). Five categories, five clues each, 100 to 500 points. Wording follows the original, with typos corrected on 2026-10-11 at Jacob's request.

### Mo-Town Ball Knowledge

| Points | Clue | Answer |
|--------|------|--------|
| 100 | What large landmark building can you often find NCSSM-Morganton students behind watching the sunrise/sunset? | The Barn |
| 200 | Where do Morganton students often go for their fresh groceries? | Aldi |
| 300 | What campus wide (club) event consistently has the highest attendance at NCSSM-Morganton? | Diwali |
| 400 | How much does a load of laundry cost? | $3.00 |
| 500 | Why was the construction of Joiner Hall originally postponed? | Endangered Species of Owl |

### Durham Ball Knowledge

| Points | Clue | Answer |
|--------|------|--------|
| 100 | This paved pathway through the Durham campus has served for decades as a major student hangout spot. | Hill Street |
| 200 | Where is the morgue rumoured to be? | Greynolds Breezeway |
| 300 | What iconic meal is served every Wednesday in the PFM? | Fried Chicken Wednesdays |
| 400 | Recite the iconic chant of the NCSSM swim team when cheering for their teammates. | 3.14159, secant tangent cosine sine, physics bio polymer chem, give them hell, go ssm! |
| 500 | Which female residence hall has the coldest water fountain on campus? | Third Beall |

### NCSSM Lore

| Points | Clue | Answer |
|--------|------|--------|
| 100 | NCSSM stands for what? | North Carolina School of Science and Mathematics |
| 200 | Before it became a school, the Durham campus was the site of this hospital. | Watts Hospital |
| 300 | NCSSM's very first class had 150 juniors, because the campus was being converted from a hospital, these students initially had to walk to a nearby elementary school for this daily necessity. | Meals |
| 400 | In 2023 NCSSM broke 43 years of tradition when this annual school event was held somewhere other than the Durham campus for the first time. | Convocation |
| 500 | In 2011 NCSSM students, faculty, and supporters set a Guinness World Record by collecting this much of one particular item in 24 hours. | 559,885 pounds of food |

### Do you know NC?

| Points | Clue | Answer |
|--------|------|--------|
| 100 | What is North Carolina's nickname? | The Tar Heel State |
| 200 | This soft drink was invented in New Bern, North Carolina, in 1898. | Pepsi Cola |
| 300 | Where did the Wright Brothers make their first powered flight? | Kitty Hawk |
| 400 | This North Carolina-born musician, often called the "High Priestess of Soul," was born Eunice Waymon in Tryon, North Carolina. | Nina Simone |
| 500 | This North Carolina county is home to Mount Mitchell, the highest point east of the Mississippi River. | Yancey County |

### Non-NCSSM: General Knowledge

| Points | Clue | Answer |
|--------|------|--------|
| 100 | What continent has no countries? | Antarctica |
| 200 | This North Carolina-born company started as a single doughnut shop in Winston-Salem in 1937. | Krispy Kreme |
| 300 | A banana is botanically classified as this type of fruit. | Berry |
| 400 | In 1919 this American city was hit by a massive wave of molasses that killed 21 people and injured more than 100. | Boston |
| 500 | The world's shortest war lasted less than an hour. It was fought in 1896 between Britain and this African sultanate. | Zanzibar |

### Corrections made to the original

- "Antartica" → "Antarctica"
- "North Carolinas nickname" → "North Carolina's nickname"
- "The Tarheel State" → "The Tar Heel State"
- "event washed somewhere" → "event was held somewhere"
- "female residents hall" → "female residence hall"
- "Aldi's" → "Aldi"
- "Winston Salem" → "Winston-Salem"
- "NCSSM Morganton" → "NCSSM-Morganton", and "24hrs" → "24 hours"
- End punctuation added or corrected on five clues

## How the existing game works

Observed in the saved JeopardyLabs page. This is the baseline the new app should at least match.

- A menu asks for the number of teams: none, 1 to 10, or a custom number.
- Team names and scores sit along the bottom of the screen and can be edited by hand.
- Each team has plus and minus buttons that add or subtract the value of the current clue.
- Clicking a square opens the clue full-screen. Spacebar reveals the answer; Escape returns to the board.
- Used squares dim and stay dimmed.
- Keyboard shortcuts: arrow keys move around the board, number keys select a team, up and down arrows add or subtract points.
- Scores and used squares are saved in the browser, so a refresh does not lose the game. A reset option starts over.

## Open questions

Working assumptions are in the last column and will be used unless changed.

| # | Question | Working assumption |
|---|----------|--------------------|
| 1 | How is the app handed to other YAC members? | One self-contained HTML file. Double-click to open in any browser; no terminal, install or internet needed. Shared by Google Drive, email or a link. |
| 2 | How do boards travel between people? | Boards save in the browser of whoever made them, so the app also exports and imports a board as a small file that can be shared. |
| 3 | How long is the timer? | 60 seconds by default, adjustable in settings. Can be paused or restarted. Ticks in the final seconds and buzzes at zero. |
| 4 | Is there an undo for the last outcome? | Yes, one click reverses the last outcome and reopens the square, alongside typing a score directly. |

## Features

### Version one

1. **Choose a board.** On opening, pick a saved board or start a new one. "NCSSM Jeopardy!" is built in.
2. **Edit a board.** Write categories, clues, answers and point values. Save, duplicate, delete, export and import boards.
3. **Play.** Set up teams, show the board, open a clue, start the timer when the teams have read it, reveal the answer, record the outcome, and watch the scores update. Any score can be clicked and retyped. Used squares dim. A refresh does not lose the game.

### Later, maybe

- Bonuses, as in the TV show: hidden Daily Double squares where a team wagers its points, and a Final Jeopardy round where every team wagers on one last clue.
- Mascot characters.

## Design

- NCSSM blue board with gold point values, light blue highlights, and plum, green and orange for team colors and reactions.
- Montserrat throughout, in heavy weights for headings and point values.
- Friendly and fun rather than corporate: rounded shapes, lively motion on reveals and score changes.
- Built to be read from across a room on a TV or projector.

## Host and mascot

Deferred. A real person hosts, so version one has no on-screen character. The original brief's ideas are kept here for a possible later addition:

- A host at a podium beside the board, reading each clue in a speech bubble
- A happy hoof-stomp for a right answer and a dramatic faint for a wrong one

## Technical approach

Proposed, not yet agreed:

- A single self-contained HTML file with the styles, code, font and sounds all inside it, so it works offline and can be shared like any document.
- Boards and the game in progress are stored in the browser's local storage.
- Board export and import use a small file, so boards can be passed between YAC members.
- Optionally, the same file can later be put at a web link so nobody needs to download anything.

## Build log

### 2026-10-11 — version one, first build

`yac-jeopardy.html` built (coded by Haiku 5.5, specified and checked by Opus 5.5).

Checked by clicking through it in a browser: home, game setup, the board, opening a clue, starting the timer by hand, revealing the answer, a steal, typing a corrected score, undo, playing all 25 squares to the winner screen, and the editor loading the starter board. No errors.

Not yet checked: the timer and outcome sounds (cannot be heard in testing), export and import of board files, opening the file by double-click rather than through a local server, and games with more than two teams.

Known gaps against the plan:

- The Montserrat font loads from Google Fonts, so it needs internet. Offline the app falls back to Verdana, NCSSM's stated fallback. Embedding the font in the file is still to do.
- In the editor, the clue boxes are small and long clues need scrolling to read.
- The home screen is plain.

## Notes

- The project folder is not yet a git repository. Initialise git before the first code is written.
- "Jeopardy" is a trademark. Fine for a private group game; worth a different name if the app is ever published publicly.
