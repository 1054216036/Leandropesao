## INTRODUCTION [![Build Status](https://travis-ci.org/rhysd/clever-f.vim.png?branch=dev)](https://travis-ci.org/rhysd/clever-f.vim)

clever-f.vim extends `f` mapping for more convenience. You may be able to forget the existence of `;`. And you can use `;` for an other mapping.
clever-f.vim is distributed under MIT license. See `doc/clever_f.txt` to get more information.



## USAGE

I'll show some examples of usage. _ is the place of cursor, -> is a move of
cursor, alphabets above -> is input by keyboard.


    input:       fh         f         f      e         fo         f
    move :  _---------->_------>_---------->_->_---------------->_->_
    input:                            F                            F
    move :                        _<-----------------------------_<-_
    text :  hoge        huga    hoo         hugu                ponyo



    input:        f        Fh       b     f                         Fo
    move :  _<----------_<------_<-_<-----------------------------_<-_
    input:        F        F          F
    move :  _---------->_------>_----------->_
    text :  hoge        huga    huyo         hugu                ponyo



    input:       th         t         t      e         to         t
    move :  _--------->_------>_---------->_-->_--------------->_->_
    input:                            T                            T
    move :                         _<-----------------------------__
    text :  hoge        huga    hoo         hugu                ponyo

## CUSTOMIZE

### Search a character only in current line

`g:clever_f_across_no_line` controls to search a character across multi lines or not.
Please set it to `1` in your vimrc to search a character only in current line.

### Ignore case

`g:clever_f_ignore_case` controls to make a search case-insensitive or not.
Please set it to `1` in your vimrc to ignore case.

### Migemo support

In Japanese environment, it is convenient that `fa` matches `あ` in some cases. This feature is provided by [migemo](http://0xcc.net/migemo/).
clever-f can search multibyte Japanese character with `f`, 'F', 't' and 'T' mappings. Migemo is not required because clever-f includes regex patterns generated by migemo.
Set `clever_f_use_migemo` to `1` to get migemo support.

## LICENSE

Distributed under MIT License. See `doc/clever_f.txt`
