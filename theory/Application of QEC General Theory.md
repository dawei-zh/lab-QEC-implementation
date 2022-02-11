### Application of QEC General Theory

Here is the detail application of QEC general theory on bit-flip, phase-flip, Shor's code, Steane code and perfect code. The detail of QEC theory we use here can be found in the appendix.

#### Bit-flip code

The code space, or the code that can be corrected in the bit-flip error case has the form
$$
\begin{align}
|\psi_L\rangle = \alpha|0_L\rangle  + \beta |1_L\rangle, \text{where }|0_L\rangle &= |000\rangle, |1_L\rangle = |111\rangle
\end{align}
$$
The corresponding projector is 
$$
P = \sum_{i}|i\rangle \langle i | = |000\rangle\langle 000 | + |111\rangle \langle 111|
$$
The noise channel for bit-flip code is 
$$
\mathcal{E}(\rho) = (1-p_1)(1-p_2)(1-p_3)I\rho I + p_{1}X_{1} \rho X_{1} + p_{2}X_{2} \rho X_{2} + p_{3}X_{3} \rho X_{3}
$$
Then the corresponding operation elements are
$$
E_0 = \sqrt{(1-p_1)(1-p_2)(1-p_3)}I, E_{1} = \sqrt{p_1}X_1, E_{2} = \sqrt{p_2}X_2,E_{3} = \sqrt{p_3}X_3
$$
The $\alpha_{ij}$ in the K-L condition is given by
$$
\alpha =
$$
Note that in this case, the code should be degenerate since
$$
Z_{1}|\psi_L\rangle = Z_2|\psi_L\rangle = Z_3|\psi_L\rangle = \alpha|000\rangle - \beta|111\rangle 
$$


### Shor's code

To make sure the Shor's code works for arbitrary noise, we only need to verify $P \sigma_{i}\sigma_{j}P = \alpha_{ij} P$. 



### Appendix - Theory of QEC

#### K-L Condition

Suppose that we have some kind of code $C$ and the noise will be raised by $\mathcal{E}$, we have

*  If the recovery operation $\mathcal{R}$ exists for code $C$ to correct noise $\mathcal{E}$, then $PE_{i}E_{j}P = \alpha_{ij}P$
* If for the code $C$ we have $PE_{i}E_{j}P = \alpha_{ij}P$, then the recovery operation $\mathcal{R}$ which will be used to correct the noise $\mathcal{E}$ in code $C$ exists

Note that here, we have

* The noise channel can be written in the form $\mathcal{E}(\rho) = \sum_{i} E_{i}\rho E_{i}^{\dagger}$, and it does not need to be performed independently on each qubit, or it does not need to be a CPTP map
* The code $C$ is a kind of code (after encoding) that can be corrected, and $P$ is the projector of $C$
* In the equality, $\alpha_{ij}\in\mathbb{C}$.

#### Stabilizer Code



#### Degenerate code

Suppose that we encode $k$ logical qubits in $n $ qubits, and suppose that at most $t$ errors will occur. Sometimes, different error will change the code into the same result. We call the initial code with such a property as **degenerate code**. For example, in Shor's code, error $Z_1$ and error $Z_2$ will change the initial state into the same result,
$$
Z_{1}|0_L\rangle = \left(\frac{|000\rangle - |111\rangle}{\sqrt{2}}\right)\left(\frac{|000\rangle + |111\rangle}{\sqrt{2}}\right) \\
Z_{2}|0_L\rangle = \left(\frac{|000\rangle - |111\rangle}{\sqrt{2}}\right)\left(\frac{|000\rangle + |111\rangle}{\sqrt{2}}\right) \\
Z_{1}|0_L\rangle = Z_{2}|0_L\rangle
$$
Thus, the code $|0_L\rangle$ is degenerate code.

#### Hamming Bound

For non-degenerate code, suppose that we encode $k$ logical qubits in $n $ qubits, and suppose that at most $t$ errors ($t\leq k$) will occur, then the total number of states after all possible noise happen should not be greater than $2^n$, that is
$$
\sum_{j=0}^{t} C_{n}^{j}3^{j}2^{k} \leq 2^{n}
$$
 where $3^{j}$ comes from the possible error $X, Y$ and $Z$, the factor $2^k$ means the code is non-degenerate for every logical qubit, then we should know what kind of error happen if we see the post-noise channel state. 

For $k=1$, we have
$$
2(1+3n)\leq 2^n
$$
Note that we have $n\geq 5$ in this case. Note also that the Hamming bound is a very rough bound on the existence of possible correction code. 
