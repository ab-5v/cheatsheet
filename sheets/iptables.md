
```
iptables -nL --line-number
```

```
iptables -I INPUT 11 -s <ip> -p tcp --destination-port <port> -m state --state NEW,ESTABLISHED -j ACCEPT -m comment --comment "text"
```

```
iptables -D INPUT 2
```
