# Keep the Rage, Cap the Scaling

*A better trade for normalized rage in WoW: Forever.*

# **[Read the proposal (PDF)](https://github.com/speak-gg/warrior-rage-proposal/blob/main/docs/rage-normalization-proposal.pdf)**


[Google Docs version](https://docs.google.com/document/d/10ibPxc1XLC9WozjiLiXwyJKh14yadSnQs6exdCGANIU/edit?usp=sharing) · [Data and sim results (Google Sheets)](https://docs.google.com/spreadsheets/d/12UjH0ZSsiMYHGztYJ707mY6k3loAYuTOLrVYlYZoiVc/edit?usp=sharing) · [Modified WarriorSim](https://speak-gg.github.io/guybrushsim-rage-norm/classic.html)

DOWNLOADS: [Word version (download)](https://github.com/speak-gg/warrior-rage-proposal/blob/main/docs/rage-normalization-proposal.docx) · [Excel version (download)](https://github.com/speak-gg/warrior-rage-proposal/blob/main/data/warrior-rage-data.xlsx)

## The problem

In April 2024, Blizzard designer Josh Greenfield (Aggrend) asked: *"what would be a good trade for some form of normalized rage at 60 if we had to do such a thing?"* WoW: Forever's beta has since replaced Classic's damage-based rage with a fixed amount per swing. That stops the "more damage = more rage" loop, but it makes weapon damage and attack power invisible to the rage bar, and in our sims it leaves a Naxx BiS, world-buffed warrior with less rage than a Classic warrior in pre-raid gear.

## The proposal

1. **Keep damage-based rage, but curve its tail end at level 60.** Rage follows Classic's formula up to roughly pre-raid gear, then bends smoothly toward a per-swing cap that scales with swing time. That gives a ceiling of the developers' choosing (for example 1,600–1,800 true rage per minute) that future gear tiers can't push through. The formula's coefficient is raised from 7.5 to 9 at every level, 1–60, to offset the ability nerfs, Forever's changes and the lost racial weapon skill.
2. **Fix warrior damage at the source:**
   - Bloodthirst 45% → 40% AP
   - Death Wish 20% → 15%
   - Execute on a 4 second cooldown
   - plus most of Forever's changes: Unbridled Wrath 60% (white swings only), Flurry 25% for 3 swings, stacking Deep Wounds, +10% off-hand hit from Furious Precision, and Whirlwind hitting with both weapons for 22 rage

## Key results

Six gear sets, from pre-raid self-buffed to Naxxramas best-in-slot with world buffs, simulated in a modified [WarriorSim](https://github.com/GuybrushGit/WarriorSim). 3 minute fight with Execute; Classic at 305 sword skill, Forever and the final proposal at 300.

| Gear | Forever vs Classic (DPS / rage) | Final proposal vs Classic (DPS / rage) |
| --- | --- | --- |
| Pre-raid, self-buffed | +1% / −8% | −4% / +7% |
| Pre-raid, raid-buffed | −9% / −33% | −8% / −22% |
| Pre-raid + world buffs | −14% / −49% | −10% / −27% |
| R14 / MC / 20-man | −11% / −42% | −7% / −17% |
| Naxx BiS | −7% / −50% | −2% / −19% |
| Naxx BiS + world buffs | −9% / −59% | −5% / −37% |

At raid gear, the final proposal deals about as much damage as Forever (1–6% more) but generates 17–60% more rage: up to about two and a half times as much rage to spend on decisions beyond the core Bloodthirst + Whirlwind rotation.

## What's here

| Path | What it is |
| --- | --- |
| `docs/rage-normalization-proposal.pdf` | The full design document |
| `docs/rage-normalization-proposal.docx` | Editable version |
| `data/warrior-rage-data.xlsx` | Every sim result behind the document, the editable rage curve, class-ratio data from Warcraft Logs, sim setup and gear lists. The README tab maps each tab to the section that uses it |

## Method

- **Sim:** a fork of Guybrush's WarriorSim ([source](https://github.com/speak-gg/guybrushsim-rage-norm), [run it in the browser](https://speak-gg.github.io/guybrushsim-rage-norm/classic.html)), extended with:
  * rage tracking;
  * Curved rage;
  * Forever's rage rules, talents, abilities and mechanics (including stacking Deep Wounds and Forever's miss/dodge rules);
  * configurable ability variants.
- **Forever rules:** from the 1 October 2026 beta build notes, beta logs, and Marrow's Eternal Compendium of Dragonslaying.
- **Class comparisons:** top Warcraft Logs parses from Classic Anniversary, Era and Season of Mastery.
- **Full setup:** gear, buffs, consumables, fight length and rotation are in Appendix B of the document.

## Credits

- WarriorSim by Guybrush.
- Forever rage research by Marrow.
- Log data from Warcraft Logs.

Full citations are in the document.

Author: speak-gg · speak_gg
