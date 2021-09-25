---
layout: post
title: Quantum Journey Day 5
date: '2021-09-25 11:01:00 +0530'
categories: jekyll update
published: true
---

### Notes


Watched this video


Started this[lecture series](https://qiskit.org/textbook/ch-states/introduction.html){:target="_blank"} by Qiskit

Reasonable video, unneccesary digressions into philosophy and other things, but had some meaty things about Quantum computer and answered some fundamental questions too.

He calls the value of each superposition dimension an amplitude. The electron has a superposition state. In the double slit experiment - by decreasing the probability of electron taking a path (by covering 1 slit) - can increase the probability that it reaches the destination. This is because of electron can have +Ve amplitude through one slit and a negative amplitude through another slit, which can cancel out.

Quantum Computer - exploits the quantum phenomena of superposition, amplitudes and interference to solve problems faster that a classical computer. To represent 1000 qubits, need 2^1000 numbers to represent the state in a classical computer. 

Entire trick with Quantum Computing algorithms - choreograph a pattern of interference of amplitudes. Paths leading to right answer should have amplitudes that point in same direction, paths leading to wrong answer should have opposing directions.

Different choices for qubit systems - Quantum computing programmer needn't worry about it ideally(Abstracted away from programmer), but because the Qubits are noisy, we don't have this abstraction yet.

Quantum Decoherence - Unwanted interaction between Qubits and environment surrounding it. When you measure a qubit it no longer is in superposition - collapses to its state. A conscious entity needn't be doing the measuring - radiation in air, wires, molecules can all interfere. "Entangled" with environmen. => Qubits need to be isolated. Solution to this was to have Quantum Error Correction - basically duplicating Qubits using redundancy. Each logical qubits need several physical Qubits. Even noisy Quantum Computers have achieved Quantum Supremacy

Quantum Supremacy - How do you demonstrate it? Easier to show it in something like sampling from probability distributions (as opposed to something like breaking RSA)

53 physical qubits were what Google used to achieve Qubit supremacy, but we need millions of Qubits to break RSA. Post quantum Cryptography - Lattic based cryptosystems

Best application of Quantum Computing - Simluations for Chemical reactions.