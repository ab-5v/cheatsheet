# Command Line Tools

## xargs

```sh
cat file | xargs -L 1 -I @ sh -c 'command1 "@" && command2 "@"'
```
