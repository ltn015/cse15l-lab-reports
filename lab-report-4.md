# Lab Report 4
##### Leo Nguyen (B260)
---
## Bash Racing

<img width="659" alt="Screen Shot 2023-03-13 at 9 59 12 PM" src="https://user-images.githubusercontent.com/122495687/224899326-b51ca5f5-f896-4aae-8df4-37b4c7191c70.png">

Keys pressed: *ctrl+r, s, enter, password, enter*

The command ```ssh cse15lwi23adq@ieng6.ucsd.edu``` logs me into the CSE remote account where I will be modifying the code later on.

<img width="1352" alt="Screen Shot 2023-01-30 at 4 14 38 PM" src="https://user-images.githubusercontent.com/122495687/215628041-b81d4b30-4306-41ab-9b65-c2b56d0146d2.png">

At this point, `bigOlBoi` still carries the previous value of "YAH\n". This second request calls the `requestHandler` method again. This time, it updates `bigOlBoi` by adding "yeet\n" to it. The contents of `bigOlBoi` are then returned to be displayed on the server.

---

## Fixing Buggy Code

#### This method does not work correctly

```
  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
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

   
   
   
   
   
     
