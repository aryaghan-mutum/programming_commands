#### Editing

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
