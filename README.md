VimNotes
========

This is a compilation of the elementary keybindings often used on a UNIX machine, so I have something to quickly refer to. Hopefully others find this useful in some capacity. 

 **command** | **action** | **useful?**
 :--|:--|:--:
 h , j , k , l | left, down, up, right | staple
 :wq! | save and exit vim | staple
 :q! |  exit vim without saving |staple
 x  | delete at cursor | occasionally
 i | insert mode before cursor  | occasionally
 ESC | takes out of insert mode | staple
A | append text to the end of line | occasionally
a | insert mode after cursor | occasionally
:![command] | execute external command | necessity!!!
:w [FILENAME] | save as | occasionally
v | enter visual mode | necessity!!!
y | copies ("yanks") text selected in visual mode | very useful
p | puts back copied/cut text, one line under cursor | quite useful
:r ![command] | puts output of command into file | exotic
o | newline below cursor and insert mode | useful
O | newline above cursor and insert mode | useful
R | replace multiple characters | very useful
r[character] | replace at cursor with [character] | very useful
CTRL-g | prints the line position in the file | occasionally
gg | top of file | useful
G  | bottom of file | useful
[#]g | jump to [#/line number] | very useful
/[keyword] | searches for [keyword] in file, n navigates downwards, N upwards | staple
?[keyword] | same as /, except directions (and thus n and N's direction are reversed.) | exotic
% | jumps to next (,[,{, given that the cursor is on one of those characters to begin with | necessity!!
:s/[old]/[new] | replaces first occurence of [old] in cursor's line with [new] |exotic
:s/[old]/[new] | replaces all occurrences of [old] in line with [new] | very useful
:%s/[old]/[new]/g | global replace, no prompt | useful, but use with care
:%s/[old]/[new]/gc | global find and replace with prompt | extremely useful
:[#],[#]s/[old],[new]/g | global replace between lines specified. | exotic
u | undo action | staple
0 | move to beginning of line | occasionally
CTRL-R | redo action | staple
dd | delete line | useful
[number]dd | delete [number] lines | a bit exotic
[number]w | moves [number] words down, to first character of [number] word | pretty useful
[number]e | moves to last character of [number] word down | useful




**motions** | **description**
:--:| :--:
$ | end of line
w | moves cursor to first character of next word, excluding spaces.
e | moves cursor to last character of current word, including spaces.

**standard vim formulae:**


```operator [number] motion```

Example:

```d3w   // deletes to the beginning of 3rd word from cursor. ```

```c3$   // removes the next 3 lines from the cursor and shifts automatically into insert mode. ```



**search term** | **action** |
:--| :-:
hlsearch | highlights searched terms.
ic | ignores case while searching, i.e searching for "the" will result in "The" as a result.
incsearch | finds the next instance of a search item while being typed.

**To turn on --> :set [search term]**

```:set ic // turns on the ignore case search option```


**To turn off --> :no[search term]**

```:set noic // turns off the ignore case option```

###Contributing:
Any Vim mavens are more than welcome to submit a PR; I'm always happy to be corrected.
