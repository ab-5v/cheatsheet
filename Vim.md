# Find and replase
- `qx{command}q` to record, `@x` to repeat
- `:s/from/to` to replace, `&` to repeat

# Normal mode
- `daw` remove the word under cursor
- `10c-a`/`c-x` change the first number under cursor
- `nrformats` setting for changing numbers
- `gu{motion}` `gU` `g~` change case

# Insert mode
- `c-w` delete back a word
- `c-u` delete back to start of line
- `c-o` insert normal mode
- `c-r0` paste from register 0
- `c-vu1234` paste symbol

# Visual mode
- `gv` reselect the last selection
- `o` go to other end of selection
- `vboe` select word from the middle
- `vr-` replace whole line with “-”
- `c-v` and `A` to modify line ends

# Command mode
- `[rande]d/y[x]` delete/yank lines to the register “x”
- `[line]p[x]` put the text from `x` after `line`
- `[range]mv/t(copy) {address}` mv/copy range below the address
- `[range]join` join specified lines
- `c-w` delete back a word
- `c-r0` paste from register 0
- `:3p` print third line
- `:.,$p` print from the current line to the last one
- `:%p` print the whole line
- `:/<html>/+1,/<\/html>/-1p` also accepts patterns
- ``mp` print line, containing mark m
- `:t.` duplicate line
- `@:` repeat last Ex command
- `c-o` revert last Ex command
- `:%normal A;` set ; at the end of each line
- `:%normal i//` comment all lines (normal runs from start of line)
- `c-d` list of possible completions
- `c-rc-w` copy the word under cursor to command promt
- `%s//<C-r><C-w>/g` `:help <C-r><C-w>`
- `q/` open command line window with history of searches
- `q:` open command line window with history of Ex
- `c-f` switch from CL mode to CL window
- `:!node %` execute current file
- `:read !{cmd}` standard output to duffer
- `:write !{cmd}` buffer as standard input
- `:2,$!sort -t',' -k2` apply external command to the rang

# Open files
- `:e %<tab>` expands current file path
- `:e %:h<tab>` expands path and removes file name
- `:set path+=app/**` and `:find main.js`
- `:!mkdir -p %:h` ensure directory for file

# Motion
- `gj` `gk` `g0` `g^` `g$` navigate inside wrapped line
- `d/ge<CR>` remove all until “ge”
- `ia )">}]twWsp` inside outside
- `d{motion}` `c{motion}` `y{motion}`
- `m{a-zA-Z}` set mark az - local to buffer, AZ - global
- `{mark}/'{mark} go to marks line/line and column
`` Position before the last jump within current file 
`. Location of last change
`^ Location of last insertion
`[ Start of last change or yank
`] End of last change or yank 
`< Start of last visual selection 
`> End of last visual selection
- `runtime macros/matchit.vim`

# Navigate between files
- `<c-o>/<c-i>` back and forward
- `H/M/L` top/middle/bottom of screen
- `<c-[>` jump to definition
- `g;/g`, back and forward through the change list
- `gi` back to the last insertion position and enter insert mode
- `:set suffixesadd+=.rb` suffixes for gf
- `:set path=.,/usr/include,,` path for gf

# Registers
- `""` unnamed register (default for y,p,d)
- `"0` yank register
- `"_` black hole register
- `"{register}[ydp]{motion}`
- `"+` clipboard register
- `"*` middle mouse button register
- `"=` expression register
- `"/` last search pattern
- `".` Last inserted text
- insert mode `<c-r>{register}`

# Macro
- `q{register}{command}q` record macro
- `@{register}` play macro
- `@@` replay last play
- playback stops on motion fail, `1000@a` to play all possible 
- search and replace: `qq;.q` then `10@q`
- execute macro for selection `:'<,'>normal @a`
- `qA append` command to macro `a`
- `~ gu gU` toggles case under cursor

# Patterns
- `c%(<C-r>")` change surrounding
- `/pattern/e` search for pattern and place cursor to the end of match
- `//` search previous pattern
- `//replacement/` replace previous search pattern
- `///gn` print number of occurrences to be replaced
- `<C-r><C-w>` Autocomplete the Search Field Based on Preview Match

# Substitution
- `:[range]s[ubstitute]/{pattern}/{string}/[flags]`
- flag `c` ask about every substitution
- `c-r/` paste from search register
- `:%s//\=@0/g` reference to the register 0 as a pattern
