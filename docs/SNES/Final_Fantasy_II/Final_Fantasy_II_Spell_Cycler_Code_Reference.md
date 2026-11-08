---
title: "Final Fantasy II / Final Fantasy IV Spell Cycler & Magic Codes Reference"
game: "Final Fantasy II"
platform: "Super Nintendo Entertainment System"
alternate_titles:
  - "Final Fantasy IV"
  - "FF2e / FF4j"
developer: "Square"
publisher: "Square"
release_year: 1991
document_type: "Strategy Guide"
author: "Jacob Quisenberry"
version: "1.0"
date: "2026-11-07"
last_updated: "2026-11-07"
language: "en"
tags:
  - final-fantasy-ii
  - final-fantasy-iv
  - snes
  - spell-cycler
  - magic-codes
  - game-genie
  - game-shark
  - pro-action-replay

summary: "Version 1.0 reference for the SNES English Final Fantasy II and Japanese Final Fantasy IV spell cycler, spell/character offsets, special abilities, known code tables, address-based spell-cell selection, and current/max MP values. It is a cheat-code and mechanics reference, not a full walkthrough."
---

# Final Fantasy II / Final Fantasy IV Spell Cycler & Magic Codes Reference

The supplied source identifies these codes as working in both English Final Fantasy II and Japanese Final Fantasy IV. This Markdown archive preserves the complete version 1.0 code reference, including its tables and explanatory notes. Email addresses were removed; the author attribution and source rights notice remain.

## Complete source text

The original text is retained below in a fixed-width block for its tables and codes. Email contact addresses have been omitted.

````text
          FF2e, FF4j MAGIC CODES 1.0



Final Fantasy II (English), Final Fantasy IV (Japan) 
[Yes, the codes work in both versions]

Super Nintendo Entertainment System 
Pro Action Replay, Game Shark, and Game Genie codes by Jacob Quisenberry
© Jacob Quisenberry 1999, 2003
[email omitted]

You may distribute this document as much as you want
IF:
(1) You maintain credit to me.
(2) You do not change anything.
(3) You do not make any money.

You may include information from this document in other documents 
IF:
(1) You give credit to me.  
(2) You do not credit me with things I did not create.
(3) You give me notice at [email omitted]

The codes I have developed are designed to allow you to assign any spell to any 
character or exchange spells between characters.  My other codes affect other 
aspects of the magic system.

Everything here is my own work and my own discoveries.  The last time they were 
available is when I posted them on Usenet back in 1999.


Part 0:  Spell Cycler, the Very Brief Version

Part 1:  FF2e FF4j SPELL CYCLER/OFFSET CODE     7E1B86xy

I.     INTRODUCTION
II.    CONVENTIONS USED HEREIN
III.   SPELL CYCLER
IV.    OFFSETS IN GENERAL
V.     HOW OFFSETS WORK
VI.    CONVERTING ROW 8 OFFSETS TO OTHER ROWS
VII.   SPECIAL ABILITIES AND EFFECTS
VIII.  HOW TO FIND OFFSETS FOR OTHER CHARACTERS
IX.    WHAT I DO NOT HAVE
X.     POSSIBLE SOURCES OF ERROR
XI.    SPELL NOTES
XII.   ORDER OF SPELLS IN THE SPELL CYCLER
XIII.  CHARACTERS AND OFFSET VALUES (finally)
XIV.   COMBINED LIST OF ALL KNOWN OFFSETS

Part 2: Choosing Specific Spells and Cells by Address

Part 3: Changing Current and Max MP Values


Part 0:  Spell Cycler, the Very Brief Version

Repeated double-selection of the spell cycler allows you view 
and select all the spells in the game.

(1) Position a spell or blank space in your character’s 
appropriate row.
(2) Enter the listed code.  
(3) Repeatedly double-select the original spell.  
(4) Stop when you come to the spell or effect you want.  
(5) Enjoy.

Not all characters have a spell cycler.  For them, I have 
provided codes to exchange spells with other characters.  
Exchange codes must be performed on the menu of
the character listed first in the sequence.


SPELL CYCLERS 

             Hex/Pro
       Action Replay  Game Genie

ROSA
Row1        7E1B869C  BAF6-228C
Row4        7E1B8693  B7F6-228C
Row8        7E1B8687  65F6-228C


EDGE
Row1        7E1B8624  40F6-228C
Row4        7E1B861B  F8F6-228C
Row8        7E1B860F  DEF6-228C

OLD RYDIA BLACK
Row1        7E1B86FC  EAF6-228C
Row4        7E1B86F3  E7F6-228C
Row8        7E1B86E7  35F6-228C

OLD RYDIA CALLER
Row1        7E1B86E4  31F6-228C
Row4        7E1B86DB  28F6-228C
Row8        7E1B86CF  AEF6-228C

CECIL
Row1       NO SUCH CODE!
Row4       NO SUCH CODE!
Row8       NO SUCH CODE!


EXCHANGES

CECIL's row 8 <=> OLD RYDIA BLACK's row 8
position 1       7E1B8648  06F6-228C
position 2       7E1B8649  0BF6-228C
position 3       7E1B8650  9DF6-228C

CECIL <=> OLD RYDIA CALLER
position 1       7E1B8660  1DF6-228C
position 2       7E1B8661  1FF6-228C
position 3       7E1B8662  14F6-228C

CECIL <=> EDGE
position 1       NO SUCH CODE!
position 2       NO SUCH CODE!
position 3       NO SUCH CODE!

CECIL <=> ROSA
position 1       7E1B86A8  C6F6-228C
position 2       7E1B86A9  CBF6-228C
position 3       7E1B86AA  CCF6-228C

ROSA <=> EDGE
position 1       7E1B8678  56F6-228C
position 2       7E1B8679  5BF6-228C
position 3       7E1B867A  5CF6-228C


Part 1:  FF2e FF4j SPELL CYCLER/OFFSET CODE     7E1B86xy

I. INTRODUCTION

In order to use the codes to their full potential, it is 
necessary to understand what they do and how they work.  When 
viewing a character’s spell menu, selecting a spell or blank
space and then selecting another spell or space will exchange 
the positions of the two spells.  Using the spell offset code 
causes a double-selection of a single spell to result in
the transposition of it and one of the following: another spell 
from the spell menu, a spell from another spell menu, or a 
location in the ROM’s memory that I like to call "spell
space".


II. CONVENTIONS USED HEREIN

All codes and values are raw hexadecimal.  Pro Action Replay 
codes are merely raw hexadecimal, but if you wish to convert to 
Game Genie, you will want a converter program.

When using the term "spell", I generally refer to spells, 
special abilities, strange effects, blank spaces, and anything 
else that may be placed in a spell menu interchangeably.  Since
I created most of these codes while playing FF4j, I will be 
using translated names from that game, which are not necessarily 
the same names as displayed in FF2e.  I refer to an empty space 
as [Blank].  A tilde (~) will be substituted for spaces, weapon 
symbols, and other non-standard characters in the names of 
special abilities/effects. I refer to the spell
cycler as an "entity" because it occupies a space in memory or 
on a spell menu, but it is not meant to function as other 
effects.  An exchange with another character’s spell will be
denoted by Character row, column, where rows are counted from 
the top and columns are counted from the left.  All values 
assume a double-selection occurs on a spell menu’s 8th
(bottom) row.  I chose row eight because a character is less 
likely to have a spell on that row than any other.


III. SPELL CYCLER:

As with most variables, the spell offset address ,7E1B86--, has 
FF (255) possible values. The most interesting entity referred 
to by such a value is the "spell cycler".  Some characters can 
exchange one of their spells for the spell cycler as if
it were a normal spell. Repeated double-selection of the spell 
cycler will result in a progression through the list of
spells available in the game.  The spells are listed in a 
specific order, and the cycle begins with the location in the 
list of the spell that was exchanged for the cycler.  Roughly 
every other spell cycled through will correspond to the known 
order.  The other half represents the spell cycler initiated at 
a point other than the initial exchange. For instance, if you
started on Berserk, your list might progress as Berserk, ~suct, 
Reflect, eathe, Holy, [Blank], etc.  The order of either set can 
be interrupted by double-selecting any other position on the 
spell menu.  In the list of offsets, the spell cycler is
referred to SPELL CYCLER.  It is a surprise, I am sure.


