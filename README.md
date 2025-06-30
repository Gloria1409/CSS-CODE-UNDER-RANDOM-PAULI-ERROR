# CSS Quantum Hamming Code under Random Pauli Error

## Project Overview

This project implements and tests the performance of the self-dual $[15,7,3]$ CSS Quantum Hamming code in the presence of random Pauli errors. The goal is to demonstrate quantum error correction by:

- Encoding the logical all-zero state,
- Introducing random Pauli errors to each physical qubit,
- Measuring error syndromes and applying recovery operations,
- Measuring the logical qubits after error correction,
- Analyzing and visualizing the success probability for different error rates.

## Methodology

1. **Logical State Preparation**  
   The logical $\lvert 0_L \rangle$ state is prepared using the $[15,7,3]$ CSS code.

2. **Noise Application**  
   Each physical qubit experiences a random Pauli error $(X, Y, or Z)$ with probability $p$, or no error with probability $1-p$.

3. **Syndrome Measurement**  
   Ancilla qubits are used to measure the syndromes (parity checks) of the stabilizers, revealing where errors have likely occurred.

4. **Error Correction (Recovery)**  
   Conditional recovery operations are applied based on the measured syndromes, targeting the most likely error locations.

5. **Measurement and Analysis**  
   All data qubits are measured. The probability of successfully recovering the original logical state is computed and plotted as a function of the physical error probability $p$.

## How to Use

- Run all cells in sequence.  
- The notebook will simulate the encoding, error, correction, and measurement process for different error probabilities.
- Key simulation results and plots will be displayed.

## Interpreting Results

- **Success Probability** is defined as the fraction of measurement outcomes matching the intended logical all-zero state after error correction.
- As error probability $p$ increases, the code’s performance decreases, demonstrating the limits of error correction.
- Plots show how the $[15,7,3]$ code handles rare vs. frequent errors.


## References

- Nielsen, M. A., & Chuang, I. L. (2010). *Quantum Computation and Quantum Information*. Cambridge University Press.
- Gottesman, D. (1996). *Class of quantum error-correcting codes saturating the quantum Hamming bound*. Physical Review A.
