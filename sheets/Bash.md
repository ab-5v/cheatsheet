Bash
====

## Internal variables
- `$$` PID of the script itself
- `$!` PID of last job run in background
- `$?` exit status of the last command
- `$_` arguments of the last command
- `$#` number of command-line arguments
- `$*` all of the arguments
- `$@` all of the arguments, each one is quoted
- `$0` the name of the shell or shell script
- `$1`, `$2`, `$3` arguments 1, 2, 3

## Conditional statements
If `testcmd` will exit with code `0` then `conscmd` will be executed:
```bash
if testcmd; then
  conscmd;
elif testcmd2; then
  conscmd2;
else
  conscmd3;
fi
```
Each `case` is an `expression` matching a `pattern`:
```bash
case $expression in
  pattern1)
    command1
  ;;
  pattern2|pattern3)
    command2
  ;;
  *)
    default
  ;;
esac
```
