# Command line for the win
* **About:**
[CMD CHALLENGE](https://cmdchallenge.com/) is a pretty cool game challenging you on Bash skills. Everything is done via the command line and the questions are becoming increasingly complicated. It’s a good training to improve your command line skills!

## Files (9images) & Description
| S/N   |       Files          |        Description  |
|:-----:|:--------------------:|:-------------------|
| 1. |[0-first_9_tasks.jpg](alx-system_engineering-devops/command_line_for_the_win/0-first_9_tasks.jpg), <br> [0-first_9_tasks.png]( alx-system_engineering-devops/command_line_for_the_win/0-first_9_tasks.png ) |Complete the first 9 tasks, and Push the screenshot to GitHub, in either the PNG or JPEG format |
|2. | [1-next_9_tasks.jpg](alx-system_engineering-devops/command_line_for_the_win/1-first_9_tasks.jpg), <br> [1-next_9_tasks.png](alx-system_engineering-devops/command_line_for_the_win/1-first_9_tasks.png) |Complete the 9 next tasks, getting to 18 total, and Push the screenshot to GitHub, in either the PNG or JPEG format |
|3. |[2-next_9_tasks.jpg](alx-system_engineering-devops/command_line_for_the_win/2-first_9_tasks.jpg), <br> [2-next_9_tasks.png](alx-system_engineering-devops/command_line_for_the_win/2-first_9_tasks.png)| Complete the 9 next tasks, getting to 27 total, and Push the screenshot to GitHub, in either the PNG or JPEG format |


Solution 
#1 Print “Hello World”. Ans: echo hello\ world Solution 
#2 Print the current working directory. Ans: pwd Solution 
#3 List names of all the files in the current directory,one file per line. Ans: ls Solution 
#4 There is a file named “access.log” in the current directory. Print the contents. Ans: cat access.log Solution 
#5 Print the last 5 lines of “access.log”. Ans: tail -5 access.log Solution 
#6 There is a file named “access.log” in the current working directory. Print all lines in this file that contains the string “GET”. Ans: grep ‘GET’ ./access.log Solution 
#7 How many lines contain tab characters in the file named “file-with-tabs.txt” in the current directory. Ans: grep -c $’\t’ ./file-with-tabs.txt Solution 
#8 Print all files in the current directory, one per line (not the path, just the filename) that contain the string “500”. Ans: grep -l ‘500’ * Solution 
#9 Print the relative file paths, one path per line for all filenames that start with “access.log” in the current directory. Ans: find . -name "access.log*" Solution 

#10 Search for strings in files recursive Ans: grep -r -h ‘500’ — include ‘access.log*’ Solution 
#11 Extract all IP addreses from files that start with “access.log” printing one IP address per line. Ans: grep -r -h -o ‘[0–9].[0–9].[0–9].[0–9]’--include ‘access.log*’ Solution 
#12 Delete all of the files in this challenge directory including all subdirectories and their contents. Ans: find . -delete Solution 
#13 Count the number of files in the current working directory. Print the number of files as a single integer. Ans: ls | wc -l Solution 
#14 Print the contents of access.log sorted. Ans: cat access.log|sort Solution 
#15 Print the number of lines n access.log that contain the string “GET”. Ans: grep -c ‘GET’ ./access.log Solution 
#16 The file split-me.txt contains a list of numbers separated by a ‘;’ character.Split the numbers on the ‘;’ character,one number per line. Ans: cat ./split-me.txt | sed s/;/\n/g Solution 
#17 Print the numbers 1 to 100 separated by spaces. Ans: echo {1..100} Solution 
#18 There are some files in this directory that start with a dash in the filename.Remove those files. Ans: find . -name ‘-[a-z]’ -delete Solution 

#19 There are files in this challenge with different file extensions. Remove all files with the .doc extension recursively in the current working directory. Ans: find . -name ‘.doc’ -delete Solution 
#20 There are files in this challenge with different file extensions. Remove all files without the .txt and .exe extensions recursively in the current working directory. Ans: find . -type f -not ( -name ‘.txt’ -or -name ‘.exe’ ) -delete Solution 
#21 This challenge has text files (with a .txt extension) that contain the phrase “challenges are difficult”. Delete this phrase recursively from all text files.Note that some files are in subdirectories so you will need to search for them. Ans: find . -name “.txt” -exec sed -i ‘s/challenges are difficult//g’ {} + Solution 
#22 The file sum-me.txt has a list of numbers,one per line. Print the sum of these numbers. Ans: awk ‘{s+=$1} END {print s}’ sum-me.txt Solution 
#23 Print all files in the current directory recursively without the leading directory path. Ans: find . -type f -printf "%f\n" Solution 
#24 Rename all files removing the extension from them in the current directory recursively. Ans:find pwd -type f -exec bash -c 'mv "$1" "${1%.}"' - '{}' ; Solution 
#25 The files in this challenge contain spaces.List all of the files (filenames only) in the current directory but replace all spaces with a ‘.’ character. Ans:find . -type f -printf "%f\n" | xargs -0 -I {} echo {} | tr ' ' '.' Solution 
#26 here are a mix of files in this directory that start with letters and numbers. Print the filenames (just the filenames) of all files that start with a number recursively in the current directory. Ans: find . -type f -name ‘[0–9]*’ -printf ‘%f\n’ Solution
#27 Print the 25th line of the file faces.txt Ans: sed ‘25q;d’ faces.txt Solution \
#28 Print the file faces.txt, but only print the first instance of each duplicate line, even if the duplicates don’t appear next to each other.Note that order matters so don’t sort the lines before removing duplicates. Ans: awk ‘!c[$0]++’ faces.txt Solution 
#29 The file however has been corrupted, there are random ‘!’ marks inserted throughout. Print the original text. Ans: < war_and_peace.txt tr -s ‘!’ | sed ‘s/!([a-z])/\1/g’ | sed ‘s/!( [a-z])/\1/g’ | sed ‘s/!.!/./g’ | sed ‘s/ !/ /g’ Solution 
#30 access.log.1 and access.log.2 are http server logs. Print the IP addresses common to both files, one per line. Ans: comm -12 <(cut -d’ ‘ -f1 access.log.1 | sort) <(cut -d’ ‘ -f1 access.log.2 | sort)

