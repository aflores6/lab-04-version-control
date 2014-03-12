Lab - Odds and Ends
==========
Follow the instructions line-by-line.  

* Type in the commands as is, but ignore the beginning prompt.  
* Enter, tab, up and down are represented by <ENTER><TAB>,<UP> and <DOWN>.  
* "No output" or "nothing happens" are valid answers to any of the questions.
==========

==========
1. Open a new terminal window.
[NO OUTPUT]
----------
==========
2. In your home directory, start editing a text file called temp.txt using nano.

Write the command you used to do this below.
----------

nano temp.txt

==========
3. Open another terminal

[NO OUTPUT]
----------
==========
3. In this terminal, show (list) all running processes / programs.

Write the command that you used to do this, and the last two lines of output.
----------
ps aux

student         29760   0.0  0.0  2521144   4808   ??  Ss    8:01PM   0:00.02 c
student         29758   0.0  0.1  2539568  10628   ??  SN    8:01PM   0:00.11 /


==========
4. Run the same command, but look for a specific process.  (It's the version of the command that has | grep ...).  Look for the program that you started to edit a file, nano.

Write the command that you used to do this, and all of the output.
----------

ps aux | grep nano
==========
5. Go to your other terminal window.  What happened to nano?  What was the message on the screen?

----------
Received SIGHUP or SIGTERM

==========
6. Close the terminal window that nano was in, and go back to the terminal where you ran ps.

[NO OUTPUT]
----------


==========
7. Now... using nano, create a shell script in your home directory called hello.sh.  It should contain the following text exactly:

#!/bin/bash
echo "hi there!"

Quit and save when you're done.

What command did you use to do this?
----------
nano hello.sh

==========
8. Change the permissions (modify) on hello.sh so that the *user* (u) can *execute* (x) it: 

Write the commands that you used to do this below.
----------
chmod u+x hello.sh

==========
9. Run your script (hello.sh).

How did you do this?  What was the output?
----------
./hello.sh
hi there!

==========
10. Change to the root directory.  Try running your script again (hello.sh).  What was the output (if there's an error, write it out)?
----------

-bash: ./hello.sh: No such file or directory
==========
11. Now trying using the full, absolute path to your script (that is, starting with /...).  What did you write in?  What did it do?
----------
/Users/student

==========
12.  Go back to the directory that your hello.sh script was in.  What command did you use to change to this directory? 
----------
cd ~

==========
13. Type in the following command:

echo $PATH

Write down the output of this command
----------
/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/opt/X11/bin:/usr/local/git/bin

==========
14. Type in the following command to show all environment variables:

env

Write down the last two lines of output for this command
----------
_=/usr/bin/env
OLDPWD=/Users/student


==========
15. Set your PATH to include your home directory.  Do the following (substituting student or username for professor)

PATH=$PATH:/Users/professor

Now check your path again.

echo $PATH

Write down the output of the last command.  It should include your home folder.
----------
/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/opt/X11/bin:/usr/local/git/bin:/Users/professor

==========
16.  Go back to root (/)

Try running your script simply by typing

hello.sh

It should work now!  What is the output?
----------


==========
17.  Save this file in the repository that you created from parts 1 and 2.

Add and commit it to your local repository and push to the remote repository.  Check github to see that your work was submitted.
----------


==========
18.  Optional - Try writing this shell script!

In your repository, create an executable shell script called make_5_files that creates 10 files in the directory that it's called in.  The file names should be:
myfile1.txt
myfile2.txt
.
myfile10.txt

Use a for loop to do this.  Add and save in your repository, push to the remote.
----------


==========
19.  Optional - Try writing this shell script!

In your repository, create an executable shell script called say_twice.  It should take one argument - a filename.  It will cat out the contents of that file twice, with a row of dashes between each (use cat, echo... then cat again).  Create a test file calle foo.txt ... that contains foo, bar and baz... each on separate lines.

Add and save in your repository, push to the remote.

----------
