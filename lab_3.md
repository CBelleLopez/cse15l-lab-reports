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
