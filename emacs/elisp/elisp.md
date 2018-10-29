#### A General Guide To Emacs Lisp
------------

- Insert `M-x ielm` in Emacs to use _**`Interactive Emacs Lisp Mode`**_ [IELM](http://wikemacs.org/wiki/IELM). I like to call it as _**REPL**_ which stands for _**Read Eval Print Loop**_  

- Insert `(require 'cl)`. It loads the Common Lisp library.

- Insert `C-x C-e` at the end of a S-expression for evaluation.

##### Create Commands

```el
(defun buffer/insert-filename ()
  "Insert file name of current buffer at current point"

  (interactive)
  (insert (buffer-file-name (current-buffer))))
```




