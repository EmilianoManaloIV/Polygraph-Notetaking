___
**Cryptography**
* Using mathematical equations to transform data into a form which cannot be viewed normally; data not transformed but encrypted.
* It is used to **hide** data but not **modify** it.
* We use it in mission critical data that is very sensitive and shouldn't be accessible to anyone in the public.
	* **Encryption:** A process that takes data and creates the **ciphertext** using a **key** that is unreadable under normal circumstances.
	* **Decryption:** Reverse of encryption, transfer **ciphertext** into readable usable text using a **key**.
___
**What Does Cryptography Do?**
* It follows the CIA triad
	* There is proof of someone is sending the data and one receiving the data.
___
**Essential Cryptography Terminology**
* **Plaintext:** files or messages that aren't modified into a ciphertext 
* **Encrypt:** Key and cryptographic algorithm used to create ciphertext
* **Key:** Programs that cryptographic algorithm.
* **Decrypt:** Takes the key and takes the ciphertext into plaintext.
___
**Cryptography**
* **Hashing (one way):** Changing the nature of data so that it doesn't return the same way, one way cryptography.
* **Two Way:** Can be encrypted and decrypted
___
**Hashing**
* Using a mathematical function that takes an input then creates a certain length output, this is one way and can't retrieve it back once hashed.
* There is a slight change in the value and if you use the same input, you will get the same output.
* Often used in data integrity and password storage.
	* SHA-266
	* SHA-3
___
**Encryption**
* **Symmetric Encryption:** One secret key that is used both to encrypt and decrypt
* **Asymmetric Encryption:** Two keys, where one key encrypts and another key decrypts: **public** and **private** key.
___
**Symmetric Encryption**
* Used to encrypt and decrypt the message using the same Key.
* Pros and Cons
	* Pros: Fast and efficient
	* Cons: Transmission of the key is a huge risk, not way to be scalable, integrity is threatened.
* Encryption type is based on how important the data is
___
**Block Ciphers**
* Block: Taking the message and breaking it into even pieces, and we apply the same key for every single block. Isolate and take each piece to be encrypted.
* If the block has the same input, then you will get the same output.
* Block size is what determines the algorithm:
	* DES: Plaintext (64), Ciphertext (64), Key Size (128)
	* Triple DES: Plaintext (64), Ciphertext (64), Key Size (128)
	* AES: Plaintext (56), Ciphertext (112-168), Key Size (128,192, 256)
___
**DES**
* Data Encryption Algorithm which was used at a large scale. 
* 56-bit key is small and for modern processors its not hard to find.
___
**Triple DES**
* Repeats the DES algorithm three times, not as discoverable as normal DES.
* Extremely slow and inefficient to utilize on normal machines.
___
**AES**
* Known as Rijndael and often replaces the DES family in regards to performance and efficiency
___
**Capstone Project Review**
* We have enough information and data to finish both Capstone 1 & 2, you should be able to start now. 
* **FINISH BOTH CAPSTONES AS SOON AS POSSIBLE (ALOT TIME NEEDED FOR COMPLETION)**
___
**Block Cipher Modes**
* An algorithm that works on a fixed-size of data, however, can adapt to smaller modes of text and focuses on the key itself.
* How to divide the data, handle each block, link them and interlegibility
* **ECB:** A codebook that assigns plaintext into a ciphertext, the blocks are then strung together. 
	* Can someone use pattern analysis to get data that can make the data accessible.
* **CTR:** A counter and block cipher are used in tandem to create a **keystream** that provides a unique output for each input.
	* Each block is independent from one another, so that pattern recognition is not possible and makes it difficult to breakdown.
___
**Symmetric Encrypt**
* **Stream Ciphers (RC4)**
	* One byte of the time is encrypted, every key is unique and expensive to scale since it is in series and not parallel.
	* Constant encryption as data is flowing in and being a given a unique key which is more secure. 
