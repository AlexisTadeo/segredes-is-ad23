### SRA
## Objetivo

I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...

Additional details will be available after launching your challenge instance.

I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...Connect to the program on our server: `nc saturn.picoctf.net 62343`Download the program: [chal.py](https://artifacts.picoctf.net/c/298/chal.py)
## Solución
```bash
- Codigo
from pwn import *
import primefac
from itertools import combinations
from Crypto.Util.number import long_to_bytes

#function to generate all the sub lists
def sub_lists (l):
   # initializing empty list
    comb = []

    #Iterating till length of list
    for i in range(1,len(l)+1):
       # Generating sub list
        comb += [list(j) for j in combinations(l, i)]
   # Returning list
    return comb

def divisors(phi):
   print("Give me the divisors of ", phi-1)
  # this is dangerous, but I'm trusting me
   return(eval(input()))

#connect to the server
r = remote('saturn.picoctf.net', 64655)
#get ciphertext
r.recvuntil("anger =")
ciphertext=int(r.recvline())
#get d
r.recvuntil("envy =")
d=int(r.recvline())
print("cipher=",ciphertext)
print("d=",d)
print(r.recvuntil("vainglory?"))
r.recvline()
#since d is e^-1 mod (p-1)*(q-1), d*e=k*(p-1)*(q-1)+1
#so (p-1)*(q-1)*k = d*e-1
factors=divisors(d*65537)
combos = sub_lists(factors)
primes = set()
#try all possible subsets of the list of factors as the factors of (p-1)
for l in combos:
   product = 1
  # multiply them together to get p-1
   for k in l:
      product = product * k
  # if the right length and adding 1 yields a prime, then maybe
   if product.bit_length()==128 and primefac.isprime(product+1):
      primes.add(product+1)
print(primes)
primelist = list(primes)
#try all possible prime pairs
for p in primelist:
   for q in primelist:
      n=p*q
     # decode with this possible n
      plain = pow(ciphertext,d,n)
      try:
         plaintext = long_to_bytes(plain)
        # see if it corresponds to text and if so, try it
         print(plaintext.decode())
         r.sendline(plaintext.decode())
         print(r.recvline())
         print(r.recvline())
         print(r.recvline())
      except:
         continue

- Resultado

┌──(kali㉿kali)-[~/Documents/SRA] 
└─$ python3 exp.py [+] Opening connection to saturn.picoctf.net on port 64655: Done /home/kali/Documents/SRA/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See [https://docs.pwntools.com/#bytes](https://docs.pwntools.com/#bytes "https://docs.pwntools.com/#bytes") r.recvuntil("anger ![😊](https://discord.com/assets/92fac0627ff6cd675f28.svg) /home/kali/Documents/SRA/exp.py:29: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See [https://docs.pwntools.com/#bytes](https://docs.pwntools.com/#bytes "https://docs.pwntools.com/#bytes") r.recvuntil("envy ![😊](https://discord.com/assets/92fac0627ff6cd675f28.svg) cipher= 34697145712232974028402692395211878475011384154546302639503378532923495347026 d= 10048104183195587945203575364767112888455217216966364738479851308607516577073 /home/kali/Documents/SRA/exp.py:33: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See [https://docs.pwntools.com/#bytes](https://docs.pwntools.com/#bytes "https://docs.pwntools.com/#bytes") print(r.recvuntil("vainglory?")) b'vainglory?' Give me the divisors of 658522603854089247164806718680742277370689570748324645865754015212210813911633200 [2, 2, 2, 2, 3, 3, 5, 5, 11, 37, 47, 2341, 382037, 2870028545983, 1524882311432939, 563503553195982479, 4335606684762662633] {190152268533317138748722075180894713721, 244976755808153230403139131269248425881, 278035861189400652240842138901518719051, 259322241508630671823142774091321531901, 295867837705593177742675549557315865483} AxuiuB4LVGpaDonm /home/kali/Documents/SRA/exp.py:61: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See [https://docs.pwntools.com/#bytes](https://docs.pwntools.com/#bytes "https://docs.pwntools.com/#bytes") r.sendline(plaintext.decode()) b'> AxuiuB4LVGpaDonm\r\n' b'Conquered!\r\n' b'picoCTF{7h053_51n5_4r3_n0_m0r3_b2f9b414}\r\n' AxuiuB4LVGpaDonm [*] Closed connection to saturn.picoctf.net port 64655
```
## Notas adicionales

## Bandera

picoCTF{7h053_51n5_4r3_n0_m0r3_b2f9b414}
## Hints

### Referencia

- https://www.dcode.fr/prime-factors-decomposition