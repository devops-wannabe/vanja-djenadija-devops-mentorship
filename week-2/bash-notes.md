# Bandit Level 0
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port *2220*. The username is bandit0 and the password is **bandit0**. Once logged in, go to the Level 1 page to find out how to beat Level 1.
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
password: bandit0
```

# Bandit Level 0 ➡️ Level 1
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

```bash
ls -la
cat readme
exit
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

# Bandit Level 1 ➡️ Level 2

The password for the next level is stored in a file called - located in the home directory.

```bash
ls -la
cat ./-
exit
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
# Bandit Level 2 ➡️ Level 3

The password for the next level is stored in a file called spaces in this filename located in the home directory.

```bash
ls -la
cat spaces\ in\ this\ filename
exit
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

# Bandit Level 3 ➡️ Level 4

The password for the next level is stored in a hidden file in the inhere directory.

```bash
ls -la
cd inhere
cat .hidden
exit
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

# Bandit Level 4 ➡️ Level 5

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

```bash
ls -la
cd inhere
ls -la
cat ./-file07
exit
ssh bandit5@bandit.labs.overthewire.org -p 2220
```
# Bandit Level 5 ➡️ Level 6

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable

```bash
find . -type f -size 1033c ! -executable -exec ls -lh {} \;
```

# Bandit Level 6 ➡️ Level 7

The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

# Bandit Level 7 ➡️ Level 8

The password for the next level is stored in the file data.txt next to the word millionth.

```bash
cat data.txt | grep "millionth"
```

# Bandit Level 8 ➡️ Level 9

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

```bash
sort -f data.txt | uniq -c | grep "1 "
```

# Bandit Level 9 ➡️ Level 10

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

```python
strings data.txt | grep "="
```

