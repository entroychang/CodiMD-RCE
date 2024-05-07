# CodiMD RCE

This is a DEVCORE Intern project. 
https://hackmd.io/@entroy/BJizrC8wh

## Usage

```bash=
python3 exploit.py -u url --headers headers
```

* If you don't have `requests`, remember to `pip3 install requests` first.
* `url` is the target including the note id.
    * `http://target_ip_or_domain/note_id`
* `headers` is not required. If the target is private, protected or limited, you have to give a cookie to view the content. Mostly the cookie key is `connect.sid`.
* If you find out that the target cannot use PUT method to edit the note, try the steps in payload file.
    * Just a note that PUT method can only edit a note that there is no users using. 
* You can build a vulnerable version of codimd using the docker compose file. 

### Example 

```bash=
python3 exploit.py -u 'http://ip/note_id' --headers 'Cookie: connect.sid=connect.sid;'
```

* Use `R` command to recover file content. Just a note that the code will only read filename in `files` folder. 
* Demo: https://www.youtube.com/watch?v=G4P6UF2vTJo&ab_channel=EntroyC