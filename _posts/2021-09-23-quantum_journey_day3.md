---
layout: post
title: Quantum Journey Day 3
date: '2021-09-23 11:01:00 +0530'
categories: jekyll update
published: true
---

### Notes


Watched this video


[Quantum Computing for Computer Scientists](https://www.youtube.com/watch?v=F_Riqjdh2oM&t=872s){:target="_blank"}

Great talk, might be biased by title and how it is kind of tailor made for someone like me! One of his opening statements was striking. Most of us have a ballpark idea of how most mechanical / digital systems work - and that he had no idea a quantum computer worked, and that he didn't have any idea how a quantum computer could beat a classical computer. This idea resonated with me, and my motivations for trying out Quantum Computing.

### Representing Computation with Basic Linear Algebra
 -  \|0> is represented as $$\begin{bmatrix}1\\ 0\\\end{bmatrix}$$
 - \|1> is represented as $$\begin{bmatrix}0\\ 1\\\end{bmatrix}$$
 - Tensor Product of vectors: $$\begin{bmatrix}1\\ 2\\\end{bmatrix}$$ X $$\begin{bmatrix}3\\ 4\\\end{bmatrix}$$ = $$\begin{bmatrix}3\\ 4\\ 6\\ 8\end{bmatrix}$$


 - Operations on a single Classical Bit: Negation, Identity, Set to 0 and Set to 1.
 - Reversible Computing: If I tell you the operation, and the output of the operation - you can calculate the input. Negation and Identity are Reversible operations.
 - Quantum Computers use only operations that are reversible - and also they're their own inverses. (Apply reversible operation twice and you get back the original input)

### Qbits Superposition and Quantum Logic Gates

 - CNot operation - Basic gate for Reversible & Quantum Computing (Not a Universal Gate - cannot represent all functions)
 - Qbits - When we measure a qbit its value collapses to 0 or 1 with certain probability.
 - If a qbit has value $$\begin{bmatrix}a\\b\\\end{bmatrix}$$ then it collapses to 0 with probability $$\|a\|^2$$ and 1 with probability $$\|b\|^2$$ 
 - CNOT operation: 
     - If Control bit is 1, target bit is flipped.
     - If Control bit is 0, target bit is unchanged.
     - Can be represented by $$\begin{bmatrix}1 & 0 & 0 & 0\\ 0 & 1 & 0 & 0\\0 & 0 & 0 & 1\\0 & 0 & 1 & 0\\\end{bmatrix}$$ for a 2 bit state.
 - Negation operation: 
     - Represented by $$\begin{bmatrix}0 & 1\\ 1 & 0\\\end{bmatrix}$$
     - Example: $$\begin{bmatrix}0 & 1\\ 1 & 0\\\end{bmatrix}$$ $$\begin{bmatrix}1/2 \\ \sqrt3/2 \\\end{bmatrix}$$  = $$\begin{bmatrix}\sqrt3/2 \\ 1/2 \\\end{bmatrix}$$ (Inverts the probabilities)

 - Hadamard Gate : 
     - Takes a 0 or 1 bit gate and puts it into equal superposition, also takes equal superposition and makes it 0 or 1
     - H =  $$\begin{bmatrix}1/\sqrt2 & 1 / \sqrt2\\ 1/\sqrt2 & -1/\sqrt2\\\end{bmatrix}$$
     - Examples: 
         - H \|0> = $$\begin{bmatrix}1/\sqrt2 & 1 / \sqrt2\\ 1/\sqrt2 & -1/\sqrt2\\\end{bmatrix}$$ $$\begin{bmatrix}1\\ 0\\\end{bmatrix}$$  = $$\begin{bmatrix}1/\sqrt2\\ 1/\sqrt2\\\end{bmatrix}$$
         - H \|1> = $$\begin{bmatrix}1/\sqrt2 & 1 / \sqrt2\\ 1/\sqrt2 & -1/\sqrt2\\\end{bmatrix}$$ $$\begin{bmatrix}0\\ 1\\\end{bmatrix}$$  = $$\begin{bmatrix}1/\sqrt2\\ -1/\sqrt2\\\end{bmatrix}$$
         - $$\begin{bmatrix}1/\sqrt2 & 1 / \sqrt2\\ 1/\sqrt2 & -1/\sqrt2\\\end{bmatrix}$$ $$\begin{bmatrix}1/\sqrt2\\ 1/\sqrt2\\\end{bmatrix}$$ =  $$\begin{bmatrix}1\\ 0\\\end{bmatrix}$$ 
         - $$\begin{bmatrix}1/\sqrt2 & 1 / \sqrt2\\ 1/\sqrt2 & -1/\sqrt2\\\end{bmatrix}$$ $$\begin{bmatrix}1/\sqrt2\\ -1/\sqrt2\\\end{bmatrix}$$ =  $$\begin{bmatrix}0\\ 1\\\end{bmatrix}$$ 
 - State machines for negation and Hardmard gates:
     - ![image-title-here](/assets/images/state_machines.png){:class="img-responsive"}

### Simplest problem where Quantum Computer beats classical computer
 - Deustch Oracle:
     - Check if an unknown blackbox function is 
         - constant function (Always outputs 0 or always outputs 1)
         - variable (Changes depending on input - for example, identity and negation for 1 bit functions)
 - Add a qbit output (as input) - Needed to convert a non reversible function to a reversible function
 	![image-title-here](/assets/images/reversible_hack.png){:class="img-responsive"}

### Entanglement and Teleportation
 - Entanglement:
     - If product state of two qbits cannot be factored, they are said to be entangled.

       $$\begin{bmatrix}1/\sqrt2 & \\0 \\ 0 \\ 1 / \sqrt2\end{bmatrix}$$ = $$\begin{bmatrix}a\\ b\\\end{bmatrix}$$ *  $$\begin{bmatrix}c\\ d\\\end{bmatrix}$$ has no solution. 50% chance of collapsing to 0 and 50% chance of collapsing to 1
     - Use the output of Hadamard Gate as control bit for Cnot gate and boom you get an entangled pair of bits.
     - Spooky action at a distance: If you entangle two qubits and take one to other end of universe, measure one - it collapses the other (instantaneously)
 - Teleportation:
     - Process of transferring a qubit state elsewhere (using entangled qubits)
     - No cloning theorem: Cannot copy paste qubits, only cut and paste
     - Needs exchange of 2 classical bits - meaning it isn't faster than light 

### Questions:

 - He mentions some Von Something Energy limit - not really clear what that was
 - He mentions the hack of adding another qbit for converting the set to 0 functions into a revertible function, but does that mean all reversible functions are computable in a quantum computer?
 - The speedup mentioned for Deustch Oracle  (Reducing from 2 queries to 1 from Classical To Quantum) -  seems to have used only Classical Vectors and classical computation, is it not possible to tell if the blackbox function is constant or variable by adding bits as input for classical case too? 
 - How do we entangle 3...N bits??
 - With respect to locality - how does measuring one qubit on one end - collapse the other instanteously (how do we know the other is collapsed - without doing a measurement)


### Tags:



