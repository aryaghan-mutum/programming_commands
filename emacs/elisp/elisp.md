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
(setq (car insects)		      ;mantis
(setq x 10 y 20)       	      	      
(setq insects '(mantis beetle flea)
      flowers '(lilly rose jasmine)
      birds '(sparrow crane heron))

;;Incrementing a number by 1 (setting a counter)
(setq inc 0)
(setq inc (+ inc 1))

;;set variables using `setf`
****************************
(setq (car '(1 2 3)) 4)		;Wrong
(setf (car '(1 2 3)) 4) 	;Right 4
(setf (cdr insects)  		;(beetle flea)
(setf empty '()) 		;nil
(setf empty-again nil) 		;nil
```

##### Bindings
```el
;;`let` examples
****************
- `let` & `let*` gives lexical scoping in a program. 
- structure: (let ((var1 val1)
      	     	   (var2 val2)
     		  	 ...
			     )
    			 body)
    
(let ((x 5)
      (y 10))
       (setq z (* x y))
	     z)			;50
	     
(let ((x 10) (y 20))
      (cons x y))		;(10 . 20)

(let ((L1 '(:a :b :c :d))
      (L2 '(:e :f :g :h)))
      (cons (car L1) (cdr L2))) ;(:a :f :g :h)

(let ((x 4))
     (format "x val in outer let: %d." x)
  (let ((x 8))
     (format "x val in inner let: %d." x))
     (let ((y x))
     	      y))		;4



;;`let* examples`
*****************
- structure: (let* ((var1 
(let* ((x 10)
       (y (- x 10)))
       (list x y))		;(10 0)	
   
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
- `when` is a form or version of `if` without `else` expression.

(when t :a)    	   ;:a
(when nil :a)	   ;nil
(when t 'a 'b 'c)  ;c

(setq n 0)
(when (zerop n) (cons 1 n))  ;(1 . 0)

(defun is-a-number-p (n)
    (when (numberp n)
    (insert "Yes it is a number")))
(is-a-number-p n)     ;Yes it is a number


;;`unless` examples
*******************
- structure: (unless (test) form-1 form-2 .. ..)
- `unless` is a form or version of `if` which can be be expressed as: `if not` or `if !condition`

(unless t :a) 	      ;nil	
(unless nil :a)	      ;:a
(unless nil 'a 'b 'c) ;c

(unless (zerop 9) (insert  "unless"))  ;nil


;;`cond` examples
*****************
- structure: (cond (test)
  	     	   (form-1)
		   (form-2)
		       ...)) `cond` is a multiple `if` conditions or analogous to `case` statements in Algol-like langauges.   

(defun abs (x)
       	(cond ((> x 0) x)
              ((= x 0) 0)
	      ((< x 0) (- x))))
(abs -9)  ;9
```

##### Loops
```el
- Loops are 3 different types in Emacs Lisp.

;;`while examples`
******************
- structure: (while (condition)
		     body ...)

(setq num '(1 2 3 4 5))
class WhileDemo {
    public static void main(String[] args){
        int count = 1;
        while (count < 11) {
            System.out.println("Count is: " + count);
            count++;
        }
    }
}

(defun while-demo ()
     (setq count 1)
     (while (< count 11)
     	    (message count)
	    (setq count (+ count))))
       	      
	      
;;`dolist examples
******************
(setq j 0)
(dolist ((j 0) (+ j 1)))

;;`dotimes examples`
********************
```

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


