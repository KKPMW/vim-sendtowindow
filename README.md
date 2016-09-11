# vim-sendtosplit

Vim operator used to send text from one window split to another.

Main use case is sending code to and from the NeoVim's `:terminal` buffer.

## Installation ##

With your favorite plugin manager. In my case it's vim-plug:

`Plug 'KKPMW/vim-sendtosplit'`

Or manualluy copy the contents of the **plugin** folder to your
**./vim/plugin/** directory.

## Features ##

* Text can be defined by motions and text objects
* Tries to position the cursor in a convenient place after each call.
* Dot repeatable.

## Maps ##

By default it uses the following maps:

* `<c-l>` sends to the left split
* `<c-k>` sends to the top split
* `<c-j>` sends to the bottom split
* `<c-h>` sends to the right split

Here `<c-l>` is control+l

In order to change the above key maps add the following to you *vimrc*:

    let g:sendtosplit_use_defaults=0
    nmap L <Plug>SendRight
    xmap L <Plug>SendRightV
    nmap H <Plug>SendLeft
    xmap H <Plug>SendLeftV
    nmap K <Plug>SendUp
    xmap K <Plug>SendUpV
    nmap J <Plug>SendDown
    xmap J <Plug>SendDownV

This would map all the commands to L, H, K and J respectively.



