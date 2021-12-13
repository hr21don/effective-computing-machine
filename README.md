# effective-computing-machine
In this tutorial, we look at GPU accelerated bruteforce! 

**********************************************************************
## Get started 
Crack your first md5 hash in 0 seconds! which is significantly faster then within a VM  or CPU alone.
 
## What is Hashcat?
Hashcat is a popular password cracking tool designed to brute force hashes, and is commonly used to crack passwords. It enables the cracking of a specific password in multiple ways, combined with versatility and speed.

## The explanation for non-technical users?

Hashcat turns readable data into a garbled state (this is a random string of fixed-length size). Hashes do not allow someone to decrypt data with a specific key, as standard encryption protocols allow. Hashcat uses precomputed dictionaries, rainbow tables and even brute-force approaches to find an effective and efficient way to crack passwords. 

## Why GPU over CPU?|| I would choose GPU... Heres why! 

GPUs are very good at parallelising mathematical operations, which is the basis of both computer graphics and cryptography. Typically, the GPU is programmed using either CUDA or OpenCL. The reason they're good for brute-force attacks is that they're orders of magnitude faster than a CPU for certain operations - they aren't intrinisically smarter.

The same operations can be done on a CPU, they just take longer.

**********************************************************************

## Hashcat Install

Head over to https://hashcat.net/hashcat/ and download the file 'binaries' to your downloads directory.

```
| hashcat | binaries | v6.2.5 | 2021.11.21 | Download | PGP |
```
## Extract hashcat-5.1.0

## Enter the directory and create x2 text files as follows

```
1. hash.txt "Add hashes you would like to crack."  For e.g. "e99a18c428cb38d5f260853678922e03"
2. rockyou.txt "you should have cracked hashes append here." For e.g. "abc123"
```

## Testing

Start by generating an md5 hash using this online generator at https://www.md5hashgenerator.com/. 

```
1. string: qwerty123
2. md5 hash: 3fc0a7acf087f549ac2b266baf94b8b1
```

For instance, here a free hash for qwerty.

<img width="523" alt="Capture" src="https://user-images.githubusercontent.com/91548582/145874131-1c4b5990-eae5-459a-b1cc-867317f76ff0.PNG">

Place the generated hash  into hash.txt and save.

## Open CMD as Adminstrator

![cpa_2](https://user-images.githubusercontent.com/91548582/145874630-c5009ef0-8d0b-44de-9162-8cdae152d6cb.png)

**********************************************************************
##  Navigate to Hashcat directory

Use the command provided below:

```
hashcat64.exe --help
```

Here is what the console should display when running hashcat:

<img width="468" alt="Capture" src="https://user-images.githubusercontent.com/91548582/145875145-c5972f61-685e-4abd-b3a9-85bc34aa6509.PNG">

**********************************************************************

## Bruteforce attacking

Run the command below and execute!

```
hashcat64.exe -m0 -a3 -o rockyou.txt hash.txt
```

## What are we executing?

To put it simply. After, a few seconds your MD5 should be cracked! 

```
-m0 = MD5 hashes -a5 = Attack type: Brute forcing -o = output file
```

## Cracking in 0 Seconds

In this example, the hash that was getting tested belonged to the password abc123. (The user of this password needs to update this weak password)

```
e99a18c428cb38d5f260853678922e03:abc123
```
<img width="306" alt="Capture" src="https://user-images.githubusercontent.com/91548582/145876881-12e5ae5e-98a4-475e-96d6-88393aa4543d.PNG">


## References

https://security.stackexchange.com/questions/tagged/hashcat?tab=Votes 
Phil Lello(2021)https://security.stackexchange.com/questions/118147/how-are-gpus-used-in-brute-force-attacks. Date Accessed: 13/12/21
 