IV. OFFSETS IN GENERAL

If double-selecting a spell while a given offset is active 
results in a transposition, it is instructive to consider with 
what a spell it is being transposed.  The result of any offset
will be the same for any spell in a given row.  If a row is 
comprised of

KEAL4     ARISE    HOLY,
and the result is to be a transposition with METEO, then the 
result can be

METEO   ARISE     HOLY or
KEAL4    METEO   HOLY or
KEAL4    ARISE     METEO
However, it is generally not possible to make multiple exchanges 
with
the same spell.  If
you get
METEO    ARISE    HOLY and then try to double-select ARISE, you 
will get

METEO    KEAL4   HOLY.
This is because KEAL4 was placed at METEO’s address of origin.


V. HOW OFFSETS WORK

An offset number refers to the number of spells right and down 
from the first spell in the row a spell will be transposed with.  
Let us say the offset is 0 and we
start with
METEO   ARISE   HOLY  on the first row and
KEAL1    KEAL4  BAHAMUT  on the second row.
Double-selecting ARISE will result in a switch with METEO 
because METEO
is 0 spells from the first spell of the row.  Double-selecting 
METEO attempts to activate METEO because both clicks refer to 
it. Let us say the offset is 4. Double selecting HOLY results in 
a switch between it an KEAL4 because we count
METEO 0, ARISE 1, HOLY 2, KEAL1 3, and KEAL4 4.

What happens when, as all values have been designed for, the
double-selection occurs on row 8?  Let us say you have
HOLY,    KEAL3,    METEO on row 8 and an offset of 90.  Since 
there are not enough spaces left, the spell transposes with a 
location not on the character’s spell menu.  Beyond a 
character’s spell menu, the result of a given offset vary from
character to character.  If the character is Rosa, then an 
offset of 90 will result in the selected spell being replaced
with QUAKE.  This QUAKE comes from spell space.  An offset of 99 
will result in an exchange with whatever Edge has in the first 
position of his first row (Edge 1,1), even if it
happens to be a blank space.  Please note that the same offset 
may not be used on Edge’s menu to effect a similar trade.  
Ninety-nine is Rosa’s ticket to borrow a spell from Edge.
Also notice that Rosa accepts Edge 1,1 into her 8,x, not her 
1,1.  If the offset were 104, Rosa would receive in her 8,x 
Edge’s 2,3.  Negative offsets are expressed as off-x.  While
the actual offset value is always positive, the effect of 
activating it appears to be negative.


VI. CONVERTING ROW 8 OFFSETS TO OTHER ROWS

Changing a row 8 offset to another row is as simple as 
subtracting 3 from the value of the row 8 offset for each 
ascending row. For any row, add three to each row to descend or
subtract 3 from each row to ascend.


VII. SPECIAL ABILITIES AND EFFECTS

While cycling through spells, you are likely to see a number of 
spells with strange names. Some of them may appear to be 
truncated names of monster attacks.  Such names may or
may not refer to the actual attacks.  They may be alternate 
methods of invoking standard spells.  There is a fair 
probability that invoking a special ability will cause a variety 
of strange phenomena in battle.  The proper action would be to 
try to finish the battle or simply switch off the active code. 
Abilities requiring greater than 0 MP are the ones most
likely to produce a legitimate effect.

My favorite effect is ~race.  When used in battle it has a much 
higher chance than DEATH to kill one enemy instantly.   I have 
never known it to crash a battle. It costs 0 MP and is reusable.


VIII. HOW TO FIND OFFSETS FOR OTHER CHARACTERS

The maximum offset value for any character is 255.  The spell 
associated with a given row will be three offsets less than the 
row below it.  That means that if you were to start at 255
on row 8, then row 7 would access the same spell as an offset of 
252 in row 8.  Thus, you can explore offsets 232-255 by entering 
values 253, 254, and 255 and exploring the spell menu  
appropriately.  This is much more convenient than entering 0-255
and exploring only row 8.

If instead of mapping the offsets for a given character, you 
would like to try to find the an offset to access a given 
effect, you will find the map of other characters useful.  There
appears to be only one sequence of offsets.  Characters merely 
access different subsets of 255 continuous values in that 
sequence.  There are more than 255 total effects to access.
This explains why Cecil, who begins with 24 [Blank], KEAL1, 
SIGHT, HOLD, and KEAL2, does not have access to a spell cycler.  
It is more than 255 effects away from his initial value.  
Character subsets of 255 effects are not necessarily
mutually exclusive.

Rosa’s set contains KEAL4, ARISE, and SIGHT at offsets 67, 70, 
and 73 respectively.  I found that Old Rydia Caller had the same 
sequence of spells at 139, 142, and 145, respectively.  I chose 
to assume that sequence is unique, and I subtracted 67 from 139 
to get 72.  I then deduced that Rosa’s spell cycler at 134 
should be 72 less than Old Rydia Caller’s spell cycler.  I was 
pleased to find that Rydia’s spell cycler exists at 206, 
precisely as expected.  You may notice that I used sequences 
separated by threes. This was because I wanted to try enter as 
few values as possible and merely explore a spell menu.  A 
similar technique can usually be employed to find an offset for 
any character.


IX. WHAT I DO NOT HAVE

I only have found codes for these five characters (actually four
characters but five spell menus) because I created them from a 
saved game  near to the time I was to defeat
Zeromus.  I do not have any saved games with other characters, 
and I have not felt like beating the game for a fourth time 
(yet).


X. POSSIBLE SOURCES OF ERROR

History:
I developed the codes for a very specific reason.  I was playing 
a patched translation of FF4j.  After defeating the Tower of 
Bab-il, I made my way to the entrance, but the scene
in which I should have been confronted by Golbeze did not occur.  
After trying a few things, I decided to load my saved game (not 
saved state) into FF2e. When beating the goblins in the control 
room, Rosa leveled up, and she obtained a second Cure3 (Keal3).  
I returned to FF4j to play through the remainder of the game.  
At some point I earned Holy (White Meteo), but my spell menu was 
full.  Holy failed to be enrolled. I developed the
codes to replace my second Keal3 with Holy.

Possible Error 1:
In several places in my list there are KEAL3s which I think very 
well may really be HOLYs.  I believe this most likely in any 
sequence containing REFLECT, KEAL3, and DISPEL. This may be 
anything from an anomaly caused by the code to the fact that my
saved game file contains three games in which Rosa still has 2 
Keal3s.

Possible Error 2:
It is possible that some, even many, [Blanks] are really 
exchanges with other characters.  I think it is quite possible 
that blanks immediately following low level black magic spells
could be blank spaces in the spell lists of characters I no 
longer have.  In other words, perhaps a [Blank] is really the 
location which would be occupied by FLARE if Parom or
Young Rydia had obtained a high enough level to acquire it.  
Spaces after white magic spells may be from Young Rydia or 
Palom’s white spell menu.  I think it may even be the
case that even characters, such as Kain, that never use magic 
may have magic variables. Those would likely be [Blank] or 
gibberish effects.


XI. SPELL NOTES

The fourth column of each character’s offset list contains notes 
for your consideration.  I have noticed that each list appears 
to be broken into sections of 24 effects.  I also believe
the same result would be obtained if counting were commenced 
from the bottom of the list.  Items with question marks are 
things I am not sure of.  Is the right spell actually
recorded?  Is one of my counts of 24 effects valid?  You may 
want to take care to evaluate such ambiguous areas.


XII.   ORDER OF SPELLS IN THE SPELL CYCLER

Dec Hex Spell/Effect

