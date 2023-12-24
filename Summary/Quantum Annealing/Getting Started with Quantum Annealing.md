# Getting Started with Quantum Annealing

## Table of Contents

## The Underlying Physics

### Quantum Physics
**私:**  
Hello! Let's work together to write a brief introduction to quantum physics. Assuming that our readers only have a basic understanding of Newton's law, like $F = ma$, I want you to explain quantum physics, Schrodinger's equation, and the concepts of Hamiltonian, wave function to them.  



**ChatGPT:**  
Absolutely, let's dive into the intriguing world of quantum physics!

Quantum physics is a branch of physics that studies the behavior of matter and energy at the smallest scales, like atoms and subatomic particles. At this level, the classical laws of physics, such as Newton's laws, no longer apply as they do in the macroscopic world. Instead, quantum mechanics introduces a whole new set of principles that govern the behavior of particles.

~~Central to quantum mechanics is the concept of wave-particle duality, which suggests that particles like electrons and photons can behave as both particles and waves. This idea challenges our classical understanding, where objects were thought to behave exclusively as either particles or waves.~~

**Schrödinger's equation** is a fundamental equation in quantum mechanics that describes how the quantum state of a physical system changes over time. It's represented mathematically as $i\hbar\partial_tψ = \hat{H}ψ$, where $\hat{H}$ is the Hamiltonian operator, $ψ$ is the wave function representing the state of the system, and the equation essentially describes how the state evolves in time.

The Hamiltonian $\hat{H}$ is an operator that represents the total energy of the system. It includes the kinetic and potential energies of the particles within the system and is crucial in understanding how the system evolves over time according to quantum principles.

The wave function $ψ$ is a mathematical description of a particle or a system's state in terms of **probability amplitudes**. It contains information about the particle's position, momentum, and other properties. When the wave function is squared, it gives the **probability density** of finding the particle at a particular location.

In essence, Schrödinger's equation, the Hamiltonian, and the wave function are key elements in quantum mechanics that provide a mathematical framework for understanding the behavior and evolution of particles at the quantum level, introducing a probabilistic nature into the fundamental laws of physics.

<br>

**私:**   
Now let's talk about time-independent Schrodinger's equation. Please also introduce the eigenvalue, eigenstates, and ground state to our readers.


**ChatGPT:**   
Of course! The time-independent Schrödinger's equation is a specific form of the Schrödinger equation that deals with systems where the energy does not change with time. It's expressed as $Hψ = Eψ$, where $E$ represents the energy of the system, and the equation describes the stationary states of a quantum system.

Eigenvalues and eigenstates are essential concepts within quantum mechanics that are closely linked to the Schrödinger equation. An eigenvalue is a scalar (often representing energy in the context of quantum mechanics) that arises when a specific operator acts on its associated eigenstate. In the Schrödinger equation, $E$ represents the eigenvalue, signifying the energy values of the system.

Eigenstates, on the other hand, are the solutions to the Schrödinger equation for a given system. These states correspond to specific values of energy (eigenvalues) and describe the state of the system in a way that, when the Hamiltonian operator acts on them, it returns the same state multiplied by a constant (the eigenvalue). Each eigenstate is associated with a unique eigenvalue.

The ground state of a quantum system refers to the lowest energy state that the system can occupy. In terms of the Schrödinger equation, it corresponds to the lowest eigenvalue $E_0$ and its associated eigenstate $\psi_0$. The ground state holds particular importance as it often represents the most stable configuration of the system and serves as a reference point for understanding excited states (states with higher energy levels).
