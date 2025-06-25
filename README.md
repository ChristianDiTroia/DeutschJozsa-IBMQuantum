# DeutschJozsa-IBMQuantum
This project contains a python notebook that implements and runs the Deutsch Jozsa quantum algorithm on the IBM quantum cloud.

The Deutsch Jozsa algorithm solves a problem that has little practical application but is very useful for learning the basics of quantum algorithms and computing them - which is why it is known as a _toy problem_.
As such, the purpose of this project is to help learn the process of using the Qiskit library to send and run code on a quantum computer

# Deutsch Jozsa (DJ) algorithm background
The deutsch jozsa algorithm determines if a given function f(x) which accepts x, an n-bit input, is constant or balanced.

A balanced f(x) will return 0 and 1 evenly distributed across values of x.
For example, a 3 bit input will has 8 possible combinations such that four unique inputs return 0 where the other four unique inputs return 1.

**Classical**
* In the worst case scenario, a classical computer will have an O(2^n) runtime since it will have to compute every input combination in the case that f(x) is constant.
* In the best case scenario, a classical computer will need only compute two inputs in the case that f(x) is balanced and the second output differs from the first. (In most cases, we won't be this lucky)
* _Note that a classical computer cannot actually perform the DJ algorithm, but only simulate it by sequentially evaluating f(x) for different input values of x._

**Quantum**
* A quantum computer will have a constant O(1) runtime for all values of n, since it can determine the probability of f(x) returning 1 or 0 in a single iteration of the DJ algorithm.
* However, due to the unreliability of qubits, this algorithm should be re-run many times to increase accuracy. (unlike classical computers quantum computers are prone to errors).
