# QEC Implementation

Exercise lab to understand quantum error correction code and fault tolerant quantum computation. I implement those algorithm in IBM *qiskit*, will also do Rigetti, QuTip and Cirq

In EE 514, Prof. Daniel Lidar suggests us to use IBM *qiskit* package to implement error correction code as the final project of the course. I think it is interesting and beneficial to study and implement those code and here is a list of his suggestions:

1. Implementation of quantum error detection using the family of [[n,1,3]] QECCs, with n=3,5,7. For n=3 implement both the bit and phase flip codes. 

2. Implementation of the XY4 and a family of concatenated DD sequences.

3. Implementation of flag-based fault tolerance. Requires independent reading of

- [1]  R. Chao and B. W. Reichardt, Quantum error correction with only two extra qubits, Physical Review Letters 121, 050502 (2018).
- [2]  R. Chao and B. W. Reichardt, Fault-tolerant quantum computation with few qubits,npj Quantum Information 4, 1 (2018).
- [3]  C. Chamberland and M. E. Beverland, Flag fault-tolerant error correction with arbitrary distance codes, Quantum 2, 53 (2018).

4. Implementation of one more examples from the family of Bacon-Shor subsystem codes for quantum error detection.

5. Implementation of a universal set of 1 and 2-qubit gates on the collective dephasing DFS. This requires using DD to create the collective dephasing conditions.
6. Implementation of another example of a hybrid DD-DFS scheme.

7. Implementation of leakage elimination as described in the lecture notes.

8. Implementation of the [[6,4,2]] and [[8,6,2]] codes. See http://www.codetables.de/QECC.php?q=4&n=6&k=4 and http://www.codetables.de/QECC.php?q=4&n=8&k=6

Here is a table of what I have finished and shown in this directory.

| QEC Code               | Status   | Filename             |
| ---------------------- | -------- | -------------------- |
| Bit-flip code          | Finished | P1-BitFlip.ipynb     |
| Phase-flip code        | Finished | P1-PhaseFlip.ipynb   |
| Steane code            | Working  | P1-Steane.ipynb      |
| Perfect code           | Working  | P1-Perfect.ipynb     |
| Rui's Correction (PRL) | Working  | P3-PRL_RuiChao.ipynb |

