## Docker RemoteSyslog2

Docker RemoteSyslog2 leverages the deployment agility of Docker, the slickness of [Alpine Linux](https://github.com/gliderlabs/docker-alpine) and the conveniance of [remote_syslog2](https://github.com/papertrail/remote_syslog2/) to bootstrap remote logging capabilities for both Docker hosts and containers.    
It automates the collection and sending of logs to central log collectors or cloud-based log management services by tailing log files and emitting syslog messages over UDP, TCP or TCP/TLS.

Forked from https://github.com/janeczku/Docker-RemoteSyslog2
-------

### Benefits

* Bootstrap remote log management for your servers by simply starting a RemoteSyslog2 container
* Forward logs to cloud-based log management services without the hassle of installing agents or configuring syslog
* Collect file-based logs from Docker containers

### Usage examples

Configuration parameters can be passed both using environment variables and command line flags

### Compatible log management servers/services (non-exclusive list)

* Logstash
* Fluentd
* Splunk
* Papertrail
* Loggly
* Logentries
* Graylog
...

### Configuration using command line arguments
Refer to the [remote_syslog2](https://github.com/papertrail/remote_syslog2/) documentation

### Configuration using environment variables

**SYSLOG_HOST** *Required*    
Default: ` `  
Destination syslog hostname or IP

**SYSLOG_PORT**  
Default: `514`  
Destination syslog port

**SYSLOG_FILES** *Required*    
Default: ` `  
Space delimited list of log files to monitor (use absolute paths, wildcards allowed)    
e.g.: `/var/log/auth.log /var/log/nginx/*`

**SYSLOG_TCP**  
Default: `false`  
Connect over TCP (no TLS)

**SYSLOG_TLS**  
Default: `false`  
Connect over TCP with TLS

**SYSLOG_FACILITY**  
Default: `user`  
Syslog Facility

**SYSLOG_SEVERITY**  
Default: `notice`  
Syslog Severity

**SYSLOG_HOSTNAME**  
Default: ` `  
Override hostname
