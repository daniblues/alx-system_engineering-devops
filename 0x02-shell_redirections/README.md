WHAT EACH SCRIPT DOES
#!/bin/bash :instructs the operating system to use bash as a command interpreter.
echo Hello, World :Prints "Hello, World", followed by a new line to the standard output.
echo "\"(Ôo)'"  :Displays a confused smiley "(Ôo)'
cat /etc/passwd  :Displays the content of the /etc/passwdfile
cat /etc/passwd /etc/hosts :Displays the content of /etc/passwd and /etc/hosts
tail /etc/passwd  :Displays the last 10 lines of /etc/passwd
head /etc/passwd  :Displays the first 10 lines of /etc/passwd
head --lines=3 iacta | tail --lines=1  :Displays the third line of the file iacta
echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"	Creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the test Best School ending by a new line
ls -la > ls_cwd_content	:Writes into the file ls_cwd_content the result of the command ls -la.
echo -en "" | tail --lines=1 iacta >> iacta	:Duplicates the last line of the file iacta
find . -name '*.js' -type f -delete	:Deletes all the regular files with a .js extension that are present in the current directory and all its subfolders
find -mindepth 1 -type d | wc -l	:Counts the number of directories and sub-directories in the current directory
ls -t | head	:Displays the 10 newest files in the current directory
sort | uniq -u	:Takes a list of words as input and prints only words that appear exactly once
grep -i root /etc/passwd	:Displayes lines containing the pattern "root" from the file /etc/passwd
grep -i bin /etc/passwd | wc -l	:Displays the number of lines that contain the pattern "bin" in the file /etc/passwd
grep -iA 3 root /etc/passwd	:Displays lines containing the pattern "root" and 3 lines after them in the file /etc/passwd
grep -iv bin /etc/passwd	:Displays all the lines in the file /etc/passwd that do not contain the pattern "bin"
grep -i "^[a-z]" /etc/ssh/sshd_config	:Displays all lines of the file /etc/ssh/sshd_config starting with a letter
tr Ac Ze	:Replaces all characters A and c from input to Z and e respectively
tr -d cC	:Removes all letters c and C from input
rev	:Reverses its input
cut -d':' -f1,6 /etc/passwd | sort	:Displays all users and their home directories, sorted by users.
find . -empty -printf "%f\n"	:Finds all empty files and directories in the current directory and all sub-directories
find . -name \*.gif -type f -printf "%f\n" | LC_COLLATE=C sort --ignore-case | rev | cut -c 5- | rev	:Lists all the files with a .gif extension in the current directory and all its sub-directories
cut -c 1 | tr -d '\n' | sort	:Decodes acrostics that use the first letter of each line
cut -f1 -d$'\t' | sort | uniq -c | tr -s ' ' | sort -t' ' -k1 -nr | head -11 | cut -d' ' -f3	:Parses web servers in TSV format as input and displays the 11 hosts or IP addresses which did the most requests
