Using Primary Antagonists
=========================

__Examination of _Primary Antagonists_ for the [Narrative Game System](http://rpg.drivethrustuff.com/product/128522/NGS-The-Narrative-Game-System) by [Venture Land Games](http://www.venturelandgames.com).__



Contents
--------

* [Summary](#summary)
* [Primary Antagonist Opposed Roll Accuracy Table](#primary-antagonist-opposed-roll-accuracy-table)
* [Observations](#observation)
* [House Rules](#house-rule)
* [Methodology](#methodology)
* [License](#license)



Summary
-------

This table shows the likely result of an "opposed" roll against a _Primary Antagonist_; it may be helpful for managing _Primary Antagonist_ combats/challenges.



Primary Antagonist Opposed Roll Accuracy Table
----------------------------------------------

|         |  d6+6 |  d6+8 | d6+10 | d6+12 |
|--------:|:-----:|:-----:|:-----:|:-----:|
|   d6+1  | __0%__|   0%  |   0%  |   0%  |
|   d6+2  | __3%__|   0%  |   0%  |   0%  |
|   d6+3  | __8%__|   0%  |   0%  |   0%  |
|   d6+4  |__17%__|   3%  |   0%  |   0%  |
| __d6+5__|__28%__|   8%  |   0%  |   0%  |
| __d6+6__|__50%__|  17%  |   3%  |   0%  |
|   d8+1  |   6%  | __0%__|   0%  |   0%  |
|   d8+2  |  13%  | __2%__|   0%  |   0%  |
|   d8+3  |  21%  | __6%__|   0%  |   0%  |
|   d8+4  |  31%  |__13%__|   2%  |   0%  |
| __d8+5__|  44%  |__21%__|   6%  |   0%  |
| __d8+6__|  63%  |__31%__|  13%  |   2%  |
|  d10+1  |  17%  |   5%  | __0%__|   0%  |
|  d10+2  |  25%  |  10%  | __2%__|   0%  |
|  d10+3  |  35%  |  17%  | __5%__|   0%  |
|  d10+4  |  45%  |  25%  |__10%__|   2%  |
|__d10+5__|  55%  |  35%  |__17%__|   5%  |
|__d10+6__|  70%  |  45%  |__25%__|  10%  |
|  d12+1  |  29%  |  14%  |   4%  | __0%__|
|  d12+2  |  38%  |  21%  |   8%  | __1%__|
|  d12+3  |  46%  |  29%  |  14%  | __4%__|
|  d12+4  |  54%  |  38%  |  21%  | __8%__|
|__d12+5__|  63%  |  46%  |  29%  |__14%__|
|__d12+6__|  75%  |  54%  |  38%  |__21%__|



Observation
-----------

###_Primary Antagonists_ are daunting, to say the least.

Based on the chart above, assuming four d8+4 player characters are in a very advantageous position (+2 on opposed rolls), they still only have a 31% chance of hitting a _Primary Antagonist._ If those player characters engage the _Primary Antagonist_ in a fair fight, they only have a 13% chance of hitting. This means, on average, the players will miss 2-7 times per hit.


House Rule
----------

###Every time your players "hit" your _Primary Antagonist_, subtract one from its _Priority_.

For example, if your d8 players hit your d6+8 _Primary Antagonist_, downgrade the antagonist to d6+7... then d6+6, and so on.

This will simulate "wearing down" a tough opponent, and it will make the battle "feel" as challenging, as your players desperately try to land those first few hits, but will also add a satisfying conclusion to the conflict, as a tough enemy is brought low by the players' ingenuity.





Methodology
-----------

I wrote the following custom function in Excel to calculate the results of all possible rolls in an opposed roll:

    Function AverageModifiedDiePercent(Die1 As Byte, Mod1 As Byte, Die2 As Byte, Mod2 As Byte) As Double
        'PURPOSE:
            'To output the likelihood (%) for an opposed roll in the Narrative Game System (NGS) by Venture Land Games.
        'VERSION (Version Number, YYYY.MM.DD)
            '1.0, 2016.03.20: First working model.
        'AUTHOR
            'Dustinian Camburides
            'dustinian@dustinian.com
            'www.dustinian.com
        'LANGUAGE
            'Excel VBA, but the syntax used would easily convert to another flavor of Basic (FreeBASIC, for example).
        'INPUT:
            'Die1: The number of faces the attacking die has (i.e. "6" for a "d6")
            'Mod1: The attacking numerical priority (i.e. "4" for "Priority A")
            'Die2: The number of faces the defending die has (i.e. "6" for a "d6")
            'Mod2: The defending numerical priority (i.e. "4" for "Priority A")
        'USE:
            'To use this function in your own Excel workbook:
                '1. Create a macro-enabled workbook (.xlsm from Excel 2007 and on).
                '2. Bring up the "Visual Basic" interface by holding "Alt" and pressing "F11."
                '3. Create a new "module."
                '4. Paste this code into the module. You can now call this function from your Excel worksheet.
                '5. Call the function by entering a formula like this:
                    'Use this to calculate a d8+3 against a d6+1: =AverageModifiedDiePercent(8, 3, 6, 1)
                    'Use this to reference cells with the die and priorities: =AverageModifiedDiePercent(A2, B2, C2, D2)
        'VARIABLES:
            Dim intCurrentDie1Roll As Integer 'The current roll result for die 1.
            Dim intCurrentDie2Roll As Integer 'The current roll result for die 2.
            Dim dblWon As Double              'A rolling total of successes for die 1.
        'PROCESSING:
            'For every possible result on Die 1...
                For intCurrentDie1Roll = 1 To Die1
                        'For every possible result on Die 2...
                            For intCurrentDie2Roll = 1 To Die2
                                'If Die 1 rolled higher:
                                    If (intCurrentDie1Roll + Mod1) > (intCurrentDie2Roll + Mod2) Then
                                        'Add a victory:
                                            dblWon = dblWon + 1
                                'If Die 1 and Die 2 were equal:
                                    ElseIf ((intCurrentDie1Roll + Mod1) = (intCurrentDie2Roll + Mod2)) Then
                                        'If the priority was higher for Die 1...
                                            If (Mod1 > Mod2) Then
                                                'Add a victory (per p28 of NGS, Priority breaks a tie):
                                                    dblWon = dblWon + 1
                                        'If the priorities are also the same...
                                            ElseIf (Mod1 = Mod2) Then
                                                'Add half a victory (per p28 of NGS, ties with same priority broken by flat d6 roll, 50% chance):
                                                    dblWon = dblWon + 0.5
                                            End If
                                    End If
                        'Next Die 2 result...
                            Next intCurrentDie2Roll
            'Next Die 1 result...
                Next intCurrentDie1Roll
        'OUTPUT:
            'Output the number of victories divided by the number of rolls:
                AverageModifiedDiePercent = dblWon / (Die1 * Die2)
    End Function



License
-------

This work is shared under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).

This is _not_ a [Free Culture License](https://creativecommons.org/freeworks/).

My intent in marking this work as non-commercial and non-derivative is to:

* Preserve the (arguable) market value of the work in case [Venture Land Games](http://www.venturelandgames.com) decides to use this work in whole or in part in any upcoming "official" supplement. Complete ownership over this work will be granted to [Venture Land Games](http://www.venturelandgames.com) upon request at no cost/fee/payment/renumeration/compensatoin whatsoever.
* Recognize the fact that the [Narrative Game System](http://rpg.drivethrustuff.com/product/128522/NGS-The-Narrative-Game-System) is wholly-owned by [Venture Land Games](http://www.venturelandgames.com), and they've made no license available under which to distribute derivative works. This work may&mdash;in fact&mdash;be illegal, and I want to protect others from using my work and accidentally infringing upon [Venture Land Games](http://www.venturelandgames.com) intellectual property.
