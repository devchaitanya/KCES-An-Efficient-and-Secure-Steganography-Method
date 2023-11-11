
## KCES-An Efficient and Secure Steganography Method

### Introduction
This repository implements a steganography method that combines AES encryption with K-means clustering and LSB steganography. The method first encrypts the plaintext using AES encryption. Then, the ECC encripts the AES key . Then, the image's pixels are clustered using the K-means clustering technique. Finally, cluster-wise steganography using LSB technique is performed to embed the encrypted plaintext into the clustered images. These stego-images along with ECC Encripted AES key is sent to the Receiver for decryption.

### Encryption
1.	**AES and ECC encryption:**
	* Run the `main_encrypt.cpp` file in the `Encryption-AES` directory.
	* Enter the plaintext to be encrypted.
	* The AES algorithm will generate a random key to encrypt the plaintext.
	* The ECC algorithm will encrypt the AES key and send the encrypted "Key.txt" file to the "AES Decryption" folder.
	* The encrypted plaintext is stored in an "example.txt" file and sent to the "K-Means LSB Encription" folder.
	![Screenshot from 2023-11-09 14-25-51](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/03ac92f0-3b75-4495-99b8-41cdc5fc479e)

2.	**K-means and LSB encryption:**
	* Make sure that the image (testimg.png) is in the same directory and run the `k_lsb.c` file.
	* `cluster[number]` are images after k-means clustering, and `Cluster[number]` are the images generated after LSB encryption.
	![Screenshot from 2023-11-09 14-26-48](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/55a9bd6b-43af-4e12-8280-60d20d18fc26)
![Screenshot from 2023-11-09 14-27-09](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/f9fb211d-9659-4e46-9347-837ad71ce6d6)

### Decryption
1.	**LSB Decryption:**
	* Check if all the final `Cluster[number]` images obtained from above and the `stb_image` folder are in the same directory. If not, wait for 5-6 seconds and check again.
	* Run the `lsb_decrypt.c` file.
![Screenshot from 2023-11-09 14-28-06](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/11177dd7-2454-45ad-902b-5d436eadab6e)

2.	**AES Decryption:**
	* Run the `main_decrypt.cpp` file in the `Decryption-AES` directory.
	* Enter the key, which should be the same as the encryption key.
![Screenshot from 2023-11-09 14-28-57](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/b262bef0-8b2e-4d45-b621-379b49aa8178)