0 0 [Blank]
1 1 Hold   WHITE
2 2 Silence
3 3 Confuse
4 4 Blink
5 5 Protect
6 6 Shell
7 7 Slow
8 8 Haste
9 9 Berserk
10 A Reflect
11 B Holy
12 C Dispel
13 D Rabur
14 E Keal1
15 F Keal2
16 10 Keal3
17 11 Keal4
18 12 Esuna
19 13 Raise
20 14 Arise
21 15 Mini
22 16 Telep
23 17 Sight
24 18 Levita
25 19 Toad   BLACK
26 1A Piggy
27 1B Dejon
28 1C Poison
29 1D Fire
30 1E Fire2
31 1F Fire3
32 20 Blizzard1
33 21 Blizzard2
34 22 Blizzard3
35 23 Thunder1
36 24 Thunder2
37 25 Thunder3
38 26 Bio
39 27 Tornado
40 28 Quake
41 29 Sleep
42 2A Break
43 2B Death
44 2C Stop
45 2D Drain
46 2E Aspir
47 2F Meteo
48 30 Flare
49 31 Goblin CALLER
50 32 Bomb
51 33 Cocatrice
52 34 Mind
53 35 Chocobo
54 36 Shiva
55 37 Ramuh
56 38 Ifrit
57 39 Titan
58 3A Dragon
59 3B Sylph
60 3C Odin
61 3D Levia
62 3E Asura
63 3F Bahamut
64 40 ltMeteo TWIN MAGIC
65 41 ltFlare
66 42 Katon   NINJA
67 43 Siton
68 44 Rajin
69 45 Kemur
70 46 Kagsh
71 47 Bushn
72 48 _gcArr NONSTANDARD EFFECTS
73 49 owHeal
74 4A ____Ba
75 4B Sund__
76 4C _oison
77 4D a_Dagg
78 4E er__Pu
79 4F nch___
80 50 _estru
81 51 ctSton
82 52 _eakMi
83 53 ndBlst
84 54 _ick__
85 55 __Snow
86 56 _trmJu
87 57 _gment
88 58 _ellfi
89 59 reAnge
90 5A r___Mi
91 6B stBrth
92 5C _hispe
93 5D r_Iron
94 5E _wrdTs
95 5F unami_
96 60 _shura
97 61 __Ashu
98 62 ra__As
99 63 _ura__
100 64 _._Fla
101 65 reW._M
102 66 eteoMo
103 67 nst015
104 68 _onst)
105 69 16Glan
106 6A ce__Bl
107 6B aster__
108 6C _lap__
109 6D __Cold
110 6E _napPu
111 6F pil___
112 70 _ure__
113 71 __Tong
114 72 ue__Cu
115 73 rse___
116 74 _ingrt
117 75 _pDeat
118 76 ____Be
119 77 ak____
120 78 _tonGa
121 79 zeMind
122 7A _lstEm
123 7B _race_
124 7C _adBre
125 7D _hWhis
126 7E per_Wr
127 7F eather_
128 80 _all__
129 81 __Stra
130 82 _n__Co
131 83 _dMist
132 84 _xplod
133 85 e_Curs
134 86 _ongCu
135 87 rsAura
136 88 _leepG
137 89 asPois
138 8A nGasLa
139 8B Ser___
140 8C _Revlu
141 8D _nBl._
142 8E _angBl
143 8F ._Hole
144 90 _ethSo
145 91 ngDime
146 92 ntn9Ma
147 93 elstrm
148 94 _lecWa
149 95 _lchnE
150 96 xpldHa
151 97 _ching
152 98 _eal__
153 99 __Suct
154 9A _on_Me
155 9B _ic___
156 9C _ig_Ba
157 9D ngBlod
158 9E _uckDi
159 9F gest__
160 A0 _ollen
161 A1 __Cras
162 A2 _DwnAl
163 A3 arm___
164 A4 _ummon
165 A5 __Dumm
166 A6 yMgcDR
167 A7 evlutn
168 A8 _arget
169 A9 __Nuke
170 AA ____Re
171 AB _reat_
172 AC _rsDis
173 AD plBeam
174 AE ____Nu
175 AF m._199
176 B0 _lame_
177 B1 __Blaz
178 B2 e___Li
179 B3 _Flash
180 B4 _hunde
181 B5 r_D.Br
182 B6 eathBi
183 B7 g_Wave
184 B8 _nowSt
185 B9 rmTsun
186 BA ami_Tw
187 BB _ster_
188 BC _aser_
189 BD __Dest
190 BE ructQu
191 BF ake___
192 C0 _lmThr
193 C1 wrHeat
194 C2 er__Fl
195 C3 ameDgn
196 C4 _ronSw
197 C5 rdM._F
198 C6 _areNe
199 C7 edle__
200 C8 _ounte
201 C9 r_Mons
202 CA _000Mo
203 CB nst000
204 CC _egen_
205 CD __Rera
206 CE _se_Mo
207 CF nst000
208 D0 Monst0
209 D1 00Mons
210 D2 t000Mo
211 D3 nst000
212 D4 Monst0
213 D5 00Mons
214 D6 t000Mo
215 D7 nst000
216 D8 Monst0
217 D9 00Mons
218 DA t000Mo
219 DB nst000
220 DC Monst0
221 DD 00Mons
222 DE t000Mo
223 DF nst000
224 E0 Monst0
225 E1 00Mons
226 E2 t000Mo
227 E3 nst000
228 E4 Monst0
229 E5 00Mons
230 E6 t000Mo
231 E7 nst000
232 E8 Monst0
233 E9 00Mons
234 EA t000Mo
235 EB nst000
236 EC Monst0
237 ED 00Mons
238 EE t000Mo
239 EF nst000
240 F0 Monst0
241 F1 00Mons
242 F2 t000Mo
243 F3 nst000
244 F4 Monst0
245 F5 00Mons
246 F6 t000Mo
247 F7 nst000
248 F8 Monst0
249 F9 00Mons
250 FA t000Mo
251 FB nst000
252 FC Monst0
253 FD 00Mons
254 FE t000Mo
255 FF nst000


XIII. CHARACTERS AND OFFSET VALUES (finally)
Given the hex or Pro Action Replay code 781B86xy, replace xy 
with a value in the Hex column.

CECIL
Dec Hex

