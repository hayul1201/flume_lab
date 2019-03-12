
 flume-ng agent --conf /etc/flume-ng/conf \
--conf-file $DEVSH/exercises/flafka/spooldir_kafka.conf \
--name agent1 -Dflume.root.logger=INFO,console 

```
2019-03-11 23:35:22,717 (lifecycleSupervisor-1-1) [INFO - org.apache.flume.instrumentation.MonitoredCounterGroup.start(MonitoredCounterGroup.java:96)] Component type: SINK, name: kafka-sink started

```

$ kafka-console-consumer \
--zookeeper localhost:2181 \
--topic weblogs \


```
[training@localhost ~]$  $DEVSH/exercises/flume/copy-move-weblogs.sh \
> /flume/weblogs_spooldir
Copying and moving files to /flume/weblogs_spooldir
```


```
## Flume Agent
2019-03-11 23:42:35,298 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:35,300 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-01-28.log to /flume/weblogs_spooldir/2014-01-28.log.COMPLETED
2019-03-11 23:42:35,486 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:35,487 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-01-29.log to /flume/weblogs_spooldir/2014-01-29.log.COMPLETED
2019-03-11 23:42:35,685 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:35,685 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-02-08.log to /flume/weblogs_spooldir/2014-02-08.log.COMPLETED
2019-03-11 23:42:35,819 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:35,819 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-02-10.log to /flume/weblogs_spooldir/2014-02-10.log.COMPLETED
2019-03-11 23:42:35,942 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:35,942 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-02-11.log to /flume/weblogs_spooldir/2014-02-11.log.COMPLETED
2019-03-11 23:42:36,063 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:36,063 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-02-14.log to /flume/weblogs_spooldir/2014-02-14.log.COMPLETED
2019-03-11 23:42:36,188 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:36,189 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-02-15.log to /flume/weblogs_spooldir/2014-02-15.log.COMPLETED
2019-03-11 23:42:36,304 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:36,304 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-02-19.log to /flume/weblogs_spooldir/2014-02-19.log.COMPLETED
2019-03-11 23:42:36,424 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:36,424 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-03-01.log to /flume/weblogs_spooldir/2014-03-01.log.COMPLETED
2019-03-11 23:42:36,540 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.readEvents(ReliableSpoolingFileEventReader.java:258)] Last read took us just up to a file boundary. Rolling to the next file, if there is one.
2019-03-11 23:42:36,540 (pool-4-thread-1) [INFO - org.apache.flume.client.avro.ReliableSpoolingFileEventReader.rollCurrentFile(ReliableSpoolingFileEventReader.java:348)] Preparing to move file /flume/weblogs_spooldir/2014-03-09.log to /flume/weblogs_spooldir/2014-03-09.log.COMPLETED
```

