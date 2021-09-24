---
layout: post
title: Quantum Journey Day 2
date: '2021-09-22 11:01:00 +0530'
categories: jekyll update
published: true
---

### Notes


Watched these two videos.


[Beginners guide to Quantum Computing](https://www.youtube.com/watch?v=JRIPV0dPAd4){:target="_blank"}

More of an introductory talk. Motivates the need for computers by talking about an optimization problem of seating 10 people at a table (finding best seating arrangement). In a Classical computer you'd have to do exhaustive search / some heuristic based methods, whereas in Quantum - some magic apparently happens.

She highlights two effects that are used in Quantum Computers:

 - Superposition: Quantum states exist in superpositions of 0 and 1 and complex superpositions of 0s and 1s.
 - Entaglement: If 2 Qubits are "entangled" - measuring 1 gives you information about 2nd.

 Speaker then talks about how this can be used to solve the seating optimization problem, with which you apparently "Add phase" to "Quantum states", the "bad" states "cancel", because of interference and the "good" states amplify - until you get a solution. Not clear what how this works - since is beginners guide she didn't go into too much detail here.

[Lunch and Learn](https://www.youtube.com/watch?v=7susESgnDv8){:target="_blank"}

More detailed talk, starts with a little bit of Physics. Heisenberg's uncertainty principle applied on an electron means an electron that is shot through two slits is actually going through both slits - and we get an interference pattern. Every particle has an observable spin (using latest tech). Quantum Theory has not changed, tech has changed in last 20 years. 

Introduces "Entanglement" - as a quantum state where each spin is opposite to each other, but no specific direction for the spin.

Classical: The states 0s and 1s are physically represented as low and high voltage.
Quantum: An electron can have positive spin, negative spin and a superposition of the two spins. For N Qubits you need 2^N numbers to fully describe its state.

He also talks about applications for Quantum Computers: 
  - Drug Design: Quantum Mechanical calculation - for energies of each configuration of electrons in a Molecule (apprently requires "solving" a 40k*40k Matrix) - this can be done with a 7 qubit machine.
  - Ammonia production (Fertilizer - we use 2% of world energy to produce Ammonia) : Bacteria produce Ammonia at natural temperature, meaning there is a way to produce it naturally - not known to man. Since it is a Quantum Process, we should be able to find it?
  - Database Search: Grover Algorithm, N^0.5 checks to search for an entry.
  - Breaking Cryptography: Speaker is pessimistic about this, Quantum error correction requires too many Qubits (Wasn't very clear).

### Questions:

 - Kinda stupid that definition of entaglement uses "entangled". What does entangling mean, physically? I understand how 2 Qubits can be entangled (having opposite spin) - how can N Qubits be entangled with each other?
 - Why is error correction relevant to the prime factorization problem? Why does the error correction needed to be Quantum (and not classical) 
 - DIfference between Logical and Physical Qubit - rushed through this, what do they mean?

### Tags:



