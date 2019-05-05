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