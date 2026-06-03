# Cooley-Tukey FFT Implementation

A C++ implementation of the recursive **Cooley–Tukey Fast Fourier Transform (FFT)** algorithm. This project demonstrates how FFT efficiently computes the **Discrete Fourier Transform (DFT)** of complex-valued input signals using a divide-and-conquer strategy.

The implementation supports:

* Recursive radix-2 FFT
* Complex number operations
* User input validation
* Frequency-domain transformation of signals

---

## Features

* Recursive Cooley–Tukey FFT algorithm
* Complex number support
* Power-of-two input validation
* Interactive console input
* Readable complex-number output
* Educational implementation for algorithm analysis and learning

---

## Algorithm Overview

The FFT reduces the time complexity of the Discrete Fourier Transform from:

```text
O(n²)
```

to:

```text
O(n log n)
```

using a divide-and-conquer approach.

### Steps of the Algorithm

1. Split the sequence into:

   * Even-indexed elements
   * Odd-indexed elements

2. Recursively compute FFT on both halves

3. Combine results using twiddle factors:

```text
X[k] = E[k] + W_n^k * O[k]

X[k + n/2] = E[k] - W_n^k * O[k]
```

where:

```text
W_n^k = e^(-2πik / n)
```

---

## Project Structure

```text
.
├── main.cpp
├── README.md
```

---

## Requirements

* C++11 or later
* GCC / Clang / MSVC

### Header Files Used

```cpp
#include <iostream>
#include <vector>
#include <complex>
#include <cmath>

using namespace std;
```

---

## Compilation

Compile using g++:

```bash
g++ main.cpp -o fft_program -std=c++11
```

---

## Running the Program

### Linux/macOS

```bash
./fft_program
```

### Windows

```bash
fft_program.exe
```

---

## Example Input

```text
Enter the number of samples (must be a power of 2): 4

Sample 1 - Real: 1
Sample 1 - Imaginary: 0

Sample 2 - Real: 2
Sample 2 - Imaginary: 0

Sample 3 - Real: 3
Sample 3 - Imaginary: 0

Sample 4 - Real: 4
Sample 4 - Imaginary: 0
```

---

## Example Output

```text
FFT Output (Frequency Domain):

10 + 0i
-2 + 2i
-2 + 0i
-2 - 2i
```

---

## Complexity Analysis

| Operation        | Complexity |
| ---------------- | ---------- |
| Naive DFT        | O(n²)      |
| Recursive FFT    | O(n log n) |
| Space Complexity | O(n)       |

---

## Main Functions

| Function         | Description                              |
| ---------------- | ---------------------------------------- |
| `fft()`          | Performs recursive FFT computation       |
| `printComplex()` | Displays formatted complex numbers       |
| `main()`         | Handles input, validation, and execution |

---

## Applications

FFT is widely used in:

* Digital Signal Processing (DSP)
* Audio Processing
* Image Processing
* Wireless Communication
* Spectral Analysis
* Scientific Computing

---

## Future Improvements

* Inverse FFT (IFFT)
* Iterative FFT implementation
* Performance benchmarking
* FFT visualization
* Unit testing
* Polynomial multiplication using FFT

---

## Author

### [Muhammad Anas](https://github.com/Muhammad-11Anas)

Cooley–Tukey FFT Implementation in C++

