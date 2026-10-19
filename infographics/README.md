# moneycanbuy.fun infographics: card spec

12 static cards. Each card answers one question. Every number on a card is in `numbers.json` (field `display`); no other number appears. Exempt: list numbers, the footer card number (e.g. `3/12`) and the names Launch 0-3. Brand assets are in `../explainers/brand/` (colors.md, fonts/, mark-transparent-1024.png, wordmark.png).

## Frame rules (all cards)

- Size 1080x1350 (all 12). Story size 1080x1920 for cards 1, 5, 7, 10, with a vertical time axis where the card has steps.
- Background #000000, accent #3ECF7A, gold #F5C451 only on payout amounts, white text, secondary #9EA69F.
- Quicksand Bold for headings and text, IBM Plex Mono for every number. Text at least 28 px. Contrast of text to its background at least 4.5:1.
- Toad mark only as `mark-transparent-1024.png`, at most 96 px, in a corner. Never redrawn.
- Footer of every card: `moneycanbuy.fun` and the card number, e.g. `3/12`.
- Every percent names its base: "4% of the reward = $4", never "4% of 5%".
- Dollars only as the example reward of $100 USDC and its shares.
- Icons are simple shapes (wallet, NFT frame, hammer, scales, flame, padlock). No people, faces, hands, avatars, photos.

## Forbidden on every card

Any token price, FDV, market cap, "x100", "moon", price charts; "automatic", "auto", "auto-burn" next to buyback or burn; "bought back"; "guaranteed", "earn", "yield", "passive", "APY", "staking rewards"; "bet", "gamble", "odds", "win big"; "deflationary"; "fair launch", "whitelist"; "AI judge"; YOLO counts converted to dollars; any web address other than moneycanbuy.fun; any link; contract addresses.

## Cards

Card text below is the text on the card. Layout notes are in brackets.

### 1. The Dare Lifecycle
[vertical time axis, top to bottom]
1. Post: the reward is locked until the deadline. The deadline is set at posting and never moves.
2. Submit: proof plus a bond. If another submission is under review, it waits in line.
3. Review: 24 h dispute window from activation. No dispute → Accepted.
4. NFT vote: 24 h. Lead of 20 → decided at once. At the end: lead of 10 → Decided, else No decision.
5. Appeal / call the swarm: 24 h window. Swarm answers within 6 h + 1 h delivery. At most 3 swarm questions per submission.
6. Outcomes: Completed (accepted) · Expired (deadline passed, no active submission → money back) · Unwound (cancelled by the dev wallet → everything back to whoever paid it in). A rejected submission → the dare is Open again.

### 2. Who Puts Money In
[5 role rows: puts in → gets back when]
1. Author: the reward, at least 5 USDC / 0.002 ETH / 1 IMD / 1,000 YOLO. No creation fee. Locked until the deadline.
2. Anyone: top-up of the reward (same currency, before the deadline) and a YOLO add-on. Back only if not done by the deadline or cancelled.
3. Doer: bond 0.5 IMD + 3% of the author's reward, in the reward's currency. Back when accepted.
4. Disputer: bond 0.5 IMD + 1% of the author's reward. Back when the dispute is won.
5. Swarm caller: a dispute bond + 0.5 IMD per swarm call. A side of the dispute pays it from its bond; a repeat call from the wallet.
[footnote] NFT voters pay only gas. Predictors pay YOLO, from 1 YOLO.
[example] On $100 USDC: doer 0.5 IMD + 3 USDC · disputer 0.5 IMD + 1 USDC.

### 3. Dispute → NFT Vote → Swarm
[tree, top to bottom]
1. Dispute: anyone except the doer, within 24 h. One dispute per submission. A reason is required, a link is optional.
2. NFT vote: 1 NFT = 1 vote. Each holder votes for themselves. An NFT votes once per dispute, no side change.
3. Three results: Decided at once (lead of 20) · Decided at the end (lead of 10) · No decision.
4. Swarm: appeal of the NFT decision, or a call after No decision. Anyone can call. Panel of 7 agents, quorum 5, yes/no answer is final.
5. Swarm silent → a new 24 h window. After the 3rd silence the result stands as without the swarm.
6. No decision and no swarm call → the submission is accepted.
[footnote] Small dares: if NFT holders do not vote, the swarm decides.

