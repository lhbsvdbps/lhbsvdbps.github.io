Example of a subdomain takeover by [@mjarosie](https://twitter.com/mjarosie).

# How I got here:

`amass enum -active -brute -o hosts_congon4tor.me -d congon4tor.me`

result:
```
webmail.congon4tor.me
mail.congon4tor.me
mx.congon4tor.me
ftp.congon4tor.me
imap.congon4tor.me
email.congon4tor.me
pop.congon4tor.me
smtp.congon4tor.me
nktixgewpt.takeova.congon4tor.me
test.congon4tor.me
testing.takeova.congon4tor.me
ctf.congon4tor.me
docs.congon4tor.me
congon4tor.me
```

Going to `docs.congon4tor.me` resulted in GitHub 404 "Not Found" error.

`nslookup docs.congon4tor.me`:

```
Server:		10.60.111.237
Address:	10.60.111.237#53

Non-authoritative answer:
docs.congon4tor.me	canonical name = lhbsvdbps.github.io.
Name:	lhbsvdbps.github.io
Address: 185.199.110.153
Name:	lhbsvdbps.github.io
Address: 185.199.111.153
Name:	lhbsvdbps.github.io
Address: 185.199.108.153
Name:	lhbsvdbps.github.io
Address: 185.199.109.153
```

Created a `lhbsvdbps` GitHub account and this `lhbsvdbps.github.io` page.

In GitHub Pages settings I've added a `docs.congon4tor.me` custom domain
which creates a `docs.congon4tor.me -> lhbsvdbps.github.io` CNAME record.

Go to http://docs.congon4tor.me/ to see the result.

Thanks [@Cong4tor](https://twitter.com/Congon4tor)!