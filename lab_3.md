# Lab Report 3 - Researching Commands
## Grep -o
One way to use the grep command is to use it with -o.
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

---

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

I found out about this command while looking through this site: [Link](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

## Grep -n
Another way to use the grep command is to use it with -n.
This commmand finds the associated string and prints out the line number of where it's found, along with the whole string it is found in.

For the first example, I used the same file used in the previous first example, pmed.0010008.txt.

Input:

`grep -n "disease" plos/pmed.0010008.txt`

Output:

```
7:        individuals, resulting in chronic obstructive pulmonary disease (COPD) and emphysema, two
9:        helper cells in the pathogenesis of obstructive lung disease has been established with
11:        disease [4,5,6,7]. A potential role for T cells in COPD has also been suggested in several
41:        with no evidence of smoking-related lung disease. Analysis of chemokine receptor expression
45:        non-smoking-related obstructive lung disease. The same cells spontaneously secreted more
59:          COPD and no evidence of emphysema (control group) and eighteen individuals (diseased
186:          this variation did not correlate with the presence of disease in either group (data not
209:          characteristic of this disease. Further, we have shown for the first time, to our
276:        cells is unique to people with smoking-related lung disease, despite cessation of exposure
278:        obstructive lung disease or emphysema have comparatively little Th1-biased inflammation in
281:        non-smoker individuals with severe obstructive lung disease due to cystic fibrosis or
294:        severe atopic dermatitis, which decreased upon abatement of disease activity [26,43].
342:        of preventing or halting smoking-related lung disease may be possible.
```

This command looked through all the strings in the text file to find where the desired string is, in this case "disease," and printed out the line number as well as the whole string associated with the desired word. Although it isn't visible, the terminal highlights the desired word in red. This is useful to see the different contexts of the word you're looking for.

---

In the second example, I used Annual_Fee.txt again.

Input: 

`grep -n "attorneys" government/Media/Annual_Fee.txt`

Output:

```
15:inactive but wish to remain on the roll of attorneys pay $90.
29:a commitment by the full court, and by attorneys in Illinois, to
32:There are now more than 57,000 active attorneys in Illinois.
55:for all attorneys in the state how important it is that lawyers be
```

Using the same logic as the first example, the command looked through the text file for the word "attorneys" then printed out the line number and other strings surrounding the word.

I found out about this command by looking at this website: [Link](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

# Grep -c
An additional way to use the grep command is to pair it with -c.
This command allows the user to count the amount of times the specified string is found in the file.

Since we've used -o on pmed.0010008.txt, let's try using -c on this file to see if the output is correct.

Input:

`grep -c "disease" plos/pmed.0010008.txt`

Output:

`13`

By comparing the amount of time "disease" popped up when using -o and this newly used command, we can see that both of them give a resulting answer of 13. Since this command counts how many times "disease" was found within the file, it printed out 13. This would be useful for seeing the frequency of a word within a file.

---

For the second example, let's do the same thing and compare the two different commands in Annual_Fee.txt.

Input:

`grep -c "attorneys" government/Media/Annual_Fee.txt`

Output:

`4`

When comparing the commands, we can see that when we used -o, "attorneys" was printed out 4 times. Using -c also shows us that the word shows up 4 times within the file. Again, at times it would be useful to see how many times a certain word is being used within a file.

This command was found by looking at this website: [Link](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)

# Grep -l
One final way that I've found to use the grep command is to use -l.
This command searches all the files in the specified path and prints out the files that contain the specified string.

In my first example, I'll look through plos to see which files contain "organisms."

Input:

`grep -l "organisms" plos/*`

Output:

```
plos/journal.pbio.0020012.txt
plos/journal.pbio.0020035.txt
plos/journal.pbio.0020042.txt
plos/journal.pbio.0020043.txt
plos/journal.pbio.0020053.txt
plos/journal.pbio.0020068.txt
plos/journal.pbio.0020071.txt
plos/journal.pbio.0020100.txt
plos/journal.pbio.0020133.txt
plos/journal.pbio.0020146.txt
plos/journal.pbio.0020147.txt
plos/journal.pbio.0020164.txt
plos/journal.pbio.0020183.txt
plos/journal.pbio.0020190.txt
plos/journal.pbio.0020206.txt
plos/journal.pbio.0020213.txt
plos/journal.pbio.0020215.txt
plos/journal.pbio.0020232.txt
plos/journal.pbio.0020272.txt
plos/journal.pbio.0020276.txt
plos/journal.pbio.0020302.txt
plos/journal.pbio.0020306.txt
plos/journal.pbio.0020307.txt
plos/journal.pbio.0020347.txt
plos/journal.pbio.0020400.txt
plos/journal.pbio.0020406.txt
plos/journal.pbio.0020439.txt
plos/journal.pbio.0020440.txt
plos/journal.pbio.0030021.txt
plos/journal.pbio.0030062.txt
plos/journal.pbio.0030065.txt
plos/journal.pbio.0030094.txt
plos/journal.pbio.0030102.txt
plos/pmed.0020015.txt
plos/pmed.0020158.txt
plos/pmed.0020210.txt
plos/pmed.0020231.txt
```

Here we can see that it looked through all the files within plos to see if it contained the word "organisms." All files that contained this word are seen here, and the files that don't are omitted. This command is useful to see which files talk about a certain topic / contain certain things you're looking for.

---

For the second example, we will look through government/Media to find the word "taxes."

Input:

`grep -l "taxes" government/Media/*`

Output:

```
government/Media/Anthem_Payout.txt
government/Media/Helping_Out.txt
government/Media/Legal_system_fails_poor.txt
government/Media/New_funding_sources.txt
government/Media/The_Columbian.txt
```

We can see that only 5 files within the path government/Media contained the word "taxes." Again, this is useful for looking for files that talk about a certain subject that you're interested in.

I found out about this command in this website: [Link](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)
