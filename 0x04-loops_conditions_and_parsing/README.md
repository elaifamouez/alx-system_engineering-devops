# 0x04. Loops, conditions and parsing

## Concepts
- Make shell script portable with #!usr/bin/env instead of #!/bin/bash.
- cut command to cut parts of lines from specified files or piped data
- Passing command arguments to shell script.


# Tasks
## [0-RSA_public_key.pub](0-RSA_public_key.pub)
Read for this task:
 - Linux and Mac OS users
 - Windows users

man: ```ssh-keygen```

You will soon have to manage your own servers concept page hosted on remote data centers. We need to set them up with your RSA public key so that you can access them via SSH.

Create a RSA key pair.

Requirements:
 - Share your public key in your answer file 0-RSA_public_key.pub
 - Fill the SSH public key field of your intranet profile with the public key you just generated
 - Keep the private key to yourself in a secure location, you will use it later to connect to your servers using SSH. Some storing ideas are Dropbox, Google Drive, password manager, USB key. Failing to do so will prevent you to access your servers, which will prevent you from doing your projects
 - If you decide to add a passphrase to your key, make sure to save this passphrase in a secure location, you will not be able to use your keys without the passphrase

SSH and RSA keys will be covered in depth in a later project.

## [1-for_best_school](1-for_best_school)
Write a Bash script that displays Best School 10 times.

Requirement:
 - You must use the for loop (while and until are forbidden)

sylvain@ubuntu$ head -n 2 1-for_best_school 
#!/usr/bin/env bash
``# This script is displaying "Best School" 10 times
sylvain@ubuntu$ ./1-for_best_school 
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
sylvain@ubuntu$ 

Note that:
 - The first line of my Bash script starts with #!/usr/bin/env bash
 - The second line of my Bash scripts is a comment explaining what it is doing

shellcheck 1-for_best_school #Check shell script formatting
chmod a+x 1-for_best_school #Give file executable permissions
./1-for_best_school #Execute script

## [ 2-while_best_school]( 2-while_best_school)
Write a Bash script that displays Best School 10 times.

Requirements:
 - You must use the while loop (for and until are forbidden)

```
sylvain@ubuntu$ ./2-while_best_school
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
sylvain@ubuntu$
```

shellcheck 2-while_best_school #Check shell script formatting
chmod a+x 2-while_best_school #Give file executable permissions
./2-while_best_school #Execute script

## [3-until_best_school](3-until_best_school)
Write a Bash script that displays Best School 10 times.

Requirements:
 - You must use the until loop (for and while are forbidden)

```
sylvain@ubuntu$ ./3-until_best_school
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
sylvain@ubuntu$
```

shellcheck 3-until_best_school #Check shell script formatting
chmod a+x 3-until_best_school #Give file executable permissions
./3-until_best_school #Execute script

## [4-if_9_say_hi](4-if_9_say_hi)
Write a Bash script that displays Best School 10 times, but for the 9th iteration, displays Best School and then Hi on a new line.

Requirements:
 - You must use the while loop (for and until are forbidden)
 - You must use the if statement
```
sylvain@ubuntu$ ./4-if_9_say_hi
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Hi
Best School
sylvain@ubuntu$ 
```

shellcheck 4-if_9_say_hi #Check shell script formatting
chmod a+x 4-if_9_say_hi #Give file executable permissions
./4-if_9_say_hi #Execute script

## [5-4_bad_luck_8_is_your_chance](5-4_bad_luck_8_is_your_chance)
Write a Bash script that loops from 1 to 10 and:
 - displays bad luck for the 4th loop iteration
 - displays good luck for the 8th loop iteration
 - displays Best School for the other iterations

Requirements:
 - You must use the while loop (for and until are forbidden)
 - You must use the if, elif and else statements

```
sylvain@ubuntu$ ./5-4_bad_luck_8_is_your_chance
Best School
Best School
Best School
bad luck
Best School
Best School
Best School
good luck
Best School
Best School
sylvain@ubuntu$ 
```
shellcheck 5-4_bad_luck_8_is_your_chance #Check shell script formatting
chmod a+x 5-4_bad_luck_8_is_your_chance #Give file executable permissions
./5-4_bad_luck_8_is_your_chance #Execute script

## [6-superstitious_numbers](6-superstitious_numbers)
Write a Bash script that displays numbers from 1 to 20 and:
 - displays 4 and then bad luck from China for the 4th loop iteration
 - displays 9 and then bad luck from Japan for the 9th loop iteration
 - displays 17 and then bad luck from Italy for the 17th loop iteration

Requirements:
 - You must use the while loop (for and until are forbidden)
 - You must use the case statement

shellcheck 6-superstitious_numbers #Check shell script formatting
chmod a+x 6-superstitious_numbers #Give file executable permissions
./6-superstitious_numbers #Execute script

## [7-clock](7-clock)
Write a Bash script that displays the time for 12 hours and 59 minutes:
 - display hours from 0 to 12
 - display minutes from 1 to 59

