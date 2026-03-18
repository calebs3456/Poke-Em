# Poke-Em
A PvP Poker Game

# Cash Duel

A competitive poker-engine builder inspired by Balatro, built around **shared luck, asymmetric decisions, and economic warfare**.

## High concept

Two players enter the same casino duel with:

* the same starting deck
* the same shared shop offers
* the same public poker information

The difference comes from **what they buy, what they upgrade, and when they attack or defend**.

Players are not trying to reduce a separate HP bar. Instead, **cash is everything**:

* your life total
* your spending resource
* the thing your opponent is trying to steal, burn, tax, or cap

If your cash reaches **0**, you lose.

---

## Core pillars

### 1. Shared luck, different choices

Both players see the same shop each round and play under the same poker conditions. The game is meant to feel fair and competitive: players lose because of decisions, not because the RNG favored the other side.

### 2. Poker as the scoring language

Rounds resolve through a Texas Hold'em-inspired showdown. Familiar poker hand rankings give the game an immediately understandable backbone.

### 3. Economy is combat

Offensive and defensive effects mostly target **cash flow**, not raw hand scoring. Players pressure each other by stealing chips, reducing payouts, taxing income, or shielding themselves from those effects.

### 4. Short, tense matches

Matches should be fast, readable, and highly replayable, with enough room for scaling, aggression, and comeback turns.

---

## Match overview

Each player starts with:

* **20 Cash**
* **3 Income**
* a basic starting build
* no upgrades

### Win conditions

A player loses immediately when their **Cash reaches 0**.

If both players survive until the final round, the player with the **higher Cash total** wins.

### Match length

Recommended MVP length:

* **8 rounds max**

This keeps the game sharp and prevents passive turtling.

---

## Round economy

The round economy is the core of the game.

Each round, players gain chips from two sources:

1. **Guaranteed income**
2. **Showdown payout**

This keeps the game from becoming overly snowbally while still making poker wins matter.

### Cash

Cash is the central resource.

It is used for:

* buying cards
* buying upgrades
* paying taxes or penalties
* surviving attacks

If Cash reaches 0, that player dies.

### Income

Income is guaranteed round-based earnings.

Each round, both players gain chips equal to their current Income value.

Example:

* Player A Income: 3
* Player B Income: 5

At the start of the round:

* Player A gains 3 Cash
* Player B gains 5 Cash

Income is the safest long-term scaling axis in the game.

### Showdown payout

After the poker showdown, the player with the better hand receives a **showdown payout** based on hand strength.

The losing player receives **no showdown payout** by default.

If both players tie exactly, they **split the showdown payout**.

This means rounds are not completely winner-takes-all, because both players still receive guaranteed Income, but poker wins still feel meaningful.

---

## Recommended payout table

Base showdown payout by winning hand:

| Winning hand    | Payout |
| --------------- | -----: |
| High Card       |      0 |
| One Pair        |      1 |
| Two Pair        |      2 |
| Three of a Kind |      3 |
| Straight        |      4 |
| Flush           |      4 |
| Full House      |      5 |
| Four of a Kind  |      6 |
| Straight Flush  |      8 |

### Payout rule

* Both players gain **Income** first.
* The player with the better poker hand gains the **full showdown payout** for their winning hand.
* The losing player gains **0 showdown payout**.
* On an exact tie, both players split the payout.

Example:

* both players gain Income
* Player A wins with Two Pair
* Two Pair payout is 2
* Player A gains +2 Cash
* Player B gains +0 Cash

Tie example:

* both players make the same Straight
* Straight payout is 4
* each player gains +2 Cash

This structure keeps the showdown exciting without shutting the loser out of the round entirely.

---

## Why this economy works

### It avoids hard snowballing

If rounds were fully winner-takes-all, the richer player would often win more hands, gain more money, buy more upgrades, and run away with the match.

By separating **Income** from **showdown payout**, the game gives trailing players enough resources to keep making meaningful decisions.

### It preserves tension

The showdown still matters because only the winner gets the bonus.

### It creates strategic identities

Players can choose between:

* scaling Income
* maximizing showdown payouts
* attacking the opponent's economy
* defending against disruption

---

## Full round flow

Each round resolves in this order:

### 1. Income phase

Both players gain Cash equal to their Income stat.

### 2. Shared market phase

Reveal **5 shared shop options**.

Both players see the same 5 cards/upgrades.
Each player may buy from the offer independently.

This preserves the shared-luck principle.

### 3. Upgrade phase

Players may spend Cash on permanent upgrades.

Recommended upgrade tracks:

* **Income**: gain more Cash each round
* **Scoring**: improve showdown payouts for certain hands
* **Offense**: strengthen attack effects
* **Defense**: improve shields, blocks, and protection

### 4. Play phase

Players resolve a Texas Hold'em-inspired showdown.

For MVP, use poker hand ranking as the main scoring language.

### 5. Effect resolution phase

Attack and defense effects resolve in a fixed order.

Recommended order:

1. passive defense effects apply
2. offensive debuffs apply
3. reactive defense effects trigger
4. final showdown payout is calculated
5. cash gain/loss from effects is applied

