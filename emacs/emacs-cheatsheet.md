#### emacs basics
- Hold the Control/Meta key followed by the next character. Some computers do not have `<Meta>` key, therefore try `<Esc>` key.
- Elisp: Transform human readable code into compiled byte code by setting the command: `byte-compile-file`. Compiled byte code is stored in a file that has `.elc` format not `.el`

- `eval-last-sexp`

- `fill-column`

| Commands 		| Description 		          | Lisp procedure 	  		 | 
|---------------|-----------------------------|--------------------------|
| `C-x`			| Control-x			          |					         |	
| `M-x` 		| Alt-x 			          |`execute-extended-command`|
| `<RET>` 		| Return/Enter key            |							 |
| `<DEL>` 		| Backspce/Delete key or `C-?`|                   		 |

- Emacs understands Elisp, a dialect of lisp. Start emacs buffer: `emacs -Q`
- Type `q` to get rid of welcome page

#### Buffers

| Commands 		| Description 				                     		     | Lisp procedure 	 | 
|---------------|------------------------------------------------------------|-------------------|
| `C-x C-b`     | list all buffers											 |					 |
| `C-x b`       | specific buffer											 |					 |

#### Edit

| Commands 		| Description 				                     		     | Lisp procedure 	                     | 
|---------------|------------------------------------------------------------|---------------------------------------|
| `C-w`     	| cut 														 |									     | 
| `C-k`         | cuts the entire line including spaces and saves in buffer  |					 				     |
| `M-w`         | copy														 |					 				     |
| `C-y`         | paste														 |					 				     |
| `C-y` `M-y`   | replaces 1st element with 2nd and 2nd with third 			 |					                     |
| `M-y` 	    | yank-pop													 |`(insert (car kill-ring-yank-pointer))`|
| `C-x u`    	| undo														 |										 |
| `C-/`         | undo														 |										 |
| `C-g C-/`     | redo														 |										 |
| `C-x C-+` 	| increase text size										 |										 |
| `C-x C-+`     | decrease text size										 |										 |
| `C-x h`       | select all in the file  									 |									     |	
| `M-h`	        | select a paragraph										 |										 |

#### Navigaion

| Commands 		    | Description 				                     		     | Lisp procedure 	 | 
|-------------------|------------------------------------------------------------|-------------------|
| `C-v` 		    | scroll to the bottom										 |					 |
| `M-v`             | scroll to the top											 |				     |
| `C-a`		        | go to start of line   									 |					 |
| `C-e`		        | go to end of line                                          |                   |
| `C-p`	            | go to previous line                                        |                   |
| `C-n` 	   		| go to next line                                            |                   |
| `M-f`             | go forward within words                                    |                   |
| `M-b`             | go backward within words                                   |                   |
| `M-a`		        | go to beginning of prev sentence                           |                   |
| `M-e`		        | go to end of prev sentence                                 |                   |
| `M-x linum-mode`  | create line numbers                                        |                   |
| `M-g g line_num`  | go to specific line number Ex: `M-g g 2`                   |                   |

#### Search

| Commands 		| Description 				                     		        | Lisp procedure 	| 
|---------------|---------------------------------------------------------------|-------------------|
| `C-s`         | forward search                    						    |					|
| `C-r`         | backward search                 								|					|
| `C-M-x`       | regex search                    								|		            |					 
| `C-x C-f`     | search a file. If the file doesn't exist, it creates the file |                	|	
| `C-x i`       | insert a file                   								|		            |					 
| `M-x grep`    | greps a pattern in the files                   				|				    |					 
| `M-x rgrep`   | recursively grep in a dir                  					|					|					 

#### Save

| Commands 		| Description 				                     		     | Lisp procedure 	 | 
|---------------|------------------------------------------------------------|-------------------|
| `C-x C-s`     | save a file                  							     |					 |
| `C-x s`       | save all files                  							 |					 |
| `C-s C-w`     | saves the file with a different name, asks for the name.   |					 | 
| `M-x`		    | recovers the auto saved file                               |                   |


#### Exit

| Commands 		| Description 				                     		     | Lisp procedure 	 | 
|---------------|------------------------------------------------------------|-------------------|
|`C-z`          | exit and enter emacs  								     |                   |
|`C-x C-c`      | exit emacs perpetually									 |					 |
|`C-g`          | quit the current Commands                                  |					 |
|`C-x o C-x 0`  | close the current file 									 |                   |

#### Help

| Commands 		  | Description 				                     		     | Lisp procedure 	  |  
|-----------------|--------------------------------------------------------------|--------------------|
| `C-h i` 		  | opens 'The Info Directory'									 |(info)			  |
| `C-h p` 		  |	searchs the standard Emacs Lisp libraries by topic keywords. |(finder-by-keyword) |
| `C-h f` 		  |	read the documentation of a function						 |(describe-function) |
| `C-h v` 		  |	read the documentation of a variable 						 |(describe-variable) |
| `C-h t` 		  |	view an emacs help tutorial								     |(help-with-tutorial)|					 
| `C-h k` 		  |	get info on key bindind										 |(describe-key)	  |	
| `C-h b` 		  |	show all key bindings									     |(describe-bindings) |	
| `C-x 1` 		  |	return to a single window on the screen						 |					  |




