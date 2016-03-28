#Accuracy Table

##Summary

This table shows the likely result of an "opposed" roll; it may be helpful for building NPCs to challenge your PCs.

##Detail

When one character attacks another, they make opposed Mechanical Ability rolls. Below, I've plotted the "accuracy" of each possible die (d6, d8, etc.) and Priority (+1, +2, etc.). For example, a character attacking with "d12 + 3" will hit a character defending with "d8 + 4" 54% of the time.

##NGS Opposed Roll Accuracy

|          |      |  d6   |  d6   |  d6   |  d6   |  d8   |  d8   |  d8   |  d8   |  d10  |  d10  |  d10  |  d10  |  d12  |  d12  |  d12  |  d12  |
|---------:|-----:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|
|          |      |__+1__ |__+2__ |__+3__ |__+4__ |__+1__ |__+2__ |__+3__ |__+4__ |__+1__ |__+2__ |__+3__ |__+4__ |__+1__ |__+2__ |__+3__ |__+4__ |
|  __d6__  |__+1__|  50%  |  28%  |  17%  |   8%  |  38%  |  21%  |  13%  |   6%  |  30%  |  17%  |  10%  |   5%  |  25%  |  14%  |   8%  |   4%  |
|  __d6__  |__+2__|  72%  |  50%  |  28%  |  17%  |  56%  |  38%  |  21%  |  13%  |  45%  |  30%  |  17%  |  10%  |  38%  |  25%  |  14%  |   8%  |
|  __d6__  |__+3__|  83%  |  72%  |  50%  |  28%  |  69%  |  56%  |  38%  |  21%  |  55%  |  45%  |  30%  |  17%  |  46%  |  38%  |  25%  |  14%  |
|  __d6__  |__+4__|  92%  |  83%  |  72%  |  50%  |  79%  |  69%  |  56%  |  38%  |  65%  |  55%  |  45%  |  30%  |  54%  |  46%  |  38%  |  25%  |
|  __d8__  |__+1__|  63%  |  44%  |  31%  |  21%  |  50%  |  33%  |  23%  |  16%  |  40%  |  26%  |  19%  |  13%  |  33%  |  22%  |  16%  |  10%  |
|  __d8__  |__+2__|  79%  |  63%  |  44%  |  31%  |  67%  |  50%  |  33%  |  23%  |  55%  |  40%  |  26%  |  19%  |  46%  |  33%  |  22%  |  16%  |
|  __d8__  |__+3__|  88%  |  79%  |  63%  |  44%  |  77%  |  67%  |  50%  |  33%  |  65%  |  55%  |  40%  |  26%  |  54%  |  46%  |  33%  |  22%  |
|  __d8__  |__+4__|  94%  |  88%  |  79%  |  63%  |  84%  |  77%  |  67%  |  50%  |  74%  |  65%  |  55%  |  40%  |  63%  |  54%  |  46%  |  33%  |
| __d10__  |__+1__|  70%  |  55%  |  45%  |  35%  |  60%  |  45%  |  35%  |  26%  |  50%  |  36%  |  28%  |  21%  |  42%  |  30%  |  23%  |  18%  |
| __d10__  |__+2__|  83%  |  70%  |  55%  |  45%  |  74%  |  60%  |  45%  |  35%  |  64%  |  50%  |  36%  |  28%  |  54%  |  42%  |  30%  |  23%  |
| __d10__  |__+3__|  90%  |  83%  |  70%  |  55%  |  81%  |  74%  |  60%  |  45%  |  72%  |  64%  |  50%  |  36%  |  63%  |  54%  |  42%  |  30%  |
| __d10__  |__+4__|  95%  |  90%  |  83%  |  70%  |  88%  |  81%  |  74%  |  60%  |  79%  |  72%  |  64%  |  50%  |  70%  |  63%  |  54%  |  42%  |
| __d12__  |__+1__|  75%  |  63%  |  54%  |  46%  |  67%  |  54%  |  46%  |  38%  |  58%  |  46%  |  38%  |  30%  |  50%  |  38%  |  31%  |  25%  |
| __d12__  |__+2__|  86%  |  75%  |  63%  |  54%  |  78%  |  67%  |  54%  |  46%  |  70%  |  58%  |  46%  |  38%  |  62%  |  50%  |  38%  |  31%  |
| __d12__  |__+3__|  92%  |  86%  |  75%  |  63%  |  84%  |  78%  |  67%  |  54%  |  77%  |  70%  |  58%  |  46%  |  69%  |  62%  |  50%  |  38%  |
| __d12__  |__+4__|  96%  |  92%  |  86%  |  75%  |  90%  |  84%  |  78%  |  67%  |  83%  |  77%  |  70%  |  58%  |  75%  |  69%  |  62%  |  50%  |

##Methodology

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
            Dim dblWon As Double              'A rolling total of victories for die 1.
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