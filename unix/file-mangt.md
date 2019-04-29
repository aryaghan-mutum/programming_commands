#### File Management

- `cd` Change dir
- `chmod` Change access modes on files
- `cp` Copy files
- `csplit` Break files at specific locations
- `file` Determine a file’s type
- `head` Show the first few lines of a file
- `install` Set up system files
- `ln` Create filename aliases
- `ls` List files or dirs
- `more` Display files by screenful
- `pwd` Print current dir
- `rcp`  Copy files to remote system

- `mkdir dirname`  create directory

- `cp old new` Copy files

- `mv old new` Move or rename files of dirs (cut)

- `split` Split files evenly

- `tail` Show the last few lines of a file

- `wc` Count the lines, words, and characters in a file

- touch filename (create files)

- stat file/dir ( provides a complete rundown of the status of a file. everything you’d want to know about the file )



| ls 		    	| Description 				                     		    				  |
|-------------------|-----------------------------------------------------------------------------|
| `ls -l` 		    | display the long listing format 									 	 	  |
| `ls -i`           | display the index number (inode) of each file  							  |			  
| `ls -a`		    | display hidden files along with other files							      |				 
| `ls -c`		    | sort by time of last modification                                           |
| `ls -s`	        | display list of files in block size                                         |
| `ls -n` 	   		| display numeric userid and groupid instead of names                         |
| `ls -rl`          | reverse the sorting order when displaying files and directories             |
| `ls -t`           | sort the output by file modification time                                   |


| cat 		    	| Description 				                     		    				  |
|-------------------|-----------------------------------------------------------------------------|
| `cat -n` 		    | displays line numbers inside the file							  			  |
| `cat -b`          | displays line numbers that have text in them  						      |			  
| `cat -s`		    | compress multiple blank lines into a single blank line					  |				 
| `cat -T`		    | if you don’t want tab characters to appear                                  |
| `cat > filename`  | create files and the content												  |
| `cat >> filename` | add more text to end of a file, instead of replacing its contents			  |


| cp 		    	  | Description 				                     		    			  |
|---------------------|---------------------------------------------------------------------------|
| `cp -R dir1 dir2`   | allows to recursively copy the contents of an entire directory			  |
| `cp -l file1 file2` | creates a hard link for the file1 called file2   						  |			  
| `cp -s file1 file2` | creates a soft link for the file1 called file2					  		  |				 


| rm & rmdir		    	 			  | Description 				                     	  |	    
|-----------------------------------------|-------------------------------------------------------|
| `rm -i file`        					  | serious about removing the file			    		  |
| `rm -r dir/file` or `rm -rf dir/file`   | remove direcorties and files   						  |	
| `rmdir dirname`		  				  | removes empty directory		  						  |


| pr (printing file)		    	 			  | Description 				 |	    
|------------------------|-------------------------------------------------------|
| `pr -k`        		 | produces k columns of output		    		 		 |
| `pr -d filename`    	 | double-spaces the output  						     |	
| `pr -h filename`		 | takes the next item as a report header		  		 |
| `pr -t filename`		 | eliminates printing of header and top/bottom margins	 |	  		


| ps 		    	  | Description 				                     		    			  |
|---------------------|---------------------------------------------------------------------------|
| `ps -ef`            | displays everything running on the system 			    				  |
| `ps -l`    		  | displays long format output   						  					  |			  


| df (disk space)	  | Description 				                     		    			  |
|---------------------|---------------------------------------------------------------------------|
| `df -h`             | shows data in human readble format			    				  		  |


| du (disk usgae)	  | Description 				                     		    					|
|---------------------|---------------------------------------------------------------------------------|
| `du`             	  | displays all files, dirs, and sub-dirs under the current directory  	  		|
| `du -c`             | generate a total of all the files listed			    				  		|
| `du -h`             | display sizes in human-readable form, using K: kilobyte, M:megabyte, G:gigabyte	|
| `du -s`             | summarize each argument 			    				 				  		|


| sort	  			 | Description 				                     		    						|
|---------------------|---------------------------------------------------------------------------------|
| `sort`              | displays standard character sort  	  											|
| `sort -n file `     | sorts in numerical order			    				  						|


| grep	  			 	 | Description 				                     		    					|
|------------------------|------------------------------------------------------------------------------|
| `grep -n pattern file` | find the line numbers where the matching patterns are found  	  			|
| `grep -c pattern file` | see a count of how many lines contain the matching pattern		    		|


| compressing and archiving 		  		| Description 				                     		    
|-------------------------------------------|----------------------------------------------------------------------------|
| `bzip2 filename` 		    		  		| zip the file  	  													     |
| `bunzip2 filename`        		  		| unzip the file		    												 |
| `bzcat filename` 		    		  		| look inside the compressed file without uncompressing the file  	  		 |
| `gzip filename` 		    		  		| GNU's unzip the file  	  		 										 |
| `zip -r file/dir_to_be_zipped file/dir`   |																			 |


##### Environment Variables 1. Global variables 2. Local variables
| variables		  		| Description 				                     		    
|-----------------------|------------------------------------------------------------------------------------------------|
| `printenv` 		    | display global environment variables 	  													     |
| `set`        		  	| displays all the env variables set for a specific process including the global env variables   |		    	
| `unset var_name` 		| remove local env vars  	  		 															 |

