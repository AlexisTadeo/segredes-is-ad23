### PW Crack 1
## Objetivo

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.py
--2023-10-01 22:03:51--  https://artifacts.picoctf.net/c/10/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.18, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                          100%[==============================================================================================================>]     876  --.-KB/s    in 0s      

2023-10-01 22:03:51 (359 MB/s) - 'level1.py' saved [876/876]

alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
--2023-10-01 22:04:00--  https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                                100%[==============================================================================================================>]      30  --.-KB/s    in 0s      

2023-10-01 22:04:01 (11.4 MB/s) - 'level1.flag.txt.enc' saved [30/30]

alexistadeo2201-picoctf@webshell:~$ ls -la
total 852
drwxr-xr-x 4 alexistadeo2201-picoctf alexistadeo2201-picoctf   4096 Oct  1 22:04 .
drwxr-xr-x 3 root                    root                        37 Sep 25 16:29 ..
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    220 Sep 25 16:29 .bash_logout
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   3771 Sep 25 16:29 .bashrc
drwxrwxr-x 3 alexistadeo2201-picoctf alexistadeo2201-picoctf     19 Oct  1 21:36 .local
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    807 Sep 25 16:29 .profile
-rw------- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    265 Oct  1 21:59 .python_history
drwx------ 2 alexistadeo2201-picoctf alexistadeo2201-picoctf     48 Sep 25 17:33 .ssh
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    215 Oct  1 21:47 .wget-hsts
-rw-r--r-- 1 root                    root                      4443 Oct  1 21:10 README.txt
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   1278 Mar 16  2023 code.py
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf     27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf  14551 Oct 26  2020 file.1
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    705 Oct  1 21:44 fixme1.py
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   1029 Mar 16  2023 fixme2.py
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf     30 Mar 16  2023 level1.flag.txt.enc
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    876 Mar 16  2023 level1.py
-rwxrwxrwx 1 alexistadeo2201-picoctf alexistadeo2201-picoctf 776032 Oct 26  2020 strings
alexistadeo2201-picoctf@webshell:~$ cat level1.py 
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
alexistadeo2201-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
## Hints

- To view the file in the webshell, do: `$ nano level1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.