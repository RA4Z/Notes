Secure Hash Algorithm 1 is a cryptographic hash function that takes an input and produces a 160-bit (20-byte) hash value

Example of how to implement SHA-1 hash in Python:
```Python
import hashlib
def sha1_hash(input_string):
   # Create a new sha1 hash object
   sha1 = hashlib.sha1()
   # Update the hash object with the bytes of the input string
   sha1.update(input_string.encode('utf-8'))
   # Get the hexadecimal representation of the hash
   return sha1.hexdigest()
# Example usage

print(sha1_hash("hello world")) 
# Output: 2aae6c35c94fcfb415dbe95f408b9ce91ee846ed
print(sha1_hash("GeeksForGeeks")) 
# Output: addf120b430021c36c232c99ef8d926aea2acd6b
```

SHA1- has been widely used in various security applications and protocols, including including TLS and SSL, PGP, SSH, S/MIME, and IPsec. However, due to its vulnerabilities, it is recommended to use more secure hash functions like SHA-2 or SHA-