```
#Kafka	consumer


81.7.248.46 - 112986 [09/Mar/2014:00:07:17 +0100] "GET /theme.css HTTP/1.0" 200 18607 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 1100"
81.7.248.46 - 112986 [09/Mar/2014:00:07:17 +0100] "GET /code.js HTTP/1.0" 200 10287 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 1100"
67.108.194.84 - 46 [09/Mar/2014:00:06:21 +0100] "GET /KBDOC-00263.html HTTP/1.0" 200 19573 "http://www.loudacre.com"  "Loudacre CSR Browser"
67.108.194.84 - 46 [09/Mar/2014:00:06:21 +0100] "GET /theme.css HTTP/1.0" 200 5529 "http://www.loudacre.com"  "Loudacre CSR Browser"
203.149.63.88 - 49924 [09/Mar/2014:00:06:05 +0100] "GET /KBDOC-00192.html HTTP/1.0" 200 13643 "http://www.loudacre.com"  "Loudacre Mobile Browser MeeToo 4.0"
203.149.63.88 - 49924 [09/Mar/2014:00:06:05 +0100] "GET /theme.css HTTP/1.0" 200 983 "http://www.loudacre.com"  "Loudacre Mobile Browser MeeToo 4.0"
145.127.192.118 - 119093 [09/Mar/2014:00:05:38 +0100] "GET /ifruit_5_sales.html HTTP/1.0" 200 17277 "http://www.loudacre.com"  "Loudacre Mobile Browser MeeToo 4.0"
145.127.192.118 - 119093 [09/Mar/2014:00:05:38 +0100] "GET /theme.css HTTP/1.0" 200 8613 "http://www.loudacre.com"  "Loudacre Mobile Browser MeeToo 4.0"
145.127.192.118 - 119093 [09/Mar/2014:00:05:38 +0100] "GET /code.js HTTP/1.0" 200 17240 "http://www.loudacre.com"  "Loudacre Mobile Browser MeeToo 4.0"
145.127.192.118 - 119093 [09/Mar/2014:00:05:38 +0100] "GET /ifruit_5.jpg HTTP/1.0" 200 8045 "http://www.loudacre.com"  "Loudacre Mobile Browser MeeToo 4.0"
250.109.227.139 - 43577 [09/Mar/2014:00:05:25 +0100] "GET /KBDOC-00061.html HTTP/1.0" 200 8867 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F21L"
250.109.227.139 - 43577 [09/Mar/2014:00:05:25 +0100] "GET /theme.css HTTP/1.0" 200 11069 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F21L"
224.222.186.245 - 6397 [09/Mar/2014:00:05:14 +0100] "GET /KBDOC-00236.html HTTP/1.0" 200 17365 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 2000"
224.222.186.245 - 6397 [09/Mar/2014:00:05:14 +0100] "GET /theme.css HTTP/1.0" 200 1227 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 2000"
182.250.19.48 - 79652 [09/Mar/2014:00:04:19 +0100] "GET /KBDOC-00204.html HTTP/1.0" 200 13397 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 2000"
182.250.19.48 - 79652 [09/Mar/2014:00:04:19 +0100] "GET /theme.css HTTP/1.0" 200 15879 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 2000"
216.58.41.59 - 80 [09/Mar/2014:00:04:12 +0100] "GET /KBDOC-00189.html HTTP/1.0" 200 6466 "http://www.loudacre.com"  "Loudacre CSR Browser"
216.58.41.59 - 80 [09/Mar/2014:00:04:12 +0100] "GET /theme.css HTTP/1.0" 200 1901 "http://www.loudacre.com"  "Loudacre CSR Browser"
180.230.57.14 - 113690 [09/Mar/2014:00:04:07 +0100] "GET /KBDOC-00237.html HTTP/1.0" 200 19359 "http://www.loudacre.com"  "Loudacre Mobile Browser iFruit 4A"
180.230.57.14 - 113690 [09/Mar/2014:00:04:07 +0100] "GET /theme.css HTTP/1.0" 200 541 "http://www.loudacre.com"  "Loudacre Mobile Browser iFruit 4A"
236.191.81.81 - 65902 [09/Mar/2014:00:03:53 +0100] "GET /KBDOC-00163.html HTTP/1.0" 200 744 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F41L"
236.191.81.81 - 65902 [09/Mar/2014:00:03:53 +0100] "GET /theme.css HTTP/1.0" 200 3287 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F41L"
131.125.128.26 - 34085 [09/Mar/2014:00:03:47 +0100] "GET /KBDOC-00172.html HTTP/1.0" 200 10153 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F41L"
131.125.128.26 - 34085 [09/Mar/2014:00:03:47 +0100] "GET /theme.css HTTP/1.0" 200 17011 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F41L"
112.118.226.215 - 92656 [09/Mar/2014:00:03:46 +0100] "GET /KBDOC-00106.html HTTP/1.0" 200 13587 "http://www.loudacre.com"  "Loudacre Mobile Browser Ronin Novelty Note 2"
112.118.226.215 - 92656 [09/Mar/2014:00:03:46 +0100] "GET /theme.css HTTP/1.0" 200 14328 "http://www.loudacre.com"  "Loudacre Mobile Browser Ronin Novelty Note 2"
241.168.61.120 - 56394 [09/Mar/2014:00:03:39 +0100] "GET /KBDOC-00091.html HTTP/1.0" 200 7511 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 2500"
241.168.61.120 - 56394 [09/Mar/2014:00:03:39 +0100] "GET /theme.css HTTP/1.0" 200 10451 "http://www.loudacre.com"  "Loudacre Mobile Browser Titanic 2500"
58.63.145.220 - 116 [09/Mar/2014:00:01:39 +0100] "GET /KBDOC-00196.html HTTP/1.0" 200 19960 "http://www.loudacre.com"  "Loudacre CSR Browser"
58.63.145.220 - 116 [09/Mar/2014:00:01:39 +0100] "GET /theme.css HTTP/1.0" 200 3088 "http://www.loudacre.com"  "Loudacre CSR Browser"
12.159.19.160 - 24 [09/Mar/2014:00:00:39 +0100] "GET /KBDOC-00224.html HTTP/1.0" 200 3423 "http://www.loudacre.com"  "Loudacre CSR Browser"
12.159.19.160 - 24 [09/Mar/2014:00:00:39 +0100] "GET /theme.css HTTP/1.0" 200 13391 "http://www.loudacre.com"  "Loudacre CSR Browser"
229.254.210.10 - 66543 [09/Mar/2014:00:00:14 +0100] "GET /KBDOC-00131.html HTTP/1.0" 200 9807 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F24L"
229.254.210.10 - 66543 [09/Mar/2014:00:00:14 +0100] "GET /theme.css HTTP/1.0" 200 6448 "http://www.loudacre.com"  "Loudacre Mobile Browser Sorrento F24L"
```
