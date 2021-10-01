---
layout: default
---

# What I would have loved to know about Homomorphic Encryption before starting my Ph.D. (Part 1)
It is already almost two years since I embarked into the exciting world of Cryptography, and concretely, in Homomorphic Encryption (HE). While it is cutting-edge technology, my beginnings in this world were not so gentle. There are lots of background mathematical concepts needed to understand the gears of HE. After some experience dealing with it, I would like to try and simplify this complex knowledge so that a younger me could have benefited from it. This first post aims at more general knowledge with not many scientific details.

## Where does Homomorphic Encryption come from?

Before getting to the details, I would like to understand why we are in our current position and the changes from classical cryptography to modern techniques. Classical cryptography was envisioned for war, concretely, in the years of the Cold War. Contendents had the means to send information, but the information needed not to fall into unauthorized hands. 

For that classical cryptographic model elaborated tools against three different threats (confidentiality, integrity, and non-repudiation). In short, if someone sends you a message, you can acknowledge that nobody saw or modified the message and who sent the message.  

In all these cases, the common factor is finding the adversary on the communication channel. Contendents were countries, and individuals within the same band were assumed to be trustworthy. In the modern world, we are no longer at war (or are we?). Nowadays, information is power, and often, individuals are forced to release it. Nowadays, many big companies such as Google, Facebook, or Twitter, have based their business models on operating with the data users exchange in their applications. Most of these companies argue that treating this data is based on giving services to users, but this is often at the cost of privacy. 

Modern cryptographic mechanisms aim at solving more complex problems than just hiding information. Information is valuable and, we strive to process it without infringing privacy.  Homomorphic encryption enables confidentiality of data, but it also permits privacy-preserving processing. As we will see, privacy-preserving processing can secure many processes that, up to recently, involved some degree of private information release. 

## My extension of Craig Gentry's  Homomorphic Encryption intuition

Let's deep down into what private processing is with an extended analogy taken from Craig Gentry. Let's consider classical encryption as a safe with a password. Someone could open the safe and put some object inside under the password. Only someone else having the password would be able to open it. Homomorphic encryption goes one step beyond. It modifies the safe to have some gloves attached on the sides that permit touching what is inside. With the pair of gloves, someone could touch what is on the inside; displace it inside the safe; or, even if it is a malleable material to craft something from it. However, someone can't extract the content with the gloves, nor (given the thickness of the gloves) understand what is inside. 

Translating the analogy to reality is relatively straightforward. Both classical and homomorphic encryption are safes, and once there is something inside, we consider those ciphertexts. However, Homomorphic Encryption safes provide gloves to manipulate the inside (i.e., the routines to operate over the ciphertexts).

![image](https://user-images.githubusercontent.com/36102221/135646412-8bb26972-bbd8-43a5-a5cb-a7d2ce36a917.png)

## Why is it so valuable?

The idea of privacy-preserving processing has long resounded in the cryptography world as one of the holy grails. In our current computing paradigm, cloud computing has become a dominant force and, it is more and more necessary to provide mechanisms to ensure the privacy of information uploaded to the cloud. In a way, Homomorphic Encryption. strives to make cloud computing as private as using your laptop for the data you store. Not only is it enables privacy-preserving processing, but also, as of 2021, the lattice problems on which Homomorphic Encryption. is based are considered quantum secure (i.e., emerging as post-quantum secure cryptography).

## Where could HE be useful?

Alice (a rich woman) comes to Bob (a business expert) for help with her tax declaration. However, Alice does not want Bob to know her account balance since this could cause an increase in the service price. Bob and Alice decide to use Homomorphic Encryption. Alice encrypts the information about his funds and gives Bob the data. Bob can operate over the data. Bob computes a tax declaration based on the encrypted data. Finally, Alice gets back a result and decrypts it, and gets the resulting correct tax declaration. During the process, Bob did the tax declaration without learning anything about Alice's balance.

In the same way, we could apply HE to medicine, satellite communication and positioning systems, insurance calculations, and many other protocols. All while guaranteeing that information can be kept secret. 

Guaranteeing privacy could enhance having fair treatment against some unequal situations. In the following articles, I will be giving more details about the insights of Homomorphic Encryption.
