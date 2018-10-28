#### Edit

| Commands 		    | Description 				                     		     | Lisp procedure 	                     | 
|-------------------|------------------------------------------------------------|---------------------------------------|
| `C-w`     	    | cut 														 |`(kill-region)`					     | 
| `C-k`             | cuts the entire line including spaces and saves in buffer  |`kill-line)`					 		 |		 
| `M-w`             | copy														 |`(kill-ring-save)`					 |
| `C-y`             | paste														 |`(yank)`					 			 |
| `C-y` `M-y`       | replaces 1st element with 2nd and 2nd with third 			 |					                     |
| `M-y` 	        | yank-pop													 |`(insert (car kill-ring-yank-pointer))`|
| `C-a` `C-k`	    | kill the text on a line									 |										 |
| `C-/` 			| undo														 | `(undo)`								 |
| `C-x u`  		    | undo last edit 											 | `(advertised-undo`			         |		
| `C-g C-/`         | redo														 |										 |
| `C-x C-+` 	    | increase text size										 |										 |
| `C-x C-+`         | decrease text size										 |										 |
| `C-x h`           | mark whole buffer  									     | `(mark-whole-buffer)`				 |	
| `C-x C-p`         | mark page 									             | `(mark-page)`				         |	
| `M-h`	            | select a paragraph										 | `(mark-paragraph)`					 |
| `C-x i`           | insert a buffer in a file aka `(M-x insert-file)`          |       							     |		              