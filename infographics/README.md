# moneycanbuy.fun infographics v4: storyboard

16 picture cards and 6 animated loops that explain how moneycanbuy.fun moves money. An infographic here is a
diagram: bars, arrows, trees, timelines, tiles from our site. Words appear only as labels on those elements.
This file says, card by card, which cases the card must show and exactly how each one is drawn. Every case listed
for a card must be visible on that card. Every number on a card is written in this file; no other number appears.

## 1. Canvas and look (all cards and loops)

- Size: every card 1080x1350. Story version 1080x1920 for cards 1, 4, 7, 10 and 14 (same content, stacked
  vertically, more air). Loops: 1080x1350 MP4.
- Margins: every element at least 64 px from every edge. At least 24 px between neighbouring boxes. Nothing
  overlaps: no text crosses another text, an icon, an image, a bar, an arrow or a line. Arrows end at box edges.
- Background `#000000`. Panels and tiles: fill `#0D120E`, 2 px line `#222B24`, corner radius 28 px; a raised
  panel inside a panel uses `#182019`. This is the dare card of the site.
- Type: Quicksand (`../explainers/brand/fonts/`), 700 for headlines and numbers, 500 for labels. Headline at least
  64 px, one line, top left. Labels at least 32 px. Footnote at least 24 px, at most one line per card.
- Text form: a label is a name and/or a number, at most 2 lines, sitting on or right next to its element. No
  sentences in paragraphs, no bullet lists, no text-only boxes. If a case cannot be drawn without a sentence, the
  card is wrong: redraw the case.
- Every percent names its base on the card: "3% of the reward = 3 USDC", never "3% of 5%".
- Dollars only for the example reward of $100 USDC and its shares. YOLO amounts are always in YOLO, never in $.
- Footer on every card: `moneycanbuy.fun` bottom left (28 px, `#9EA69F`), card number bottom right (`4/16`).
- Toad mark (`../explainers/brand/mark-transparent-1024.png`) at most 96 px, top right, as is.

### Colors (site palette, one meaning each)

| Hex | Meaning on every card |
| --- | --- |
| `#F5C451` gold | the reward and YOLO amounts, the reward bar |
| `#3ECF7A` green | the doer's money, LEGIT, WILL DO, "paid", the Claim button |
| `#F43F5E` red-pink | FAKE, a lost bond |
| `#FFFFFF` white | NFT voters' share |
| `#9EA69F` grey | treasury share, secondary labels |
| `#FF8A3D` orange | buyback wallet share |
| `#FF4D2E` flame, core `#FFB020` | burned YOLO, only with the flame icon |
| `#82B63E` toad green | the IMD swarm, outlines of swarm boxes |

Red flame: a filled flame, `#FF4D2E` with a `#FFB020` core, at least 56 px high, next to every burned amount.
Never green, never a drop. No other element uses `#FF4D2E`.

### Fixed icons (same icon for the same actor on every card, 72-96 px)

| Actor | Icon |
| --- | --- |
| Author | padlock on a gold coin |
| Doer | green check in a circle |
| Disputer | red-pink flag |
| NFT voters | one identity.md NFT image from `../explainers/imd/` (`nft-*.png`) in a square frame |
| IMD swarm | the IMD coin `../explainers/imd/imd-token-logo.png` |
| Treasury | grey vault box |
| Buyback wallet | orange wallet |
| Burn | the red flame |
| Predictor | the WILL DO / WON'T DO tiles in miniature |
| Dev wallet | grey key |

NFT images and the IMD coin are used as supplied: no redraw, recolor, stretch or crop; words inside them belong to
the image. No people, faces, hands or photos.

### Site parts to reuse

Rebuild these in HTML/CSS with the look of the screenshots (font, radius, colors, spacing) and the numbers of the
card. Never show a wallet address, a date or a name from a screenshot.