0 0 Off 0 Total offsets =24
1 1 Off 1
2 2 Off 2
3 3 [Blank] 24 [Blank]
4 4 [Blank] Perhaps a non-magic user
5 5 [Blank]
6 6 [Blank]
7 7 [Blank]
8 8 [Blank]
9 9 [Blank]
10 A [Blank]
11 B [Blank]
12 C [Blank]
13 D [Blank]
14 E [Blank]
15 F [Blank]
16 10 [Blank]
17 11 [Blank]
18 12 [Blank]
19 13 [Blank]
20 14 [Blank]
21 15 [Blank]
22 16 [Blank]
23 17 [Blank]
24 18 [Blank]
25 19 [Blank]
26 1A [Blank]
27 1B Keal1 4 White spells + 20 [Blank]
28 1C Sight
29 1D Hold
30 1E Keal2
31 1F [Blank]
32 20 [Blank]
33 21 [Blank]
34 22 [Blank]
35 23 [Blank]
36 24 [Blank]
37 25 [Blank]
38 26 [Blank]
39 27 [Blank]
40 28 [Blank]
41 29 [Blank]
42 2A [Blank]
43 2B [Blank]
44 2C [Blank]
45 2D [Blank]
46 2E [Blank]
47 2F [Blank]
48 30 [Blank]
49 31 [Blank]
50 32 [Blank]
51 33 Rydia B 1,1 All 24 Older Rydia Black Exchanges
52 34 Rydia B 1,2
53 35 Rydia B 1,3
54 36 Rydia B 2,1
55 37 Rydia B 2,2
56 38 Rydia B 2,3
57 39 Rydia B 3,1
58 3A Rydia B 3,2
59 3B Rydia B 3,3
60 3C Rydia B 4,1
61 3D Rydia B 4,2
62 3E Rydia B 4,3
63 3F Rydia B 5,1
64 40 Rydia B 5,2
65 41 Rydia B 5,3
66 42 Rydia B 6,1
67 43 Rydia B 6,2
68 44 Rydia B 6,3
69 45 Rydia B 7,1
70 46 Rydia B 7,2
71 47 Rydia B 7,3
72 48 Rydia B 8,1
73 49 Rydia B 8,2
74 4A Rydia B 8,3
75 4B Rydia C 1,1 All 24 Older Rydia Caller exchanges
76 4C Rydia C 1,2
77 4D Rydia C 1,3
78 4E Rydia C 2,1
79 4F Rydia C 2,2
80 50 Rydia C 2,3
81 51 Rydia C 3,1
82 52 Rydia C 3,2
83 53 Rydia C 3,3
84 54 Rydia C 4,1
85 55 Rydia C 4,2
86 56 Rydia C 4,3
87 57 Rydia C 5,1
88 58 Rydia C 5,2
89 59 Rydia C 5,3
90 5A Rydia C 6,1
91 6B Rydia C 6,2
92 5C Rydia C 6,3
93 5D Rydia C 7,1
94 5E Rydia C 7,2
95 5F Rydia C 7,3
96 60 Rydia C 8,1
97 61 Rydia C 8,2
98 62 Rydia C 8,3
99 63 Keal2 23 Spells and 1 [Blank]
100 64 Confuse Why is Holy missing?
101 65 Blink
102 66 Esuna
103 67 Raise
104 68 Teleport
105 69 Hold
106 6A Silence
107 6B Protect
108 6C Shell
109 6D Slow
110 6E Haste
111 6F Berserk
112 70 Reflect
113 71 Dispel
114 72 Rabur
115 73 Keal1
116 74 Keal3
117 75 Keal4
118 76 Arise
119 77 Mini
120 78 Sight
121 79 Levitate
122 7A [Blank] Holy?
123 7B Fire1 21 Black spells + 3 [Blank]
124 7C Blizzard1
125 7D Thunder1
126 7E Stop
127 7F Aspir
128 80 Toad
129 81 Piggy
130 82 Dejon
131 83 Poison
132 84 Fire2
133 85 Fire3
134 86 Blizzard2
135 87 Blizzard3
136 88 Thunder2
137 89 Thunder3
138 8A Bio
139 8B Tornado
140 8C Sleep
141 8D Break
142 8E Drain
143 8F Meteo
144 90 [Blank]
145 91 [Blank]
146 92 [Blank]
147 93 Rosa 1,1 All 24 Rosa exchanges
148 94 Rosa 1,2
149 95 Rosa 1,3
150 96 Rosa 2,1
151 97 Rosa 2,2
152 98 Rosa 2,3
153 99 Rosa 3,1
154 9A Rosa 3,2
155 9B Rosa 3,3
156 9C Rosa 4,1
157 9D Rosa 4,2
158 9E Rosa 4,3
159 9F Rosa 5,1
160 A0 Rosa 5,2
161 A1 Rosa 5,3
162 A2 Rosa 6,1
163 A3 Rosa 6,2
164 A4 Rosa 6,3
165 A5 Rosa 7,1
166 A6 Rosa 7,2
167 A7 Rosa 7,3
168 A8 Rosa 8,1
169 A9 Rosa 8,2
170 AA Rosa 8,3
171 AB Fire1 10 Black magic + 14 [Blank]
172 AC Blizzard1
173 AD Thunder1
174 AE Sleep
175 AF Poison
176 B0 Blizzard2
177 B1 Piggy
178 B2 Fire2
179 B3 Thunder2
180 B4 Stop
181 B5 [Blank]
182 B6 [Blank]
183 B7 [Blank]
184 B8 [Blank]
185 B9 [Blank]
186 BA [Blank]
187 BB [Blank]
188 BC [Blank]
189 BD [Blank]
190 BE [Blank]
191 BF [Blank]
192 C0 [Blank]
193 C1 [Blank]
194 C2 [Blank]
195 C3 Keal1 10 White magic + 14 [Blank]
196 C4 Hold
197 C5 Rabur
198 C6 Slow
199 C7 Sight
200 C8 Raise
201 C9 Protect
202 CA Keal2
203 CB Silence
204 CC Berserk
205 CD [Blank]
206 CE [Blank]
207 CF [Blank]
208 D0 [Blank]
209 D1 [Blank]
210 D2 [Blank]
211 D3 [Blank]
212 D4 [Blank]
213 D5 [Blank]
214 D6 [Blank]
215 D7 [Blank]
216 D8 [Blank]
217 D9 [Blank]
218 DA [Blank]
219 DB Hold 16 White magic
220 DC Silence
221 DD Confuse
222 DE Blink
223 DF Protect
224 E0 Shell
225 E1 Slow
226 E2 Haste
227 E3 Berserk
228 E4 Reflect
229 E5 Keal3
230 E6 Dispel
231 E7 Rabur
232 E8 Keal1
233 E9 Keal2
234 EA Keal3
235 EB Off-21 Total offsets =24
236 EC Off-20
237 ED Off-19
238 EE Off-18
239 EF Off-17
240 F0 Off-16
241 F1 Off-15
242 F2 Off-14
243 F3 Off-13
244 F4 Off-12
245 F5 Off-11
246 F6 Off-10
247 F7 Off-9
248 F8 Off-8
249 F9 Off-7
250 FA Off-6
251 FB Off-5
252 FC Off-4
253 FD Off-3
254 FE Off-2
255 FF Off-1


OLD RYDIA BLACK
Dec Hex

