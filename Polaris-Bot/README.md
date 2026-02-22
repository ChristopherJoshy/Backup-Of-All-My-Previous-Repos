# Polaris

A Discord bot for snowball combat with RPG progression, gambling, and a friendly Santa chat.

---

## What is Polaris?

Polaris turns your Discord server into a snowball arena. Players throw snowballs at each other, earn Icicles (currency), level up to unlock better weapons, and compete on leaderboards.

---

## Commands

| Command | Description |
|---------|-------------|
| `/throw @user` | Attack another player |
| `/stats` | View your profile |
| `/stats @user` | View someone else's profile |
| `/inventory` | See your weapons and equip them |
| `/shop` | Buy healing items, buffs, and gear |
| `/gamble` | Play slots or challenge someone to coin flip |
| `/daily` | Claim daily Icicles reward |
| `/leaderboard` | See top players |
| `/help` | Full guide with all features |
| `@Polaris [message]` | Chat with Santa |

---

## Combat

Use `/throw @user` to attack. Each throw has a chance to:

| Outcome | Chance | Effect |
|---------|--------|--------|
| Hit | 75% | Normal damage |
| Critical | 5% | Double damage |
| Miss | 15% | No damage |
| Fumble | 5% | Hit yourself |

When you hit someone, you earn:
- **2-5 Icicles** per hit
- **XP equal to damage dealt**

When you knock someone out (reduce to 0 HP), you earn:
- **+25 bonus Icicles**
- **Kill added to your stats**

The victim respawns with full HP.

---

## Weapons

Weapons unlock as you level up. Higher level = more damage.

| Level | Weapon | Damage Range |
|-------|--------|--------------|
| 1 | Snowball | 5-12 |
| 3 | Packed Snow | 10-18 |
| 6 | Ice Ball | 14-24 |
| 10 | Ice Bomb | 18-30 |
| 15 | Avalanche | 25-40 |
| 20 | Blizzard Ball | 32-50 |
| 30 | Permafrost | 40-60 |
| 50 | Absolute Zero | 50-75 |

Use `/inventory` to view unlocked weapons and equip them.

---

## Leveling Up

You gain XP from combat damage. The XP needed for each level is `level * 100`.

When you level up, you may unlock:
- New weapons
- Icicle rewards (50-2500 depending on level)
- Free items at milestones (shield at Lv5, cannon at Lv15, etc.)

---

## Shop

Use `/shop` to buy items. All items cost Icicles.

### Healing
| Item | Cost | Effect |
|------|------|--------|
| Hot Cocoa | 10 | +25 HP |
| Healing Surge | 25 | +50 HP |
| Full Restore | 50 | Restore to max HP |

### Buffs
| Item | Cost | Effect |
|------|------|--------|
| Energy Drink | 30 | +50% damage on next hit |
| XP Boost | 40 | 2x XP for 5 hits |
| Lucky Charm | 35 | +10% crit chance for 5 hits |

### Gear
| Item | Cost | Effect |
|------|------|--------|
| Frost Shield | 40 | Blocks 1 incoming attack |
| Ice Armor | 75 | -25% damage taken for 5 hits |
| Cannon | 80 | +8 damage for 10 hits |
| Ice Fortress | 100 | Permanently +15 max HP |

---

## Gambling

Use `/gamble` to access gambling features. Minimum bet is 5 Icicles.

### Slot Machine
Solo game. Bet your Icicles and spin.

| Result | Payout |
|--------|--------|
| No match | Lose bet |
| 2 matching | 1.5x bet |
| 3 matching | 3x bet |
| 3 stars | 5x bet |
| 3 diamonds | 10x bet (JACKPOT) |

### Coin Flip
1v1 game. Challenge another player by entering their user ID.

Both players bet the same amount. A coin is flipped and the winner takes the entire pot. The loser loses their bet.

---

## Daily Rewards

Use `/daily` every day to claim free Icicles. Coming back on consecutive days builds your streak for bigger rewards.

| Streak | Reward |
|--------|--------|
| Day 1 | 15 Icicles |
| Day 2 | 30 Icicles |
| Day 3 | 50 Icicles + bonus |
| Day 7 | 150 Icicles + mystery box |
| Day 14 | 350 Icicles + rare item |
| Day 30 | 750 Icicles + legendary |

Missing a day resets your streak to 1.

---

## Achievements

Unlock achievements for bonus Icicles:

| Achievement | Requirement | Reward |
|-------------|-------------|--------|
| First Blood | Get your first knockout | 50 |
| Daily Warrior | 7-day login streak | 500 |
| Big Spender | Spend 1000 Icicles | 200 |
| High Roller | Win 500+ from slots | 250 |
| Lucky Flip | Win 10 coin flips | 200 |
| Survivor | Survive with 1 HP | 100 |

---

## Santa Chat

Mention the bot (`@Polaris`) followed by a message to chat with Santa. Responses are concise and cheerful.

---

## Setup

**Requirements**: Python 3.10+

```bash
pip install -r requirements.txt
```

Create `.env` file:
```
DISCORD_TOKEN=your_discord_bot_token
GEMINI_API_KEY=your_gemini_api_key
```

Run:
```bash
python bot.py
```

---

Built by Christopher Joshy