| Site part | Look at | Used on cards |
| --- | --- | --- |
| Dare card (title, type badge, YOU GET amount) | `../ui/card-*.png`, `../pov/screens/milk-dare-90.png` | 1, 3, 7 |
| YOU GET block, big green amount | `../ui/prize.png`, `../pov/screens/milk-dare-90.png` | 7, 9 |
| Bond rows (`Bond · fixed 0.5 IMD`, `Bond · 3% of author's reward`, Total) | `../pov/screens/yolo-submit-bond.png` | 2, 3 |
| Dispute reason sheet | `../pov/screens/milk-dispute-reason.png` | 4 |
| NFT vote bar (LEGIT green left, FAKE red-pink right, `decided: FAKE`) | `../pov/screens/vote-0-24-decided.png`, `vote-row-0-10.png` | 4, 5 |
| WILL DO / WON'T DO tiles, WEIGHT pill | `../pov/screens/milk-banks.png` | 10, 11 |
| Burn panel (pixel flame, YOLO BURNED, Burn button) | `../pov/screens/burn-total.png` | 12 |
| Trophy minted | `../pov/screens/yolo-trophy-minted.png` | 12 |
| Claim button (green) | `../ui/claim.png` | 7, 8, 10 |

## 2. The cards

Each card: headline, the cases it must show, the diagram, where every element sits, the labels.

### 1. A dare from post to payout

Cases: post (reward locked, deadline fixed), submit (proof + bond), a second submission waits in line, no
dispute in 24 h → paid, disputed → NFT vote → swarm, fake → open again, deadline passed with nothing accepted →
reward back to the author, cancelled by the dev wallet → everything back.

Diagram: a vertical time axis (2 px `#222B24`) down the left third, x = 160. Six stops as round nodes (48 px):
POST, SUBMIT, 24 h REVIEW, 24 h NFT VOTE, SWARM, PAID. Each node has a small site tile to its right:
- POST: a dare card tile with a gold `$100 USDC` and a padlock; label `locked until the deadline`.
- SUBMIT: proof tile + bond row `0.5 IMD + 3 USDC`; a second, dimmed tile behind it labelled `waits in line`.
- 24 h REVIEW: an hourglass; label `no dispute → paid`; a green arrow jumps from here straight to PAID.
- 24 h NFT VOTE: the vote bar at 0 : 24 `decided`.
- SWARM: the IMD coin; label `6 h + 1 h`.
- PAID: green YOU GET `$90` with the Claim button.
Three side exits branch to the right from the axis with dashed arrows and end in small end tiles:
from NFT VOTE / SWARM → `FAKE → dare open again` (red-pink flag); from POST's deadline → `deadline passed →
$100 back to the author` (gold arrow back to the author icon); a grey key tile `dev wallet cancel → everything
back` attached to the whole axis by a bracket.
Story 1080x1920: same, the axis runs the full height.

### 2. Who puts money in

Cases: author reward and minimums per currency, no creation fee, top-ups and YOLO add-ons, doer bond, dispute
bond, swarm call fee, NFT voters pay only gas, predictors from 1 YOLO.

Diagram: a funnel into one central vault tile ("the dare", 360 px wide, center). Six actor icons sit around it,
each with one arrow into the vault, the arrow labelled with what goes in:
- Author (top left): `$100 USDC reward`; under it a strip of four minimum chips: `5 USDC` `0.002 ETH` `1 IMD`
  `1,000 YOLO`; a chip `no creation fee`.
- Anyone (top right): `top-up / YOLO add-on`.
- Doer (middle left): the bond rows from the site: `0.5 IMD` + `3% of the author's reward = 3 USDC`.
- Disputer (middle right): `0.5 IMD` + `1% of the author's reward = 1 USDC`.
- Swarm caller (bottom left): `+0.5 IMD per call` with the IMD coin at the arrow's end outside the vault.
- NFT voter (bottom right): no arrow into the vault; label `gas only`.
Bottom chip row: `Predictors: from 1 YOLO` with the mini WILL DO / WON'T DO tiles.
Footnote: `Bonds count only the author's own reward.`

### 3. Submitting proof

Cases: proof plus reasons in one step, bond 0.5 IMD + 3%, optional mark `moneycanbuy.fun` in the proof, the
proof check before submit is only a hint, second submission waits in line, predictions pause during review.

Diagram: a phone-sized site sheet (600 px wide, center left) built like the site's submit sheet: proof link
field, `why it is honest` field, bond rows, green Submit button. Callouts with thin lines to parts of the sheet:
- to the proof field: a small paper note showing the text `moneycanbuy.fun` and the label `optional mark`.
- to a red warning line inside the sheet: `red warning = hint, you can still submit`.
- to the bond rows: `back when accepted`.
Right column, two small states stacked: `under review` tile with a pause icon over the WILL DO / WON'T DO tiles
(label `predictions paused`), and a dimmed second proof tile labelled `next proof waits in line`.

### 4. Dispute and the NFT vote

