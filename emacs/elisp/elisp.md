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
(+ 3 7)			;10
(+ (* 2 4) (/ 10 5))    ;10
```

##### Variables
```el

- `set` is used to set value of symbols
- `setq` is used to set value of variables
- `setf` is a used to set variables, symbols, arrays ...

;;set variables using `set`
***************************
(set number '(1 2 3))	;Wrong
(set 'numbers '(1 2 3)) ;Right

;;set variables using `setq`
****************************
(setq 'insects '(mantis beetle flea)) ;Wrong
(setq insects '(mantis beetle flea))  ;Right

(setq x 10 y 20) 

(setq insects '(mantis beetle flea)
      flowers '(lilly rose jasmine)
      birds '(sparrow crane heron))

;;Incrementing a number by 1 (setting a counter)
(setq inc 0)
(setq inc (+ inc 1))

(setq (car insects) ;mantis

;;set variables using `setf`
****************************
(setq (car '(1 2 3)) 4)		;Wrong
(setf (car '(1 2 3)) 4) 	;Right 4

(setf (cdr insects) ;(beetle flea)

(setf empty '()) ;nil

(setf empty-again nil) ;nil

```

##### Conditionals
```el

- Conditionals are 4 different types in Emacs Lisp.

;;`if` examples
*************** 
(if t 'a 'b)	;a
(if nil 'a 'b)  ;b

(defun match-list (L)
    (if (equal L '(1 3 5 7))
        (message "List matched!")
	(message "List not matched!")))
	
(match-list '(1 3 5 7))    ;list macthed
(match-list '(2 4 6 8))    ;list not macthed


;;`when` examples
*****************
- `when` is a form or version of `if` without `else` expression.

(when


;;`unless` examples
*******************

;;`cond` examples
*****************


```

##### Loops

##### Functions
```el
(defun print-flowers (f) (print f))
(print-flowers flowers) ;(lilly rose jasmine)

(defun square (x) (* x x))
(square 3) ;9

(defun cube (x) (* x x x))
(cube 3) ;27
```

##### Recursions





