#### Emacs Readme!

- The `~/.emacs` file contains all the Elisp statements.
- The `~/.emacs.d` diretory contains all the packages(lisp cmds) for Emacs.
- One can load a package with `require 'expression'`


##### 1. Open a file with emacs
- `emacs myfile`

##### 2. Find a personal customization file(~/.emacs) in the system 
- `C-x C-f ~/.emacs`

##### 3. You'd see few function definition such as: 
```el
(custom-set-variables
 ;; custom-set-variables was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 '(ansi-color-faces-vector
   [default default default italic underline success warning error])
 '(ansi-color-names-vector
   ["#242424" "#e5786d" "#95e454" "#cae682" "#8ac6f2" "#333366" "#ccaa8f" "#f6f3e8"])
 '(custom-enabled-themes (quote (wheatgrass))))
(custom-set-faces
 ;; custom-set-faces was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 )
(put 'upcase-region 'disabled nil)
```

##### 4. Add the bellow functions in the same file
```el
(package-initialize)

(require 'package)
(add-to-list 'package-archives '("melpa" . "http://melpa.org/packages/"))
(package-initialize)

(add-to-list 'exec-path "usr/local/bin")

(set-keyword-coding-system nil)
```
##### 5. Save the file
`C-x C-s`