Cases: anyone except the doer disputes within 24 h, one dispute per submission, reason required and link
optional, 1 NFT = 1 vote, own wallet and gas, an NFT votes once and cannot switch, lead of 20 at any time →
decided at once, at 24 h lead of 10 → decided, otherwise no decision, no decision and no swarm call → accepted.

Diagram: top: the dispute sheet (reason field marked `required`, link field marked `optional`) with the
disputer flag and a timer chip `24 h`. Middle: a row of NFT images (5-8 identity.md images in frames) with
arrows to a big vote bar. Below the bar, a three-branch tree, each branch ending in a mini vote bar from the
site:
- `LEAD 20 → decided at once`: bar `0 : 20`, a lightning icon.
- `24 h · LEAD 10 → decided`: bar `3 : 14`, a clock icon.
- `24 h · lead under 10 → no decision`: bar `6 : 9`, grey; a green arrow from it to `accepted` with the label
  `if nobody calls the swarm`.
Small chips along the NFT row: `1 NFT = 1 vote`, `own gas`, `no side change`.
Footnote: `Small dares: if NFTs do not vote, the swarm decides.`
Story 1080x1920: the tree gets one row per branch.

### 5. Calling the swarm

Cases: anyone calls within the 24 h appeal window, panel 7 agents quorum 5, yes/no answer is final, answer
in 6 h + 1 h; a side of the dispute pays 0.5 IMD out of its bond, the same side again pays 0.5 IMD from the
wallet, an outsider pays a dispute bond + 0.5 IMD; swarm silent → a new 24 h window, at most 3 calls per
submission, after the 3rd silence the NFT result stands; fees of silent calls are not refunded.

Diagram: center: the IMD coin (160 px) with 7 identity.md NFT images in an arc above it, label `7 agents ·
quorum 5 · final`. Left: three callers stacked, each with a coin arrow into the swarm:
- `side of the dispute` → `0.5 IMD from its bond`.
- `same side again` → `0.5 IMD from the wallet`.
- `outsider` → `bond + 0.5 IMD`.
Right: a vertical strip of three call slots `1` `2` `3`, each a small tile; slots 1 and 2 show a mute icon and
`silent → new 24 h`; after slot 3 an arrow to `NFT result stands`. A timer chip `6 h + 1 h` on the swarm.
Footnote (24 px): `Outsider who wins gets 0.5 IMD back first, if the loser's bond still holds IMD.`

### 6. Who gets the loser's bond

Cases: loser is the doer (fake) or the disputer (honest proof); NFT decided and it held → 50% winner, 50% NFT
voters who voted right; NFT wrong or no decision → 100% winner; the winner always gets its own bond back; each
currency split separately.

Diagram: a 2x2 grid. Rows: `fake proof` (loser = doer, bond `0.5 IMD + 3 USDC`), `honest proof` (loser =
disputer, bond `0.5 IMD + 1 USDC`). Columns: `NFT right`, `NFT wrong / no decision`. In every cell the loser's
bond is a stack of two coins (IMD coin and a USDC chip) that splits along arrows:
- fake · NFT right: `0.25 IMD + 1.5 USDC` → disputer, `0.25 IMD + 1.5 USDC` → NFT voters.
- fake · NFT wrong: `0.5 IMD + 3 USDC` → disputer.
- honest · NFT right: `0.25 IMD + 0.5 USDC` → doer, `0.25 IMD + 0.5 USDC` → NFT voters.
- honest · NFT wrong: `0.5 IMD + 1 USDC` → doer.
The losing side's icon is red-pink with a crossed bond, the winner's icon green with a return arrow labelled
`own bond back`.

### 7. Where $100 goes when the proof is accepted

Cases: no dispute with no stake, full stake, power half the reward, power 5% of the reward; dispute with NFT
right, no stake and full stake; dispute where NFT were wrong or did not decide, no stake and full stake.

