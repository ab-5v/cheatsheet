# Command Line Tools

- [xargs](#xargs)
- [iptables](#iptables)
- [df](#df)
- [du](#du)
- [tr](#tr)


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

## df
Display free disk space
```
df -H
```

## du
Disk usage by folder
```
sudo du -sh /*
```
## tr
Remove non-printable ASCII characters
```
tr -cd '\11\12\15\40-\176' < dirty > clean
```
