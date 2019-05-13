# experiments with Music21 :-)

Chris Greenhalgh, The University of Nottingham 2019.

On MacOS, may need:
- [python3](https://www.python.org/downloads/release/python-373/)
- [music21](http://web.mit.edu/music21/doc/usersGuide/usersGuide_01_installing.html) 
- [QuickTime 7](https://support.apple.com/kb/dl923?locale=en_US) to play midi
- [musescore](https://musescore.org/en/download) to display scores (note, now version 3 so need to update music21 environment:
```
us = environment.UserSettings()
us['musicxmlPath'] = '/Applications/MuseScore 3.app'
```

## e.g.

```
python3
from music21 import *
c = converter.parse('examples/Leo, I-Nc 34.2.6-2 fol. 30v No. 6 reduction.xml')
c.show()
```

## Example 1

Leo, Solfeggio I-Nc 34.2.6-2, fol. 30v No.6 G major Allegro

some transformations
- twice, e.g. Do/G -> Do/[G,G] or Do/G, (Do)/G
- octave, e.g. Do/G4 -> Do/G5
- pair/short, e.g. Do/G4/1.0,Re/A4/1.0 -> [Do/G4/0.5,Re/A4/0.5]
- note then 3rd above, e.g. Do/G4/0.5 -> Do/[G4/0.25,B4/0.25] (note, lower half of scale)
- note then 3rd below, e.g. Me/B4/0.5 -> Me/[B4/0.25,G4/0.25] (note, mid/upper half of scale, after 3rd above)
- twice, e.g. notes/bars(Do,Re,Me,Fa,Sol) x2
- N,+M3,+M2,N,-C1?,N,-C1?,N, e.g. La/E5/2.0 (almost all adjacent?)

NB *online process* with limited (short and long-term) working memory. 
Moving back (a little) in the basic note line is a key strategy for 
keeping track, expanding, repeating and also elaborating/varying. 

Common strategies. Personal strategies. short-term memory - just played.
Long-term memory - "usally" play...

Specific note & elaboration sequences.

(subjective) rolling window/time-discounted estimates of duration distributions
and tone distributions??

what's the relationship between initial key and changes of Do?

Note, presence of "allegro" as mood goal for whole piece.

Social signalling?! e.g. rit to end? standard cadences?