Diagram: 8 horizontal stacked bars, each exactly the same length = $100 (952 px). Segment widths are to scale.
Segments: doer green, NFT voters white, buyback wallet orange, treasury grey. The amount sits inside the segment
when it fits, otherwise above it with a 2 px leader line. Left of each bar a case tag (icons, not words): stake
padlock full / half / small / none, and a vote bar mini (none / LEGIT right / crossed).
- no dispute, no stake: doer `$90` · treasury `$10`
- no dispute, full stake: doer `$94` · buyback `$5.50` · treasury `$0.50`
- no dispute, power = half the reward: doer `$92` · buyback `$6.50` · treasury `$1.50`
- no dispute, power = 5% of the reward: doer `$90.20` · buyback `$7.40` · treasury `$2.40`
- dispute, NFT right, no stake: doer `$90` · NFT `$5` · treasury `$5`
- dispute, NFT right, full stake: doer `$94` · NFT `$5` · buyback `$0.50` · treasury `$0.50`
- dispute, NFT wrong or no decision, no stake: doer `$90` · treasury `$10`
- dispute, NFT wrong or no decision, full stake: doer `$94` · buyback `$5.50` · treasury `$0.50`
Top: a site dare card with gold `$100 USDC` and label `fee = 10% of the reward = $10`. Legend row of the four
colors with their icons. Footnote: `Top-ups and YOLO add-ons are paid by the same rule.`
Story 1080x1920: one bar per row with more air, legend at the bottom.

### 8. When $100 is not paid out

Cases: fake proof → the reward stays and the dare is open again, the doer's bond goes to the disputer and the
NFT voters; deadline passed with nothing accepted → $100 back to the author, YOLO add-ons back to who added;
cancelled by the dev wallet → every coin back to whoever put it in, each claims its own.

Diagram: three columns, each a short vertical flow from the same gold `$100 USDC` vault:
- `FAKE`: vault stays gold with a looping arrow `open again`; under it the doer bond coins split
  `0.25 IMD + 1.5 USDC` → disputer, `0.25 IMD + 1.5 USDC` → NFT voters.
- `DEADLINE`: a clock; gold arrow `$100` → author; a YOLO coin arrow `add-ons` → `who added`.
- `CANCELLED`: grey key; fan of arrows back to author, doer, disputer, predictors, each `back in full`;
  label on the key `takes nothing`.

### 9. The doer stake

