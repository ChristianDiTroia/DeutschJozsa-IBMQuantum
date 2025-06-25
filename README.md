# DeutschJozsa-IBMQuantum
This project contains a python notebook that implements and runs the Deutsch Jozsa quantum algorithm on the IBM quantum cloud.

The Deutsch Jozsa algorithm solves a problem that has little practical application but is very useful for learning the basics of quantum algorithms and computing them - which is why it is known as a _toy problem_.
As such, the purpose of this project is to help learn the process of using the Qiskit library to send and run code on a quantum computer

# Deutsch Jozsa (DJ) algorithm background
The deutsch jozsa algorithm determines if a given function f(x) which accepts x, an n-bit input, is constant or balanced.

A constant f(x) will either return 0 for all inputs or 1 for all inputs.
For example, an x with a 2-bit input space will have 4 possible combinations such that all four either ruturn 0 or 1.

A balanced f(x) will return 0 and 1 evenly distributed across values of x.
For example, an x with a 3-bit input will have 8 possible combinations such that four unique inputs return 0 where the other four unique inputs return 1.

**Classical**
* In the worst case scenario, a classical computer will have an O(2^n) runtime since it will have to compute every input combination in the case that f(x) is constant.
* In the best case scenario, a classical computer will need only compute two inputs in the case that f(x) is balanced and the second output differs from the first. (In most cases, we won't be this lucky)
* _Note that a classical computer cannot actually perform the DJ algorithm, but only simulate it by sequentially evaluating f(x) for different input values of x._

**Quantum**
* A quantum computer will have a constant O(1) runtime for all values of n, since it can determine the probability of f(x) returning 1 or 0 in a single iteration of the DJ algorithm.
* However, due to the unreliability of qubits, this algorithm should be re-run many times to increase accuracy. (unlike classical computers quantum computers are prone to errors).

# Sample results for a constant f(x) over 1000 shots
_Note that the simulator has errors from simulated random noise similar to the actual quantum computer results_

### Qiskit Simulator

![29b22e8c-c17a-4633-9b34-02f04e36d8ef](https://github.com/user-attachments/assets/f606c80f-33ab-460b-bf7f-da352ce7ea69)

### IBM Quantum Cloud

![882966e2-e2bb-4cc5-8c2a-9372c33e9617](https://github.com/user-attachments/assets/1f2f6ce9-ca82-46a8-ba02-8d2d63d62b64)

### Qiskit Circuit Diagram for DJ Algorithm

![f3df4215-f385-4de8-b4fc-53fce415a3de](https://github.com/user-attachments/assets/598d3564-86af-48b1-a077-f9e75edf8471)

