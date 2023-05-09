# Lab Report 3 - Researching Commands
## Find -o
One way to use the find command is to use it with -o.
This command displays the matched string on new lines found within the file.

For the first example, I used the command on a txt file in plos called pmed.0010008.txt.

Input:

`grep -o "disease" plos/pmed.0010008.txt`

Output:

```
disease
disease
disease
disease
disease
disease
disease
disease
disease
disease
disease
disease
disease
```

What this command did in particular for this file was scrounge through the file for the exact string "disease." Every time it finds that word, it prints "disease" out on a new line. This is useful for when you want to see how many of the same word is being used in the file.

For the second example, I used the command on a file in government/Media called Annual_Fee.txt.

Input:

`grep -o "attorneys" government/Media/Annual_Fee.txt`

Output:

```
attorneys
attorneys
attorneys
attorneys
```

As described like in the previous example, the command looked through the Annual_Fee.txt file and printed out the word "attorneys" every time it is found in the file. 
