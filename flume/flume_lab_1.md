Configuration파일 작성($DEVSH/exercises/flume/spooldir_exer.conf)

```
# Name the components on this agent
a1.sources = mySource
a1.sinks = mySink
a1.channels = myChannel


# Describe/configure the source
a1.sources.mySource.type = netcat
a1.sources.mySource.bind = localhost
a1.sources.mySource.port = 44445
a1.sources.mySource.spoolDir = /flume/weblogs_spooldir
a1.sources.mySource.channels = myChannel



# Describe the sink
a1.sinks.mySink.type = logger
a1.sinks.mySink.hdfs.path = /loudacre/weblogs_flume/
a1.sinks.mySink.channel = myChannel


# Use a channel which buffers events in memory
a1.channels.myChannel.type = memory
a1.channels.myChannel.capacity = 1000
a1.channels.myChannel.transactionCapacity = 100
```

conf 실행 
```
flume-ng agent \
--conf /etc/flume-ng/conf \
--conf-file $DEVSH/exercises/flume/spooldir_exer.conf \
--name a1 -Dflume.root.logger=INFO,console
```
```
$ telnet localhost 44445
Trying 127.0.0.1...
Connected to localhost.localdomain (127.0.0.1).
Escape character is '^]'.
Hello world! <ENTER>
OK

2019-03-11 18:17:33,366 (SinkRunner-PollingRunner-DefaultSinkProcessor) [INFO - org.apache.flume.sink.LoggerSink.process(LoggerSink.java:94)] Event: { headers:{} body: 48 65 6C 6C 6F 20 57 6F 72 6C 64 0D             Hello World. }
```


© 2019 GitHub, Inc.
