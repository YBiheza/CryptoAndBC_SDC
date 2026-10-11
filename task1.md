# HOMETASK 1
#### steps:

## **1. Identify the correct symmetric key:**

### Given three 128-bit keys in HEX and the SHA-256 hash of the correct key, find the key that matches the provided hash.

Symmetric keys. Here they are in HEX

- 174f2d1a16fde76dee842c90f126aab9

- 95ce2d1a16fde76dee842c90f126aab9

- 95ce2d1a1691906dee842c90f126aab9

SHA-256 hash of the correct key. Hash is below in HEX

- 26249de240f5479bee4b2b20c25bed94cd76d8c7b95708ce39a8f603545b1b88

## **SOLUTION**

I get the SHA-256 hash of the each key using the [source](https://emn178.github.io/online-tools/sha256.html)
So, 
- for - 174f2d1a16fde76dee842c90f126aab9 the hash is a6321ee00ae07403b91d97c796a10e7ddc7d861f5b1e8b41344d8833939745f4 (not equal to the task)

- for 95ce2d1a16fde76dee842c90f126aab9 the hash is  26249de240f5479bee4b2b20c25bed94cd76d8c7b95708ce39a8f603545b1b88 (!RIGHT! EQUAL TO THE TASK)

- for 95ce2d1a1691906dee842c90f126aab9 the hash is 87b6ba62cde0dd4c765c1ddbde1b53a0896a517431af4f3732c87ce966dc4d7f (not equal to the task)

So, the right answer is the 2nd key 95ce2d1a16fde76dee842c90f126aab9

## **TASK**

## **2. Decrypt the AES-128 encrypted message:**

### Use the correct symmetric key to decrypt the given message in HEX, with AES configured in CBC mode and the provided initialization vector in HEX.

- AES encrypted message: d818117c21fa8ca1316a6698f0dba8eb7fbca565883755231973a6cd527d795c3a604e1eb868fb625faf8811f3102c0e

- CBC initialization vector: 8dddd8975a61ff0ec359130f28fa218c

## **SOLUTION**

Using the [source](http://aes.online-domain-tools.com/) and right options I decrypt a message and get the answer:
- 000000000000001000000020
or:
43	6f	6e	73	65	6e	73	75	73	20	6b	65	65	70	73	20
74	68	65	20	6c	65	64	67	65	72	20	68	6f	6e	65	73
74	0f	0f	0f	0f	0f	0f	0f	0f	0f	0f	0f	0f	0f	0f	0f
or:
C	o	n	s	e	n	s	u	s		k	e	e	p	s	
t	h	e		l	e	d	g	e	r		h	o	n	e	s
t	.	.	.	.	.	.	.	.	.	.	.	.	.	.	.
- (Consensus keeps the ledger honest.)

[Link to the website](http://aes.online-domain-tools.com/link/3328fdfgjcMkWobwXx/)

## **TASK** 

## **3.Generate an asymmetric Elliptic Curve key-pair:**

### - Generate a key-pair using any Elliptic Curve parameters, either in node.js/java/etc or online.

## **Create a digital signature:**

### Using the asymmetric key-pair, generate a digital signature over the original decrypted plaintext message.

## SOLUTION

Using the [source](https://8gwifi.org/ecsignverify.jsp) I generate 2 keys - public and private
- public: -----BEGIN PUBLIC KEY-----
MFYwEAYHKoZIzj0CAQYFK4EEAAoDQgAEC6fE8FDybXYwEJw0zT1d8lE7Qnd4Rjf+
gKZMS+PFIyStEtZJ2rALQFEicqpO/zcfOcNCvQPqER6elYfoAJ8pqA==
-----END PUBLIC KEY-----

- private: -----BEGIN EC PRIVATE KEY-----
MHQCAQEEIOs+WWVRxtBv5T0siVtaTO2jMo0IvuGjlKYDtBO6lczuoAcGBSuBBAAK
oUQDQgAEC6fE8FDybXYwEJw0zT1d8lE7Qnd4Rjf+gKZMS+PFIyStEtZJ2rALQFEi
cqpO/zcfOcNCvQPqER6elYfoAJ8pqA==
-----END EC PRIVATE KEY-----

I used the secp256k1 elliptic curve which is used for bitcoin e.g.

And then I used the message from the 1st task to create the signature:

result: MEUCIA61Rqo2auuR9nF+e3Nl4KJx7+NuYcS6H+ktwQkyGMRTAiEA4CB+RZjd/vfNMM/2NTL8Xnw0oCbHFFn6oHAP58FKgDM=