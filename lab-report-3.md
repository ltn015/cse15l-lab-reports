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

Example 2:
```
grep -r -i "they ruled the seas, plundering ships at will"
```

returns:
```
./travel_guides/berlitz2/Bahamas-Intro.txt:The islands of the Bahamas were claimed by the English, but hundreds of secret coves became home to pirates and smugglers who turned their backs on nationality to enter the brotherhood of buccaneers. They ruled the seas, plundering ships at will, and then spent their ill-gotten gains in the bars and brothels of Nassau town, the main settlement.
```

#### grep -c

This can be useful for determining the importance of certain keywords by referencing their popularity in the file or directory.

Example 1:
```
grep -r -c "Italy" travel_guides/berlitz1/WhatToItaly.txt
```
returns:
```
/WhatToItaly.txt
travel_guides/berlitz1/WhatToItaly.txt:8
```
Example 2:
```

```

#### Fixed Code

```
  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int prev = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = prev;
    }
  }
```

This change fixes the bug because, instead of having to iterate through the entire array and accidentally duplicate values, this method now tracks each opposite value and uses it instantly rather than accidentally overwriting it.

---

## What I Learned

I learned that B260 is the smelliest class I have in my current schedule. I also learned how to create Junit tests. I also learned how to lift the chairs in the classroom. I also learned I can get from the CSE building to YORK in about 12 minutes.