0 0 Off 0 Total offsets =24
1 1 Off 1
2 2 Off 2
3 3 Rydia C 1,1 All 24 Rydia Call exchanges
4 4 Rydia C 1,2
5 5 Rydia C 1,3
6 6 Rydia C 2,1
7 7 Rydia C 2,2
8 8 Rydia C 2,3
9 9 Rydia C 3,1
10 A Rydia C 3,2
11 B Rydia C 3,3
12 C Rydia C 4,1
13 D Rydia C 4,2
14 E Rydia C 4,3
15 F Rydia C 5,1
16 10 Rydia C 5,2
17 11 Rydia C 5,3
18 12 Rydia C 6,1
19 13 Rydia C 6,2
20 14 Rydia C 6,3
21 15 Rydia C 7,1
22 16 Rydia C 7,2
23 17 Rydia C 7,3
24 18 Rydia C 8,1
25 19 Rydia C 8,2
26 1A Rydia C 8,3
27 1B Keal2 23 white magic + 1 [Blank]
28 1C Confuse
29 1D Blink
30 1E Esuna
31 1F Raise
32 20 Teleport
33 21 Hold
34 22 Silence
35 23 Protect
36 24 Shell
37 25 Slow
38 26 Haste
39 27 Berserk
40 28 Reflect
41 29 Dispel
42 2A Rabur
43 2B Keal1
44 2C Keal3
45 2D Keal4
46 2E Arise
47 2F Mini
48 30 Sight
49 31 Levitate
50 32 [Blank] Holy?
51 33 Fire1 21 black magic + 3 [Blank]
52 34 Blizzard1
53 35 Thunder1
54 36 Stop
55 37 Aspir
56 38 Toad
57 39 Piggy
58 3A Dejon
59 3B Poison
60 3C Fire2
61 3D Fire3
62 3E Blizzard2
63 3F Blizzard3
64 40 Thunder2
65 41 Thunder3
66 42 Bio
67 43 Tornado
68 44 Sleep
69 45 Break
70 46 Drain
71 47 Meteo
72 48 [Blank]
73 49 [Blank]
74 4A [Blank]
75 4B Rosa 1,1 All 24 Rosa exchanges
76 4C Rosa 1,2
77 4D Rosa 1,3
78 4E Rosa 2,1
79 4F Rosa 2,2
80 50 Rosa 2,3
81 51 Rosa 3,1
82 52 Rosa 3,2
83 53 Rosa 3,3
84 54 Rosa 4,1
85 55 Rosa 4,2
86 56 Rosa 4,3
87 57 Rosa 5,1
88 58 Rosa 5,2
89 59 Rosa 5,3
90 5A Rosa 6,1
91 6B Rosa 6,2
92 5C Rosa 6,3
93 5D Rosa 7,1
94 5E Rosa 7,2
95 5F Rosa 7,3
96 60 Rosa 8,1
97 61 Rosa 8,2
98 62 Rosa 8,3
99 63 Fire1 10 black magic + 14 [Blank]
100 64 Blizzard1
101 65 Thunder1
102 66 Sleep
103 67 Poison
104 68 Blizzard2
105 69 Piggy
106 6A Fire2
107 6B Thunder2
108 6C Stop
109 6D [Blank]
110 6E [Blank]
111 6F [Blank]
112 70 [Blank]
113 71 [Blank]
114 72 [Blank]
115 73 [Blank]
116 74 [Blank]
117 75 [Blank]
118 76 [Blank]
119 77 [Blank]
120 78 [Blank]
121 79 [Blank]
122 7A [Blank]
123 7B Keal1 10 white magic + 14 [Blank]
124 7C Hold
125 7D Rabur
126 7E Slow
127 7F Sight
128 80 Raise
129 81 Protect
130 82 Keal2
131 83 Silence
132 84 Berserk
133 85 [Blank]
134 86 [Blank]
135 87 [Blank]
136 88 [Blank]
137 89 [Blank]
138 8A [Blank]
139 8B [Blank]
140 8C [Blank]
141 8D [Blank]
142 8E [Blank]
143 8F [Blank]
144 90 [Blank]
145 91 [Blank]
146 92 [Blank]
147 93 Hold 24 white magic
148 94 Silence
149 95 Confuse
150 96 Blink
151 97 Protect
152 98 Shell
153 99 Slow
154 9A Haste
155 9B Berserk
156 9C Reflect
157 9D Keal3 Holy?
158 9E Dispel
159 9F Rabur
160 A0 Keal
161 A1 Keal2
162 A2 Keal3
163 A3 Keal4
164 A4 Esuna
165 A5 Raise
166 A6 Arise
167 A7 Mini
168 A8 Teleport
169 A9 Sight
170 AA Levitate
171 AB Toad 24 black magic
172 AC Piggy
173 AD Dejon
174 AE Poison
175 AF Fire1
176 B0 Fire2
177 B1 Fire3
178 B2 Blizzard1
179 B3 Blizzard2
180 B4 Blizzard3
181 B5 Thunder1
182 B6 Thunder2
183 B7 Thunder3
184 B8 Bio
185 B9 Tornado
186 BA Quake
187 BB Sleep
188 BC Break
189 BD Death
190 BE Stop
191 BF Drain
192 C0 Aspir
193 C1 Meteo
194 C2 Flare
195 C3 Edge 1,1 All 24 Edge exchanges
196 C4 Edge 1,2
197 C5 Edge 1,3
198 C6 Edge 2,1
199 C7 Edge 2,2
200 C8 Edge 2,3
201 C9 Edge 3,1
202 CA Edge 3,2
203 CB Edge 3,3
204 CC Edge 4,1
205 CD Edge 4,2
206 CE Edge 4,3
207 CF Edge 5,1
208 D0 Edge 5,2
209 D1 Edge 5,3
210 D2 Edge 6,1
211 D3 Edge 6,2
212 D4 Edge 6,3
213 D5 Edge 7,1
214 D6 Edge 7,2
215 D7 Edge 7,3
216 D8 Edge 8,1
217 D9 Edge 8,2
218 DA Edge 8,3
219 DB [Blank] 16?
220 DC [Blank]
221 DD [Blank]
222 DE [Blank]
223 DF [Blank]
224 E0 [Blank]
225 E1 [Blank]
226 E2 [Blank]
227 E3 ~Suct
228 E4 eathe
229 E5 Keal2
230 E6 SPELL CYCLER
231 E7 SPELL CYCLER
232 E8 ~ellfi
233 E9 Hold
234 EA per~Wr
235 EB Off-21 Total offsets =24
236 EC Off-20
237 ED Off-19
238 EE Off-18
239 EF Off-17
240 F0 Off-16
241 F1 Off-15
242 F2 Off-14
243 F3 Off-13
244 F4 Off-12
245 F5 Off-11
246 F6 Off-10
247 F7 Off-9
248 F8 Off-8
249 F9 Off-7
250 FA Off-6
251 FB Off-5
252 FC Off-4
253 FD Off-3
254 FE Off-2
255 FF Off-1


OLD RYDIA CALLER
Dec Hex

0 0 Off 0 Total offsets =24
1 1 Off 1
2 2 Off 2
3 3 Keal2 23 white magic +1 [Blank]
4 4 Confuse
5 5 Blink
6 6 Esuna
7 7 Raise
8 8 Teleport
9 9 Hold
10 A Silence
11 B Protect
12 C Shell
13 D Slow
14 E Haste
15 F Berserk
16 10 Reflect
17 11 Dispel
18 12 Rabur
19 13 Keal1
20 14 Keal3
21 15 Keal4
22 16 Arise
23 17 Mini
24 18 Sight
25 19 Levitate
26 1A [Blank] Holy?
27 1B Fire1 21 black magic + 3 [Blank]
28 1C Blizzard1
29 1D Thunder1
30 1E Stop
31 1F Aspir
32 20 Toad
33 21 Piggy
34 22 Dejon
35 23 Poison
36 24 Fire2
37 25 Fire3
38 26 Blizzard2
39 27 Blizzard3
40 28 Thunder2
41 29 Thunder3
42 2A Bio
43 2B Tornado
44 2C Sleep
45 2D Break
46 2E Drain
47 2F Meteo
48 30 [Blank]
49 31 [Blank]
50 32 [Blank]
51 33 Rosa 1,1 All 24 Rosa Exchanges
52 34 Rosa 1,2
53 35 Rosa 1,3
54 36 Rosa 2,1
55 37 Rosa 2,2
56 38 Rosa 2,3
57 39 Rosa 3,1
58 3A Rosa 3,2
59 3B Rosa 3,3
60 3C Rosa 4,1
61 3D Rosa 4,2
62 3E Rosa 4,3
63 3F Rosa 5,1
64 40 Rosa 5,2
65 41 Rosa 5,3
66 42 Rosa 6,1
67 43 Rosa 6,2
68 44 Rosa 6,3
69 45 Rosa 7,1
70 46 Rosa 7,2
71 47 Rosa 7,3
72 48 Rosa 8,1
73 49 Rosa 8,2
74 4A Rosa 8,3
75 4B Fire1 10 White Magic + 14 [Blank]
76 4C Blizzard1
77 4D Thunder1
78 4E Sleep
79 4F Poison
80 50 Blizzard2
81 51 Piggy
82 52 Fire2
83 53 Thunder2
84 54 Stop
85 55 [Blank]
86 56 [Blank]
87 57 [Blank]
88 58 [Blank]
89 59 [Blank]
90 5A [Blank]
91 6B [Blank]
92 5C [Blank]
93 5D [Blank]
94 5E [Blank]
95 5F [Blank]
96 60 [Blank]
97 61 [Blank]
98 62 [Blank]
99 63 Keal1 10 White Magic + 14 [Blank]
100 64 Hold
101 65 Rabur
102 66 Slow
103 67 Sight
104 68 Raise
105 69 Protect
106 6A Keal2
107 6B Silence
108 6C Berserk
109 6D [Blank]
110 6E [Blank]
111 6F [Blank]
112 70 [Blank]
113 71 [Blank]
114 72 [Blank]
115 73 [Blank]
116 74 [Blank]
117 75 [Blank]
118 76 [Blank]
119 77 [Blank]
120 78 [Blank]
121 79 [Blank]
122 7A [Blank]
123 7B Hold 24 White Magic, no Holy, 2Keal3s
124 7C Silence
125 7D Confuse
126 7E Blink
127 7F Protect
128 80 Shell
129 81 Slow
130 82 Haste
131 83 Berserl
132 84 Reflect
133 85 Keal3 HOLY?
134 86 Dispel
135 87 Rabur
136 88 Keal1
137 89 Keal2
138 8A Keal3
139 8B Keal4
140 8C Esuna
141 8D Raise
142 8E Arise
143 8F Mini
144 90 Teleport
145 91 Sight
146 92 Levitate
147 93 Toad 24 Black Magic
148 94 Piggy
149 95 Dejon
150 96 Poison
151 97 Fire1
152 98 Fire2
153 99 Fire3
154 9A Blizzard1
155 9B Blizzard2
156 9C Blizzard3
157 9D Thunder1
158 9E Thunder2
159 9F Thunder3
160 A0 Bio
161 A1 Tornado
162 A2 Quake
163 A3 Sleep
164 A4 Break
165 A5 Death
166 A6 Stop
167 A7 Drain
168 A8 Aspir
169 A9 Meteo
170 AA Flare
171 AB Edge 1,1 All 24 Edge Exchanges
172 AC Edge 1,2
173 AD Edge 1,3
174 AE Edge 2,1
175 AF Edge 2,2
176 B0 Edge 2,3
177 B1 Edge 3,1
178 B2 Edge 3,2
179 B3 Edge 3,3
180 B4 Edge 4,1
181 B5 Edge 4,2
182 B6 Edge 4,3
183 B7 Edge 5,1
184 B8 Edge 5,2
185 B9 Edge 5,3
186 BA Edge 6,1
187 BB Edge 6,2
188 BC Edge 6,3
189 BD Edge 7,1
190 BE Edge 7,2
191 BF Edge 7,3
192 C0 Edge 8,1
193 C1 Edge 8,2
194 C2 Edge 8,3
195 C3 [Blank] 24?
196 C4 [Blank]
197 C5 [Blank]
198 C6 [Blank]
199 C7 [Blank]
200 C8 [Blank]
201 C9 [Blank]
202 CA [Blank]
203 CB ~Suct
204 CC eather
205 CD Keal2
206 CE SPELL CYCLER
207 CF SPELL CYCLER
208 D0 ~gment
209 D1 Hold
210 D2 per~Wr
211 D3 [Blank]
212 D4 [Blank]
213 D5 [Blank]
214 D6 Flare
215 D7 Silence
216 D8 Silence
217 D9 [Blank]
218 DA Hold
219 DB Silence 16?
220 DC [Blank]
221 DD [Blank]
222 DE [Blank]
223 DF [Blank]
224 E0 [Blank]
225 E1 [Blank]
226 E2 [Blank]
227 E3 [Blank]
228 E4 [Blank]
229 E5 [Blank]
230 E6 [Blank]
231 E7 [Blank]
232 E8 [Blank]
233 E9 [Blank]
234 EA [Blank]
235 EB Off-21 Total offsets =24
236 EC Off-20
237 ED Off-19
238 EE Off-18
239 EF Off-17
240 F0 Off-16
241 F1 Off-15
242 F2 Off-14
243 F3 Off-13
244 F4 Off-12
245 F5 Off-11
246 F6 Off-10
247 F7 Off-9
248 F8 Off-8
249 F9 Off-7
250 FA Off-6
251 FB Off-5
252 FC Off-4
253 FD Off-3
254 FE Off-2
255 FF Off-1


