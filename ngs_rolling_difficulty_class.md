Rolling Difficulty Class
========================

__An alternate way to establish _Difficulty Class_ (DC) for _Unopposed Rolls_ in the [Narrative Game System](http://rpg.drivethrustuff.com/product/128522/NGS-The-Narrative-Game-System) by [Venture Land Games](http://www.venturelandgames.com).__



Contents
--------

* [Summary](#summary)
* [Detail](#detail)
* [Rolled Difficulty Class Table](#rolled-difficulty-class-table)
* [Methodology](#methodology)
* [License](#license)



Summary
-------

This essay describes a house rule for rolling the DC on an _Unopposed Roll_.



Detail
------

Tired of picking an arbitrary number for your players' _Unopposed Rolls_?

Roll a die, instead!

I don't do this all the time, but if I'm not sure how well that guard is paying attention... or I wasn't sure how hard that lock would be to pick under pressure... then I'll roll the DC! _Then_ I'll describe the scene.

>__Player:__ "Hey, I want to sneak past that guard."
>__Game Master:__ "Sure! Sneaking isn't in your wheelhouse, so I'm going require a roll. How are you sneaking in? You can use _Physicality_ to 'cat-burglar' your way in. You can use _Intellect_ to time the patrols and identify that perfect moment to walk on in. Or you can use _Personality_ to try to talk the guards into letting you in."
>__Player:__ "_Physicality_ for sure! What do I need to roll?"
>__Game Master:__ "You know, I'm not sure. Hang on." Rolls a d12, get a 7. "You need to hit a 7. These guards have been guarding this place for months, and nothing ever happens. The last thing they're expecting is for someone to actually try and sneak in..."

As you'll see below, players will succeed _most_ of the time.

|  Die  | Average DC | 50% Success |
|------:|-----------:|:------------|
| __d6__|     3.5    |     Any     |
| __d8__|     4.5    |     Any     |
|__d10__|     5.5    |    d6+2     |
|__d12__|     6.5    |    d6+3     |



Rolled Difficulty Class Table
-----------------------------

|         |  d6 |  d8 | d10 | d12 |
|--------:|:---:|:---:|:---:|:---:|
| __d6+1__| 72% | 56% | 45% | 38% |
| __d6+2__| 83% | 69% | 55% | 46% |
| __d6+3__| 92% | 79% | 65% | 54% |
| __d6+4__| 97% | 88% | 75% | 63% |
| __d8+1__| 79% | 67% | 55% | 46% |
| __d8+2__| 88% | 77% | 65% | 54% |
| __d8+3__| 94% | 84% | 74% | 63% |
| __d8+4__| 98% | 91% | 81% | 71% |
|__d10+1__| 83% | 74% | 64% | 54% |
|__d10+2__| 90% | 81% | 72% | 63% |
|__d10+3__| 95% | 88% | 79% | 70% |
|__d10+4__| 98% | 93% | 85% | 77% |
|__d12+1__| 86% | 78% | 70% | 62% |
|__d12+2__| 92% | 84% | 77% | 69% |
|__d12+3__| 96% | 90% | 83% | 75% |
|__d12+4__| 99% | 94% | 88% | 81% |



Methodology
-----------
I wrote the following custom function in Excel to calculate the results of all possible rolls against a _DC_:

    Function AverageUnopposedDiePercent(Die As Byte, Modifier As Byte, Difficulty As Byte) As Double
        'PURPOSE:
            'To output the likelihood (%) for an unopposed roll in the Narrative Game System (NGS) by Venture Land Games.
        'VERSION (Version Number, YYYY.MM.DD)
            '1.0, 2016.04.04: First working model.
        'AUTHOR
            'Dustinian Camburides
            'dustinian@dustinian.com
            'www.dustinian.com
        'LANGUAGE
            'Excel VBA, but the syntax used would easily convert to another flavor of Basic (FreeBASIC, for example).
        'INPUT:
            'Die: The number of faces the attacking die has (i.e. "6" for a "d6")
            'Modifier: The attacking numerical priority (i.e. "4" for "Priority A")
            'Difficulty: The difficulty class of the environment (unopposed) roll.
        'USE:
            'To use this function in your own Excel workbook:
                '1. Create a macro-enabled workbook (.xlsm from Excel 2007 and on).
                '2. Bring up the "Visual Basic" interface by holding "Alt" and pressing "F11."
                '3. Create a new "module."
                '4. Paste this code into the module. You can now call this function from your Excel worksheet.
                '5. Call the function by entering a formula like this:
                    'Use this to calculate a d8+3 against DC of 6: =AverageUnopposedDiePercent(8, 3, 6)
                    'Use this to reference cells with the die and priorities: =AverageUnopposedDiePercent(A2, B2, C2)
        'VARIABLES
            Dim intCurrentDieRoll As Integer 'The current roll result for die.
            Dim intWon As Integer            'A rolling total of successes.
        'PROCESSING:
            'For every possible result on the Die...
                For intCurrentDieRoll = 1 To Die
            For intCurrentDieRoll = 1 To Die
                'If the rating is higher:
                    If (((Die / 2) - 2) + Modifier) >= Difficulty Then
                        'Add a victory:
                            intWon = intWon + 1
                'ElseIf Die rolled higher:
                    ElseIf (intCurrentDieRoll + Modifier) >= Difficulty Then
                        'Add a victory:
                            intWon = intWon + 1
                    End If
            'Next Die result...
                Next intCurrentDieRoll
        'OUTPUT:
            'Output the number of victories divided by the number of rolls:
                AverageUnopposedDiePercent = intWon / Die
    End Function



License
-------

This work is shared under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).

This is _not_ a [Free Culture License](https://creativecommons.org/freeworks/).

My intent in marking this work as non-commercial and non-derivative is to:

* Preserve the (arguable) market value of the work in case [Venture Land Games](http://www.venturelandgames.com) decides to use this work in whole or in part in any upcoming "official" supplement. Complete ownership over this work will be granted to [Venture Land Games](http://www.venturelandgames.com) upon request at no cost/fee/payment/renumeration/compensatoin whatsoever.
* Recognize the fact that the [Narrative Game System](http://rpg.drivethrustuff.com/product/128522/NGS-The-Narrative-Game-System) is wholly-owned by [Venture Land Games](http://www.venturelandgames.com), and they've made no license available under which to distribute derivative works. This work may&mdash;in fact&mdash;be illegal, and I want to protect others from using my work and accidentally infringing upon [Venture Land Games](http://www.venturelandgames.com) intellectual property.