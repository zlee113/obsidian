Date: 2024-07-18
Hub: [[linux]]
Tags: #book
URL/Title: Learning Modern Linux

Streams refer to inputs or outputs often shorthanded as I/O. Every shell has three default file descriptors
- stdin: Standard input so the keyboard
- stdout: Standard output so the monitor or shell terminal visuals
- stderr: Standard output also a visual effect normally outputted to the monitor
Streams can be redirected like sending all errors to files instead of being displayed.
example:
```
$ curl https://example.com &> /dev/null
$ curl https://example.com > /tmp/content.txt 2> /tmp/curl-status
$ head -3 /tmp/content.txt
<!doctype html>
<html>
<head>
$ cat /tmp/curl-status
 % Total % Received % Xferd Average Speed Time Time Time Current
 Dload Upload Total Spent Left Speed
100 1256 100 1256 0 0 3187 0 --:--:-- --:--:-- --:--:-- 3195
$ cat > /tmp/interactive-input.txt
Basics | 35
$ tr < /tmp/curl-status [A-Z] [a-z]
 % total % received % xferd average speed time time time current
 dload upload total spent left speed
100 1256 100 1256 0 0 3187 0 --:--:-- --:--:-- --:--:-- 3195
```

1. The first time we curl we use the &> to send both stdout and stderr to /dev/null so nothing is displayed
2. the second time we curl > into /tmp/content.txt so default 1> is stdout and 2> is stderr
3. We can see with the head command that stdout was printed into content and the status was sent to curl-status

