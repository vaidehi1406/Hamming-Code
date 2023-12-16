# Hamming-Code
Hamming code for a simple error detection and correction mechanism in C programing language.

---

**About Hamming Code**
Hamming code is a type of error-correcting code named after its inventor, Richard Hamming. 
It is designed to detect and correct single bit errors in binary data. 
The basic idea behind Hamming codes is to add redundant bits to the original data in such a way that the errors can be detected and corrected.

---

**Here's a step-by-step description of the code:**

**Initialization:**

* Two arrays data and rec of size 9 are declared to store the original data bits and the received bits, respectively.
* The variable i is declared for loop iteration.

**User Input for Original Message:**

* The user is prompted to enter a 5-bit message one by one.
* The bits are stored in the data array at positions 3, 5, 6, 7, and 9.

**Hamming Code Encoding:**

* Parity bits are calculated and stored in the data array at positions 1, 2, 4, and 8.
* Parity bit 1 (data[1]) covers bits 3, 5, 7, and 9.
* Parity bit 2 (data[2]) covers bits 3, 6, and 7.
* Parity bit 4 (data[4]) covers bits 5, 6, and 7.
* Parity bit 8 (data[8]) covers bit 9.

**Display Encoded Message:**

The encoded message, including original and parity bits, is displayed.

**User Input for Received Message:**

* The user is prompted to enter the received 7 bits one by one.
* The received bits are stored in the rec array.

**Error Detection and Correction:**

* Error positions are determined by XOR operations on received bits.
* The error position is calculated and stored in the variable error_position.
* If error_position is 0, there is no error, and a message is displayed accordingly.
* If an error is detected, the program corrects the error by flipping the bit at the detected error position.
* The corrected message is then displayed.

**Output:**

The program outputs whether there is an error and, if so, the position of the error and the corrected message.
