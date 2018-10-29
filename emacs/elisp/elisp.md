#### A General Guide To Emacs Lisp
------------

- Insert `M-x ielm` in Emacs to use _**`Interactive Emacs Lisp Mode`**_ [IELM](http://wikemacs.org/wiki/IELM). I like to call it as _**REPL**_ which stands for _**Read Eval Print Loop**_  

- Insert `(require 'cl)`. It loads the Common Lisp library.

- Insert `C-x C-e` at the end of a S-expression for evaluation.

##### Basics

```el
1			;1
3.14			;3.14
t			;t
nil			;nil
'()			;nil
:this-is-a-symbol	;:this-is-a-symbol
"this-is-a-string" 	;"this is a string"
(+ 3 7)	;10
(+ (* 2 4) (/ 10 5))   ;10
```

##### Setting Variables
```el
(setq flowers '(lilly rose jasmine))
```
##### Functions
```el
(defun print-flowers (f) (print f))
(print-flowers flowers) ;(lilly rose jasmine)

(defun square (x) (* x x))
(square 3) ;9

(defun cube (x) (* x x x))
(cube 3) ;27
```





