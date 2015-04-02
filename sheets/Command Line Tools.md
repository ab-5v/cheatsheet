# Command Line Tools

- [xargs](#xargs)
- [iptables](#iptables)


## xargs

Pass each line as arguments for few commands
```sh
cat file | xargs -L 1 -I @ sh -c 'command1 "@" && command2 "@"'
```

## iptables

List all rules with line and port numbers
```
iptables -nL --line-number
```

Insert new rule to the specified place
```
iptables -I INPUT 5 -s <ip> -p tcp --destination-port <port> -m state --state NEW,ESTABLISHED -j ACCEPT -m comment --comment "text"
```

Remove rule on specified position
```
iptables -D INPUT 5
```
