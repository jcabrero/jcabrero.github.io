---
layout: default
---

# What I would have loved to know about HE before starting my Ph.D. (Part 1)
It is already almost two years since I embarked into the exciting world of Cryptography, and concretely, in Homomorphic Encryption (HE). While it is cutting-edge technology, my beginnings in this world were not gentle (at all). There are lots of background mathematical concepts needed to understand the gears of HE. After some experience dealing with it, I would like to try and simplify this complex knowledge so that a younger me could have profited from it. This first post aims at more general knowledge, and not many scientific details are provided.

## Where does Homomorphic Encryption come from?

Before getting to the details, I would like to understand why we are in our current position and the changes from classical cryptography to modern techniques. Classical cryptography was envisioned for war, concretely, in the years of the Cold War. Contendents had the means to send information, but the information needed not to fall into unauthorized hands. 

For that, the classical cryptographic model elaborated mechanisms to solve three needs. First, the information contained in a message should only be revealed to whom owners authorized (i.e., confidentiality). Second, the information on a message should be kept from unauthorized modifications (i.e., integrity). Third, providing means to ensure authenticity and ownership of information (i.e., non-repudiation). 

In all these cases, the common factor is finding the adversary on the communication channel. Contendents were countries, and individuals within the same band were assumed to be trustworthy. In the modern world, we are no longer at war (or are we?). Nowadays, information is power, and often, individuals are forced to release it. Modern cryptographic mechanisms aim at solving more complex problems than just hiding information, for example, processing information that we cannot see. Homomorphic encryption enables confidentiality and access control to information, but it also permits privacy-preserving processing.

## My extension of Craig Gentry's  Homomorphic Encryption intuition

Let's deep down into what private processing is with an extended analogy taken from Craig Gentry. Let's consider classical encryption as a safe with a password. Someone could open the safe and put some object inside under the password. Only someone else having the password would be able to open it. Homomorphic encryption goes one step beyond. It modifies the safe to have some security gloves towards the inside. With this pair of gloves, someone could touch what is on the inside, move it on the safe, or, even if it is a malleable material craft something from it. However, someone can't open the box and extract its content, nor (given the thickness of the gloves) understand what is inside. 

Translating the analogy to reality is relatively straightforward. Both classical and homomorphic encryption are safes, and once there is something inside, we consider those ciphertexts. However, Homomorphic Encryption safes provide gloves to manipulate the inside (i.e., the routines to operate over the ciphertexts).

## Why is it so valuable?

The idea of privacy-preserving processing has long resounded in the cryptography world as one of the holy grails. In our current computing paradigm, cloud computing has become a dominant force and, it is more and more necessary to provide mechanisms to ensure the privacy of objects. In a way, HE enables that using cloud computing becomes as private as using your laptop for the data you store. Not only is it enables privacy-preserving processing, but also, as of 2021, the lattice problems on which HE is based are considered quantum secure (i.e., emerging as post-quantum secure cryptography).

## What is HE? 

At this point, I would like to start getting into how HE works, what it allows to do, and (more importantly) its limitations. With this section, I would also like to overview the complexity of dealing with this kind of cryptography and writing HE code.  

HE security is based on the Learning with Errors (LWE) lattice problem. LWE is based on complexity to solve a system of linear equations with noise. One could relate it to usual systems as the ones explored in high school:
$ x + y = 3
2x - y = 3$
While this problem is trivial to solve, it becomes much more difficult if we add noise. If the coefficients of x and y (i.e., the values that accompany x (1, 2) and y (1, - 1)) are changed by a bit, then the solution may disappear or change completely. While the system may still have a solution, it is unlikely to find the correct one. 

## Is it feasible 

The first time a programmer has to deal with HE code, it is a traumatic experience. Modern programming languages have elaborated a handful of computing structures that structure the way we think code. However, HE significantly limits the amount of directives one can use. For example, arrays are present in HE, but the directives to manipulate them are very limited. Furthermore, most HE schemes allow only for limited computation, that is, after s  Most programmers and computer scientistswe are used to several directives in our code (e.g., arrays, matrices or arbitrary dimension and arbitrary long code).  common the use of arrays, matrices of arbitrary dimensions. Furthermore, it is typical to enable  even  

 




