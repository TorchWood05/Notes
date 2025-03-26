Cryptography is used to protect confidentiality, integrity, and authenticity. When handling credit cards, the company must follow and enforce the Payment Card Industry Data Security Standard (PCI DSS). In this case, the PCI DSS ensures a minimum level of security to store, process, and transmit data related to card credits. When handling medical records  laws and regulations has  HIPAA (Health Insurance Portability and Accountability Act) and HITECH (Health Information Technology for Economic and Clinical Health) in the USA, GDPR (General Data Protection Regulation) in the EU, DPA (Data Protection Act) in the UK. 

![[Pasted image 20250324224332.png]]
![[Pasted image 20250324224403.png]]

From a cryptography perspective, “plaintext” messages are waiting to be encrypted. The plaintext is passed through the encryption function along with a proper key. the encryption function returns a ciphertext. The encryption function is part of the cipher, a cipher is an algorithm to convert a plaintext into a ciphertext and vice versa.

1. **Plaintext** is the original, readable message or data before it’s encrypted. It can be a document, an image, a multimedia file, or any other binary data.
2. **Ciphertext** is the scrambled, unreadable version of the message after encryption. Ideally, we cannot get any information about the original plaintext except its approximate size.
3. **Cipher** is an algorithm or method to convert plaintext into ciphertext and back again. A cipher is usually developed by a mathematician.
4. **Key** is a string of bits the cipher uses to encrypt or decrypt data. In general, the used cipher is public knowledge; however, the key must remain secret unless it is the public key in asymmetric encryption. We will visit asymmetric encryption in a later task.
5. **Encryption** is the process of converting plaintext into ciphertext using a cipher and a key. Unlike the key, the choice of the cipher is disclosed.
6. **Decryption** is the reverse process of encryption, converting ciphertext back into plaintext using a cipher and a key. Although the cipher would be public knowledge, recovering the plaintext without knowledge of the key should be impossible (infeasible).

Idea behind Caesar Cipher is simple where characters are shifted by a certain number to encrypt the message and shifted back to decrypt example :
Plaintext: TRYHACKME
Key: Right shift by 3
Ciphertext : WUBKDFNPH

![[Pasted image 20250324230014.png]]

# The two main categories of encryption are symmetric and asymmetric.

1. **Symmetric Encryption** :
	Symmetric encryption, also known as symmetric cryptography, uses the same key to encrypt and decrypt the data. It is also called private key cryptography. Furthermore, communicating the key to the intended parties can be challenging as it requires a secure communication channel. Maintaining the secrecy of the key can be a significant challenge, especially if there are many recipients. 
	![[Pasted image 20250324230524.png]]
	Examples of Symmetric :
	1. **DES** was adopted as a standard in 1977 and uses a 56-bit key. With the advancement in computing power, in 1999, a DES key was successfully broken in less than 24 hours.
	2. **3DES** is DES applied three times; consequently, the key size is 168 bits, though the effective security is 112 bits. 3DES was more of an ad-hoc solution when DES was no longer considered secure. 3DES was deprecated in 2019. 
	3. **AES** was adopted as a standard in 2001. Its key size can be 128, 192, or 256 bits.
	
2. **Asymmetric Encryption** :
	Unlike symmetric encryption, which uses the same key for encryption and decryption, asymmetric encryption uses a pair of keys, one to encrypt and the other to decrypt.  To protect confidentiality, asymmetric encryption or asymmetric cryptography encrypts the data using the public key; hence, it is also called public key cryptography 
	![[Pasted image 20250324231349.png]]
	
	Examples are RSA, Diffie-Hellman, and Elliptic Curve cryptography (ECC). The two keys involved in the process are referred to as a public key and a private key. Data encrypted with the public key can be decrypted with the private key. Asymmetric encryption tends to be slower, and many asymmetric encryption ciphers use larger keys than symmetric encryption. For example, RSA uses 2048-bit, 3072-bit, and 4096-bit keys; 2048-bit is the recommended minimum key size. Diffie-Hellman also has a recommended minimum key size of 2048 bits but uses 3072-bit and 4096-bit keys for enhanced security. On the other hand, ECC can achieve equivalent security with shorter keys. For example, with a 256-bit key, ECC provides a level of security comparable to a 3072-bit RSA key.

**Basic Operations that are used :

![[Screenshot_2025-03-24_13_51_23.png]]
![[Screenshot_2025-03-24_13_54_50.png]]





