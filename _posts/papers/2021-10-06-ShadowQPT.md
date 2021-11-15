---
layout: single
title:  "Classical Shadows for Quantum Process Tomography on Near-term Quantum Computers"
toc: false
categories: 
  - papers
header:
  overlay_image: /assets/images/choi.png
  overlay_color: "#333"
  overlay_filter: 0.75
excerpt: Reconstructing quantum channels using classical shadows
---

I recently posted a new paper on [arXiv](https://arxiv.org/abs/2110.02965)! Titled _Classical Shadows for Quantum Process Tomography on Near-term Quantum Computers_, I alongside Di Luo and Bryan Clark develop a way to bring classical shadows [1] to process tomography. Check it out!

<details>
  <summary>Abstract
</summary>
  
  <div class="notice--info"><p>
<b>Ryan Levy</b>,  Di Luo, Bryan K. Clark <br /><br />
Quantum process tomography is a powerful tool for understanding quantum channels and characterizing properties of quantum devices. Inspired by recent advances using classical shadows in quantum state tomography[1], we have developed a classical shadow method, ShadowQPT, for quantum process tomography. ShadowQPT allows for the reconstruction of the Choi matrix for unitary and non-unitary processes including an efficient reconstruction of fixed-sized reduced processes; we also show how to predict the overlap between any arbitrary state and the output of the quantum channel on a different arbitrary state. We introduce both a scheme using ancilla qubits as well as a two-sided scheme with unitaries before and after the channel. A number of additional approximations and improvements are developed including the use of a pair-factorized Clifford shadow and a series of post-processing techniques which significantly enhance the accuracy for recovering the quantum channel. Both the theoretical scaling for large systems and the practicality of using shadow tomography on NISQ-era hardware are considered. Our algorithms have been implemented with both Pauli and Clifford measurements on the IonQ trapped ion quantum computer for quantum processes up to n=4 qubits (equivalent to the experimental complexity of n=8 qubits for quantum state tomography) and achieved good performance.
</p></div>

</details>
[arXiv:2110.02965](https://arxiv.org/abs/2110.02965){: .btn .btn--success}
 
[1] See [https://www.nature.com/articles/s41567-020-0932-7](https://www.nature.com/articles/s41567-020-0932-7)

