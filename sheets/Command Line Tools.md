# Command Line Tools

- [xargs](#xargs)


## xargs

Pass each line as arguments for few commands
```sh
cat file | xargs -L 1 -I @ sh -c 'command1 "@" && command2 "@"'
```
