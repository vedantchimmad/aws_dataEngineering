# KMS

---
Key Management service
* Data encryption can't be accessed by unauthorized user
* Encryption is done `data-in-transit` and `data-at-rest`
### Two main method to implement encryption at rest
* Client-side encryption : Client encrypts the data and managed the keys
  * Kye types :
    * Symmetric :Single key is used for encryption and decryption
    * Asymmetric :Public and private key pair for encryption and decryption 
* Server-side-encryption : AWS Encrypt the data and manges the keys