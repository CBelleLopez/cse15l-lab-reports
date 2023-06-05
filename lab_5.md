# Lab Report 5 - Debugging
## Debugging Scenario
Below is a makeshift debugging scenario on EdStem:

> What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?

I am using my personal MacBook Air and using the terminal in VSCode.

> Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.

After running `bash test.sh` on the files from this link https://github.com/ucsd-cse15l-s23/lab7, it gives me errors such as "illegal start of type," and "[symbol] expected," and "class, interface, enum, or record expected." I'm supposed to just see that JUnit ran the tests successfully and passed. Why am I getting this error?

![Image](Lab5_Pics/terminal_error)

> Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.

In order to access the files from that github link, I `git clone` the link then `cd lab7`. After that, I made sure to change the error in TestExamples.java so that the error pointed out in lab 7 was correctly changed by using `vim TestExamples.java`. I saved and quit my changes then ran bash test.sh and got that error. It says the tests passed but the code in ListExamples.java is wrong apparently.
