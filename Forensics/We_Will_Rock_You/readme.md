# We Will Rock You (Forensics - 100 Points)

> Isn't Queen the best?

Solution
--------

You are given a [zip](wewillrockyou.zip) containing an encrypted flag. The flag can be recovered by bruteforcing the key on the zip archive. The title "We Will **Rock You**" is a hint that the zip can be bruteforced with the rockyou dictionary.

```
fcrack -u -D -p /usr/share/wordlists/rockyou.txt wewillrockyou.zip
```
![](./zipcrack.PNG)

After learning the password is **__purple__** we can then use it to extract the flag.

```
unzip wewillrockyou.zip
```
![](./unzip.PNG)

The first element is the image of the Wonka bar while the second element is the hidden flag.

Flag: 'GoldenTICKET{Qu33n_roolz_y0#1}'

