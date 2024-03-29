---
layout: single
title: Research
permalink: /research/
classes_: wide
toc: false
toc_sticky: true
toc_icon: scroll
author_profile: true
---

Here are some of the papers and work I've been involved with

## Quantum Monte Carlo

<details>
<summary>  
<!--<img src="{{ "/assets/images/site_logo.png" | absolute_url }}" style="width:5em;margin-bottom:0.2em" class="align-left"/>-->
Automatic Order Detection and Restoration Through Systematically Improvable Variational Wave Functions</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b> Miguel Morales, Shiwei Zhang<br /><br />

Variational wave function ansatze are an invaluable tool to study the properties of strongly correlated systems. We propose such a wave function, based on the theory of auxiliary fields and combining aspects of auxiliary-field quantum Monte Carlo and modern variational optimization techniques including automatic differentiation. The resulting ansatz, consisting of several slices of optimized projectors, is highly expressive and systematically improvable. We benchmark this form on the two-dimensional Hubbard model, using both cylindrical and large, fully periodic supercells. The computed ground-state energies are competitive with the best variational results. Moreover, the optimized wave functions predict the correct ground-state order with near full symmetry restoration (i.e. translation invariance) despite initial states with incorrect orders. The ansatz can become a tool for local order prediction, leading to a new paradigm for variational studies of bulk systems. It can also be viewed as an approach to produce accurate and systematically improvable wave functions in a convenient form of non-orthogonal Slater determinants (e.g., for quantum chemistry) at polynomial computational cost. </p></div>

