##This a tutorial adapted from Edward Snowden's video to Glenn Greenwald about how to create and use a PGP key.

On December 1, 2012, Glenn Greenwald received his first communication with Edward Snowden. This communication was anonymous, and in the form of an email that simply urged Greenwald to consider using PGP encryption so that Snowden could contact could contact him more directly. 

In Greenwald's own words, PGP encryption is a program that "wraps every email in a protective shield, which is a code composed of hundreds, or even thousands, of random numbers and case-sensitive letters." He adds, "People who most fear having their communications monitored, such as intelligence operatives, spies, human rights activists, and hackers, trust this form of encryption to protect their messages." 

Still, Greenwald was not enticed by the anonymous email, nor did the nudge towards more secure methods of contact come as a surprise. By December of 2012, Greenwald had long been writing for Wikileaks and for whistleblowers as well as for a few individuals inside the US national security establishment. As such he was too busy to take on a story proposed by an anonymous source unwilling to give up even the smallest hint of information without a drastically enhanced medium of communcation. So Greenwald ingnored Snowden's first attempt at contact. 

After severals more attempts by Snowden to get into contact anonymously and Greenwald's prolonged inaction, Snowden increased his efforts. He put togeter a video for Greenwald called PGP for Journalists. The video provides a very clear, step-by-step guide to installing GPG on a Windows computer, narrated by Snowden himself. 

Greenwald ultimately ignored this attempt at communication as well -- it wasn't until several months later that Greenwald jumped into action to begin reporting the story that Snowden brought to him. However, the video can now be found on youtube and, despite its fewer-than-4,000 views, is actually a very helpful tutorial. A fun bonus is Snowden's very charming and particular sense of humor. The following is a clarified and annotated transcription of Snowden's video.


##A brief overview
"Information has to transit the internet somehow, which is an untrusted environment, particularly for email, which is unencrypted by default. Any router you cross could be monitored by an intelligence agency..., but so could any endpoints on the way there, a mail server or a service providor such as gmail. If the journalist [who you are trying to contact] uses a webmail service, personally or that has been provisioned by their company..., that email can always be retrieved later on subpoena or some other mechanism legal or illegal instead of catching [the email] [in transit.] 

"The solution to that is to actually encrypt the message. One of the problems with encryption typically is that it requires a shared secret - a key or password that goes between the journalist or the source. But if the source sends an encrypted file across the internet to his journalist, that says "hey here's the encrypted file, the password is cheescake," the internet's going to know the password was cheesecake. 

"Public key encryption such as gpg allows the journalist to publish a key that anyone can have based on the design of the algorithm and it doesn't provide any advantage to the adversary because the knowledge of that will allow him to encrypt a message specifically to the journalist. He can send his message... across the internet along with a copy of his public key so the journalist can respond. This has never been broken... over the past 20 years it's had an unbroken record of security success. That's a solid measure of security and it's reasonable to rely on that."

###Step 1
"The first thing that we're going to do is go to GPG4win.org. Download the latest version by clicking the download button." 

###Step 2
[When clicking through the installer, you will come to a screen that tells you to 'check the components you want to install and uncheck the components you don't want to install.' Make sure you have checked BOTH GPA AND CLEOPATRA]

###Step 3
"When installation is complete, you will have two choices [in your windows menu], Cleopatra and GPA. Use GPA. It's better in almost every way -- its older." 

###Step 4
[When you launch the GPA application] "a window that says "key manager" will come up. This is your interface. The first thing you want to do as a new user is go to preferences and click the advanced mode. If you don't click this -- and it's not enabled by default -- you won't be able to choose your key length. You want it stronger than the default length." 

###Step 5
"Then go to keys, generate new key, chose 3072 instead of 2048 [for key size.] Enter your information. This will be public. It's important to have accurate information if you're a journalist." 

###Step 6
"Then you're going to have to create a password. The only thing that protects the security of the information are the passphrase and the strength of the certificate itself. The certificate won't be broken, the passphrase could be broken, using a dictionary attack or a brute force attack... so use something strong. Pick a memorable quote that you don't have to write down, that's meaningful to you and that no one else knows, like 'Margaret Thatcher is %110 sexy' that has special characters like the percent sign, numbers, upper and lowercase letters, and that's very long. You want a password that's more than 20 characters, minimum." 

###Step 7
"SO our key is finished generating... now we need to share it. We send [the keys] to key servers, that's where anyone can get public keys. Click server --> send keys: http://keys.gnupg.net is a good one. Now people can search for keys via your name, email [or] address." 

###Step 8
"Let's take a quick look at publishing, and getting keys from people we've never had contact with. pgp.mit.edu is a public key server -- anyone can put their keys up there for free. You can search by emails... you want to use exact matches."

###Step 9 
[When you have successfully found someone's public key, by searching the server using either their name or email,] "You copy the key [which looks like a long block of gibberish), go to GPA [your GPG client], "hit control V for pasting and it'll import the key into the key ring. Now they're there, you can encrypt emails to them however you like." 

 ###Step 10
"Now that we have somebody's key, we can compose a message. Please pause the screen and read this note, this is critically important, webmail providers like gmail and some other clients will compromise your privacy." 

[At this point in the video, the screen shows a note that Snowden wrote in TextEdit. The note reads as follows:]

	"DO NOT COMPOSE YOUR EMAILS IN AN INTERNET BROWSER. Webmail clients like Gmail will 'autosave' a draft copy 
	of your sensitive email BEFORE YOU HAVE HAD A CHANCE TO ENCRYPT IT. Only put the completed CYPHERTEXT (that 
	is, the encrypted block of gibberish) into webmail. That way, the email provider cannot access the plaintext 
	of your message." 

###Step 11
"So this is what we use: we use something like notebad, copy the text [that you wrote, i.e., the body of your email] and then we open up clipboard in the privacy agent [the GPA interface that you've been using all along.] This is where you put your text, you can also draft things in here, then you just click encrypt. You click which key you want to send it to, and then email it to [the address associate with that key.] This will allow us to decrypt our own text: by selecting both people as recipients, the [journalist] and ourselves. You have to enter your passphrase, and with that the messaeg will become enrypted. If anyone intercepts this over the wire when it's being emailed it's useless to them... without the recipient's private key." 

###Step 12
"[If we've received an enrypted message] we copy that into the clipboard, you click decrypt, put in your private passphrase, and once you've got that it's going to decrypt it." 

Please keep in mind: this is a tutorial for Windows users. Sierra Eckert, another contributor to the Minimally Viable Digital Citizen project, has provded a great tutorial for Mac users right here: https://github.com/xpmethod/mvdc/blob/master/cryptography-tutorial.md

Sources Cited: 

[1] Greenwald, Glenn. "Contact." No Place to Hide: Edward Snowden, the NSA, and the U.S. Surveillance State. New York City: Metropolitan, 2014. Print.

[2] PGP for Journalists. Youtube, 2012. Film.

