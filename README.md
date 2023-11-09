The text message is encrypted using 128 bit key AES encryption. Then, the image's pixels are clustered using the K-means clustering technique. The stego-image is then transmitted after performing cluster-wise steganography using LSB technique. 

## How to execute:
### Encryption
#### i) AES and ECC encryption:
In the directory Encryption-AES, run the main_encrypt.cpp file. Enter the plaintext.
The key is the randomly generated key by the AES Algorithm to encrypt the plain text.
The ECC Algorithm encripts the AES Key and sends the encripted "Key.txt" file to the "AES Decryption" Folder.
The Encripted plain Text is stored in a "example.txt" file and send to "K-Means LSB Encription" Folder.
![Screenshot from 2023-11-09 14-25-51](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/03ac92f0-3b75-4495-99b8-41cdc5fc479e)

#### ii) K-means and LSB encryption:
Make sure that the image (testimg.png) is in the same directory and run the k_lsb.c file. 
cluster[number] are images after k-means and Cluster[number] are the images generated after LSB encryption.

The stego images are encripting are sent to the receiver (LSB Decryption).
![Screenshot from 2023-11-09 14-26-48](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/55a9bd6b-43af-4e12-8280-60d20d18fc26)
![Screenshot from 2023-11-09 14-27-09](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/f9fb211d-9659-4e46-9347-837ad71ce6d6)

### Decryption
#### i) LSB Decryption
Check if all the final Cluster[number] images obtained from above and stb_image folder are in the same directory (if not wait for 5 - 6 seconds and check the stego images would be there) then run the lsb_decrypt.c file.
![Screenshot from 2023-11-09 14-28-06](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/11177dd7-2454-45ad-902b-5d436eadab6e)


#### ii) AES Decryption:
In the directory Decryption-AES, run the main_decrypt.cpp file. Enter the key. (Make sure its the same as the encryption key.)
![Screenshot from 2023-11-09 14-28-57](https://github.com/devchaitanya/KCES-An-Efficient-and-Secure-Steganography-Method/assets/100561320/b262bef0-8b2e-4d45-b621-379b49aa8178)
