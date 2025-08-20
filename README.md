# CRC (Cyclic Redundancy Check) Implementation in Java

This Java program provides a simple command-line interface to demonstrate the Cyclic Redundancy Check (CRC) algorithm for error detection in binary data.

## Description

The program performs two main operations:

1.  **CRC Code Generation:** It takes a binary message and a generator polynomial from the user and calculates the CRC checksum. It then displays the complete codeword (original message + CRC checksum).
2.  **Error Detection:** It takes a received codeword and the same generator polynomial to check for errors. It then reports whether the data is valid or if a CRC error has been detected.

## How to Use

### Prerequisites

- Java Development Kit (JDK) installed.

### Compilation

To compile the program, open a terminal in the `src` directory and run:

```sh
javac CRC19.java
```

### Execution

To run the compiled program:

```sh
java CRC19
```

The program will then prompt you to enter the message and generator bits.

## Usage Flow

The program runs in a sequence:

1.  **Checksum Calculation:**
    - The program first asks for the original message bits (e.g., `100100`).
    - It then asks for the generator polynomial bits (e.g., `1101`).
    - It computes and displays the final "Checksum code" that should be transmitted.

2.  **Data Validation:**
    - After displaying the code, the program asks you to enter the "checksum code" that was received. You can copy the code generated in the first step or enter a modified one to simulate an error.
    - It then asks for the same generator polynomial again.
    - It runs the CRC algorithm on the received data and prints whether the data stream is valid or invalid.

### Example

```
--Error Detection using CRC--
Enter message bits : 100100
Enter generator : 1101

The Checksum code is : 100100001
Enter checksum code: 100100001

Enter generator : 1101

Data stream is valid
```

To see an error being detected, you can alter the checksum code:

```
--Error Detection using CRC--
Enter message bits : 100100
Enter generator : 1101

The Checksum code is : 100100001
Enter checksum code: 100101001  <-- Altered bit

Enter generator : 1101

Data stream is invalid, CRC error occurred
```
