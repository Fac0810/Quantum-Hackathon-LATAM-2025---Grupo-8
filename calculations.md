Let \( B'' \) be given by its spectral decomposition

\[
B'' = \sum_i \lambda_i |b_i''\rangle \langle b_i''|
\]

Thus, we can represent any vector in terms of the eigenbasis of \( B'' \):

\[
|V^{-1} \Delta Q\rangle = \sum_i \alpha_i |b_i''\rangle
\]

So with that:

\[
|\Delta V\rangle = B''^{-1} |V^{-1} \Delta Q\rangle = \sum_i \lambda_i^{-1} \alpha_i |b_i''\rangle
\]

---

We create 3 quantum registers: \( R_C, R_v \), and \( R_l \). The initial state of the algorithm in every respective register is:

\[
|\psi_0\rangle = |0\rangle \otimes |V^{-1} \Delta Q\rangle \otimes |0\rangle 
= |0\rangle \otimes \sum_i \alpha_i |b_i''\rangle \otimes |0\rangle
\]

Applying the QPE to the first 2 registers (taking as unitary \( U = e^{-i2\pi B''} \)):

\[
|\psi_1\rangle = \sum_i \alpha_i (|\lambda_i\rangle \otimes |b_i''\rangle) \otimes |0\rangle
\]

Applying the AQE to adjust the ancilla register \( R_l \):

\[
|\psi_2\rangle = \sum_i \alpha_i (|\lambda_i\rangle \otimes |b_i''\rangle) \otimes 
\left( \sqrt{1 - \frac{c^2}{\lambda_i^2}} |0\rangle + \frac{c}{\lambda_i} |1\rangle \right)
\]

Applying \( QPE^\dagger \) to clean the first register:

\[
|\psi_3\rangle = |0\rangle \otimes \sum_i \alpha_i |b_i''\rangle \otimes 
\left( \sqrt{1 - \frac{c^2}{\lambda_i^2}} |0\rangle + \frac{c}{\lambda_i} |1\rangle \right)
\]

\[
= |0\rangle \otimes \sum_i \frac{c \alpha_i}{\lambda_i} |b_i''\rangle |1\rangle + K |a\rangle \otimes |0\rangle
\]

And after measuring the \( K_1 \) register, we get this:

\[
= |0\rangle \otimes c |\Delta V\rangle \otimes |1\rangle
\]