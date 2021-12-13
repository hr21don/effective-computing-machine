# effective-computing-machine
In this tutorial, we look at GPU accelerated bruteforce! 

## Get started 
Crack your first md5 hash in 0 seconds! which is significantly faster then within a VM  or CPU alone.
 
## What is Hashcat?
Hashcat is a popular password cracking tool designed to brute force hashes, and is commonly used to crack passwords. It enables the cracking of a specific password in multiple ways, combined with versatility and speed.

## The explanation for non-technical users?

Hashcat turns readable data into a garbled state (this is a random string of fixed-length size). Hashes do not allow someone to decrypt data with a specific key, as standard encryption protocols allow. Hashcat uses precomputed dictionaries, rainbow tables and even brute-force approaches to find an effective and efficient way to crack passwords. 

## Why GPU over CPU?|| I would choose GPU... Heres why! 

GPUs are very good at parallelising mathematical operations, which is the basis of both computer graphics and cryptography. Typically, the GPU is programmed using either CUDA or OpenCL. The reason they're good for brute-force attacks is that they're orders of magnitude faster than a CPU for certain operations - they aren't intrinisically smarter.

The same operations can be done on a CPU, they just take longer.

## Hashcat Install

Head over to https://hashcat.net/hashcat/ and grab the file below:

```
| hashcat | binaries | v6.2.5 | 2021.11.21 | Download | PGP |
```
Extract hashcat-5.1.0

Enter the directory and create x2 text files as follows

```
hash.txt "Add hashes you would like to crack."  For e.g. "e99a18c428cb38d5f260853678922e03"
rockyou.txt "you should have cracked hashes append here." For e.g. "abc123"
```

## Testing

## References

https://security.stackexchange.com/questions/tagged/hashcat?tab=Votes 
Phil Lello(2021)https://security.stackexchange.com/questions/118147/how-are-gpus-used-in-brute-force-attacks. Date Accessed: 13/12/21
 