Requirements:
 - You must use the while loop (for and until are forbidden)

Note that in this example, we only display the first 70 lines using the head command.

```
sylvain@ubuntu$ ./7-clock | head -n 70
Hour: 0
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
Hour: 1
1
2
3
4
5
6
7
8
9
sylvain@ubuntu$ 
```

shellcheck 7-clock #Check shell script formatting
chmod a+x 7-clock #Give file executable permissions
./7-clock #Execute script

## [8-for_ls](8-for_ls)
Write a Bash script that displays:
 - The content of the current directory
 - In a list format
 - Where only the part of the name after the first dash is displayed (refer to the example)

Requirements:
 - You must use the for loop (while and until are forbidden)
 - Do not display hidden files
```
sylvain@ubuntu$ ls
100-read_and_cut -  -  -   1-for_best_school -  -  6-superstitious_numbers
101-tell_the_story_of_passwd  2-while_best_school -  - 7-clock
102-lets_parse_apache_logs - 3-until_best_school -  - 8-for_ls
103-dig_the-data -  -  -   4-if_9_say_hi -  -  -  -   9-to_file_or_not_to_file
10-fizzbuzz -  -  -  -  - 5-4_bad_luck_8_is_your_chance
sylvain@ubuntu$  ./8-for_ls
read_and_cut
tell_the_story_of_passwd
lets_parse_apache_logs
dig_the-data
fizzbuzz
for_best_school
while_best_school
until_best_school
if_9_say_hi
4_bad_luck_8_is_your_chance
superstitious_numbers
clock
for_ls
to_file_or_not_to_file
sylvain@ubuntu$ 
```

shellcheck 8-for_ls #Check shell script formatting
chmod a+x 8-for_ls #Give file executable permissions
./8-for_ls #Execute script

## [9-to_file_or_not_to_file](9-to_file_or_not_to_file)
Write a Bash script that gives you information about the school file.

Requirements:
  - You must use if and, else (case is forbidden)
  - Your Bash script should check if the file exists and print:
		- if the file exists: school file exists
		- if the file does not exist: school file does not exist
  - If the file exists, print:
		- if the file is empty: school file is empty
		- if the file is not empty: school file is not empty
		- if the file is a regular file: school is a regular file
		- if the file is not a regular file: (nothing)
```
sylvain@ubuntu$ file school
school: cannot open `school' (No such file or directory)
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file does not exist
sylvain@ubuntu$ touch school
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file exists
school file is empty
school is a regular file
sylvain@ubuntu$ echo 'betty' > school 
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file exists
school file is not empty
school is a regular file
sylvain@ubuntu$ rm school 
sylvain@ubuntu$ mkdir school
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file exists
school file is not empty
sylvain@ubuntu$ 
```

shellcheck 9-to_file_or_not_to_file #Check shell script formatting
chmod a+x 9-to_file_or_not_to_file #Give file executable permissions
./9-to_file_or_not_to_file school #Execute script

# [10-fizzbuzz](10-fizzbuzz)
Write a Bash script that displays numbers from 1 to 100.

Requirements:
 - Displays FizzBuzz when the number is a multiple of 3 and 5
 - Displays Fizz when the number is multiple of 3
 - Displays Buzz when the number is a multiple of 5
 - Otherwise, displays the number
 - In a list format
```
sylvain@ubuntu$ ./10-fizzbuzz | head -20
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz
sylvain@ubuntu$ 
```

shellcheck 10-fizzbuzz #Check shell script formatting
chmod a+x 10-fizzbuzz #Give file executable permissions
./10-fizzbuzz school #Execute script

## [100-read_and_cut](100-read_and_cut)
shellcheck 100-read_and_cut #Check shell script formatting
chmod a+x 100-read_and_cut #Give file executable permissions
./100-read_and_cut school #Execute script

## [101-tell_the_story_of_passwd](101-tell_the_story_of_passwd)
shellcheck 101-tell_the_story_of_passwd #Check shell script formatting
chmod a+x 101-tell_the_story_of_passwd #Give file executable permissions
./101-tell_the_story_of_passwd school #Execute script

## [102-lets_parse_apache_logs](102-lets_parse_apache_logs)
shellcheck 102-lets_parse_apache_logs #Check shell script formatting
chmod a+x 102-lets_parse_apache_logs #Give file executable permissions
./102-lets_parse_apache_logs school #Execute script

## [103-dig_the-data](103-dig_the-data)
shellcheck 103-dig_the-data #Check shell script formatting
chmod a+x 103-dig_the-data #Give file executable permissions
./103-dig_the-data school #Execute script

# Git push command
git add --all; git commit -m "";git push

# References
 1. [shellcheck](https://github.com/koalaman/shellcheck#installing)
 2. [Bash For Loop Examples](https://www.cyberciti.biz/faq/bash-for-loop/#Examples)
 3. [How to Check if a File or Directory Exists in Bash](https://linuxize.com/post/bash-check-if-file-exists/)
 4. [Cut Command in Linux](https://linuxize.com/post/linux-cut-command/)