ROSA
Dec Hex

0 0 Off 0 Total offsets =24
1 1 Off 1
2 2 Off 2
3 3 Fire1 Black Magic+14 [Blank] =24
4 4 Blizzard1 Young Rydia?
5 5 Thunder1
6 6 Sleep
7 7 Poison
8 8 Blizzard2
9 9 Piggy
10 A Fire2
11 B Thunder2
12 C Stop
13 D [Blank]
14 E [Blank]
15 F [Blank]
16 10 [Blank]
17 11 [Blank]
18 12 [Blank]
19 13 [Blank]
20 14 [Blank]
21 15 [Blank]
22 16 [Blank]
23 17 [Blank]
24 18 [Blank]
25 19 [Blank]
26 1A [Blank]
27 1B Keal1 White Magic+14 [Blank]
28 1C Hold Young Rydia?
29 1D Rabur
30 1E Slow
31 1F Sight
32 20 Raise
33 21 Protect
34 22 Keal2
35 23 Silence
36 24 Berserk
37 25 [Blank]
38 26 [Blank]
39 27 [Blank]
40 28 [Blank]
41 29 [Blank]
42 2A [Blank]
43 2B [Blank]
44 2C [Blank]
45 2D [Blank]
46 2E [Blank]
47 2F [Blank]
48 30 [Blank]
49 31 [Blank]
50 32 [Blank]
51 33 Hold 24 WHITE
52 34 Silence
53 35 Confuse
54 36 Blink
55 37 Protect
56 38 Shell
57 39 Slow
58 3A Haste
59 3B Berserk
60 3C Reflect
61 3D Holy
62 3E Dispel
63 3F Rabur
64 40 Keal1
65 41 Keal2
66 42 Keal3
67 43 Keal4
68 44 Esuna
69 45 Raise
70 46 Arise
71 47 Mini
72 48 Teleport
73 49 Sight
74 4A Levita
75 4B Toad 24 BLACK
76 4C Piggy
77 4D Dejon
78 4E Poison
79 4F Fire
80 50 Fire2
81 51 Fire3
82 52 Blizzard1
83 53 Blizzard2
84 54 Blizzard3
85 55 Thunder1
86 56 Thunder2
87 57 Thunder3
88 58 Bio
89 59 Tornado
90 5A Quake
91 6B Sleep
92 5C Break
93 5D Death
94 5E Stop
95 5F Drain
96 60 Aspir
97 61 Meteo
98 62 Flare
99 63 Edge 1,1 All 24 Edge exchanges
100 64 Edge 1,2
101 65 Edge 1,3
102 66 Edge 2,1
103 67 Edge 2,2
104 68 Edge 2,3
105 69 Edge 3,1
106 6A Edge 3,2
107 6B Edge 3,3
108 6C Edge 4,1
109 6D Edge 4,2
110 6E Edge 4,3
111 6F Edge 5,1
112 70 Edge 5,2
113 71 Edge 5,3
114 72 Edge 6,1
115 73 Edge 6,2
116 74 Edge 6,3
117 75 Edge 7,1
118 76 Edge 7,2
119 77 Edge 7,3
120 78 Edge 8,1
121 79 Edge 8,2
122 7A Edge 8,3
123 7B [Blank] 24?
124 7C [Blank]
125 7D [Blank]
126 7E [Blank]
127 7F [Blank]
128 80 [Blank]
129 81 [Blank]
130 82 [Blank]
131 83 ~Suct
132 84 eathe
133 85 Keal2
134 86 SPELL CYCLER
135 87 SPELL CYCLER
136 88 ~trmJu
137 89 Hold
138 8A per~Wr
139 8B [Blank]
140 8C [Blank]
141 8D [Blank]
142 8E Flare
143 8F Silence
144 90 Silence
145 91 [Blank]
146 92 Hold
147 93 Silence 24?
148 94 [Blank] 78 [Blank]
149 95 [Blank]
150 96 [Blank]
151 97 [Blank]
152 98 [Blank]
153 99 [Blank]
154 9A [Blank]
155 9B [Blank]
156 9C [Blank]
157 9D [Blank]
158 9E [Blank]
159 9F [Blank]
160 A0 [Blank]
161 A1 [Blank]
162 A2 [Blank]
163 A3 [Blank]
164 A4 [Blank]
165 A5 [Blank]
166 A6 [Blank]
167 A7 [Blank]
168 A8 [Blank]
169 A9 [Blank]
170 AA [Blank]
171 AB [Blank] 24?
172 AC [Blank]
173 AD [Blank]
174 AE [Blank]
175 AF [Blank]
176 B0 [Blank]
177 B1 [Blank]
178 B2 [Blank]
179 B3 [Blank]
180 B4 [Blank]
181 B5 [Blank]
182 B6 [Blank]
183 B7 [Blank]
184 B8 [Blank]
185 B9 [Blank]
186 BA [Blank]
187 BB [Blank]
188 BC [Blank]
189 BD [Blank]
190 BE [Blank]
191 BF [Blank]
192 C0 [Blank]
193 C1 [Blank]
194 C2 [Blank]
195 C3 [Blank] 24?
196 C4 [Blank]
197 C5 [Blank]
198 C6 [Blank]
199 C7 [Blank]
200 C8 [Blank]
201 C9 [Blank]
202 CA [Blank]
203 CB [Blank]
204 CC [Blank]
205 CD [Blank]
206 CE [Blank]
207 CF [Blank]
208 D0 [Blank]
209 D1 [Blank]
210 D2 [Blank]
211 D3 [Blank]
212 D4 [Blank]
213 D5 [Blank]
214 D6 [Blank]
215 D7 [Blank]
216 D8 [Blank]
217 D9 [Blank]
218 DA [Blank]
219 DB [Blank] 16?
220 DC [Blank]
221 DD [Blank]
222 DE [Blank]
223 DF [Blank]
224 E0 [Blank]
225 E1 [Blank]
226 E2 [Blank]
227 E3 Confuse
228 E4 Hold
229 E5 ~race
230 E6 Hold
231 E7 [Blank]
232 E8 Silence
233 E9 Confuse
234 EA Berserk
235 EB Off-21 Total offsets =24
236 EC Off-20
237 ED Off-19
238 EE Off-18
239 EF Off-17
240 F0 Off-16
241 F1 Off-15
242 F2 Off-14
243 F3 Off-13
244 F4 Off-12
245 F5 Off-11
246 F6 Off-10
247 F7 Off-9
248 F8 Off-8
249 F9 Off-7
250 FA Off-6
251 FB Off-5
252 FC Off-4
253 FD Off-3
254 FE Off-2
255 FF Off-1


