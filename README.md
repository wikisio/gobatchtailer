# gobatchtailer
A syslog sender by tailing from a batch of files.


## feature

1. Tail all files from a directory or part files by regex filters.
2. Rate limit to to tuning the cpu and io load.
3. Work as a relay syslog server to aggregate syslogs from upstream syslog sources.
## Running
```shell
% ./gobatchtailer --config config.toml
```

## configuration 

```toml

[relayServer]
bindAdress: 127.0.0.1
port: 5141

[server]
bindAdress: 10.187.1.100
port: 5141
type: UDP

[[logger]]
path: /var/log/**
file: *.log

[[logger]]
path: /data/log/**
file: *.log


```

## to do 

1. tls support
