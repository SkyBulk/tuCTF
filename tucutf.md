# Mrs. White's <br> Messy Maids

** Hint **

> Mrs. White's simple website might be hiding some murderous intentions...


![maids](https://github.com/SkyBulk/tuCTF/blob/master/images/maids.png)

	
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

