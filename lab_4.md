# Lab Report 4 - Command Line
## Logging into ieng6
First I logged into the remote server with:

`ssh cs15lsp23ru@ieng6.ucsd.edu`

then pressed `<Enter>`.

This screen indicated that I logged in:
  
![Image](Lab4_Pics/login_ieng6.png)

## Cloning fork of repository
  
After that process, I made a clone of my fork of the repository by typing:
  
`git clone git@github.com:CBelleLopez/lab7.git`
  
then pressed `<Enter>` to confirm.
  
This is what shows up after running the command:
  
![Image](Lab4_Pics/git_clone_2.png)

## Running the tests

I made sure to `cd` into lab7 so that I could run the tests by typing:
  
`bash test.sh`
  
The picture below indicates that the tests fail:
  
![Image](Lab4_Pics/test_failure.png)

## Editing the file
  
To edit the file causing the errors, we have to use `vim` so we type:
  
`vim ListExamples.java`
  
The file should open up and looks like this:
  
![Image](Lab4_Pics/ListExamples_file.png)
  
To navigate where the error is, I started typing in `/while(index2` then pressed `<Enter>`. Next I pressed
`<j><j><j><2w><h><h>` then deleted the "1" by pressing `<x>`. To insert "2", I pressed `<i><2>`. To exit 
insert mode, I pressed `<esc>` and to save the changes I've made, I typed in `:wq`.

This is what it should look like after the change has been made:

![Image](Lab4_Pics/change_file.png)

## Running the tests (again)
  
This is what should show up after running `bash test.sh` again:
  
![Image](Lab4_Pics/test_success.png)

## Commiting & Pushing
  
To commit and push the changes to my Github account, I ran the command:
  
`git add ListExamples.java` then `git commit`

Running `git commit` will lead you to this page:

![Image](Lab4_Pics/new_commit.png)

To edit that page and add a commit message, press `<i>` to enter INSERT mode then I typed in the message `Updated ListExamples.java`. After typing that in, I pressed `<esc>` to exit INSERT mode then saved and quit the commit message by typing `:wq`.
  
![Image](Lab4_Pics/commit_message.png)
  
The changes should show up like this after a commit message is added:
  
![Image](Lab4_Pics/git_commit.png)

Last but not least, this is what should show up when `git push` is successfully executed:

![Image](Lab4_Pics/git_push.png)
