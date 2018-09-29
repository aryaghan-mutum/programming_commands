#### Search 
- `!$` 				   Finds the next line ends with an exclamation point 
- `/the`               Find the next line that begins with the string line 'the'
- `.` 				   Indicates any char 
- `\<`				   Indicates the beginning of a word
- `\>`				   Indicates the end of a word
- `[]`				   
- `/and`               Finds the next occurrence of the string 'and'. Ex: and, anderson, antelope
- `\<and\>`            Finds the next occurrence of the string 'and'. Ex: and
- `/^[0-9][0-9]`       Finds the next line that starts with a 2 digit number followed by a right bracket
- `cn` 			       Jump to next match
- `cp`			       Jump to previous match 
- `copen`              Open a window includes list of matches
- `/pattern`           Search a pattern
- `vimgrep /pattern/ {file}` Search a pattern in more than 1 files 

- special characters:  `.  \<  />  [ ]`

#### Search & Replace
- `/pattern`  Search the pattern
- `?pattern`  Search backward the pattern


##### Regular Expressions 
- `^`                 Matches beginning of line
- `$`		      Matches end of line
- `.`                 Matches any single char	 
- `*`                 Matches any prev char
- `.*`                Matched any char 


##### search in multiple files
- `vimgrep /pattern / {file}`  
- `cn` Jump to next match
- `cp` Jump to prev match
- `copen` Open a screen consists of list of matches

