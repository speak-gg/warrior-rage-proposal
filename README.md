# A Better Trade for Normalized Rage

*Bounding warrior scaling in WoW: Forever without losing what makes rage fun.*

**[Read the proposal (PDF)](docs/rage-normalization-proposal.pdf)** · [Google Docs version](https://docs.google.com/document/d/1slDoLsU9cN3qjq9S_-06Ojo53PTH07unQMNqFwH2cWE/edit?usp=sharing) · [Word version (download)](docs/rage-normalization-proposal.docx) · [Data and sim results (Google Sheets)](https://docs.google.com/spreadsheets/d/1qweL-JtXsbx5mTtrQmffD1H3CIoDGQ2Z8uG_fj5_Ahs/edit?usp=sharing) · [Excel version (download)](data/warrior-rage-data.xlsx) · [Modified WarriorSim](https://github.com/speak-gg/guybrushsim-rage-norm)

## The problem

In April 2024, Blizzard designer Josh Greenfield (Aggrend) asked: *"what would be a good trade for some form of normalized rage at 60 if we had to do such a thing?"* WoW: Forever's beta has since replaced Classic's damage-based rage with a fixed amount per swing. That fixes the "more damage = more rage" loop, but it also makes weapon damage and attack power invisible to the rage bar, and it leaves geared warriors with far fewer decisions to make.

## The proposal

1. **Curved rage.** Keep Classic's damage-based formula up to pre-raid gear. Above that, bend rage per swing smoothly toward a cap that scales with swing time, which gives a ceiling of about 1,800–1,900 rage per minute that future gear tiers can't push through. Where diminishing returns start and where the ceiling sits are tunable.
2. **Ability adjustments.** Fix warrior damage at the source:
   - Bloodthirst 40% AP
   - Flurry 35% for 2 swings
   - Death Wish 15%
   - Execute on a 4 second cooldown
   - plus Forever's Unbridled Wrath and two-handed Whirlwind

## Key results

Six gear sets, from pre-raid self-buffed to Naxxramas best-in-slot with world buffs, simulated in a modified [WarriorSim](https://github.com/GuybrushGit/WarriorSim).

| Gear | Forever vs Classic (DPS / rage) | Proposal vs Classic (DPS / rage) |
|---|---|---|
| Pre-raid, raid-buffed | −7% / −32% | −4% / −7% |
| R14 / MC / 20-man | −13% / −44% | −9% / −11% |
| Naxx BiS | −12% / −51% | −5% / −13% |
| Naxx BiS + world buffs | −14% / −61% | −7% / −26% |

At raid gear, the proposal deals about the same damage as Forever (3–9% more) but generates 36–91% more rage. That is two to three times as much rage to spend on decisions beyond the core Bloodthirst + Whirlwind rotation.

## What's here

| Path | What it is |
|---|---|
| `docs/warrior-rage-proposal.pdf` | The full design document |
| `docs/warrior-rage-proposal.docx` | Editable version |
| `data/warrior-rage-data.xlsx` | Every sim result, the rage curve with editable parameters, class-ratio data from Warcraft Logs, sim setup and gear lists |

## Method

- **Sim:** a fork of Guybrush's WarriorSim, extended with:
  - rage tracking;
  - Curved rage;
  - Forever's rage rules, talents and abilities;
  - configurable ability variants.
- **Forever rules:** come from Marrow's Eternal Compendium of Dragonslaying and Blizzard's beta notes, as of 1 October 2026.
- **Class comparisons:** use top Warcraft Logs parses from Classic Anniversary, Era and Season of Mastery.
- **Full setup:** gear, buffs, consumables, fight length and rotation are in Appendix B of the document.

## Credits

- WarriorSim by Guybrush.
- Forever rage research by Marrow.
- Log data from Warcraft Logs.

Full citations are in the document.

Author: speak-gg · speak_gg