EDGE
Dec Hex

0 0 Off 0 Total offsets =24
1 1 Off 1
2 2 Off 2
3 3 [Blank] 8 [Blank] + 16?
4 4 [Blank]
5 5 [Blank]
6 6 [Blank]
7 7 [Blank]
8 8 [Blank]
9 9 [Blank]
10 A [Blank]
11 B ~Suct
12 C eathe
13 D Keal2
14 E SPELL CYCLER
15 F SPELL CYCLER
16 10 ~ellfi
17 11 Hold
18 12 per~Wr
19 13 [Blank]
20 14 [Blank]
21 15 [Blank]
22 16 Flare
23 17 Silence
24 18 Silence
25 19 [Blank]
26 1A Hold
27 1B Silence 1 white magic +23 [Blank]
28 1C [Blank]
29 1D [Blank]
30 1E [Blank]
31 1F [Blank]
32 20 [Blank]
33 21 [Blank]
34 22 [Blank]
35 23 [Blank]
36 24 [Blank]
37 25 [Blank]
38 26 [Blank]
39 27 [Blank]
40 28 [Blank]
41 29 [Blank]
42 2A [Blank]
43 2B [Blank]
44 2C [Blank]
45 2D [Blank]
46 2E [Blank]
47 2F [Blank]
48 30 [Blank]
49 31 [Blank]
50 32 [Blank]
51 33 [Blank] 24 [Blank]
52 34 [Blank]
53 35 [Blank]
54 36 [Blank]
55 37 [Blank]
56 38 [Blank]
57 39 [Blank]
58 3A [Blank]
59 3B [Blank]
60 3C [Blank]
61 3D [Blank]
62 3E [Blank]
63 3F [Blank]
64 40 [Blank]
65 41 [Blank]
66 42 [Blank]
67 43 [Blank]
68 44 [Blank]
69 45 [Blank]
70 46 [Blank]
71 47 [Blank]
72 48 [Blank]
73 49 [Blank]
74 4A [Blank]
75 4B [Blank] 24 [Blank]
76 4C [Blank]
77 4D [Blank]
78 4E [Blank]
79 4F [Blank]
80 50 [Blank]
81 51 [Blank]
82 52 [Blank]
83 53 [Blank]
84 54 [Blank]
85 55 [Blank]
86 56 [Blank]
87 57 [Blank]
88 58 [Blank]
89 59 [Blank]
90 5A [Blank]
91 6B [Blank]
92 5C [Blank]
93 5D [Blank]
94 5E [Blank]
95 5F [Blank]
96 60 [Blank]
97 61 [Blank]
98 62 [Blank]
99 63 [Blank] 8 [Blank] + 16?
100 64 [Blank]
101 65 [Blank]
102 66 [Blank]
103 67 [Blank]
104 68 [Blank]
105 69 [Blank]
106 6A [Blank]
107 6B Confuse
108 6C Hold
109 6D ~race
110 6E Hold
111 6F [Blank]
112 70 Silence
113 71 Confuse
114 72 Berserk
115 73 ngBlod
116 74 r~Mons
117 75 [Blank]
118 76 [Blank]
119 77 Mini
120 78 Raise
121 79 Haste
122 7A [Blank]
123 7B Monst0
124 7C ~~~~Be
125 7D Hold
126 7E Bio
127 7F ndBlast
128 80 Hold
129 81 Sleep
130 82 Chocobo
131 83 Hold
132 84 nst000
133 85 ~dMist
134 86 [Blank]
135 87 Hold
136 88 ~uckDi
137 89 r~Mons
138 8A [Blank]
139 8B Hold
140 8C Death
141 8D nst000
142 8E [Blank]
143 8F Hold
144 90 Mini
145 91 Raise
146 92 Silence
147 93 [Blank] 24?
148 94 t000Mo
149 95 Ifrit
150 96 [Blank]
151 97 Cockatrice
152 98 [Blank]
153 99 00Mons
154 9A Pois
155 9B Toad
156 9C ~shura
157 9D Keal3
158 9E Protect
159 9F ~~Ashu
160 A0 ~estru
161 A1 Keal3
162 A2 nst015
163 A3 Keal3
164 A4 Levitate
165 A5 ~onst0
166 A6 Keal2
167 A7 Blink
168 A8 16Glan
169 A9 Keal3
170 AA Keal2
171 AB ce~Bl 24?
172 AC Toad
173 AD Levitate
174 AE ~ingrt
175 AF ~ongCu
176 B0 Rabur
177 B1 ce~Bl
178 B2 ~ethSo
179 B3 Fire3
180 B4 aster
181 B5 Holy
182 B6 Rabur
183 B7 ~pDeat
184 B8 Teleport
185 B9 Slow
186 BA aster
187 BB Keal1
188 BC Arise
189 BD ~~~~Be
190 BE Shell
191 BF Confuse
192 C0 aster
193 C1 ~lecWa
194 C2 Fire3
195 C3 ~lap 24?
196 C4 Teleport
197 C5 Mini
198 C6 zeMind
199 C7 Reflect
200 C8 Blink
201 C9 ~~~Cold
202 CA Rabur
203 CB Arise
204 CC ~nupPu
205 CD ngDime
206 CE Raise
207 CF pil
208 D0 xpldHa
209 D1 Sight
210 D2 ~~ure
211 D3 ~ching
212 D4 Levitate
213 D5 ~~Tong
214 D6 ~areNe
215 D7 Arise
216 D8 ~~Nuke
217 D9 Levitate
218 DA Slow
219 DB ~rsDis 16?
220 DC Teleport
221 DD slow
222 DE ~~~Re
223 DF Sight
224 E0 slow
225 E1 ~~~Re
226 E2 Sight
227 E3 slow
228 E4 ~~Nuke
229 E5 Levitate
230 E6 slow
231 E7 ~~~Re
232 E8 Arise
233 E9 slow
234 EA ~rsDis
235 EB Off-21 Total offsets =24
236 EC Off-20
237 ED Off-19
238 EE Off-18
239 EF Off-17
240 F0 Off-16
241 F1 Off-15
242 F2 Off-14
243 F3 Off-13
244 F4 Off-12
245 F5 Off-11
246 F6 Off-10
247 F7 Off-9
248 F8 Off-8
249 F9 Off-7
250 FA Off-6
251 FB Off-5
252 FC Off-4
253 FD Off-3
254 FE Off-2
255 FF Off-1


XIV. COMBINED LIST OF ALL KNOWN OFFSETS

COMBINED

