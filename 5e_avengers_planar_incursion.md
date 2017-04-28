# Avengers Planar Incursion

## Summary

An Avengers one-shot using Tribality's [5E Avengers Builds](http://tribality.com/2015/05/03/avengers-assemble-character-builds-for-dd-5e).

## Setting

[Hammerfast](http://nentirvale.wikidot.com/hammerfast), in the [Nentir Vale](http://nentirvale.wikidot.com/setting).

I've wanted to run Mike Mearls' "Hammerfast" supplement for years, and the Avengers need a good, fleshed-out urban environment for their adventures.

## Hook

Mission from god(s).

Since this is a one-shot, the Avengers are already a team, members of "The Holy Order of the Shield." They're sent to Hammerfast by Abbot Nicholas the Furious to investigate a planar incursion detected by the seers.

## DM Notes

* Kleitos Caiside, a bitter warlock, briefly opened a portal during a ritual gone awry.
* A symbiotic entity slipped through, joined with Kleitos, and turned his bitterness into homicidal rage.
* The symbiote is using Kleitos to wreak havoc on this plane, sewing thieves, bandits, and wretches with its offspring.
* The symbiote offspring that Kleitos implanted in his first victim--his former manservant--is near full maturity. See the henchman under "Villains."
* Other, less mature, symbiote offspring are causing problems in Hammerfast as well. See the minions under "Villains."
* Are these symbiots on a cheerful, bloody rampage, sewing terror throughout Hammerfast? Or is the parent symbiote/Kleitos playing it safe and keeping the minions under wraps (but still with minor killings here and there), sewing more rumors than terror? You decide!

## Plot

Search and destroy.
The PCs will follow the trail of bodies and/or follow their investigation with city officials to eventually discover a group of minions, then the main henchman, then the super-villain himself.

## Villains

[Carnage](https://en.wikipedia.org/wiki/Carnage_\(comics\)).

I wanted a Marvel villain that's instantly recognizable, but hasn't been done in the Marvel Cinematic Universe, so I chose Carnage.

* **Carnage** (Yochlol; MM p.65; CR 10; 5,900XP) Carnage is a yochlol in stats and abilities only. Any flavor text or visual descriptions of the yochlol should be changed to fit Carnage's description.
* **[Symbiote](https://en.wikipedia.org/wiki/Symbiote_\(comics\))** (Black Pudding; MM p.241; CR 4; 1,100XP) The symbiote is only fought after Carnage is defeated. A surprise "part II" to the big bad boss fight. If the players have trouble beating carnage, the DM could lower the sybiote's starting hit points, or even omit this battle.
* **Henchman** (Chain Devil; MM p.72; CR 8; 3,900XP) The main henchman--perhaps [Doppelganger](https://en.wikipedia.org/wiki/Doppelganger_\(comics\))--should be flavorfully altered on the fly... chains become webbing, for example.
* **Minion** (Ghast; MM p.148; CR 2; 450XP) Thugs and thieves taken over by weaker offspring of the symbiote.

## Notes

* **Be flexible.** This is a one-shot, and it should be highly PC-driven. Keep them "on task" (search and destroy the planar entity), but give them free reign within that task. If they want to hit the taverns and look for rumors, why not? If they want to have meetings with city officials, sure! As long as the clues they get lead them to an encounter with with the minions, and as long as all roads lead to Carnage, reward their actions! In my estimation, the only real sin a player can commit in a one-shot is inaction.
* **Build urgency.** If your PCs waffle on their next action, or get into protracted arguments about what's next, describe the horrific atrocities committed by the villains during the PC's inaction.
* **Make encounters harder on the fly.** Start the minion encounter with one minion for each PC, and then have more minions join the fray based on how ably your PCs navigate their 12th-level pre-gens. Add minions to the Henchman or Carnage encounters as you see fit.
* **Make encounters easier on the fly.** The DMG advises 3,000 XP in an encounter for 4 12th-level PCs. I can't imagine that the Carnage encounter will be that hard for 4 12th-level PCs, but the Yochlol is technically 5,900 XP. Shave hit points or omit abilities to keep from overwhelming PCs.

## Feedback

I haven't had a chance to playtest this yet. I've not played 5E above 7th-level yet, so I'm not entirely sure on how to gage the thread a Yolchol or Chain Devil would pose to those 12th-level pregens. Any thoughts on that?

Any other thoughts/ideas/soundbites that could add those "Marvel" touches to this one-shot?

Thanks for thoughts, and I hope you can use the framework for a fun one-shot.


{
"name": "Chain Devil",
"size": "Medium",
"type": "fiend",
"subtype": "devil",
"alignment": "lawful evil",
"armor_class": 16,
"hit_points": 85,
"hit_dice": "10d8",
"speed": "30 ft.",
"strength": 18,
"dexterity": 15,
"constitution": 18,
"intelligence": 11,
"wisdom": 12,
"charisma": 14,
"damage_vulnerabilities": "",
"damage_resistances": "cold; bludgeoning, piercing, and slashing from nonmagical weapons that aren't silvered",
"damage_immunities": "fire, poison",
"condition_immunities": "poisoned",
"senses": "darkvision 120 ft., passive Perception 8",
"languages": "Infernal, telepathy 120 ft.",
"challenge_rating": "11",
"special_abilities": [
{
"name": "Devil's Sight",
"desc": "Magical darkness doesn't impede the devil's darkvision.",
"attack_bonus": 0
},
{
"name": "Magic Resistance",
"desc": "The devil has advantage on saving throws against spells and other magical effects.",
"attack_bonus": 0
}
],
"actions": [
{
"name": "Multiattack",
"desc": "The devil makes two attacks with its chains.",
"attack_bonus": 0
},
{
"name": "Chain",
"desc": "Melee Weapon Attack: +8 to hit, reach 10 ft., one target. Hit: 11 (2d6 + 4) slashing damage. The target is grappled (escape DC 14) if the devil isn't already grappling a creature. Until this grapple ends, the target is restrained and takes 7 (2d6) piercing damage at the start of each of its turns.",
"attack_bonus": 8,
"damage_dice": "2d6",
"damage_bonus": 4
},
{
"name": "Animate Chains (Recharges after a Short or Long Rest)",
"desc": "Up to four chains the devil can see within 60 feet of it magically sprout razor-edged barbs and animate under the devil's control, provided that the chains aren't being worn or carried.\nEach animated chain is an object with AC 20, 20 hit points, resistance to piercing damage, and immunity to psychic and thunder damage. When the devil uses Multiattack on its turn, it can use each animated chain to make one additional chain attack. An animated chain can grapple one creature of its own but can't make attacks while grappling. An animated chain reverts to its inanimate state if reduced to 0 hit points or if the devil is incapacitated or dies.",
"attack_bonus": 0
}
],
"reactions": [
{
"name": "Unnerving Mask",
"desc": "When a creature the devil can see starts its turn within 30 feet of the devil, the devil can create the illusion that it looks like one of the creature's departed loved ones or bitter enemies. If the creature can see the devil, it must succeed on a DC 14 Wisdom saving throw or be frightened until the end of its turn.",
"attack_bonus": 0
}
]
},


{
"name": "Black Pudding",
"size": "Large",
"type": "ooze",
"subtype": "",
"alignment": "unaligned",
"armor_class": 7,
"hit_points": 85,
"hit_dice": "10d10",
"speed": "20 ft., climb 20 ft.",
"strength": 16,
"dexterity": 5,
"constitution": 16,
"intelligence": 1,
"wisdom": 6,
"charisma": 1,
"damage_vulnerabilities": "",
"damage_resistances": "",
"damage_immunities": "acid, cold, lightning, slashing",
"condition_immunities": "blinded, charmed, deafened, exhaustion, frightened, prone",
"senses": "blindsight 60 ft. (blind beyond this radius), passive Perception 8",
"languages": "",
"challenge_rating": "4",
"special_abilities": [
{
"name": "Amorphous",
"desc": "The pudding can move through a space as narrow as 1 inch wide without squeezing.",
"attack_bonus": 0
},
{
"name": "Corrosive Form",
"desc": "A creature that touches the pudding or hits it with a melee attack while within 5 feet of it takes 4 (1d8) acid damage. Any nonmagical weapon made of metal or wood that hits the pudding corrodes. After dealing damage, the weapon takes a permanent and cumulative -1 penalty to damage rolls. If its penalty drops to -5, the weapon is destroyed. Nonmagical ammunition made of metal or wood that hits the pudding is destroyed after dealing damage. The pudding can eat through 2-inch-thick, nonmagical wood or metal in 1 round.",
"attack_bonus": 0,
"damage_dice": "1d8"
},
{
"name": "Spider Climb",
"desc": "The pudding can climb difficult surfaces, including upside down on ceilings, without needing to make an ability check.",
"attack_bonus": 0
}
],
"actions": [
{
"name": "Pseudopod",
"desc": "Melee Weapon Attack: +5 to hit, reach 5 ft., one target. Hit: 6 (1d6 + 3) bludgeoning damage plus 18 (4d8) acid damage. In addition, nonmagical armor worn by the target is partly dissolved and takes a permanent and cumulative -1 penalty to the AC it offers. The armor is destroyed if the penalty reduces its AC to 10.",
"attack_bonus": 5,
"damage_dice": "1d6 + 4d8",
"damage_bonus": 3
}
],
"reactions": [
{
"name": "Split",
"desc": "When a pudding that is Medium or larger is subjected to lightning or slashing damage, it splits into two new puddings if it has at least 10 hit points. Each new pudding has hit points equal to half the original pudding's, rounded down. New puddings are one size smaller than the original pudding.",
"attack_bonus": 0
}
]
},


{
"name": "Phase Spider",
"size": "Large",
"type": "monstrosity",
"subtype": "",
"alignment": "unaligned",
"armor_class": 13,
"hit_points": 32,
"hit_dice": "5d10",
"speed": "30 ft., climb 30 ft.",
"strength": 15,
"dexterity": 15,
"constitution": 12,
"intelligence": 6,
"wisdom": 10,
"charisma": 6,
"stealth": 6,
"damage_vulnerabilities": "",
"damage_resistances": "",
"damage_immunities": "",
"condition_immunities": "",
"senses": "darkvision 60 ft., passive Perception 10",
"languages": "",
"challenge_rating": "3",
"special_abilities": [
{
"name": "Ethereal Jaunt",
"desc": "As a bonus action, the spider can magically shift from the Material Plane to the Ethereal Plane, or vice versa.",
"attack_bonus": 0
},
{
"name": "Spider Climb",
"desc": "The spider can climb difficult surfaces, including upside down on ceilings, without needing to make an ability check.",
"attack_bonus": 0
},
{
"name": "Web Walker",
"desc": "The spider ignores movement restrictions caused by webbing.",
"attack_bonus": 0
}
],
"actions": [
{
"name": "Bite",
"desc": "Melee Weapon Attack: +4 to hit, reach 5 ft., one creature. Hit: 7 (1d10 + 2) piercing damage, and the target must make a DC 11 Constitution saving throw, taking 18 (4d8) poison damage on a failed save, or half as much damage on a successful one. If the poison damage reduces the target to 0 hit points, the target is stable but poisoned for 1 hour, even after regaining hit points, and is paralyzed while poisoned in this way.",
"attack_bonus": 4,
"damage_dice": "1d10",
"damage_bonus": 2
}
]
},


{
"name": "Ghast",
"size": "Medium",
"type": "undead",
"subtype": "",
"alignment": "chaotic evil",
"armor_class": 13,
"hit_points": 36,
"hit_dice": "8d8",
"speed": "30 ft.",
"strength": 16,
"dexterity": 17,
"constitution": 10,
"intelligence": 11,
"wisdom": 10,
"charisma": 8,
"damage_vulnerabilities": "",
"damage_resistances": "",
"damage_immunities": "necrotic",
"condition_immunities": "poisoned",
"senses": "darkvision 60 ft., passive Perception 10",
"languages": "Common",
"challenge_rating": "2",
"special_abilities": [
{
"name": "Stench",
"desc": "Any creature that starts its turn within 5 ft. of the ghast must succeed on a DC 10 Constitution saving throw or be poisoned until the start of its next turn. On a successful saving throw, the creature is immune to the ghast's Stench for 24 hours.",
"attack_bonus": 0
},
{
"name": "Turn Defiance",
"desc": "The ghast and any ghouls within 30 ft. of it have advantage on saving throws against effects that turn undead.",
"attack_bonus": 0
}
],
"actions": [
{
"name": "Bite",
"desc": "Melee Weapon Attack: +3 to hit, reach 5 ft., one creature. Hit: 12 (2d8 + 3) piercing damage.",
"attack_bonus": 3,
"damage_dice": "2d8",
"damage_bonus": 3
},
{
"name": "Claws",
"desc": "Melee Weapon Attack: +5 to hit, reach 5 ft., one target. Hit: 10 (2d6 + 3) slashing damage. If the target is a creature other than an undead, it must succeed on a DC 10 Constitution saving throw or be paralyzed for 1 minute. The target can repeat the saving throw at the end of each of its turns, ending the effect on itself on a success.",
"attack_bonus": 5,
"damage_dice": "2d6",
"damage_bonus": 3
}
]
},


{
"name": "Bandit",
"size": "Medium",
"type": "humanoid",
"subtype": "any race",
"alignment": "any non-lawful alignment",
"armor_class": 12,
"hit_points": 11,
"hit_dice": "2d8",
"speed": "30 ft.",
"strength": 11,
"dexterity": 12,
"constitution": 12,
"intelligence": 10,
"wisdom": 10,
"charisma": 10,
"damage_vulnerabilities": "",
"damage_resistances": "",
"damage_immunities": "",
"condition_immunities": "",
"senses": "passive Perception 10",
"languages": "any one language (usually Common)",
"challenge_rating": "1/8",
"actions": [
{
"name": "Scimitar",
"desc": "Melee Weapon Attack: +3 to hit, reach 5 ft., one target. Hit: 4 (1d6 + 1) slashing damage.",
"attack_bonus": 3,
"damage_dice": "1d6",
"damage_bonus": 1
},
{
"name": "Light Crossbow",
"desc": "Ranged Weapon Attack: +3 to hit, range 80 ft./320 ft., one target. Hit: 5 (1d8 + 1) piercing damage.",
"attack_bonus": 3,
"damage_dice": "1d8",
"damage_bonus": 1
}
]
},


{
"name": "Gladiator",
"size": "Medium",
"type": "humanoid",
"subtype": "any race",
"alignment": "any alignment",
"armor_class": 16,
"hit_points": 112,
"hit_dice": "15d8",
"speed": "30 ft.",
"strength": 18,
"dexterity": 15,
"constitution": 16,
"intelligence": 10,
"wisdom": 12,
"charisma": 15,
"strength_save": 7,
"dexterity_save": 5,
"constitution_save": 6,
"athletics": 10,
"intimidation": 5,
"damage_vulnerabilities": "",
"damage_resistances": "",
"damage_immunities": "",
"condition_immunities": "",
"senses": "passive Perception 11",
"languages": "any one language (usually Common)",
"challenge_rating": "5",
"special_abilities": [
{
"name": "Brave",
"desc": "The gladiator has advantage on saving throws against being frightened.",
"attack_bonus": 0
},
{
"name": "Brute",
"desc": "A melee weapon deals one extra die of its damage when the gladiator hits with it (included in the attack).",
"attack_bonus": 0
}
],
"actions": [
{
"name": "Multiattack",
"desc": "The gladiator makes three melee attacks or two ranged attacks.",
"attack_bonus": 0
},
{
"name": "Spear",
"desc": "Melee or Ranged Weapon Attack: +7 to hit, reach 5 ft. and range 20/60 ft., one target. Hit: 11 (2d6 + 4) piercing damage, or 13 (2d8 + 4) piercing damage if used with two hands to make a melee attack.",
"attack_bonus": 7,
"damage_dice": "2d6",
"damage_bonus": 4
},
{
"name": "Shield Bash",
"desc": "Melee Weapon Attack: +7 to hit, reach 5 ft., one creature. Hit: 9 (2d4 + 4) bludgeoning damage. If the target is a Medium or smaller creature, it must succeed on a DC 15 Strength saving throw or be knocked prone.",
"attack_bonus": 7,
"damage_dice": "2d4",
"damage_bonus": 4
}
],
"reactions": [
{
"name": "Parry",
"desc": "The gladiator adds 3 to its AC against one melee attack that would hit it. To do so, the gladiator must see the attacker and be wielding a melee weapon.",
"attack_bonus": 0
}
]
},
