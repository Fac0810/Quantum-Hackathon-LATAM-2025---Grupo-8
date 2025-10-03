Let $B''$ given by it´s spectral descomposition
$B''=\sum_i\lambda_i\ket{b_i''}\bra{b_i''}$

Thus, we can represent any vector in function of the eigenbase of $B''$

$\ket{V^{-1}\Delta Q}=\sum_i\alpha_i\ket{b_i''}$


So with that  $\ket{\Delta V}=B''^{-1} \ket{V^{-1} \Delta Q} 
= \sum_{i} \lambda_i^{-1} \alpha_i \ket{b_i''}$

We create 3 quantum registers: $R_C, R_v$ and $R_l$. The initial state of the algorithm in every respective register is

$\ket{\psi_0}=\ket{0}\otimes\ket{V^{-1}\Delta Q}\otimes \ket{0}=\ket{0}\otimes\sum_i\alpha_i\ket{b_i''}\otimes\ket{0}$

Aplying the QPE to the first 2 registes (taking as unitary $U=e^{-i2\pi B''}$)

$\ket{\psi_1}=\sum_i\alpha_i(\ket{\lambda_i}\otimes\ket{b_i''})\otimes\ket{0}$

Aplying the AQE to adjust the ancilla register $R_l$


$\ket{\psi_2}=\sum_i\alpha_i(\ket{\lambda_i}\otimes\ket{b_i''})\otimes(\sqrt{1-\frac{c^2}{\lambda_i^2}}\ket{0}+\frac{c}{\lambda_i}\ket{1})$

Aplying $QPE^\dagger$ to clean the first register

$\ket{\psi_3}=\ket{0}\otimes \sum_i\alpha_i\ket{b_i''})\otimes(\sqrt{1-\frac{c^2}{\lambda_i^2}}\ket{0}+\frac{c}{\lambda_i}\ket{1})$

$=\ket{0}\otimes \sum_i\frac{c\alpha_i}{\lambda_i}\ket{b_i''}\ket{1}+K\ket{a}\ket{0}$

And after measuring the $K_l$ register, we get this

$=\ket{0}\otimes c\ket{\Delta V}\otimes \ket{1}$}