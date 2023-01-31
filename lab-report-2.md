# Remote Access Tutorial
##### Leo Nguyen (B260)
---
## StringServer

<img width="1352" alt="Screen Shot 2023-01-30 at 4 14 11 PM" src="https://user-images.githubusercontent.com/122495687/215628063-0da19c13-c639-4021-834c-384aff188d1e.png">

This example shows a request which calls my `requestHandler` method. `requestHandler` takes in parameter `url` and pulls the path from the url. Since this is the first request, the string field `bigOlBoi` was previously empty. Now, `bigOlBoi` is currently equal to the input "YAH" + "\n".

<img width="1352" alt="Screen Shot 2023-01-30 at 4 14 38 PM" src="https://user-images.githubusercontent.com/122495687/215628041-b81d4b30-4306-41ab-9b65-c2b56d0146d2.png">

At this point, `bigOlBoi` still carries the previous value of "YAH\n". This second request calls the `requestHandler` method again. This time, it updates `bigOlBoi` by adding "yeet\n" to it. The contents of `bigOlBoi` are then returned to be displayed on the server.

---

## Fixing bug

1. fsdjl
2. sdhfkl
3. jfksdl
4. jkfdhsl

---

## What I Learned
