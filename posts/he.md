---
layout: default
---

# What I would have loved to know about Homomorphic Encryption before starting my Ph.D. (Part 1)
It is already almost two years since I embarked into the exciting world of Cryptography, and concretely, in Homomorphic Encryption (HE). While it is cutting-edge technology, my beginnings in this world were not so gentle. There are lots of background mathematical concepts needed to understand the gears of HE. After some experience dealing with it, I would like to try and simplify this complex knowledge so that a younger me could have benefited from it. This first post aims at more general knowledge, and not many scientific details are provided.

## Where does Homomorphic Encryption come from?

Before getting to the details, I would like to understand why we are in our current position and the changes from classical cryptography to modern techniques. Classical cryptography was envisioned for war, concretely, in the years of the Cold War. Contendents had the means to send information, but the information needed not to fall into unauthorized hands. 

For that, the classical cryptographic model elaborated tools against three different threats. First, the information contained in a message should only be revealed to whom owners authorized (i.e., confidentiality). Second, the information on a message should not be modified by unauthorized parties (i.e., integrity). Third, providing means to ensure authenticity and ownership of information (i.e., non-repudiation). 

In all these cases, the common factor is finding the adversary on the communication channel. Contendents were countries, and individuals within the same band were assumed to be trustworthy. In the modern world, we are no longer at war (or are we?). Nowadays, information is power, and often, individuals are forced to release it. Nowadays, many big companies such as Google, Facebook, or Twitter, have based their business models on operating with the data users exchange in their applications. Most of these companies argue that treating this data is based on giving services to users, but this is often at the cost of privacy. 

Modern cryptographic mechanisms aim at solving more complex problems than just hiding information. Information is useful, and like that, we strive for the information to be processed without infringing privacy.  Homomorphic encryption enables confidentiality and access control to information, but it also permits privacy-preserving processing. As we will see, this private processing can enhance many processes, that up to recently, required a privacy infringement. 

## My extension of Craig Gentry's  Homomorphic Encryption intuition

Let's deep down into what private processing is with an extended analogy taken from Craig Gentry. Let's consider classical encryption as a safe with a password. Someone could open the safe and put some object inside under the password. Only someone else having the password would be able to open it. Homomorphic encryption goes one step beyond. It modifies the safe to have some gloves attached on the sides that permit touching what is inside. With this pair of gloves, someone could touch what is on the inside, displace it inside the safe, or, even if it is a malleable material to craft something from it. However, someone can't open the box and extract its content, nor (given the thickness of the gloves) understand what is inside. 

Translating the analogy to reality is relatively straightforward. Both classical and homomorphic encryption are safes, and once there is something inside, we consider those ciphertexts. However, Homomorphic Encryption safes provide gloves to manipulate the inside (i.e., the routines to operate over the ciphertexts).


## Why is it so valuable?

The idea of privacy-preserving processing has long resounded in the cryptography world as one of the holy grails. In our current computing paradigm, cloud computing has become a dominant force and, it is more and more necessary to provide mechanisms to ensure the privacy of information uploaded to the cloud. In a way, Homomorphic Encryption. strives to make cloud computing as private as using your laptop for the data you store. Not only is it enables privacy-preserving processing, but also, as of 2021, the lattice problems on which Homomorphic Encryption. is based are considered quantum secure (i.e., emerging as post-quantum secure cryptography).


## Where could HE be useful?

Alice (a rich woman) comes to Bob (a business expert) for help with her tax declaration. However, Alice does not want Bob to know her account balance, since this could cause an increase in the service price. Bob and Alice decide to use Homomorphic Encryption. Alice encrypts the information about his funds and gives Bob the data. Bob is able to operate over the data. Bob computes a tax declaration based on the encrypted data. Finally, Alice gets back a result and decrypts it, and gets the resulting correct tax declaration. During the process, Bob did the tax declaration without learning anything about Alice's balance.

In the same way, we could apply HE to medicine, satellite communication and positioning systems, insurance calculations and many other protocols. All while guaranteeing that information can be kept secret. 

Guaranteeing privacy could enhance having a fair treatment against some unequal situations. While this article has not included substantially technical information, I hope it can lead you to read the following one, where I will be giving more details about the insights of Homomorphic Encryption.


## What is HE? 

After understanding some use casesAt this point, I would like to start getting into how HE works, what it allows to do, and (more importantly) its limitations. With this section, I would also like to overview the complexity of dealing with this kind of cryptography and writing HE code.  

HE security is based on the Learning with Errors (LWE) lattice problem. LWE is based on complexity to solve a system of linear equations with noise. One could relate it to usual systems as the ones explored in high school:
$ x + y = 3
2x - y = 3$
While this problem is trivial to solve, it becomes much more difficult if we add noise. If the coefficients of x and y (i.e., the values that accompany x (1, 2) and y (1, - 1)) are changed by a bit, then the solution may disappear or change completely. While the system may still have a solution, it is unlikely to find the correct one. 

## Is it feasible 

The first time a programmer has to deal with HE code, it is a traumatic experience. Modern programming languages have elaborated a handful of computing structures that structure the way we think code. However, HE significantly limits the number of directives one can use. For example, arrays are present in HE, but the directives to manipulate them are very limited. Furthermore, most HE schemes allow only for limited computation, that is, afters  Most programmers and computer scientists we are used to several directives in our code (e.g., arrays, matrices or arbitrary dimension and arbitrary long code).  common the use of arrays, matrices of arbitrary dimensions. Furthermore, it is typical to enable  even  

 