Cecil 8,1
Cecil 8,2
Cecil 8,3
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
Keal1
Sight
Hold
Keal2
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
Rydia B 1,1
Rydia B 1,2
Rydia B 1,3
Rydia B 2,1
Rydia B 2,2
Rydia B 2,3
Rydia B 3,1
Rydia B 3,2
Rydia B 3,3
Rydia B 4,1
Rydia B 4,2
Rydia B 4,3
Rydia B 5,1
Rydia B 5,2
Rydia B 5,3
Rydia B 6,1
Rydia B 6,2
Rydia B 6,3
Rydia B 7,1
Rydia B 7,2
Rydia B 7,3
Rydia B 8,1
Rydia B 8,2
Rydia B 8,3
Rydia C 1,1
Rydia C 1,2
Rydia C 1,3
Rydia C 2,1
Rydia C 2,2
Rydia C 2,3
Rydia C 3,1
Rydia C 3,2
Rydia C 3,3
Rydia C 4,1
Rydia C 4,2
Rydia C 4,3
Rydia C 5,1
Rydia C 5,2
Rydia C 5,3
Rydia C 6,1
Rydia C 6,2
Rydia C 6,3
Rydia C 7,1
Rydia C 7,2
Rydia C 7,3
Rydia C 8,1
Rydia C 8,2
Rydia C 8,3
Keal2
Confuse
Blink
Esuna
Raise
Teleport
Hold
Silence
Protect
Shell
Slow
Haste
Berserk
Reflect
Dispel
Rabur
Keal1
Keal3
Keal4
Arise
Mini
Sight
Levitate
[Blank]
Fire1
Blizzard1
Thunder1
Stop
Aspir
Toad
Piggy
Dejon
Poison
Fire2
Fire3
Blizzard2
Blizzard3
Thunder2
Thunder3
Bio
Tornado
Sleep
Break
Drain
Meteo
[Blank]
[Blank]
[Blank]
Rosa 1,1
Rosa 1,2
Rosa 1,3
Rosa 2,1
Rosa 2,2
Rosa 2,3
Rosa 3,1
Rosa 3,2
Rosa 3,3
Rosa 4,1
Rosa 4,2
Rosa 4,3
Rosa 5,1
Rosa 5,2
Rosa 5,3
Rosa 6,1
Rosa 6,2
Rosa 6,3
Rosa 7,1
Rosa 7,2
Rosa 7,3
Rosa 8,1
Rosa 8,2
Rosa 8,3
Fire1
Blizzard1
Thunder1
Sleep
Poison
Blizzard2
Piggy
Fire2
Thunder2
Stop
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
Keal1
Hold
Rabur
Slow
Sight
Raise
Protect
Keal2
Silence
Berserk
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
Hold
Silence
Confuse
Blink
Protect
Shell
Slow
Haste
Berserk
Reflect
Keal3
Dispel
Rabur
Keal1
Keal2
Keal3
Cecil 1,1
Cecil 1,2
Cecil 1,3
Cecil 2,1
Cecil 2,2
Cecil 2,3
Cecil 3,1
Cecil 3,2
Cecil 3,3
Cecil 4,1
Cecil 4,2
Cecil 4,3
Cecil 5,1
Cecil 5,2
Cecil 5,3
Cecil 6,1
Cecil 6,2
Cecil 6,3
Cecil 7,1
Cecil 7,2
Cecil 7,3
Bio
Tornado
Quake
Sleep
Break
Death
Stop
Drain
Aspir
Meteo
Flare
Edge 1,1
Edge 1,2
Edge 1,3
Edge 2,1
Edge 2,2
Edge 2,3
Edge 3,1
Edge 3,2
Edge 3,3
Edge 4,1
Edge 4,2
Edge 4,3
Edge 5,1
Edge 5,2
Edge 5,3
Edge 6,1
Edge 6,2
Edge 6,3
Edge 7,1
Edge 7,2
Edge 7,3
Edge 8,1
Edge 8,2
Edge 8,3
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
~Suct
eathe
Keal2
SPELL CYCLER
SPELL CYCLER
~trmJu
Hold
per~Wr
[Blank]
[Blank]
[Blank]
Flare
Silence
Silence
[Blank]
Hold
Silence
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
[Blank]
Confuse
Hold
race
Hold
[Blank]
Silence
Confuse
Berserk
ngBlod
r~Mons
[Blank]
[Blank]
Mini
Raise
Haste
[Blank]
Monst0
~~~~Be
Hold
Bio
ndBlast
Hold
Sleep
Chocobo
Hold
nst000
~dMist
[Blank]
Hold
~uckDi
r~Mons
[Blank]
Hold
Death
nst000
[Blank]
Hold
Mini
Raise
Silence
[Blank]
t000Mo
Ifrit
[Blank]
Cockatrice
[Blank]
00Mons
Pois
Toad
~shura
Keal3
Protect
~~Ashu
~estru
Keal3
nst015
Keal3
Levitate
~onst0
Keal2
Blink
16Glan
Keal3
Keal2
ce~Bl
Toad
Levitate
~ingrt
~ongCu
Rabur
ce~Bl
~ethSo
Fire3
aster
Holy
Rabur
~pDeat
Teleport
Slow
aster
Keal1
Arise
~~~~Be
Shell
Confuse
aster
~lecWa
Fire3
~lap
Teleport
Mini
zeMind
Reflect
Blink
~~~Cold
Rabur
Arise
~nupPu
ngDime
Raise
pil
xpldHa
Sight
~~ure
~ching
Levitate
~~Tong
~areNe
Arise
~~Nuke
Levitate
Slow
~rsDis
Teleport
slow
~~~Re
Sight
slow
~~~Re
Sight
slow
~~Nuke
Levitate
slow
~~~Re
Arise
slow
~rsDis
Off-21
Off-20
Off-19
Off-18
Off-17
Off-16
Off-15
Off-14
Off-13
Off-12
Off-11
Off-10
Off-9
Off-8
Off-7
Off-6
Off-5
Off-4
Off-3
Off-2
Off-1


Part 2: Choosing Specific Spells and Cells by Address

   CHOOSING SPELLS BY ADDRESS

It is possible to place any specific spell into a given cell by 
adding the spell code (in hex) to the cell's address. If 0B is 
the spell code for HOLY, then 7E15600B will put Holy into 
Cecil's spell menu at row 1, column 1 All codes are in Pro 
Action Replay / Gameshark but can be converted to Game Genie by 
a converter. All codes work with both FF4j and FF2us.

CECIL
 1      2       3
1 7E1560 7E1561 7E1562
2 7E1563 7E1564 7E1565
3 7E1566 7E1567 7E1568
4 7E1569 7E156A 7E156B
5 7E156C 7E156D 7E156E
6 7E156F 7E1570 7E1571
7 7E1572 7E1573 7E1574
8 7E1575 7E1576 7E1577

OLD RYDIA BLACK
 1      2      3
1 7E15A8 7E15A9 7E15AA
2 7E15AB 7E15AC 7E15AD
3 7E15AE 7E15AF 7E15B0
4 7E15B1 7E15B2 7E15B3
5 7E15B4 7E15B5 7E15B6
6 7E15B7 7E15B8 7E15B9
7 7E15BA 7E15BB 7E15BC
8 7E15BD 7E15BE 7E15BF

OLD RYDIA CHARM
 1      2      3
1 7E15C0 7E15C1 7E15C2
2 7E15C3 7E15C4 7E15C5
3 7E15C6 7E15C7 7E15C8
4 7E15C9 7E15CA 7E15CB
5 7E15CC 7E15CD 7E15CE
6 7E15CF 7E15D0 7E15D1
7 7E15D2 7E15D3 7E15D4
8 7E15D5 7E15D6 7E15D7

ROSA
 1      2      3
1 7E1608 7E1609 7E160A
2 7E160B 7E160C 7E160D
3 7E160E 7E160F 7E1610
4 7E1611 7E1612 7E1613
5 7E1614 7E1615 7E1616
6 7E1617 7E1618 7E1619
7 7E161A 7E161B 7E161C
8 7E161D 7E161E 7E161F

EDGE
 1      2      3
1 7E1680 7E1681 7E1682
2 7E1683 7E1684 7E1685
3 7E1686 7E1687 7E1688
4 7E1689 7E168A 7E168B
5 7E168C 7E168D 7E168E
6 7E168F 7E1690 7E1691
7 7E1692 7E1693 7E1694
8 7E1695 7E1696 7E1697




Part 3: Changing Current and Max MP Values

  MAGIC POINTS

It is possible to change character MP by adding the desired
values (in hex) to the below address.  Since MP is defined as
two bytes, you must use two addresses.
The values will be 256*the value of the top address +1* the 
value of the bottom address.  To give Cecil a Max HP of 580, use
02 and 42 because 2*256+66=580.  (42 hex is 66 in decimal)
The codes would be 7E104E02  and 7E104D42
All codes are in Pro Action Replay / Gameshark but can be
converted to Game Genie by a converter.
All codes work with both FF4j and FF2us.

 Current MP Max MP

Cecil 7E104C 7E104E
      7E104B 7E104D

Rydia 7E10CC 7E10CE
      7E10CB 7E10CD

Kain 7E100C 7E100E
     7E100B 7E100D

Rosa 7E110C 7E110E
     7E110B 7E110D

Edge 7E108C 7E108E
     7E108B 7E108D
````
