# roundrobin
image rotation
roundrobin2019
# roundrobin system
```
use the gist.
image filesize shorted the 30KB. big calc the 50KB.
if gist truncked 1024*10KB = 10MB or 300files.
10000/50 = 200 images and files.
simply calc 100images rotation.

index file the one. data scheme. hash,raw_url,timestamp
[['xxxyyyzzzz','https://www.eee.eeeeee/raw/xxxxxyyyzzz.png','123554444']]

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

 share the localStorage
 prefix = 'roundrobin.'
 hash ='44agbie7'//ex
 //key=> roundrobin.44agbie7
```

# draft method worker is best
```
indexurl=''
nowgistid=''
toHash
toUrl
has(hash) //true or false
get(hash).then() //because fetch the gist
set(base64).then() //return hash
;
createGist
updateGist
saveGist
saveLocal
hasLocal
hasGist
hasIndex
```

# simply api
```
let rr=roundrobin('') //indexgist,null is localStorage
rr.get(hash).then(src=>img.src=src) //return url
rr.set(base64).then(hash=>rr.get(hash)) //return hash, 'roundrobin.44agbie7'
rr.raw(hash).then(raw_url=>...) //return raw_url
```


