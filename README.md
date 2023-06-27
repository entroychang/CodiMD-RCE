# CodiMD RCE

## Usage

```bash=
python3 exploit.py -u url --headers headers
```

* If you don't have `requests`, remember to `pip3 install requests` first.
* `url` is the target including the note id.
    * `http://target_ip_or_domain/note_id`
    * If you have no idea, maybe you can try `/features`.
* `headers` is not required. If the target is private, protected or limited, you have to give a cookie to view the content. Mostly the cookie key is `connect.sid`.

### Example 

```bash=
python3 exploit.py -u 'http://ip/note_id' --headers 'Cookie: connect.sid=connect.sid;'
```