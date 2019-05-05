# roundrobin
image rotation

# roundrobin system
```
use the gist.
image filesize shorted the 30KB. big calc the 50KB.
if gist truncked 1024*10KB = 10MB or 300files.
10000/50 = 200 images and files.
simply calc 100images rotation.

index file the one. data scheme. hash,raw_url
[['xxxyyyzzzz','https://www.eee.eeeeee/raw/xxxxxyyyzzz.png']]

index file rotation per 100files
if 13files drop, then old gist and create new gist.
or one action, one gist is simple. but overlimit the 10MB.

data and translate.
let raw_url='...'
let b=fetch(raw_url).then(d=>d.text()) //base64image
let u=createObjectUrl(b)
el.src=u;

localStorage save
let hash='....'
let flg=localStorage.keys.filter(d=>d.hash)
if(!flg) localStorage.setItem(hash,base64)
```
