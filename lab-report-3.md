# GREP
##### Leo Nguyen (B260)
---
## Some GREP options

```
grep -i (ignores cases in the search)
grep -c (returns the count of lines that match the search)
grep -A n (returns the searched line + n lines after)
grep -l (returns a list of matching filenames)
```

---

## Examples

#### grep -i

This command can be useful in situations where you only need to search for a keyword regardless of whether or not it begins a sentence.

Example 1:
```
grep -r -i "god of the sea"
```

returns:
```
./travel_guides/berlitz2/Athens-History.txt:In ancient Greek mythology Athens is named following a contest between Athena, goddess of wisdom, and Poseidon, god of the sea. Both had their eye on the prize real estate, so it was agreed that whoever could come up with the more useful gift for mortals would win. The half-human, half-serpent king of Athens, Cecrops, acted as arbiter. 
```
This example searches recursively for any lines that contain the words "god of the sea" regardless of case.

Example 2:
```
grep -r -i "they ruled the seas, plundering ships at will"
```

returns:
```
./travel_guides/berlitz2/Bahamas-Intro.txt:The islands of the Bahamas were claimed by the English, but hundreds of secret coves became home to pirates and smugglers who turned their backs on nationality to enter the brotherhood of buccaneers. They ruled the seas, plundering ships at will, and then spent their ill-gotten gains in the bars and brothels of Nassau town, the main settlement.
```
This example searches recursively for the given quote and can be useful for finding certain quotes in files.

#### grep -c

This can be useful for determining the importance of certain keywords by referencing their popularity in the file or directory.

Example 1:
```
grep -c "Italy" travel_guides/berlitz1/WhatToItaly.txt
```

returns:
```
/WhatToItaly.txt
travel_guides/berlitz1/WhatToItaly.txt:8
```
This example finds the count of lines in WhatToItaly.txt that contain the word "Italy".

Example 2:
```
grep -i -c "the" travel_guides/berlitz1/HandRIstanbul.txt
```

returns:
```
5
```
This command returns the count of lines in HandRIstanbul.txt that contain the word "the".

#### grep -A n

This can be useful for finding context surrounding a certain keyword.

Example 1:
```
grep -A 1 "often narrated" non-fiction/OUP/Castro/chB.txt
```

returns:
```
As the tale is often narrated, a disobedient young girl goes to the dance without her parents’ permission, or she goes against her mother’s express wishes. While at the dance a handsome beautifully dressed man asks her to dance. They dance all night, until she suddenly notices with a shock that he isn’t wearing shoes, and in fact he doesn’t even have feet; instead he has chicken feet, goat’s hooves, or a pig’s foot and a chicken foot. It is usually at this point, after he’s discovered, that he disappears into thin air, leaving the odor of sulfur in the air, or, in some versions of the legend, just runs out the door. The girl he was dancing with either faints or burns to death as she goes up in smoke. If the girl doesn’t die, as in some stories, she might suffer a burn on the shoulder or a man’s handprint might be found on her back. A small circle of people who are present at the dance observe this encounter, and the narrator of the story usually says that she or he heard it from someone who was there.
The lesson learned is that one must not disobey one’s parents, for the handsome man is known to be the devil and the personification of evil. It is noted that mostly women narrate these legends, among themselves or from mothers to daughters, in a didactic fashion, to instill fear in young women so that they will not disregard parental authority. In some variants a young girl specifically transgresses religious beliefs by insisting on going to a dance on Good Friday, a religious holy day, and a revered day of prayer in Chicano Catholic households. The appearance of the devil on this day is an especially ominous sign.
```
This command returns the line containing "often narrated" and the one after that.

Example 2:
```
grep -A 1 "romantic cowboy of Hollywood" non-fiction/OUP/Castro/chV.txt
```

returns:
```
The Mexican vaquero was a laborer, a peon who was used by the missionaries to ride the horses and take care of the cattle. So it was the culture of the vaquero that became the basis for the romantic cowboy of Hollywood. The ensemble, equipment, and clothing of the vaquero evolved through the years as a combination of Spanish leather and regional indigenous fabrics. He always wore a sombrero with a wide brim, a leather chaqueta (jacket), tight-fitting knee-length sotas (breeches), and botas (leather leggings) for protection. The vaquero also wore iron spurs, like those worn by the Conquistadores, which are still worn to this day. The various styles of saddles, from the Moorish to the Spanish war saddle, eventually changed when the vaqueros began making their own saddles, more suitable for riding hard and for quick mounting and dismounting.
The early vaqueros, those of the sixteenth and seventeenth centuries, were mestizos, Indians, Negroes, and mulattos. When Anglo Americans moved into Texas and bought enormous tracts of land, they established huge ranches and hired Mexican vaqueros to work them. They recruited and moved whole families from Mexico to work and live on their ranches. The King and Kennedy ranches of east Texas are contemporary examples of this tradition and have many generations of Mexican vaqueros still living on their ranches. A social historical study of the vaquero life on the King and Kennedy ranches, from the early nineteenth century to the present, has been written by Monday and Colley.
```
This command returns the line containing "romantic cowboy of Hollywood" and the line after.

#### grep -l

This can be useful for figuring out which files to look through for certain words.

Example 1:
```
grep -r -l "romantic cowboy of Hollywood"
```

returns:
```
./non-fiction/OUP/Castro/chV.txt
```
This command returns the name of the text file that contains the search "romantic cowboy of Hollywood".

Example 2:
```
grep -r -l "often narrated"
```

returns:
```
./non-fiction/OUP/Castro/chB.txt
```
This command returns the name of the text file that contains the search "often narrated".

---

## Source

All command options used in this report were found on 

[Source](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
