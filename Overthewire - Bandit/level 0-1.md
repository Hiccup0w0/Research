```
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

Commands you may need to solve this level
ls , cd , cat , file , du , find

TIP: Create a file for notes and passwords on your local machine!

Passwords for levels are not saved automatically. If you do not save them yourself, you will need to start over from bandit0.

Passwords also occasionally change. It is recommended to take notes on how to solve each challenge. As levels get more challenging, detailed notes are useful to return to where you left off, reference for later problems, or help others after you’ve completed the challenge.
```

At this level you just need to learn how to use `ssh` to connect to bandit server.

EX: `bandit0@bandit.labs.overthewire.org -p 2220`  pass is bandit 0 and after getting the password you need to `exit` to exit the server

And at this level you only need to use `ls` command to show how many files and directories there are and `cat` command to read or edit it. you can solve this level or others by many different way.


```
bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: 

bandit0@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.

```