### 4. Who Gets the Loser's Bond
[2x2 grid]
1. The loser is the doer (fake proof) or the disputer (honest proof).
2. NFT decided and the result holds: 50% to the winning side, 50% to the NFT voters who voted right.
3. NFT wrong (the swarm overturned) or no decision: 100% to the winning side.
4. The winner always gets its own bond back. An outside appellant who wins first gets 0.5 IMD from the loser's IMD bond.
[footnote] Split separately in IMD and in the reward's currency. Swarm fees are not refunded.
[example] Fake proof on $100 USDC: doer bond 0.5 IMD + 3 USDC → 0.25 IMD + 1.5 USDC to the disputer, 0.25 IMD + 1.5 USDC to the NFT voters who voted right. The reward stays in the dare.

### 5. Where $100 Goes
[6 horizontal bars, each = $100; segments: doer (gold), NFT voters, buyback wallet, treasury]
1. No dispute, no stake: doer $90 · treasury $10
2. No dispute, full stake: doer $94 · buyback wallet $5.50 · treasury $0.50
3. No dispute, power half the reward: doer $92 · buyback wallet $6.50 · treasury $1.50
4. No dispute, power 5% of the reward: doer $90.20 · buyback wallet $7.40 · treasury $2.40
5. Dispute, NFT right, no stake: doer $90 · NFT voters $5 · treasury $5
6. Dispute, NFT right, full stake: doer $94 · NFT voters $5 · buyback wallet $0.50 · treasury $0.50
[footnote] Fee = 10% of the reward = $10. NFT wrong or no decision: their $5 goes to the treasury (no stake) or to the buyback wallet (stake). Reward in YOLO: the treasury part burns. ETH, USDC and IMD go to the buyback wallet; only YOLO burns.

