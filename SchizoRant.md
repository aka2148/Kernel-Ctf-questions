Potential distribution of first 5 quetions:

1 Webex Medium
Use sql injection to obtain the admin name and cookie to be able to then use burpsuite and then change the username and then forward the post.
sanitize the basic exploits and require some knowledge to be able to inject it properly.
Okay lets think a little bit more about the Webex portion of this.

Okay let' try to be a bit more specific regarding this question.
So I want anyone to be able to login but there's a specific user that upon logging in with that uer you gain admin access.
You can get the username from devtools maybe but the password is unkiwn to you.
Possibly hide somewhere in devtools or sscript or website that

okay so for a simpler version keeo it very easy to login as a user ad

1 Crypto Med


so there would be 2 separate codes, one would have a cipher that is rot with each bit being rotated a different number.
The other cipher would give you the number of bits that you need to sshift for the rot cipher.

ex kernel{hi_my_name_} > abihbhjlkhfryobv467 ( encrypted version)  
the second cipher would decode to something like 2_12_3_18_5 etc to give the bits it needs to be shifted by individually.
Keep all shifts under 26 and have one as 26 to help hint towards a rotation cipher.

For the decryption of the cipher that hold the bit shifts, maybe veigenier.

Maybe have the question name be something like the key is blank and then have the key to a veigeniere cipher 



Possible problems that may arise with this question:
2 ciphers may seem unnecessary
How difficult do i make the second decryption
What do i make the second encryption?
Maybe a hash but how would i give a hint towards that since people relatively new to ctfs wont have an idea about hash identifier
I could use it as a medium hard type question though. Maybe use one of the lesser known hashes alternatively.

More possible way to encrypt the second cipher:


Another crypto?
Ok so i lowkey suck at thinking of a Webex question so i'll think of another crypto question maybe.
I want this one to have more to do with making a script or using math 
I rlly only know the rsa basics so idk about that
Possibly a twist on the AES cipher
A simpler ine could deal with modular arithmetic

Okay so potentially all they get is a matrix and thats the sbox for the AES cipher and i wanna add one more twist somewhere
I like the idea of the aes cipher and all and switching the ssboxes
Involves minro brute forcing but that shouldn't be too hard to understand/solve.

Okayso the idea for this crypto question is an aes cipher with the sbox and sinv switched, and the bytes are shifted up by an integer k, this allows for easy bruteforcing since they only have to check 256 cases while also making them look for the issue themselves.
One problem that might arise here is that it might be too easy to gpt it and spot the changes
yeah this might be a dud.

Forensics:
Okay so now i want to do one question that focuses more on the data part of the forensics side.
I want a question that deals more in the hexdump portion
Initially have the file be in wrong format to serve as sort of a red herring, they might think all they have to do is change the header but that only shows u the image and the image can contain maybe a secondary hint such as that one image of the guy mining and giving up right before he hits gold 

I like the idea of having a hidden file in the hexdump of one file
Hidden file can contain the flag.

Okay so the first step can be to find the second img file hidden in the first one.
Don't wanna do another stego challenge so maybe the file can be a text file?
if it is an image it should deal with metadata or further analyzing the hexdump




OK COMPLETE ALTERNATIVE

Give a dd file which they have to mount, with deleted images and they have to use a tool like test disk to recover them, upon recovering the deleted image, the image seems to be a red herring but the second image is hidden in the metadata after the EOF of the first img.



1 Forensics/Stego 
Large zip file with maybe some 50-100 images each with a unique file name
There is only one image file that can be opened and on using maybe exiftool on it you take the authors name which points to one of the files which iss locked and you open it.  
Alternative is running binwalk on it and the dump includes the name of the file that needs to be opened.
Hide hints in meta data, like maybe the author name is the name of the file that needs to be examined.
All files are hiding data or whatever with steghide.
On identifying the correct file maybe password can be brute forced through rockyou?
Problem is that most new people wont be familiar with rockyous existence so that may be slightly difficult unless i change it to be a little harder then it can fit into a harder category.
So how would i now make the password of the steg file accessible?

Leading the alternative path maybe the binwalk also contains a separate image file that will contain the password to the steghide.
How could i hide the data in the image?
Well i could use change of exposure, brightness, filter.
Don't wanna use binwalk again that seems kind of lame.
Maybe make the go greyscale to be able to see the text.

Alternatively it could be a video/audio file
There i could have the password be hidden in morse code
It could be hidden in waveform
Maybe it would be in spectrogram.


Overall currently the main flow of the question flows like this:
Zip file contains 50-100 folders which are blocked by Steg and one which is not, this will be obvious that which one is openable.
Thi file will contain an image.
On Exiftooling that Image, you get the name of one of the other files in the zip file. That can be in a comment or the author etc
On binwalking it you get a Audio file which on analyzing will give you the password for it.
	Possible analysis include spectrogram, waveform, morse code, oscilloscope maybe, that thing pissed me off a lot.
Use the password to open the file which will have an image that will include the flag.


Change the exposure/filters of an image to get the data
Maybe spectogram

1 OSINT
So the endgame here is finding an "unsent" message about kernel on the unsent project or a similar website etc.
I need to figure out the layer that come before this.
Could start with a usesrname that would lead to a social media account but that's kinda generic, I want it to be more unique.
Where else could the account be that would be plausible enough to look but hidden enough that a simple google search would not show it up.
Ok so it'll start of simple, maybe have a username and have a hint being like, cryptohack is a great way to learn cryptography, especially modular arithmetic.
And one of the olution to the challenge can have a secondary hint, maybe a simple tinyurl/pastebin extension which can lead to a Wikipedia page, called kernel or whatever and in there you'll find a hidden, but obvious to the eyes once seen cipher.
Decoding this cipher will give you one lat ort of cryptic message like
"Oh no, i made a mistake, we have to unsend the project" 
Once the hint correlates to the unsent project in their head they can go there, simply search up the name kernel and find the flag.




Okay so I've finally hit what seems to be a roadblock. I have 4 possible questions but this possible 5th one iss giving me trouble. I'm just not sure what to do with it. I don't know enough about webdev or c to do webexx, rev, bine and all. I cant do another forensic, i alrdy made 2.
I dont rlly fuck with crypto well enough to make another decent question.

Ig at this point im looking at another oint question but i really fdont want to go in that direction, maybe i try another cyrpto question uing modular arithmetic but all of that eem eail gptable.
Might be worth looking more into rsa and trying to make an rsa question
Ig its time to read a bunch of crypto writeups.




Ok so i now have 1 Webex, 2 forensics, 1 osint, 1 crypto.
Questions aren't the hardest or the most unique but they're decent level questions mostly.

I'll spend some time tomorrow trying to come up with one extrahard/unique question that seems relatively hard.

On a side note i should do some dsa tonight, at least do linked lists and hashmaps it cant be that hard to lock in for a bit dumbass.


