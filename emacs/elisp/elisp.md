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
- structure: (if (condition) true false)

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
- structure: (when (test) form-1 form-2 .. ..)
- `when` is a form or a version of `if` without `else` expression.

(when t :a)    	   ;:a
(when nil :a)	   ;nil
(when t 'a 'b 'c)  ;c

(setq n 0)
(when (zerop n) (cons 1 n))  ;(1 . 0)

(defun is-a-number-p (n)
    (when (numberp n)
    (message "Yes it is a number")))
(is-a-number-p n)     ;Yes it is a number


;;`unless` examples
*******************
- structure: (unless (test) form-1 form-2 .. ..)
- `unless` is a form or version of `if` which can be be expressed as: `if not` or `if !condition`

(unless t :a) 	      ;nil	
(unless nil :a)	      ;:a
(unless nil 'a 'b 'c) ;c

(unless (zerop n) (message "unless"))  ;nil


;;`cond` examples
*****************
- structure: (cond (test)
  	     	   (form-1)
		   (form-2)
		       ...))
- `cond` is a multiple `if` conditions  

(defun abs (x)
       	(cond ((> x 0) x)
              ((= x 0) 0)
	      ((< x 0) (- x))))
(abs -9)  ;9


```

##### Loops

##### Functions
```el
(setq prime-nums '(2 3 5 7 11))

(defun print-first-five-prime-nums (n) (print n))
(print-first-five-prime-nums prime-nums)       ;(2 3 5 7 11)

(defun square (x) (* x x))
(square 3) ;9

(defun cube (x) (* x x x))
(cube 3) ;27
```

##### Recursions