### 6. The Doer Stake
1. Lock: any amount of YOLO for 1-52 weeks. Add and extend, never reduce, no early exit.
2. Power = amount x weeks / 52. Fixed at lock, never drops until the end.
3. Bonus = 4% of the reward x min(1, power / author's reward).
4. Scale: power = reward → +4% = $4 · half → +2% = $2 · 5% → +0.2% = $0.20 · 0 → 0.
5. Counted at submission. At payout the same lock must still run.
6. One lock serves every submission. A fake proof does not touch the lock; the bond is the penalty.
7. Lock, not burn: the YOLO returns to its owner after the term.

### 7. WILL DO / WON'T DO
[story size: vertical]
1. Entry of 100 YOLO: 90 to the side's pool · 5 burn at the outcome · 5 wait for the outcome.
2. Weight = (time left / whole term)², term counted from dare creation. Early entries weigh more.
3. Entries until the deadline, paused while a submission is under review, no withdrawal, open to anyone.
4. Done → WILL DO takes its 90 + the losers' pool by weight. The waiting 5% → 2.5% to the author, 2.5% to the doer.
5. Not done → WON'T DO wins. The waiting 5% burns.
6. Nobody on the winning side: done → the losers' pool half to the author, half to the doer; not done → all to the author. Losers get nothing.
7. Cancelled (Unwound) → every entry back in full.
[example] 100 on WILL DO, 5 on WON'T DO, done → 90 + 4.5 = 94.5.

### 8. Where Every Fee Goes
[sources left; receivers right: 0x…dEaD, BUYBACK WALLET, TREASURY, back to people]
1. Dare fee 10% of the reward → NFT voters / doer bonus / treasury / buyback wallet (ETH, USDC, IMD) / burn (YOLO).
2. YOLO add-on fee 10% of the add-on → the same rule; the treasury part burns.
3. Predict: 5% of every entry → 0x…dEaD at the outcome; the waiting 5% → author and doer, or 0x…dEaD.
4. Trophy: 7,777 YOLO → 0x…dEaD.
5. First-hour tax in YOLO → treasury → burned.
6. Pool fee: 1% of YOLO/IMD pool volume → treasury; its YOLO side → burned.
7. Loser bonds → winners and NFT voters. Swarm fees → the swarm.
8. Burn button: YOLO to 0x…dEaD. Send button: ETH, USDC, IMD to the buyback wallet. Anyone can press, no reward for pressing.
[layout] The line from the buyback wallet onward is dashed and labelled "by hand".

### 9. YOLO Supply and Unlocks
[bars, not a pie]
1. 1,000,000,000 YOLO. No owner, no mint, no pause.
2. Incentives 25% = 250,000,000: 62,500,000 at launch, the rest over 24 months.
3. Treasury 22.2222223% = 222,222,223: 74,074,074 at launch, the rest over 12 months.
4. Liquidity 15% = 150,000,000: in the pool, locked forever.
5. Stabilizer / MM fund 15% = 150,000,000: at launch.
6. Swarm 10% = 100,000,000: at launch.
7. Dev 7.7777777% = 77,777,777 and Future team 5% = 50,000,000: over 12 months, no cliff.
8. Unlocked: day 0 54% · month 6 72% · month 12 91% · month 24 100%.
[footnote] Vestings have no owner and cannot be sped up. No mechanic pays out of a fund.

### 10. The Launch Hour
[vertical time axis 0 → 60 min]
1. Before openAt: no trading. openAt is at most 30 days after deploy.
2. Minutes 0-30: only wallets in the NFT holder snapshot buy, 500,000 YOLO per NFT for the whole window. No buy tax. Every sell pays 30%.
3. Minutes 30-60: everyone buys. Buy and sell tax falls in a straight line from 30% to 0% at minute 60.
4. Minute 60+: a plain ERC-20, no tax, no limits.
5. The tax is in YOLO → treasury → burned.
[example] Sell 1,000 YOLO at 30%: 700 to the pool, 300 tax. At most 70% of a balance can be sold in the window.

### 11. Who's Who
[8 role tiles: can / pays / can get]
1. Author: posts a dare, can also do it. Pays the reward. Can get: the reward back (not done or cancelled), 2.5% of entries, half or all of an empty-side pool.
2. Doer: submits proof with reasons. Pays a bond. Can get: 90% of the reward (up to 94% with a stake), 2.5% of entries.
3. Disputer: disputes a submission. Pays a bond. Can get: the loser's bond (50% or 100%).
4. NFT holder: votes with each NFT. Pays gas. Can get: 5% of the reward and half the loser's bond when voting right.
5. Predictor: enters WILL DO or WON'T DO. Pays YOLO. Can get: its 90 back + the losers' pool by weight.
6. Swarm caller: calls the swarm. Pays a bond + 0.5 IMD. Can get: what the winning side gets.
7. IMD swarm: judges appeals. Gets the call fee.
8. Dev wallet: cancels a dare (everything back to whoever paid it in). Gets nothing.
[footnote] The treasury pays nothing for the mechanics.

### 12. Contract Map
[4 tiers = 4 launches; money as gold arrows, calls as grey arrows]
1. Launch 0: NftGate, 4 vestings, YoloSplitter (project YOLO only).
2. Launch 1: YoloToken, DevPrices, swap adapter, ParamsRegistry, TextRules, SwarmQuestion, VotePower, AttestationChecker, BuybackBurner.
3. Launch 2 (core): YoloLockHub (stakes), CaseDesk, DisputeDesk, TaskVault (rewards and bonds; users talk only to it).
4. Launch 3: YoloSweetener (add-ons), TrophyCatalog, DareTrophy, ProtocolDirectory, HiddenList, YoloPredict (entries).
5. Outside: IMD swarm (Intake); treasury, buyback and dev wallets.
6. No server, no keeper. Each step is done by whoever calls it. Each launch fits 16,777,216 gas.
