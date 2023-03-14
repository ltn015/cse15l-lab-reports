# Lab Report 4
##### Leo Nguyen (B260)
---
## Bash Racing

<img width="659" alt="Screen Shot 2023-03-13 at 9 59 12 PM" src="https://user-images.githubusercontent.com/122495687/224899326-b51ca5f5-f896-4aae-8df4-37b4c7191c70.png">

Keys pressed: *ctrl+r, s, enter, password, enter*

The initial shortcut, *ctrl+r*, allows me to search my command history to find the command I need. The *s* is to search for the ssh command.

The command ```ssh cse15lwi23adq@ieng6.ucsd.edu``` logs me into the CSE remote account where I will be modifying the code later on.

<img width="1352" alt="Screen Shot 2023-03-13 at 9 59 43 PM" src="https://user-images.githubusercontent.com/122495687/224902867-58a4fdb9-ab05-4788-967d-69bc2dd54af9.png">

Keys pressed: *ctrl+r, g, i, t, @, enter*

I again use *ctrl+r* to search for a command. I typed "git@" to find the command I needed. Then, *enter* runs the command.

The command ```git clone git@github.com:ltn015/lab7.git && cd lab7 && javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java && java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` is a combination of many commands that allows me to save time by putting them together. First, it clones my fork of the lab7 repository into the home directory. Then, it navigates into the lab7 directory. It then compiles all java files in the directory. Lastly, it runs the ListExamplesTests file which runs the Junit tests.

<img width="467" alt="Screen Shot 2023-03-13 at 10 01 57 PM" src="https://user-images.githubusercontent.com/122495687/224904109-f9b1c2ab-f0fd-429e-a82d-89dcedca74e1.png">

Keys pressed: *ctrl+r, n, enter*

I searched again for the "nano" command I needed and pressed enter to run the command.

The command ```nano +43,13 ListExamples.java``` allows me to edit the ListExamples.java file.

<img width="1352" alt="Screen Shot 2023-03-13 at 10 00 43 PM" src="https://user-images.githubusercontent.com/122495687/224904408-e280800a-9add-4a16-b2a8-3d3abdde6e63.png">

Keys pressed: *ctrl+x, down (until at the right row), right (until at the right column), backspace, 2, ctrl+x, y, enter*

The first keypresses, *ctrl+x* allows me to edit ListExamples.java rather than creating a new text file. Then, I used the arrow keys to navigate to the incorrect code and corrected it. Then, *ctrl+x* again allows me to exit and save the file. Then, when prompted if I want to save the file, *y* and *enter* save the file.

<img width="1352" alt="Screen Shot 2023-03-13 at 10 01 41 PM" src="https://user-images.githubusercontent.com/122495687/224904887-9100f026-bb46-4f1c-b64a-ccb4214550f8.png">

Keys pressed: *ctrl+r, g, enter*

I again use *ctrl+r* to search for commands as well as *g* as the keyword, then I use *enter* to run the command.

The command ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java && java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests && git add ListExamples.java && git commit -m "finished" && git push``` is also a combination of many commands. First, it compiles all java files in the directory again, after the edit. Then, it runs the tests again. Then, it saves the updated ListExamples.java file and commits and pushes the changes with the message "finished".
---

   
   
   
   
   
     
