<p align="center">
  <img width="460" height="200" src="https://daniel.haxx.se/blog/wp-content/uploads/2016/04/good_curl_logo-1200x459.png">
</p>

# curl-command
curl is used in command lines or scripts to transfer data.

# Description
curl is a tool to transfer data from or to a server, using one of the supported protocols (DICT, FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, MQTT, POP3, POP3S, RTMP, RTMPS, RTSP, SCP, SFTP, SMB, SMBS, SMTP, SMTPS, TELNET and TFTP). The command is designed to work without user interaction.

# Tool
- Git
- tiny-curl

## Simple GET Request
- curl https://jsonplaceholder.typicode.com/posts
- curl https://jsonplaceholder.typicode.com/posts/1

## Include HTTP Header (--include, -i)
curl --include https://jsonplaceholder.typicode.com/posts/1

## Header Only (--head, -I)
curl --head https://jsonplaceholder.typicode.com/posts/1

## Write output to file (-o, --output)
curl -o test.txt https://jsonplaceholder.typicode.com/posts/1

## Download File (-O, --remote-name)
curl -O http://i.imgur.com/QRlAg0b.png

## Limit Transfer Rate
curl -O --limit-rate 1000B http://i.imgur.com/QRlAg0b.png

## Spoof user agent
curl -O test.txt http://wajeeha.com/test.txt -A "Mozilla"

##  POST Data (-d, --data)
curl -d "title=Hello&body=Hello World" https://jsonplaceholder.typicode.com/posts

##  PUT Data (-X PUT -d)
curl -X PUT -d "title=Hello&body=Hello World" https://jsonplaceholder.typicode.com/posts/1

##  Delete Data (-X DELETE)
curl -X DELETE https://jsonplaceholder.typicode.com/posts/1

## Secured Routes
curl -u Wajeeha:mypassword https://jsonplaceholder.typicode.com/posts/1

## Follow Redirection (-L)
- curl http://google.com
- curl -L http://google.com

## Download Files From FTP Server
curl -u ftpuser:ftppass -O ftp://x.x.x.x/public_html/sopmefile.php

## Upload via FTP
curl -u test@site:credential! -T hello.txt ftp://ftp.test.com

## Download via FTP
curl -u test@site:credential! -O ftp://ftp.test.com/hello.txt
