##This a tutorial adapted from Edward Snowden's video to Glenn Greenwald about how to create and use a PGP key.

On December 1, 2012, Glenn Greenwald received his first communication with Edward Snowden. This communication was anonymous, and in the form of an email that simply urged Greenwald to consdier using a PGP encryption so that the anonymous contact could convey some vitally important information. 

In Greenwald's own words, a PGP encryption is a program that "wraps every email in a protective shield, which is a cod ecomposed of hundreds, or even thousands, of random numbers and case-sensitive letters." He adds, "People who most fear having their communications monitored, such as intelligence operatives, spies, human rights activists, and hackers, trust this form of encryption to protect their messages." 

Still, Greenwald was not enticed by the anonymous Snowden's email, nor did the nudge towards more secure methods of contact come as a surprise. By December of 2012, Greenwald had long been writing for Wikileaks and for whistleblowers as well as for a few individuals inside the US national security establishment. As such he was too busy to take on a story propsed by an anonymous source unwilling to give up even the smallest hint of information without a drastically enhanced medium of communcation. So Greenwald ingnored Snowden's first attempt at contact. 

After severals more attempts by Snowden to get into contact anonymously and Greenwald's inaction, Snowden increased his efforts. He put togeter a video for Greenwald called PGP for Journalists. The video provides a very clear, step-by-step guide to installing GPG on a Windows computer, narrated by Snowden himself. 

Greenwald ultimately ignored this attempt at communication as well -- it wasn't until several months later that Greenwald jumped into action to begin reporting the Snowden story. However, the video can now be found on youtube and, despite its fewer than 4,000 views, is actually a very helpful tutorial. A fun bonus is Snowden's very charming and particular sense of humor. The following is a clarified and annotated transcription of Snowden's video.

Please keep in mind: this is a tutorial for Windows users. Sierra Eckert, another contributor to the Minimally Viable Digital Citizen project, has provded a tutorial for Mac users right here: https://github.com/xpmethod/mvdc/blob/master/cryptography-tutorial.md. 

##A brief overview
"Information has to transit the internet somehow, which is an untrusted environmnt, particularly for email, which is unencrypted by default. Any router you cross could be monitored by an intelligence agency..., but so could any endpoints on the way there, a mail server or a service providor such as gmail. If the journalist [who you are trying to contact] uses a webmail service, personally or that has been provisioned by their company..., that email can always be retrieved later on via subpoena or some other mechanism legal or illegal instead of catching [the email] [in transit.] 

"The solution to that is to actually encrypt the message. One of the problems with encryption typically is that it requires a shared secret - a key or password that goes between the journalist or the source but if the source sends an encrypted file across the internet to his journalist, that says "hey here's the encrypted file, the password is cheescake," the internet's going to know the password was cheesecake. 

"Public key encryption such as gpg allows the journalist to publish a key that anyone can have based on the design of the algorithm and it doesn't provide any advantage to the adversary because the knowledge of that will allow him to encrypt a message specifically to the journalist. He can send his message... across the internet along with a copy of his public key so the journalist can respond. This has never been broken... over the past 20 years it's had an unbroken record of security success. That's a solid measure of security and it's reasonable to rely on that.

###