Cases: lock any YOLO for 1-52 weeks, add or extend, never reduce, no early exit, the YOLO comes back after the
term; power = amount × weeks / 52, fixed at lock; bonus = 4% of the reward × min(1, power / author's reward);
counted at submission, paid only if the same lock still runs; one lock serves every submission; a fake does not
touch the lock.

Diagram: left: a padlock on a YOLO coin stack with a week ruler `1 … 52 weeks`; two example locks as bars:
`52 weeks → power = amount`, `26 weeks → power = half`. Right: a bonus meter (vertical bar 0 → 4% of the
reward) with four marks, each also a mini YOU GET block:
- power = reward → `+4% of the reward = $4` → doer `$94`
- power = half → `+2% = $2` → `$92`
- power = 5% → `+0.2% = $0.20` → `$90.20`
- no lock → `$0` → `$90`
Bottom row, three small tiles with icons: `one lock → every submission` (one padlock, three proof tiles),
`lock ended before payout → no bonus` (padlock open, crossed), `back after the term` (arrow to wallet).

### 10. WILL DO / WON'T DO

Cases: an entry of 100 YOLO splits 90 / 5 / 5; done → WILL DO takes its 90s back plus the WON'T DO pool by
points, the waiting 5% goes 2.5% to the author and 2.5% to the doer; not done → WON'T DO wins, the waiting 5%
burns; nobody on the winning side → done: the other pool half to the author, half to the doer; not done: all
to the author; cancelled → every entry back in full; entries until the deadline, paused during review, no
withdrawal, anyone can enter.

Diagram: top: the site WILL DO (green outline) / WON'T DO (grey outline) tiles. Under them one entry coin
`100 YOLO` splitting into three separate boxes in a row: `90 → pool`, `5 → burn` with the red flame, `5 →
waits`. Middle: a branching tree from the dare outcome:
- `DONE`: WILL DO tile lights green, an arrow pulls the WON'T DO pool into it, label `90s back + their pool`;
  the `5 waits` box splits `2.5% author` + `2.5% doer`.
- `NOT DONE`: WON'T DO tile wins the same way; the `5 waits` box burns (red flame).
- `CANCELLED`: both tiles return coins to entrants, `back in full`.
Example strip at the bottom: `1,000 vs 1,000 · done → WILL DO 1,800 · author 50 · doer 50 · burned 100`.
Footnote: `Nobody on the winning side: done → author and doer split the pool; not done → author.`
Story 1080x1920: entry split on top, the three outcomes stacked.

### 11. Early beats late

Cases: weight = (time left / whole term)², counted from dare creation; same amount, early entry gets more; a
small other side can leave a right entry below its stake; a single entry on an empty side takes the whole
other pool.

Diagram: top: a timeline from `created` to `deadline` with a curve of the weight falling from `×1.00` through
`×0.25` (half way) to `×0.01` (90% of the term gone); WEIGHT pills from the site sit on the curve.
Middle: two entrants on WILL DO, 100 YOLO each: A at creation `×1.00`, B half way `×0.25`; WON'T DO pool `900`.
Done → two bars: A `810`, B `270`.
Bottom: two mini scales:
- `100 vs 5 · right → 94.5` (scale tips, label `under 11% on the other side = loss`).
- `empty side + 1 late entry → takes the whole pool`.

### 12. What burns, and the trophy

Cases: 5% of every prediction entry; the waiting 5% when not done; trophy 7,777 YOLO; YOLO rewards and YOLO
add-ons: the treasury part of the fee; the launch-hour tax; the YOLO side of the pool fee; anyone can press
Burn, no reward for it; ETH, USDC and IMD shares go to the buyback wallet in the payout, no arrow goes past the
wallet; the trophy is an optional NFT of an accepted proof, only its doer mints it, the reward does not depend
on it.

Diagram: center: the site Burn panel with the red flame and `YOLO BURNED`. Six YOLO streams flow into it from
the left, each a gold arrow with an icon and a label:
- `prediction entry 5%`, `waiting 5% if not done`, `trophy 7,777 YOLO`, `YOLO reward fee`, `launch-hour tax`,
  `pool fee, YOLO side`.
Under the panel: the Burn button and `anyone can press`.
Right: a separate box with three coin chips `ETH` `USDC` `IMD` → orange wallet `buyback wallet`; the arrow
stops at the wallet.
Bottom box, apart from the rest: the trophy from the site (`yolo-trophy-minted.png` look), label
`optional · 7,777 YOLO burned` with a red flame.
Example chip: `reward 100,000 YOLO, no stake → doer 90,000 · 10,000 burned`.

### 13. YOLO supply

Cases: 1,000,000,000 YOLO, no mint; seven shares; what is unlocked when; no mechanic pays out of a fund.

Diagram: one long horizontal bar = 1,000,000,000 YOLO cut into 7 segments to scale, each with name and %:
Incentives `25%`, Treasury `22.2222223%`, Liquidity `15%` (padlock `locked forever`), Stabilizer / MM fund
`15%`, Swarm `10%` (IMD coin), Dev `7.7777777%`, Future team `5%`. Below: a step chart of the unlocked share
over time: `day 0 54%` · `month 6 72%` · `month 12 91%` · `month 24 100%`. Footnote: `No mint. No mechanic pays
out of a fund.`

### 14. The launch hour

Cases: before openAt nobody buys, openAt at most 30 days after deploy; minutes 0-30 only snapshot NFT wallets
buy, 500,000 YOLO per NFT, no buy tax, every sell pays 30%; minutes 30-60 everyone buys, buy and sell tax falls
in a straight line from 30% to 0%; after minute 60 no tax, no limits; the tax is YOLO → treasury → burned; a
sell of 1,000 YOLO at 30% puts 700 in the pool and 300 in tax.

Diagram: a chart, x = minutes 0 → 60+, y = tax %. Buy line green, sell line red-pink. 0-30: buy line at 0%,
sell line flat at 30%; 30-60 both fall straight to 0; 60+ both at 0. Above 0-30 a band with NFT images and
`snapshot NFTs only · 500,000 YOLO per NFT`. Left of 0 a padlock `before openAt: closed`. Under the chart a
1,000 YOLO coin splitting `700 → pool`, `300 → tax → treasury → burned` (red flame).
Story 1080x1920: the time axis runs top to bottom.

### 15. Who's who

Cases: author, doer, disputer, NFT holder, predictor, swarm caller, IMD swarm, dev wallet.

Diagram: 8 tiles (2 columns x 4 rows), each tile: icon, role name, then two chips: `pays` (arrow in) and
`can get` (arrow out):
- Author: pays `reward` · gets `reward back if not done · 2.5% of entries`
- Doer: pays `bond` · gets `90% of the reward = $90, up to $94`
- Disputer: pays `bond` · gets `loser's bond`
- NFT holder: pays `gas` · gets `5% of the reward = $5 + bond share`
- Predictor: pays `YOLO` · gets `90s back + losers' pool`
- Swarm caller: pays `0.5 IMD` · gets `winner's share`
- IMD swarm: gets `0.5 IMD per call`
- Dev wallet: `cancels a dare → everything back` · gets `nothing`

### 16. Contract map

Cases: four launches; users talk to one vault; no server, no keeper; each launch fits 16,777,216 gas.

Diagram: four horizontal tiers top to bottom, `Launch 0` … `Launch 3`, each tier a row of small contract boxes
with names only: Launch 0 `NftGate`, `4 vestings`, `YoloSplitter`; Launch 1 `YoloToken`, `DevPrices`,
`swap adapter`, `ParamsRegistry`, `TextRules`, `SwarmQuestion`, `VotePower`, `AttestationChecker`,
`BuybackBurner`; Launch 2 `YoloLockHub`, `CaseDesk`, `DisputeDesk`, `TaskVault` (larger, gold outline, label
`users talk only to it`); Launch 3 `YoloSweetener`, `TrophyCatalog`, `DareTrophy`, `ProtocolDirectory`,
`HiddenList`, `YoloPredict`. Outside right: the IMD coin box `IMD swarm`. Money arrows gold,
calls grey. Footnote: `No server. Each step is done by whoever calls it.`

## 3. Animated loops (MP4)

Six loops: cards 1, 4, 7, 10, 12 and 14. Each loop is the finished card coming alive. 1080x1350, H.264,
yuv420p, 30 fps, 8 s, no audio. Seamless: the last frame equals the first frame. Static parts never move; text
never moves or fades mid-read (it may appear once and stay). Easing ease-in-out, no shake, no flash.

- Loop 1 (card 1): 0-1 s full card dim; a gold coin starts at POST; 1-5 s it travels down the axis node by
  node, each node lights green as the coin passes (REVIEW skips straight to PAID on the first pass); 5-6.5 s
  the YOU GET `$90` counts up from `$0`; 6.5-8 s fade back to the first frame.
- Loop 4 (card 4): 0-1 s empty vote bar `0 : 0`; 1-4 s NFT frames light one by one and the FAKE side fills to
  `0 : 20`; 4-5 s lightning icon and `decided at once`; 5-7 s the other two branches light in turn (`3 : 14`,
  `6 : 9`); 7-8 s back to the first frame.
- Loop 7 (card 7): bars grow from zero left to right one after another (0.6 s each, 8 bars in 5 s); amounts
  appear when their segment is complete; 5-7 s hold; 7-8 s bars shrink back to the first frame.
- Loop 10 (card 10): 0-2 s the `100 YOLO` coin drops and splits into `90 / 5 / 5`, the flame flickers on the 5;
  2-5 s DONE branch: the WON'T DO pool slides into WILL DO, `2.5%` chips fly to author and doer; 5-7 s NOT DONE
  branch lights, the waiting 5 burns; 7-8 s reset.
- Loop 12 (card 12): the six YOLO streams pulse into the Burn panel in sequence (1 s each), the YOLO BURNED
  number ticks up by small steps and returns to its start value in the last 0.5 s; the flame flickers the whole
  time; the buyback arrow pulses once and stops at the wallet.
- Loop 14 (card 14): a playhead moves along minutes 0 → 60 in 6 s; the tax lines are drawn behind it; at 30 the
  NFT band fades out; at 60 a `0%` chip pops; 6-8 s playhead returns to 0.

## 4. Forbidden on every card and loop

Any token price, FDV, market cap, YOLO converted to dollars, price charts, "x100", "moon"; "guaranteed",
"earn", "yield", "passive", "APY", "staking rewards"; "bet", "gamble", "odds", "win big"; "automatic" or
"auto" next to buyback or burn, "bought back"; "deflationary", "fair launch", "whitelist", "AI judge"; any web
address other than moneycanbuy.fun; any link; any wallet or contract address, including the dead address;
dates; names of people.

## 5. Check every card

Measure the rendered card, not the source. For every PNG list every element (text, icon, image, bar, arrow,
line, mark, footer) with its box x, y, width, height from the render (getBoundingClientRect or getBBox). A card
fails if an element is closer than 64 px to an edge, two text boxes intersect, a text box crosses an icon, image,
bar, arrow or line other than its own container, a label is under 32 px or a footnote under 24 px, a label runs
over 2 lines, or a case listed for the card is missing. For every card list the cases it shows, in the words of
section 2. Put all cards on one contact sheet.
For loops: ffprobe of each file (size, fps, duration, codec), the first and the last frame side by side, and the
pixel difference between them (must be near 0).
