#### Search

| Commands 		| Description 				                     		        | Lisp procedure 	      | 
|---------------|---------------------------------------------------------------|-------------------------|
| `C-s`         | forward search (press `C-s` multiple times)                   |`(isearch-forward)`	  |
| `C-r`         | reverse (backward) search (press `C-r` multiple times)        |`(isearch-backward)`	  |
| `C-M-x`       | regex search                    								|		                  |					 
| `C-x C-f`     | search a file. If the file doesn't exist, it creates the file |`(find-file "filename")` |	
| `C-x C-v`     | search an alternative file                                    |`(find-alternate-file)`  |        	
| `C-x C-r`     | search a readonly file     								    |`(find-file-read-only)`  |						 
| `M-x grep`    | greps a pattern in the files                   				|				          |					 
| `M-x rgrep`   | recursively grep in a dir                  					|					      |					 


##### Regex table

| Character 	| Description 				        		|		
|---------------|-------------------------------------------|
|`^`		    | matches beginning of a line       		|
|`$`			| matches end of a line 					|
|`.`			| matches any isngle character      		|
|`.*`			| matches any group of zero or more chars	|
|`\<`			| mateches beginning of a word				|
|`\>`			| mateches end of a word					|

- The regular expression table has taken from [Learning GNU Emacs](http://shop.oreilly.com/product/9781565921528.do)

