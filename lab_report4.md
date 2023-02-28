# Lab Report 4 - Lab 7 Competition Recreation (Steps 4 to 9)

## First Step (Step 4)~ Logging into ieng6 Account
- I opened the terminal & typed in "`ssh`" in the first available command-line. Following this, I press `<Ctrl>` + `<R>` simultaneously, & proceeded to enter "`ie`" in terminal until it showed up my UCSD username, "`cs15lwi23aoh@ieng6.ucsd.edu`" in the command-line, I pressed `<Enter>` to select the option. Following this I was successfully logged onto the server (usually I would need a password but I set up prior to skip this step).
![image](https://user-images.githubusercontent.com/122498399/221482594-0df86fe5-9cf0-415e-aa9a-df166e2a39c5.png)

## Second Step (Step 5)~ Cloning Fork of Repository
- This step was straightforward,I went ahead and clicked on the linked page in the Week 7 Github, through "`the lab 7 repo`" link where I would click on "`<> code`" for a drop down. Through this drop down, I will click on the icon next to the URL in the drop down, to successfully copy the repository. Following this, I will type in the command, "`git clone https://github.com/ucsd-cse15l-w23/lab7.git`" to clone the repository onto the server.

![image](https://user-images.githubusercontent.com/122498399/221489122-2bd0c1c2-cc5a-4702-8416-434dc690800b.png)
  
## Third Step (Step 6)~ Compile & Run Test
- The steps to compile & run was simple. I accessed the javac compiler (`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`) by going 5 up in the search history, while the java command for running (`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`) was 6 up in the search history. (Keys pressed for compile: " `<up>` `<up>` `<up>` `<up>` `<up>` `<enter>` "; Keys pressed for run: " `<up>` `<up>` `<up>` `<up>` `<up>` `<up>` `<enter>` ")
![image](https://user-images.githubusercontent.com/122498399/221745610-547bc3fb-52f1-4bcc-a644-4114f58617db.png)

## Fourth Step (Step 7)~ Fixing The Code
- To go into the code file to edit the code & fix it, we need to use type in "nano" followed by the file name, in this case, we would type in, "`nano ListExamples.java`". Once we have access to the code file, we will use the up, down, left & right arrow keys on our keyboard to navigate around. The problem is located towards the bottom of the file at the last while statement. The while statement is supposed to be checking for & altering variable "index2" yet it alters the value for "index1" instead. So the solution is altering the name for what value is changed in the while statement from "`index1`" to "`index2`". The segment changed is highlighted in yellow (shows as yellow letters)
![image](https://user-images.githubusercontent.com/122498399/221692522-aa889cec-862a-42ff-9b2e-aaeb0e860046.png)
![image](https://user-images.githubusercontent.com/122498399/221692680-6e1e24b9-5d0c-4650-8f14-003c5f0b65eb.png)


## Fifth Step (Step 8)~ Re-run & Re-compile Test
Re-running & re-compiling in step 8 was practically the same as step 6 where we initially compiled & run the tests. I had gone back through terminal history to copy & paste (`<Ctrl>` + `<C>` to copy & `<Ctrl>` + `<V>` to paste) the previous compile command-line (`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`). pressed `<Enter>`, & then copy & paste the run command-line (`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`), & pressed `<Enter>` to finally run the tests again. We should be greeted by 2 tests passing & an `OK (2 tests)` message in the terminal.
![image](https://user-images.githubusercontent.com/122498399/221742199-652b6137-24ac-46c5-968a-c25a7ca257ab.png)

## Final Step (Step 9)~ Commit & Push Results
- The final step is to `commit` & `push` your results onto Github. For this step, I went ahead and ran the command-line `git add ListExamples.java` pressed `<Enter>` & follow that with command-line `git commit -m "fix"`. The `git add ListExamples.java` command-line adds the file into the list of things you'll be adding onto Github, while the `git commit -m "fix"` command-line will commit the changes onto Github, with the "`-m "fix"`" being there to display the message "fix" when you successfully commit the file onto Github.
![image](https://user-images.githubusercontent.com/122498399/221744551-fd5877fc-1b3d-4e7c-9bfa-7b781343e2b3.png)