### 6. End phase

Temporary effects expire.
Check defeat conditions.
If neither player has died and the match has not reached round limit, begin next round.

---

## Hold'em-inspired play phase

The poker phase should feel familiar, but it does not need full real-world betting and bluffing.

In this game, poker is primarily the **showdown engine**, not the entire game.

That means:

* standard poker hand rankings remain recognizable
* upgrades and effects determine how profitable certain hands are
* attacks and defenses influence cash results before or after payout

The exact dealing format can be finalized later, but the intended direction is:

* both players operate under the same public conditions
* both players have equivalent access to luck
* differences come from builds and tactical effects

---

## Card families

The game should be built around a few clear card families.

### Scoring cards

These improve how much value you get from poker hands.

Examples:

* Pairs pay +1
* Flushes pay +2
* Face cards give bonus payout
* Straights become easier to monetize

### Offensive cards

These pressure the opponent's economy.

Examples:

* steal cash
* burn cash
* reduce next round Income
* cap opponent showdown payout
* increase shop costs

### Defensive cards

These protect your economy.

Examples:

* shield cash loss
* block one debuff
* reflect one debuff
* protect Income from reduction
* guarantee a minimum payout on loss

### Economy cards

These improve resource flow directly.

Examples:

* gain +1 Income permanently
* discounts on purchases
* bonus cash for saving
* bonus cash if not attacked

### Utility cards

These improve consistency or control.

Examples:

* redraw support
* preview future offers
* duplicate a temporary effect
* improve upgrade efficiency

---

## Upgrade board

The upgrade board should be simple and legible.

### Income track

Improves guaranteed chips per round.

Example levels:

* 3 -> 4 -> 5 -> 6

### Scoring track

Improves showdown value.

Example effects:

* One Pair pays +1
* Flush pays +1
* winning with face cards grants +1 Cash

### Offense track

Improves attacks.

Example effects:

* Steal +1 extra Cash
* taxes are harder to block
* first attack each round costs 1 less

### Defense track

Improves protection.

Example effects:

* Shield +1 additional Cash
* first debuff each round is weakened
* Income cannot be reduced once per match

---

## Economy design rules

These rules should guide balancing.

### 1. Guaranteed income should never fully disappear

Players should usually have at least a small minimum guaranteed income floor. This prevents total lockouts.

### 2. Most disruption should be temporary

Effects that steal, tax, cap, or weaken should usually last for only one round unless they are expensive or rare.

### 3. Direct theft should be limited

Stealing cash is very strong because it both hurts the opponent and helps the attacker. It should be used carefully.

### 4. Defense must be proactive

Players should have access to stable defensive tools instead of relying only on reactive counters.

### 5. Showdown payout should stay modest

Guaranteed Income should be the stable backbone of the economy; showdown payout should be the swing factor, not the whole economy.

---

## Example round

Start of round:

* Player A: 12 Cash, 3 Income
* Player B: 10 Cash, 4 Income

### Income phase

* Player A goes to 15 Cash
* Player B goes to 14 Cash

### Shared market phase

5 shared options are revealed.

Player A buys a scoring upgrade.
Player B buys an attack card.

### Play phase

* Player A makes One Pair
* Player B makes a Flush

### Showdown payout

* One Pair payout = 1
* Flush payout = 4
* Player B has the stronger hand

Result:

* Player B gains +4 Cash
* Player A gains +0 showdown Cash

### Effect resolution

If Player B also played an effect like "Steal 1 on showdown win," it resolves here.

Possible end state:

* Player A: 14 Cash
* Player B: 19 Cash

This is readable, punchy, and easy to tune.

---

## MVP scope

A strong first prototype should be intentionally small.

### Recommended MVP

* 1v1 only
* 8 rounds
* 20 starting Cash
* 3 starting Income
* Texas Hold'em-inspired showdown
* 5 shared shop options each round
* 4 upgrade tracks
* around 24 total cards:

  * 8 scoring
  * 6 offense
  * 6 defense
  * 4 economy

This is enough to test whether the economy, pressure, and showdown loop are fun.

---

## Project goals for early prototypes

The first playable version should answer these questions:

1. Does shared-luck shopping feel fair and interesting?
2. Is the Income + showdown payout model exciting without snowballing too hard?
3. Are attack and defense effects understandable in the middle of a poker round?
4. Does cash-as-life create good tension?
5. Are 8-round matches the right length?

---

## Future extensions

Potential expansions after the MVP:

* more specialized hand archetypes
* rarer attack/defense cards
* contested shop slots
* seasonal modifiers or round events
* ranked ladder
* spectator support
* 2v2 or tournament mode

---

## Current design summary

**Cash Duel** is a multiplayer poker-engine battler where both players share the same luck but weaponize it differently.

The core loop is:

* gain Income
* buy from the same 5-card market
* improve your economy and hand payouts
* attack or defend against economic disruption
* resolve a Hold'em-style showdown
* bankrupt the opponent before they bankrupt you

It is meant to feel fair, tense, readable, and highly replayable.
