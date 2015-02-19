VimNotes
========

This is a compilation of the elementary keybindings often used on a UNIX machine, so I have something to quickly refer to. Hopefully others find this useful in some capacity. 

 **command** | **action** 
 :--|:--|:--:
 :wq! | save and exit vim
 :q! |  exit vim without saving 
 x  | delete at cursor 
 i | insert mode before cursor  
 ESC | takes out of insert mode 
A | append text to the end of line
a | insert mode after cursor
:![command] | execute external command
:w [FILENAME] | save as 
v | enter visual mode 
y | copies ("yanks") text selected in visual mode
p | puts back copied/cut text, one line under cursor
:r ![command] | puts output of command into file 
o | newline below cursor and insert mode 
O | newline above cursor and insert mode 
R | replace multiple characters 
r[character] | replace at cursor with [character]
CTRL-g | prints the line position in the file 
/[keyword] | searches for [keyword] in file, n navigates downwards, N upwards 
?[keyword] | same as /, except directions (and thus n and N's direction are reversed.)
% | jumps to next (,[,{, given that the cursor is on one of those characters to begin with 
:s/[old]/[new] | replaces first occurence of [old] in cursor's line with [new] 
:s/[old]/[new] | replaces all occurrences of [old] in line with [new] 
:%s/[old]/[new]/g | global replace, no prompt 
:%s/[old]/[new]/gc | global find and replace with prompt 
:[#],[#]s/[old],[new]/g | global replace between lines specified. 
u | undo action 
CTRL-R | redo action 
dd | delete line 
[number]dd | delete [number] lines 
[number]w | moves [number] words down, to first character of [number] word 
[number]e | moves to last character of [number] word down
:syntax on| turns on syntax highlighting. Very useful. 




**motions** | **description**
:--:| :--:
h , j , k , l | left, down, up, right
$ | end of line
0 | move to beginning of line 
w | moves cursor to first character of next word, excluding spaces.
e | moves cursor to last character of current word, including spaces.
gg | top of file 
G  | bottom of file
[#]g | jump to [#/line number]

**standard vim formulae:**


```operator [number] motion```

Example:

```d3w   // deletes to the beginning of 3rd word from cursor. ```

```c3$   // removes the next 3 lines from the cursor and shifts automatically into insert mode. ```

```dG    // deletes to end of file. ```

**search term** | **action** |
:--| :-:
hlsearch | highlights searched terms.
ic | ignores case while searching, i.e searching for "the" will result in "The" as a result.
incsearch | finds the next instance of a search item while being typed.

**Useful tricks**
:--|:-:
To commment out lines at once: | Ctrl v over the selection you desire commented, and then hit I#(ESC)


**To turn on --> :set [search term]**

```:set ic // turns on the ignore case search option```


**To turn off --> :no[search term]**

```:set noic // turns off the ignore case option```

###Contributing:
Any Vim mavens are more than welcome to submit a PR; I'm always happy to be corrected.
