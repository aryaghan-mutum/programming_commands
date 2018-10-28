Emacs basics
------------

- `C-` : _**`CONTROL Key`**_
- `M-` : _**`META Key`**_

Emacs is written in Emacs Lisp(Elisp) and C programming language. Elisp transforms human readable code into compiled byte code by setting the command: `byte-compile-file`. Compiled byte code is stored in a file that has `.elc` format not `.el`

__ __ __ __

| Commands 		| Description 		          | Lisp procedure 	  		 | 
|---------------|-----------------------------|--------------------------|
| `C-x`			| Control-x	(x: eXtended)	  |					         |	
| `M-x` 		| Alt-x (x: eXtended)		  |`execute-extended-command`|
| `<RET>` 		| Return/Enter key            |							 |
| `<DEL>` 		| Backspce/Delete key or `C-?`|                   		 |

- Emacs understands Elisp, a dialect of lisp. Start emacs buffer: `emacs -Q`
- Type `q` to get rid of welcome page

__ __ __ __

#### Buffers
| Commands 		| Description 				                     		     | Lisp procedure 	   | 
|---------------|------------------------------------------------------------|---------------------|
| `C-x C-b`     | list all buffers (shows buffer & file name of the buffer	 |`(list-buffers)`	   |
| `C-x b`       | open specific buffer										 |`(switch-to-buffer)` |					 

__ __ __ __

#### Capitalization
| Commands 		    | Description 				                     		     | Lisp procedure 	                     | 
|-------------------|------------------------------------------------------------|---------------------------------------|
| `C-x` `C-u`       | uppercase	all the file   									 | `(upcase-region)`					 |
| `C-x` `C-l`       | downcase all the file			 							 | `(downcase-region)`					 |
| `M-c`             | upcase the letter in a word 								 | `(capitalize-word)`					 |
| `M-u`   		    | uppercase the word				                  	     | `(upcase-word)`					     |
| `M-l`   		    | downcase the word				                             | `(downcase-word)`					 |

__ __ __ __

#### Edit
| Commands 		| Description 				                     		     | Lisp procedure 	                     | 
|---------------|------------------------------------------------------------|---------------------------------------|
| `C-w`     	| cut 														 |`(kill-region)`					     | 
| `C-k`         | cuts the entire line including spaces and saves in buffer  |`kill-line)`					 		 |		    
| `M-w`         | copy														 |`(kill-ring-save)`					 |
| `C-y`         | paste														 |`(yank)`					 			 |
| `C-y` `M-y`   | replaces 1st element with 2nd and 2nd with third 			 |					                     |
| `M-y` 	    | yank-pop													 |`(insert (car kill-ring-yank-pointer))`|
| `C-a` `C-k`	| kill the text on a line									 |										 |
| `C-x u`    	| undo														 | `(undo)`								 |
| `C-/`         | undo														 | `(undo)`								 |
| `C-g C-/`     | redo														 |										 |
| `C-x C-+` 	| increase text size										 |										 |
| `C-x C-+`     | decrease text size										 |										 |
| `C-x h`       | select all in the file  									 |										 |
| `M-h`	        | select a paragraph										 | `(mark-paragraph)`					 |
| `C-x i`       | insert a buffer in a file aka `(M-x insert-file)`          |       							     |		              
__ __ __ __

#### Exit
| Commands 		| Description 				                     		     | Lisp procedure 	 			| 
|---------------|------------------------------------------------------------|------------------------------|
|`C-z`          | exit and enter emacs  								     |`(suspend-frame)`             |
|`C-x C-c`      | exit emacs perpetually									 |`(save-buffers-kill-terminal)`|				 
|`C-g`          | quit the current command                                   |					 			|

__ __ __ __

#### Help
| Commands 		  | Description 				                     		     | Lisp procedure 	       |  
|-----------------|--------------------------------------------------------------|-------------------------|
| `C-h b` 		  |	show all key bindings									     |`(describe-bindings)`	   |	
| `C-h i` 		  | opens 'The Info Directory'									 |`(info)`			       |
| `C-h r`		  | opens 'The Emacs Editor'									 |`(info-emacs-manual)`    |
| `C-h p` 		  |	searchs the standard Emacs Lisp libraries by topic keywords. |`(finder-by-keyword)`    |
| `C-h f` 		  |	read the documentation of a function						 |`(describe-function)`    |
| `C-h v` 		  |	read the documentation of a variable 						 |`(describe-variable)`    |
| `C-h t` 		  |	view an emacs help tutorial								     |`(help-with-tutorial)`   | 					
| `C-h k` 		  |	get info on key bindind										 |`(describe-key)`	       |	
| `C-h s` 		  |	opens syntax table										     |`(describe-syntax)`	   |

__ __ __ __

#### Mode
| Commands 				 | Description 				                     		      | Lisp procedure 	                      | 
|------------------------|------------------------------------------------------------|---------------------------------------|
| `C-x` `C-q`  			 | switch on/off read only mode aka: `M-x read-only-mode`     | `(toggle-read-only)`                  |
| `M-x *-mode <tab>`     | display all modes										  |										  |
| `M-x describe-mode`    | describe modes 											  | `(describe-mode)` 					  |

__ __ __ __

#### Navigaion
| Commands 		    | Description 				                     		     | Lisp procedure 	          | 
|-------------------|------------------------------------------------------------|----------------------------|
| `C-v` 		    | scroll to the bottom										 |`(scroll-up)`				  |
| `M-v`             | scroll to the top											 |`(scroll-down)`			  |
| `C-a`		        | go to start of line   									 |`(move-beginning-of-line)`  |					
| `C-e`		        | go to end of line                                          |`(move-end-of-line)`        |
| `C-p`	            | go to previous line                                        |`(previous-line)`           |
| `C-n` 	   		| go to next line                                            |`(next-line)`               |
| `M-f`             | go forward a word                                          |`(forward-word)`            |
| `M-b`             | go backward a word                                         |`(backward-word)`           |
| `M-a`		        | go to beginning of prev sentence                           |`(backward-sentence)`       |
| `M-e`		        | go to end of prev sentence                                 |`(forward-sentence)`        |

__ __ __ __

#### Save
| Commands 		| Description 				                     		     | Lisp procedure 	         | 
|---------------|------------------------------------------------------------|---------------------------|
| `C-x C-s`     | save a file                  							     |`(save-buffer)`		     |
| `C-x s`       | save all buffers to their files                  			 |`(save-some-buffers)`      |					 
| `C-s C-w`     | saves the file with a different name, asks for the name.   |`(write-file)`		     | 
| `M-x`		    | recovers the auto saved file                               |`(set-visited-file-name)`  |                  

__ __ __ __

#### Search
| Commands 		| Description 				                     		        | Lisp procedure 	      | 
|---------------|---------------------------------------------------------------|-------------------------|
| `C-s`         | forward search                    						    |`(isearch-forward)`	  |
| `C-r`         | reverse (backward) search                 					|`(isearch-backward)`	  |
| `C-M-x`       | regex search                    								|		                  |					 
| `C-x C-f`     | search a file. If the file doesn't exist, it creates the file |`(find-file)`            |	
| `C-x C-v`     | search an alternative file                                    |`(find-alternate-file)`  |        	
| `C-x C-r`     | search a readonly file     								    |`(find-file-read-only)`  |						
| `M-x grep`    | greps a pattern in the files                   				|				          |					 
| `M-x rgrep`   | recursively grep in a dir                  					|					      |					 
           		
__ __ __ __

#### Settings
| Commands 			            | Description                               |
|-------------------------------|-------------------------------------------|
| `M-x menu-set-font`	        | chage fonts				                |
| `M x customize-themes`        | change themes                             |
| `M-x list-packages`	  		| find all the packages                     |
| `M-x linum-mode`  			| create line numbers                       |                   
| `M-g g line_num`  			| go to specific line number Ex: `M-g g 2`  |     

__ __ __ __

#### Useful
| Commands 			            | Description                            													  |
|-------------------------------|---------------------------------------------------------------------------------------------|
| `M-x shell`					| displays bash shell 																		  |
| `M-x ielm`   				    | interactive emacs lisp mode                        										  | 
| `M-x count-words`			    | counts the words in a file    															  |
| `M-x newline`			        | create a new line in a file    															  |
| `M-x newline`			        | create a new line in a file    															  |
| `M-x calendar`				| display calender 																			  |

__ __ __ __

#### Windows (frames)
| Commands 		| Description 				                     		     | Lisp procedure 	       | 
|---------------|------------------------------------------------------------|-------------------------|
|`C-x o`		| switch between windows                                     |`(other-window)`         |
|`C-x 0` 		| exit the selected window     								 |`(delete-window)`		   |			  
|`C-x 1` 		| exit all windows except one 								 |`(delete-other-windows)` |	
|`C-x 2`        | horizontal split.                                      	 |`(split-window-right)`   |
|`C-x 3`        | vertical split 										     |`(split-window-right)`   |					 

__ __ __ __



 