___
**Block Vs Stream**
* Fixed block vs constant data
* Slower for data streams vs continues data
* Large data vs real time communication
___
**Asymmetric Encryption**
* It uses two separate keys (public & private keys), public is known, private is hidden.
* Public and private key are mathematically related to one another
* An individual will have her own Private and public key, but only can utilize another party's **PUBLIC** key. 
* You don't need to transmit keys.
* There is instances where its flipped where you encrypt with a private key first before using another end-user's public key.
___
**Key Creation**
* A random number should be a flat curve, there is no deduction from one another to another, number cannot be predicted.
* True Random (Number found in nature).
* Pseudorandom (Random enough for most use-cases).
* Requirements:
	* Create key value pairs
	* Can be bidirectional in nature
	* Encrypted perfectly
	* Easy on sender and receiver
	* Cannot be easily deduced which is private or public keys
___
**Asymmetric Pros And Cons**
* Its scalable, fixes key exchange problem, digital signature availability.
* However, can be slow it regards to time.
___
**Modular Arithmetic**
* Takes the remainder of the divisible operator, think days of the week or a clock.
___
**RSA (Rivest-Shamir-Alderman)**
1. Key Encryption
2. Encryption
3. Decryption
* Difficulty of factoring large prime numbers, easy to multiply, but hard to get the factors when multiplied. Make the private key harder.
* **N** represents the connection between the private and public key.
	* Look in slides on "RSA: EXAMPLE"
	* Read up on mathematical encryption and decryption.
___
**Authentication**
* Ensures the identity of the one receiving data and maintains the integrity of the data (is this person true? Is it who I'm send it to?) confidentiality.
* **Encryption:** Maintains confidentiality and integrity. 
___
**Hashing**
* One way mathematical functions that creates a has value that is associated with the input.
___
**MAC**
* Verifies the integrity and authenticity of data, also requires secret key.
* **HASH:** simply takes the plain text to create a hash function.
* STEPS
	* Key + Message + Mac Algorithm = MAC
	* Message + MAC
	* Message + MAC + Mac Algorithm + Key= MAC COMPARE
	* If MAC = MAC COMPARE, message is genuine and being sent to the right person
___
**MA**
* Uses hashes instead of MAC's to authenticate 
* Since we are using hashes, it should be impossible to infer the original message and the hash function should make distinct outputs for every distinct input.
___
**PKI: Public Key Infrastructure**
* How can we distribute keys without letting people know the key itself?
* Components that aid or store asymmetric cryptography.
	* There is a degree of communication to give a key to the receiver and transmitter safely, but often has its own risks. 
	* This allows the key to also be encrypted and a way to safely share the public keys.
___
**Certificate Authority (CA)**
* Third-party authority, determines if the place of origin is genuine by issuing certificates.
* References back to the certificate authority for certification of any piece of data.
* **Digital Certificate:** Entrusts that an entity is the actual entity that has a certification.
* May be installed pre-emptively on hardware or at organizations.
* The signatures on both sides of the encrypt and decrypt will be compared to check if they are valid.
___
* Certificate's have a data and expiration system
* Registration Authority: Verified the data of the identity
___
**X.509**
* General formation of the PKI systems, look in slides for form.
___
**Digital Signature**
* A unique code using a key to verify the sender and data integrity.
	* Integrity
	* Authentication
	* Non-Repudiation
		* Origin
		* Delivery
* Often used in Emails, Code Signing, Legal Document, 
___
**Digital Envelopes Technique**
* Message and key is encrypted, this adds an extra layer of protection.
___
**Kerberos Protocol**
* Maintains the single sign in option utilizing a ticketing scheme, both the client and server authenticates with one another.
* Features
	* Passwords are not across the network
	* Encryption keys are never directly exchanged
	* Mutual Authentication
___
**KDC**
* Uses a ticketing a system and is a middle man to determine if someone has a proper identity between the server and the client.
___
**Attacking Symmetric Encryption**
* BRUTE FORCE:
	* Utilizes some knowledge already given, often uses social monikers to force the password.
___

