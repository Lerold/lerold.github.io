
________________________
**There are solutions to the CTF in this write up so if you don't want to know the answers, please stop reading now.**
________________________


> Security Fest is an inspiring and unique IT security conference held in Gothenburg, Sweden. The event is an excellent opportunity to learn more about IT security, and a great way to connect with both the renowned international speakers, and the other attendees.

Visit their [website](https://securityfest.com) for more information about the Event.

And make sure to catch [watch all the talks on YouTube.](https://www.youtube.com/playlist?list=PL0Jph6SmWIuMmZpl5NVjPQ_uDXHYw5Jii)

[Abhinav Pandagale](https://www.linkedin.com/in/abhinavpandagale/) did a 14 minute talk on it that can be found on the stream from [Security Fest Day 1 - Lightning talk: Badge challenge: Abhinav Pandagale](https://www.youtube.com/watch?v=c5_kFwVHUbY&list=PL0Jph6SmWIuMmZpl5NVjPQ_uDXHYw5Jii&index=1&t=23224s)

The story of the Badge for Security Fest 2023 is also on [Security Fest 2023 Badge on Hackster.io](https://www.hackster.io/HacksFromPanda/the-gothenburg-skyline-badge-security-fest-eed557)

---
## The hardware
### Front

![Front of the Badge](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gvtjr0j5czuhtsayc5so.png)
The front depicts a skyline with land marks from Gothenburg, it’s UV-printed. The Print was done after the components on the back was soldered on to keep the vibrant look of the picture. On the left is of course the Security Fest robot

### Back

![Back of the Badge](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jpkatbted49tn9rg41v2.png)
The back hosts all the components and most came pre soldered. To combine the hardware and software the makers cleverly omitted 9 SMD LEDs so that the participants have to get to hardware village and sit down and solder them on.

Even though there are 2 LEDs already on there it’s only one that shows and that was because they wanted to be able to see that the board was functional.

Figure out how to solder look at the [[PDF]](https://hackerwares.in/Gothenburg%20Badge%20Soldering%20Tutorial.pdf) from [Hackerwares.in](https://hackerwares.in)


---
## CTF

> Before we get started, if you at any point disconnect the badge and want to come back to where you were, you always have to start with sending  `***` to the board via the serial monitor in the Arduino IDE.

### Getting started with the CTF
To get started and to interface with the board you can follow Abhinavs guide [here](https://hackerwares.in/Gothenburg%20Badge%20Soldering%20Tutorial.pdf).

_It is important to make sure the power switch SW1 is off or remove the battery_

But the short of it is that you have to connect the board to your computer with a microUSB cable, download the Arduino IDE, change it to the right port number and start the Serial Monitor. More details in the PDF. 
_Turn of timestamp in the Serial Monitor, the graphics will look way better._

---
### Challenge 1
The first challenge is just to get started with it and se it in the serial monitor of the Arduino IDE. And in the PDF it’s outlined that to get started you need to send `***` to the board. 
The first LED is already on as mentions earlier and.
\*\*\* 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yxcua9pgd7dwsj0cfzrb.png)


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gmbo0f3n5sj8q303dyvz.png)

We are presented with a string that follows: `TDRwcHN0MWZ0M3Q=`


Looking at it it you can recognise the Base64 encoding.
You can also google _”cipher with = at the end”_
After that all you have to do is decode the Base64 with the help of an installed tool or online. Again turn to google and search for _”Base64 decoder”_. Any of the tools will tell you that the first flag is: `L4ppst1ft3t`

```
Enter your flag.
L4ppst1ft3t
```

The flag is the Swedish word for lipstick but in [leetspeak](https://en.wikipedia.org/wiki/Leet).

```
The Lipstick building is unlocked!

Why the robot is blinking......is there any rhythm in what's it saying?
```
The Second LED turns on and then on to the next challenge.

---
### Challenge 2
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3248b8o7zach3n0w6c1u.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gff92kwovoer2cvyo4w1.gif)

Why the robot is blinking......is there any rhythm in what's it saying?

The LED for the robot is blinkning in a pattern that is repeating.
After identifying it as Morse Code it’s on to solving it.

I found that sitting with the . and - keys ready as the pattern goes on.

`—-- - .... --.`

After getting out my [Morse Code](https://en.wikipedia.org/wiki/Morse_code) - Decoder paper (Google) I solved it as follow

![Morde Code key](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/llhpp32jo9ni1pi7zmlt.png)


```
--— = O
- = T
.... = H
--. = G
```
After looking at it was easy to see that it wasn’t the flag that needed because of  course I got the order wrong. Correct order is `--. --- - ....`
And that spells GOTH instead

```
Verifying please wait...
GOTH
```


Welcome to the home of the Security Fest - Eriksbergshallen!

![LED 3](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gl7t102pbidj7gktvevu.png)

---
### Challenge 3
![Challange 3](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/l8kmgrgiaclpwcjpxpzj.png)

I have to be honest and say I that I recognised it but didn’t know what this was, every time I tried to Google the whole or part of it google drew a blank.

Ended up asking ChatGPT.

![Challange 3 ChatGPT](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6t0jt2dopn3qm6hjdqhy.png)

As a side note, when sitting at Security Fest 2023 on the 25-26 May. ChatGPT was experiencing heavy traffic load so it didn’t work to login but. You could get in and use the API Playground to send queries, although a bit slower than normal.

So now that we figured out it’s [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck) all we have to do is Google “Brainfuck decoder” and [dcode.fr - Brainfuck](https://www.dcode.fr/brainfuck-language)

_Important here is to make sure that you copy the whole text from the serial output and not miss anything, if you do it won’t translate right_

And with `f3sk3k0rk4` we get the new LED working.

![LED 4](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7s95id8l8ru2b1umscay.png)

---
### Challenge 4
![Challange 4](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oa3jfk66ryr9w7bi50rp.png)

![Cipher image 1](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fwr038npqs66jz5rkiiw.jpeg)
This flag is hidden be hind a chipper with a shift of half a dozen or 6, also know as [Ceasar cipher](https://en.wikipedia.org/wiki/Caesar_cipher).  
After searching Google for Ceasar cipher decoders we spot the tool used in the last Challenge, [decode.fr - Ceasar Cipher](https://www.dcode.fr/caesar-cipher) and after decoding with a shift of 6 we get our answer, the numbers are as in left in place and not changed or shifted.

So the coded phrase: `_m0zn1g-z0c3xy_` turns in to `_g0th1a-t0w3rs_`

![LED 5 & 6](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/b9zyclolh70hjfivbb4p.png)

---
### Challenge 5
![Challange 5](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/36xoi0rob1pjayf58n6c.png)

![Cipher image 2](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/q68q37tv70jh7jjc3qnk.jpeg)
The next challenge is using the [Pidgen Cipher](https://en.wikipedia.org/wiki/Pigpen_cipher) mixed with leetspeak. 
With the key it’s easy to read what it says.

![Pidgen cipher key](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/seakp0xc5ar0htlarri4.png)
And as before the numbers are left. And after knowing the answer it’s very easy to read it even with out solving it. `_ull3v1_`

![LED 7](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/idhwihisnamy2i55tdh3.png)

---
### Challenge 6
![Challange 6](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pjeaj742kwpu96jhcn5o.png)

![Cipher image 3](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oiyc5mpxwacqe5aymkx9.jpeg)
With a hint in the image saying “Bacon” and searching “Bacon Cipher” on Google we learn about the [Bacon’s Cipher](https://en.wikipedia.org/wiki/Bacon%27s_cipher) and in the same search result with get [dcode.fr - Bacon's cipher](https://www.dcode.fr/bacon-cipher) again and we are left with `_l1s3b3rg_`


![LED 8 & 9](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yxa8yed4z0h9cyooec59.png)

---
### Challenge 7
![Challange 7](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yyaqsi53sa2lg22hojrq.png)
(img)
We get a link to an image to inspect. The image that “DATA ABOUT THE DATA” and from that you could guess that it might be something in the exiff or metadata of the image. Here I downloaded the image first and check what I could find and found some interesting “Make” and “Image Description” of the image. 


![EXIF Tools 2](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ovdnzovekxvh4zn1f0fw.png)

Make was _Vignere_ 
And the Description was _ko4px3r-ck0f4r_
Searched for [Vignere Cipher](https://en.wikipedia.org/wiki/Vigenère_cipher) on google and found that [dcode.fr - Vigenere decoder](https://www.dcode.fr/vigenere-cipher) had a tool for it. 
How ever it requires a key that I didn’t find. After trying several different keys to no affect and asking around Abhinav what I was missing he said to look again. So after looking at it some more I instead uploaded the image to [EXIF.tools](https://exif.tools/upload.php) and found that I had missed something the “Artist” was _secfest_


![EXIF Tools 2](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/avq2ayhxsmhfvxiy870t.png)

And after trying `secfest` as the decryption key I was presented with `sk4ns3n-kr0n4n` and that worked as the flag.


![LED 10](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ug7unrv1tll5a2954bim.png)

---
### Challenge 8
![Challange 8](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1n32jp1ndofc0n75so0z.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8aflhohmkx25doxcvq7g.jpeg)
The hint in the serial monitor mentions Steghide so we Google “steghide tool online” and after trying the first tool from [stylesuxx on github.io](https://stylesuxx.github.io/steganography/) and only getting garbage I tried a second tool and again didn’t get anything. 
I Instead tried to use steghide in Linux and it asked for a password phrase and I after not finding any passphrase ( still don’t know if it’s mentioned anywhere) I tried the one the last challange _secfest_ and that gave me the flag  `g0th3b0rg-sh1p`
I’ve later tried the second tool on Google from [futureboy.us](https://futureboy.us/stegano/decinput.html) and that tool aslo produces the right flag.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ler5p369hznvipxv6gyi.png)

### Conclusion
I thought it was a very well made badge that was fun to solder and easy to get going with. It was fun to help others to get going and during the remainder of the event and I meet many who came and asked me for hits and tips about the CTF even when sitting and talking with Abhinav who obviously knew everything there was to know about the badge.

Even late in the evening when I was about to leave a group that was sitting working on the CTF threw hands up in the air in delight at seeing someone that could help to solve the last flags. 

Thank you Abhinav and Hackerwares for a well made badge and a CTF that everyone could easily get going with.

And thank you Security Fest for an amazing event with many interesting talks.
