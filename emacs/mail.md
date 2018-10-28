#### Mail

| Commands 			            | Description                              | Lisp procedure        | 
|-------------------------------|------------------------------------------|-----------------------|	
| `M-x m`						| display mail buffer					   | `(mail)`		       |
| `C-c C-f C-c`					| _**`CC`**_ 							   | `(mail-cc)` 	       | 
| `C-c C-f C-b`					| _**`BCC`**_ 							   | `(mail-bcc)` 	       |
| `C-c C-f C-s`					| _**`Subject`**_ 						   | `(mail-subjbect)` 	   |
| `C-c C-c`						| send and exit a mail from `*mail*` buffer| `(mail-send-and-exit)`|
| `C-c C-s`						| send a mail and stay in `*mail*` buffer  | `(mail-send)`         |
| `C-c C-w`						| minsert the contents of `.signature` file| `(mail-signature)`    |


