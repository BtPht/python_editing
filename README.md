This is a mirror of python http://www.vim.org/scripts/script.php?script_id=1494

* Description :

Folding goes like this:

1. Only top level class or function definitions are folded (no nesting)
2. Folding is done one line after the class or function definition, so
    for example the line 'class foo( bar )' is right above the fold
3. Fold text is the first line of the corresponding docstring (if any)
    together with the number of folded lines
4. Toggle all folds on/off with the key F
5. Toggle the fold under the cursor on/off with the key f
6. In some rare cases folding can break down which can be fixed by :call ReFold()
    The reason for this break down is not known sometimes it happens when jumping
    between different files using tags.

In addition the script binds the key <Shift-e> (hint: _e_xecute) to saving the file and executing it in the interpreter assuming that /usr/bin/env exists otherwise you need to change this key mapping slightly. The keys 'gd' (hint: _g_o _d_efinition) are also bound to look for the definition of a function under the cursor similarly to the same key binding for C. 

* Install details :

Drop the file in your .vim/ftplugin/ directory (in case you already have a file there called python_editing.vim, don't forget to change the name).
