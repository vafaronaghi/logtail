This small perl script is intended to 

- read HTTP access logs from flat files (generated by a web server like nginx,    lighty, apache, ...), 
- then format them to JSON format as logstash does,
- and finally send them to a redis broker

It supports log rotation using Linux inotify2, and try to read and write in
bulk mode. It has been developped to deal with more than 500 events/second,
with success.

Feel free to modify it to fit to your needs.