</details>
[arXiv:2308.08594](https://arxiv.org/abs/2308.08594){: .btn .btn--success} 
<details>
<summary>  
<!--<img src="{{ "/assets/images/site_logo.png" | absolute_url }}" style="width:5em;margin-bottom:0.2em" class="align-left"/>-->
Mitigating the Sign Problem Through Basis Rotations</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b> and Bryan K. Clark<br /><br />

Quantum Monte Carlo simulations of quantum many body systems are plagued by the Fermion sign problem. The computational complexity of simulating Fermions scales exponentially in the projection time \(\beta\) and system size. The sign problem is basis dependent and an improved basis, for fixed errors, lead to exponentially quicker simulations.  We show how to use sign-free quantum Monte Carlo simulations to optimize over the choice of basis on large two-dimensional systems.  
We numerically illustrate these techniques decreasing the 'badness' of the sign problem by optimizing over single-particle basis rotations on one and two-dimensional Hubbard systems.  We find a generic rotation which improves the average sign of the Hubbard model for a wide range of \(U\) and densities for \(4\times L\) systems.  In one example improvement, the average sign (and hence simulation cost at fixed accuracy) for the \(16\times 4\) Hubbard model at \(U/t=4\) and \(n=0.75\) increases by \(\exp\left[8.64(6)\beta\right]\). For typical projection times of \(\beta\gtrapprox 100\), this accelerates such simulation by many orders of magnitude. </p></div>

</details>
[Phys Rev Lett](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.126.216401){: .btn .btn--info} [arXiv:1907.02076](https://arxiv.org/abs/1907.02076){: .btn .btn--success} 

<!--===================================================================--->

<hr style="border-top: 1px dotted #000;" />

<details>
  <summary>Implementation of the Maximum Entropy Method for Analytic Continuation</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b> J.P.F. LeBlanc, and Emanuel Gull<br /><br />

We present `Maxent`, a tool for performing analytic continuation of spectral functions using the maximum entropy method. The code operates on discrete imaginary axis datasets (values with uncertainties) and transforms this input to the real axis. The code works for imaginary time and Matsubara frequency data and implements the 'Legendre' representation of finite temperature Green's functions. It implements a variety of kernels, default models, and grids for continuing bosonic, fermionic, anomalous, and other data. Our implementation is licensed under GPLv2 and extensively documented. This paper shows the use of the programs in detail.</p></div>

</details>
[Comp Phys Comm](https://www.sciencedirect.com/science/article/abs/pii/S0010465517300309?via%3Dihub){: .btn .btn--info}  [arXiv:1606.00368](https://arxiv.org/abs/1606.00368){: .btn .btn--success}

<!--===================================================================--->

<details>
  <summary>Magnetic susceptibility and simulated neutron signal in the two-dimensional Hubbard model</summary>
  
  <div class="notice--info"><p>
J. P. F. LeBlanc, Shaozhi Li, Xi Chen, <b>Ryan Levy</b>, A. E. Antipov, Andrew J. Millis, and Emanuel Gull<br /><br />

We compute dynamic spin susceptibilities in the two-dimensional Hubbard model usingthe method of dual fermions, and we provide a comparison to lattice Monte Carlo and cluster dynamical mean-field theory. We examine the energy dispersion identified by peaks in Imχ(ω,q), which define spin modes, and we compare the exchange scale and magnon dispersion to neutron experiments on the parent La2CuO4 cuprate. We present the evolution of the spin excitations as a function of Hubbard interaction strengths and doping, and we explore the particle-hole asymmetry of the spin excitations. We also study the correlation lengths and the spin excitation dispersion peak structure, and we find a Y-shaped dispersion similar to neutron results on doped HgBa2CuO4+δ.
</p>
</div>
</details>
[Phys Rev B](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.100.075123){: .btn .btn--info}  [arXiv:1904.10782](https://arxiv.org/abs/1904.10782){: .btn .btn--success}
<!--===================================================================--->
## Quantum Computing

<details>
  <summary>Towards solving the Fermi-Hubbard model via tailored quantum annealers</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b>,  Zoe Gonzalez Izquierdo, Zhihui Wang, Jeffrey Marshall, Joseph Barreto, Louis Fry-Bouriaux, Daniel T. O'Connor, Paul A. Warburton, Nathan Wiebe, Eleanor Rieffel, Filip A. Wudarski <br /><br />
The Fermi-Hubbard model (FHM) on a two dimensional square lattice has long been an important testbed and target for simulating fermionic Hamiltonians on quantum hardware. We present an alternative for quantum simulation of FHMs based on an adiabatic protocol that could be an attractive target for next generations of quantum annealers. Our results rely on a recently introduced low-weight encoding that allows the FHM to be expressed in terms of Pauli operators with locality of at most three. We theoretically and numerically determine promising quantum annealing setups for both interacting 2D spinless and spinful systems, that enable to reach near the ground state solution with high fidelity for systems as big as 6x6 (spinless) and 4x3 (spinful). Moreover, we demonstrate the scaling properties of the minimal gap and analyze robustness of the protocol against control noise. Additionally, we identify and discuss basic experimental requirements to construct near term annealing hardware tailored to simulate these problems. Finally, we perform a detailed resource estimation for the introduced adiabatic protocol, and discuss pros and cons of this approach relative to gate-based approaches for near-term platforms.
</p></div>

</details>
[arXiv:2207.14374](https://arxiv.org/abs/2207.14374){: .btn .btn--success}
<!--===================================================================--->
<details>
  <summary>Classical Shadows for Quantum Process Tomography on Near-term Quantum Computers
</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b>,  Di Luo, Bryan K. Clark <br /><br />
Quantum process tomography is a powerful tool for understanding quantum channels and characterizing properties of quantum devices. Inspired by recent advances using classical shadows in quantum state tomography[1], we have developed a classical shadow method, ShadowQPT, for quantum process tomography. ShadowQPT allows for the reconstruction of the Choi matrix for unitary and non-unitary processes including an efficient reconstruction of fixed-sized reduced processes; we also show how to predict the overlap between any arbitrary state and the output of the quantum channel on a different arbitrary state. We introduce both a scheme using ancilla qubits as well as a two-sided scheme with unitaries before and after the channel. A number of additional approximations and improvements are developed including the use of a pair-factorized Clifford shadow and a series of post-processing techniques which significantly enhance the accuracy for recovering the quantum channel. Both the theoretical scaling for large systems and the practicality of using shadow tomography on NISQ-era hardware are considered. Our algorithms have been implemented with both Pauli and Clifford measurements on the IonQ trapped ion quantum computer for quantum processes up to n=4 qubits (equivalent to the experimental complexity of n=8 qubits for quantum state tomography) and achieved good performance.
</p></div>

</details>
[arXiv:2110.02965](https://arxiv.org/abs/2110.02965){: .btn .btn--success}

## Tensor Network Methods

<details>
  <summary>Entanglement Entropy Transitions with Random Tensor Networks
</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b>,  Bryan K. Clark <br /><br />
Entanglement is a key quantum phenomena and understanding transitions between phases of matter with different entanglement properties are an interesting probe of quantum mechanics. We numerically study a model of a 2D tensor network proposed to have an entanglement entropy transition first considered by Vasseur et al.[Phys. Rev. B 100, 134203 (2019)]. We find that by varying the bond dimension of the tensors in the network we can observe a transition between an area and volume phase with a logarithmic critical point around \(D\approx 2\). We further characterize the critical behavior measuring a critical exponent using entanglement entropy and the tripartite quantum mutual information, observe a crossover from a 'nearly pure' to entangled area law phase using the the distributions of the entanglement entropy and find a cubic decay of the pairwise mutual information at the transition. We further consider the dependence of these observables for different Rényi entropy. This work helps further validate and characterize random tensor networks as a paradigmatic examples of an entanglement transition.
</p></div>

</details>
[arXiv:2108.02225](https://arxiv.org/abs/2108.02225){: .btn .btn--success}


<details>
  <summary>Distributed-Memory DMRG via Sparse and Dense Parallel Tensor Contractions
</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b>, Edgar Solomonik, Bryan K. Clark <br /><br />

The Density Matrix Renormalization Group (DMRG) algorithm is a powerful tool for solving eigenvalue problems to model quantum systems. DMRG relies on tensor contractions and dense linear algebra to compute properties of condensed matter physics systems. However, its efficient parallel implementation is challenging due to limited concurrency, large memory footprint, and tensor sparsity. We mitigate these problems by implementing two new parallel approaches that handle block sparsity arising in DMRG, via Cyclops, a distributed memory tensor contraction library. We benchmark their performance on two physical systems using the Blue Waters and Stampede2 supercomputers. Our DMRG performance is improved by up to 5.9X in runtime and 99X in processing rate over ITensor, at roughly comparable computational resource use. This enables higher accuracy calculations via larger tensors for quantum state approximation. We demonstrate that despite having limited concurrency, DMRG is weakly scalable with the use of efficient parallel tensor contraction mechanisms.</p></div>

</details>
[SC'20 Proceedings](https://dl.acm.org/doi/10.5555/3433701.3433732){: .btn .btn--info}  [arXiv:2007.05540](https://arxiv.org/abs/2007.05540){: .btn .btn--success}

<!--===================================================================--->
<details>
  <summary>Topology and the one-dimensional Kondo-Heisenberg model</summary>
  
  <div class="notice--info"><p>
Julian May-Mann, <b>Ryan Levy</b>, Rodrigo Soto-Garrido, Gil Young Cho, Bryan K. Clark, Eduardo Fradkin<br /><br />

  The Kondo-Heinsberg chain is an interesting model of a strongly correlated system which has a broad superconducting state with pair-density wave (PDW) order. Some of us have recently proposed that this PDW state is a symmetry-protected topological (SPT) state, and the gapped spin sector of the model supports Majorana zero modes. In this work, we reexamine this problem using a combination of numeric and analytic methods. In extensive density matrix renormalization group calculations, we find no evidence of a topological ground state degeneracy or the previously proposed Majorana zero modes in the PDW phase of this model. This result motivated us to reexamine the original arguments for the existence of the Majorana zero modes. A careful analysis of the effective continuum field theory of the model shows that the Hilbert space of the spin sector of the theory does not contain any single Majorana fermion excitations. This analysis shows that the PDW state of the doped 1D Kondo-Heisenberg model is not an SPT with Majorana zero modes.
</p></div>

</details>
[Phys Rev B](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.101.165133){: .btn .btn--info}  [arXiv:2002.01483](https://arxiv.org/abs/2002.01483){: .btn .btn--success}

<!--===================================================================--->


## Experimental Work

In another life, I worked on analyzing quantum dot formation.

<details>
  <summary>Mechanisms of InAs/GaAs quantum dot formation during annealing of In island</summary>
  
  <div class="notice--info"><p>
S. Huang, S.J. Kim, <b>Ryan Levy</b> X.Q. Pan, and R.S. Goldman<br /><br />

We have examined the formation mechanisms of InAs quantum dots (QDs) via annealing In islands under As flux. We report two distinct mechanisms, droplet epitaxy (DE) and solid phase epitaxy (SPE), which depend on As surface coverage. On c(4 × 4) GaAs surfaces, QDs form by DE. For c(4 × 4)α, one-to-one conversion from In islands to InAs QDs is observed. For c(4 × 4)β, lower densities of larger QDs are observed, presumably due to enhanced In surface diffusion in the absence of metastable Ga-As dimers. For the As capped surface, In deposition leads to an amorphous film, from which QDs nucleate by SPE during annealing.
</p>
</div>
</details>
[Appl Phys Lett](https://aip.scitation.org/doi/abs/10.1063/1.4822052){: .btn .btn--info}  <!--[arXiv:](){: .btn .btn--success}-->

<!--===================================================================--->
