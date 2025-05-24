<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async
 src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# Fundamental Quantum Computation

Notes of quantum computing

A space for quantum computation knowledge storage.

---

## Wave Functions

Wave functions describe the quantum state of a system. They encode the probability amplitude of a particle being in a certain state.

* Notation: $|\psi\rangle$
* Born Rule: $P(x) = |\psi(x)|^2$
* The wave function must be **normalized**:
  $\int |\psi(x)|^2 dx = 1$

---

## Electron Spins

* Electron spin is an intrinsic form of angular momentum.
* Represented by two basis states: $|\uparrow\rangle = |0\rangle$, $|\downarrow\rangle = |1\rangle$
* Spin states can be in superpositions: $\alpha|\uparrow\rangle + \beta|\downarrow\rangle$

---

## Qubit

A qubit is a two-level quantum system.

### Normalized

* Any qubit state $|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$ must satisfy:
  $|\alpha|^2 + |\beta|^2 = 1$

### Orthogonal

* States $|0\rangle$ and $|1\rangle$ are orthogonal:
  $\langle 0|1 \rangle = 0$

---

## Photon Polarizations

* Photons can be polarized in different directions, such as horizontal $|H\rangle$ and vertical $|V\rangle$
* These states can form a qubit basis
* Can also be diagonal ($|D\rangle$) or circular polarizations ($|L\rangle, |R\rangle$)

---

## Hilbert Space

* The space of quantum states is a **Hilbert space**, a complex vector space with an inner product.
* Properties:

  * Complete
  * Inner product defined
  * Finite or infinite dimensions

---

## ⟨ Bra ⟩ and | Ket ⟩ Vectors

* **Ket**: $|\psi\rangle$ is a column vector representing a quantum state
* **Bra**: $\langle\psi|$ is the conjugate transpose (row vector)

Example:

$$
|\psi\rangle = \begin{bmatrix}\alpha \\ \beta\end{bmatrix}, \quad \langle\psi| = [\alpha^*, \beta^*]
$$

---

## Tensor Product

Used to describe composite quantum systems.

$$
|a\rangle \otimes |b\rangle = |a, b\rangle
$$

* The **order matters**: $|0\rangle \otimes |1\rangle \neq |1\rangle \otimes |0\rangle$

---

## Inner Product on Tensor Product

* Inner product extends naturally to multi-qubit systems.
* Two states are orthogonal if their inner product is 0:

  $$
  \langle \psi|\phi \rangle = 0
  $$
* If qubits differ in value, the composite states are orthogonal:

  $$
  \langle 01|10 \rangle = 0
  $$

---

## Outer Product

* The outer product of two vectors produces a matrix:

$$
|\psi\rangle\langle\phi| \rightarrow \text{Operator}
$$

Used to build **projectors**, **density matrices**, etc.

---

## Spectral Theorem

Any Hermitian operator can be diagonalized:

$$
A = \sum_i \lambda_i |v_i\rangle\langle v_i|
$$

Where $\lambda_i$ are eigenvalues and $|v_i\rangle$ are orthonormal eigenvectors.

---

## Completeness Relation

The set of orthonormal basis vectors $|i\rangle$ satisfies:

$$
\sum_i |i\rangle\langle i| = I
$$

This is the **identity operator** in Hilbert space.

Used in measurement, quantum gates, and expansion of states.

---


