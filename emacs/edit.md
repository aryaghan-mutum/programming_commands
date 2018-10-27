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
| `C-x` `C-u`   | uppercase	all the file   									 | `(upcase-region)`					 |
| `C-x` `C-l`   | downcase all the file			 							 | `(downcase-region)`					 |
| `M-u`   		| uppercase the next word				                     | `(upcase-word)`					     |
| `M-l`   		| downcase the next word				                     | `(downcase-word)`					 |
| `C-x C-+` 	| increase text size										 |										 |
| `C-x C-+`     | decrease text size										 |										 |
| `C-x h`       | select all in the file  									 | `(mark-whole-buffer)`				 |	
| `M-h`	        | select a paragraph										 | `(mark-paragraph)`					 |
| `C-x i`       | insert a buffer in a file aka `(M-x insert-file)`          |       							     |		              
