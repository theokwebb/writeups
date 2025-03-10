## This is solutions  of a problem "Problem: Crypto#1 “-.-”" from TAMUctf 19

# Files
Attachment flag.txt

# Problem statement

### Our coworker Bob loves a good classical cipher. Unfortunately, he also loves to send everything encrypted with these ciphers. Can you go ahead and decrypt this for me?

# Problem solution

The attached file "Attachment flag.txt" looks like a sequence of "dah", "di", "dit", "-", " ": 

```dah-dah-dah-dah-dah dah-di-di-dah di-di-di-di-dit dah-dah-di-di-dit dah-dah-di-di-dit dah-dah-dah-dah-dah di-di-dah-dah-dah di-dah dah-di-di-di-dit dah-di-dah-dit di-di-di-di-dit dah-dah-dah-di-dit dah-dah-di-di-ditdi-di-di-di-dah di-di-di-di-dah dah-dah-di-di-dit di-di-di-di-dit di-dah-dah-dah-dah di-di-di-dah-dah dah-dah-dah-di-dit dah-di-di-di-dit di-di-di-di-dit di-di-di-dah-dah dah-dah-dah-di-dit dah-dah-di-di-dit di-dah-dah-dah-dah dah-di-di-di-dit dit dah-di-di-di-dit dah-di-dit di-di-di-di-dah dah-di-dit di-di-di-...```

When we try to google this sequence "dag-di-dit" we found that simbols is used for Morse code encryption, for example "A" is "di-dah", "B" is "dah-di-di-dit" etc. 

### A piece of theory. Usually the Morse code is consist of "dots" = "." (for now called "dit") and "dash" line = "-" (for now called "dah"). 

In our case "di" is ".", "dah" is "-", "dit" is "di" before space. Let's encode the attached file using this Morse code. The full decode message is: 

```
0X57702A6C5874475138653871696D4D59552A737646486B6A49742A5251264A705A766A6D2125254B446B667023594939666B346455346C423372546F5430505A516D4351454B5942345A4D762A21466B386C25626A716C504D6649476D612525467A4720676967656D7B433169634B5F636C31434B2D7930755F683476335F6D3449317D20757634767A4B5A7434796F6D694453684C6D38514546695574774A4049754F596658263875404769213125547176305663527A56216A217675757038426A644949714535772324255634555A4F595A327A37543235743726784C40574F373431305149
```

Due to the message starts from "0X" it might be Hexadecimal representation of the data. Using any decoder (for example https://gchq.github.io/CyberChef/) to decoder message text after "0X" we will get the next full message:

```Wp*lXtGQ8e8qimMYU*svFHkjIt*RQ&JpZvjm!%%KDkfp#YI9fk4dU4lB3rToT0PZQmCQEKYB4ZMv*!Fk8l%bjqlPMfIGma%%FzGgigem{C1icK_cl1CK-y0u_h4v3_m4I1} uv4vzKZt4yomiDShLm8QEFiUtwJ@IuOYfX&8u@Gi!1%Tqv0VcRzV!j!vuup8BjdIIqE5w#$%V4UZOYZ2z7T25t7&xL@WO7410QI```

### So, the flag is here: 
```gigem{C1icK_cl1CK-y0u_h4v3_m4I1}```
