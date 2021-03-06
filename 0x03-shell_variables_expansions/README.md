A detailed description of shell variables expansions
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google: General
What happens when you type $ ls -l *.txt
Shell Initialization Files
What are the /etc/profile file and the /etc/profile.d directory
What is the ~/.bashrc file
Variables
What is the difference between a local and a global variable
What is a reserved variable
How to create, update and delete shell variables
What are the roles of the following reserved variables: HOME, PATH, PS1
What are special parameters
What is the special parameter $??
Expansions
What is expansion and how to use them
What is the difference between single and double quotes and how to use them properly
How to do command substitution with $() and backticks
Shell Arithmetic
How to perform arithmetic operations with the shell
The alias Command
How to create an alias
How to list aliases
How to temporarily disable an alias
Other help pages
How to execute commands from a file in the current shell
Requirements General
Allowed editors: vi, vim, emacs
All your scripts will be tested on Ubuntu 14.04 LTS
All your scripts should be exactly two lines long ($ wc -l file should print 2)
All your files should end with a new line (why?)
The first line of all your files should be exactly #!/bin/bash
A README.md file, at the root of the folder of the project, describing what each script is doing
You are not allowed to use &&, || or ;
You are not allowed to use bc, sed or awk
All your files must be executable
More Info
Read your /etc/profile, /etc/inputrc and ~/.bashrc files.
Look at some files in the /etc/profile.d directory.
Note: You do not have to learn about awk, tar, bzip2, date, scp, ulimit, umask, or shell scripting, yet.
What each of the scripts does:
#!/bin/bash (which is always the first line) instructs the operating system to use bash as a command interpreter.
alias ls="rm *" creates an alias with name "ls" and value "rm*"
echo "hello $USER" Prints hello user, where user is the current Linux user.
PATH=$PATH:/action Adds /action to the PATH. /action should be the last directory the shell looks into when looking for a program
echo $PATH | tr ":" "\n" | wc -l Counts the number of the directories in the PATH
printenv Lists environment variables
set Lists all local variables and environment variables, and functions.
BEST="School" Creates a new local variable named BEST with a value "School".
export BEST="School" Creates a new global variable named "BEST" with a value "School".
echo $(($TRUEKNOWLEDGE+128)) Prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
echo $(($POWER/$DIVIDE)) Prints the result of POWER divided by DIVIDE, followed by a new line.
echo $(($BREATH**$LOVE)) Displays the result of BREATH to the power LOVE.
echo $((2#$BINARY)) Converts a number from base 2 to base 10.
echo {a..z}{a..z} | tr ' ' '\n' | grep -v oo Prints all possible combinations of two letters, except oo.
printf "%0.2f\n" $NUM Prints a number with two decimal places. The number is stored in the environment variable NUM.
printf "%x\n" $DECIMAL Converts a number from base 10 to base 16.
tr 'A-Za-z' 'N-ZA-Mn-za-m' Encodes and decodes text using the rot13 encryption
paste -d" " - - | cut -d " " -f 1 Prints every other line from the input, starting with the first line
echo $(printf %o $(($((5#$(echo $WATER | tr 'water' '01234'))) + $((5#$(echo $STIR | tr 'stir.' '01234'))))) | tr '01234567' 'bestchol') Adds the two numbers stored in the environment variables WATER and STIR and prints the result
