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

While it's supposed to reverse the input array, the bounds for the integer `i` are too wide, causing the method copy the entire length of the array. Which leaves us with a mirrored doubling of a half of the array. 

```
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```

Despite the buggy code, this test method will run flawlessly because, since the length of the array is 1, there is nothing to be mirrored or copied.

<img width="916" alt="Screen Shot 2023-01-30 at 5 08 48 PM" src="https://user-images.githubusercontent.com/122495687/215633123-686f9350-f908-4e76-95ef-bd58e3c4ce78.png">

However, this test method fails.

```
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3, 2 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 2, 3 }, input1);
	}
```

<img width="922" alt="Screen Shot 2023-01-30 at 5 07 59 PM" src="https://user-images.githubusercontent.com/122495687/215633224-826188fc-4de1-43af-a00d-1a2c38b7d442.png">

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
