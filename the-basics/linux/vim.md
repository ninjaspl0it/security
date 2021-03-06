# Vim

[http://www.viemu.com/a-why-vi-vim.html](http://www.viemu.com/a-why-vi-vim.html)  
And also this classic answer: [https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim](https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim)

## Core concepts <a id="core-concepts"></a>

In vim you have the concept of buffers.

```text

:buffers



b1
b2

b [name]



:bdelete
:bd
```

## Movement - Motion commands <a id="movement---motion-commands"></a>

**Left,up,down,right**

`hjkl`

**start of line**

`0` \(zero\)

**end of line**

`$`

**beginning of next word**

`w`

**beginning of next word, defined by white space**

`W`

**end of the next word**

`e`

**end of the next word, defined by white space**

`E`

**back to the beginning of previous word**

`b`

**back to the end of previous word**

`B`

**go to next character of your choice**

If you want to go to the next comma

`f,`

**start of file**

`gg`

**end of file**

`G`

## Additional Commands <a id="additional-commands"></a>

```text
:q                          - Quit.
:wq                         - Save and close.
:syntax on                  - Turn on Syntax highlighting for C programming and other languages.
:history                    - Shows the history of the commands executed
:set number                 - Turn on the line numbers.
:set nonumber               - Turn off the line numbers.
```

## Operators <a id="operators"></a>

Operators are commands that do things. Like delete, change or copy.

`c` - change  
`ce` - change until end of the word.  
`c$` - change until end of line.

## Combining Motions and Operators <a id="combining-motions-and-operators"></a>

Now that you know some motion commands and operator commands. You can start combining them.

`dw` - delete word  
`d$` - delete to the end of the line

## Count - Numbers <a id="count---numbers"></a>

You can add numbers before motion commands. To move faster.

`4w` - move cursor three words forward  
`0` - move curso to the start of the line

You can use numbers to perform operations.  
`d3w` - delete three words

`3dd` - delete three lines

## Replace <a id="replace"></a>

If you need to replace a character, there is no need to enter insert-mode. You can just use replace

Go to a character and the press `r` followed by the character you want instead.

`rp` if you want to replace p.

`R`

## Clipboard <a id="clipboard"></a>

In order to copy something FROM vim to the OS-clipboard you can do this:

The `"` means that we are not entering a registry. And the `*` means the OS-clipboard. So we are yanking something and putting it in the OS-clipboard registry.

```text
"*y
```

## Substitute - Search and replace <a id="substitute---search-and-replace"></a>

:s/thee/the/g

## Entering insert-mode <a id="entering-insert-mode"></a>

`i` - current character  
`o` - next line  
`O` - line before  
`a` - end of word  
`A` - end of line

## .vimrc <a id="vimrc"></a>

Here is all your vim-configuration.

Contains optional runtime configuration settings to initialize Vim when it starts. Example: If you want Vim to have syntax on and line numbers on, whenever you open vi, enter syntax on and set number in this file.

```text
##Sample contents of .vimrc

syntax on
set number
```

## Plugins <a id="plugins"></a>

Install vundle here  
[https://github.com/VundleVim/Vundle.vim](https://github.com/VundleVim/Vundle.vim)

**Add plugin**

Add plugin to your .vimrc-file and then open vim and write

`:PluginInstall`

## References <a id="references"></a>

[https://bitvijays.github.io/LFF-ESS-P0B-LinuxEssentials.html](https://bitvijays.github.io/LFF-ESS-P0B-LinuxEssentials.html)

