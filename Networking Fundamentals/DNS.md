Dns stands for domain name system , it translates a human readable website name such as google.com to an ip address because computers use ip addresses not names , dns was created because humans are good at remembering names not ip addresses.

Whole dns process :

Your pc first checks the browser's cache for the website ip if the browser has the ip cached there is no dns query if there is no cache , we check the operating system cache if there is no cache there will be a dns query , our computer sends the query to its resolver which is usually the router , isp dns server or a public resolver such as google or cloudflare. The resolver asks the root dns server where it can find the ip of that website name , if the website name has .com the root server sends the resolver to a tld dns server which would be .com tld dns server for google.com  , the tld dns server sends the resolver to the authoritative dns server which actually holds the ip to that website name.
Here the root dns server , TLD dns server doesn't have the ip it redirects the resolver to the dns server which is called authoritative dns server which has the actual ip.
