---
layout: post
title: "Hype and brute-force in quantum computing"
categories: Physics
tags: [en-us, quantum computing, brute-force, proof-of-work, quantum physics]
math: true
toc: true
---

For the sake of exploring the theoretical limits of quantum computing, let us take an optimistic perspective—setting aside current hardware challenges such as qubit coherence, gate fidelity, error correction, and the lack of scalable, high-quality quantum systems. If we assume, for argument's sake, that these limitations are fully resolved and that practical quantum computers can operate with perfect stability and unlimited scalability, we can focus on what quantum algorithms are able to achieve in principle, regardless of present-day engineering constraints.

This approach allows us to analyze how quantum algorithms, especially Grover's, could impact cryptographic systems or complex computational challenges if quantum hardware could equal or surpass the speed and reliability of today's fastest classical systems. The subsequent discussion and calculations are based on this best-case scenario, illustrating the upper bounds of quantum computational power—even when every technical hurdle is assumed to be overcome.

## Misconception about quantum computing

Quantum computing is often mistakenly perceived as a direct replacement for classical computers, believed to deliver exponentially faster performance. This misunderstanding stems from the concept of quantum superposition, which is sometimes depicted as the ability to compute all possible solutions to a classical problem simultaneously. However, this is only part of the story.

Unlike classical computers, which process one input and yield one output at a time—representing either a 1 or a 0—a quantum computer operates on vectors that represent all possible combinations of 1s and 0s at once. The result of a quantum computation is not a single value, but rather a vector of probabilities for each possible state. Initially, each state has an equal probability, but as quantum operations are applied, these probabilities are adjusted through interference.

To obtain a concrete result, a measurement is performed, causing the probability vector to collapse randomly into one of the possible states—typically weighted by their calculated probabilities. Once measured, the quantum state is lost, and only the measured outcome remains. This means that, even if the desired solution has a probability of 99.999%, there is still a chance that the final result may be an incorrect state. If the measurement does not yield the correct answer, the computation must be started over.

It is important to note that quantum computation should not be confused with parallel computing. Rather, it represents a fundamentally different approach to processing information and designing algorithms.

## Grover's algorithm in simple words

Grover’s algorithm is a special tool quantum computers use when trying to guess something by brute force, like finding the combination to a lock or, in the case of cryptocurrencies, dealing with proof-of-work systems. In classical computing, brute force means trying every possible answer one after another until the right one is found. Quantum computers use Grover’s algorithm to make this process faster, but not as much as people sometimes think.

Unlike the belief that quantum computers can check all answers at the same time, what Grover’s algorithm actually does is adjust the odds so that the right answer stands out more and more with each step. Imagine you have a giant lottery drum with a billion balls, but you want to pull out the winning one. Grover’s algorithm shuffles the balls with each round, making it more likely that the winner will be picked, but not guaranteed all at once. The trick is that quantum computers, thanks to Grover’s algorithm, can find the winner in about the square root of the total number of tries needed by classical computers. This shortcut is called "quadratic speedup." For example, if a normal computer would need one million tries, Grover’s algorithm needs only about one thousand, which is much faster but still a huge number if the possible answers are enormous.

This means quantum computers have a geometric advantage, not an explosive (exponential) one. In the context of cryptocurrencies, where proof-of-work relies on massive guessing to secure the network (like Bitcoin mining), Grover’s algorithm is currently the most effective brute-force approach that quantum computers can offer. However, this shortcut is still not nearly enough to break proof-of-work systems, even if we imagine a quantum computer running as fast as today’s fastest classical hash machines. The number of possible answers is so huge that, realistically, it would still take more than 300 billion of years to succeed. Right now, and with the quantum algorithms known today—including Grover’s—there is no practical way for quantum computers to defeat proof-of-work protections in any reasonable time-frame.

Although Grover’s algorithm cannot break today’s proof-of-work systems, it highlights how quantum computers approach brute-force searching differently than classical computers. Grover’s algorithm is best understood as a faster—but still limited—brute-force method that offers a mathematical shortcut, not a game-changing breakthrough. Quantum computers do not instantly check every possible answer; instead, they use quantum mechanics to increase the chance of finding the right answer more quickly. However, even with this advantage, quantum computers remain far from making classical proof-of-work systems vulnerable or obsolete. With the algorithms we know today, proof-of-work remains secure against quantum attacks for the foreseeable future.

## Estimating how long Grover’s slgorithm would take

To estimate the time required for a quantum computer using Grover’s algorithm to brute-force SHA-256, you can use the following formula:

$$
\text{time} = \frac{\text{number of steps}}{\text{steps per second} \times \text{seconds per year}}
$$

Here, "number of steps" refers to the total queries a quantum or classical computer must make, “steps per second” is the hash rate (how many attempts can be tried every second), and “seconds per year” is roughly 31,536,000.

The results below use:

- **Classical brute-force**: $$2^{256}$$ steps (the theoretical work needed to search SHA-256 exhaustively).
- **Quantum brute-force (Grover’s algorithm)**: $$2^{128}$$ steps (the theoretically reduced work with quantum search).
- A **hash rate** of $$3.4×10^{19}$$ per second, similar to the global Bitcoin network rate (optimistic for quantum hardware).

| Task      | Queries Needed         | Steps     | Hash Rate Used (hashes per second) | Time (years)         |
| --------- | ---------------------- | --------- | ---------------------------------- | -------------------- |
| Classical | $$\mathcal{O}(N)$$       | $$2^{256}$$ | $$3.4\times 10^{19}$$ (SHA-256)      | $$1.08\times10^{50}$$  |
| Quantum   | $$\mathcal{O}(\sqrt N)$$ | $$2^{128}$$ | $$3.4\times 10^{19}$$ (optimistic)   | $$3.17\times 10^{11}$$ |

## Quantum algorithms: Focus, challenges, and genuine applications

Developing effective quantum algorithms for classical problems is extremely difficult. While there are a handful of notable quantum algorithms that outperform classical ones for certain structured mathematical tasks (like Shor’s and Grover’s algorithms), for the vast majority of classical computational challenges, quantum approaches either offer very limited speedups or struggle to match what is achievable with optimized classical solutions. This is mainly because most classical problems do not naturally fit the quantum computing paradigm: encoding their logic, constraints, and objectives into quantum circuits is complex, and often results in no substantial gain over classical computation.

In practice, hybrid methods—combining quantum and classical resources—are explored to overcome these barriers, but even these often face limitations: not all constraints can be efficiently translated into a quantum form, the measured outcomes don’t always align with what’s needed classically, and any quantum advantage may be marginal or non-existent for real-world instances.

Quantum computers are fundamentally designed to simulate and solve problems that are quantum in nature—those involving the behaviors and interactions of quantum systems. Classical computers cannot efficiently simulate many-particle quantum systems due to exponential resource demands, but quantum systems can naturally encode and process this information. This is why the clearest and strongest applications for quantum computers are found in quantum physics, chemistry, and materials science, where they are expected to model complex molecules, compute ground-state energies, or simulate quantum phenomena far more efficiently than is possible classically

Some algorithms are specifically created to solve problems that are inherently quantum or are best approached using quantum principles. Notable examples include:

- **Quantum Phase Estimation (QPE):** Central to finding eigenvalues of unitary operators—key in quantum simulation and chemistry.
- **Variational Quantum Eigensolver (VQE):** Used for approximating the ground-state energy of quantum systems, widely applied in electronic structure calculations for molecules.
- **Quantum Approximate Optimization Algorithm (QAOA):** Useful for certain optimization problems and has applications in quantum simulations and chemistry.
- **Deutsch-Jozsa Algorithm:** Early example demonstrating quantum speedup for a specially constructed problem that distinguishes between balanced and constant functions with a single query.
- **Quantum Simulation Algorithms:** Tailored to model the dynamics of quantum physical systems (e.g., time evolution of Hamiltonians).

These techniques are especially valued in disciplines like quantum chemistry, condensed matter physics, and quantum materials, which are innately quantum and largely intractable for classical computing.

## Conclusion

In summary, inventing new quantum algorithms for classical problems is fundamentally hard because quantum information processing is not always a natural match to classical logic. Quantum computing’s true promise lies in problems that are quantum themselves, where there are a growing number of specialized algorithms already demonstrating meaningful advantages. For most practical, everyday classical tasks, classical computers remain dominant, with quantum reserved for the mysteries of the quantum world.

---

1. [Playing Pool with Iψ〉: from Bouncing Billiards to Quantum Search](https://arxiv.org/pdf/1912.02207)
2. [A fast quantum mechanical algorithm for database search](https://doi.org/10.1145/237814.237866)
3. [Quantum computers can search rapidly by using almost any selective transformations](http://arxiv.org/pdf/0711.4299.pdf)
4. [Invariants of Grover’s algorithm and the rotation in space](https://link.aps.org/doi/10.1103/PhysRevA.66.044304)
5. [Coherence fraction in Grover's search algorithm](https://link.aps.org/doi/10.1103/PhysRevA.110.062429)
6. [Explaining Grover’s algorithm with a colony of ants: a pedagogical model for making quantum technology comprehensible](https://iopscience.iop.org/article/10.1088/1361-6552/ad2976)
7. [Grover’s Algorithm – Implementations and Implications](https://doi.org/10.54097/hset.v38i.5997)
8. [Explaining Grover's Quantum Algorithm to College Students](https://ieeexplore.ieee.org/document/10487498)
9. [Solving Nonnative Combinatorial Optimization Problems Using Hybrid Quantum–Classical Algorithms](https://arxiv.org/pdf/2403.03153)
10. [Assessing Quantum and Classical Approaches to Combinatorial Optimization: Testing Quadratic Speed-ups for Heuristic Algorithms](https://arxiv.org/pdf/2412.13035)
11. [Turning the Tables in Hybrid Classical-Quantum Systems—Classical Optimization of Quantum Algorithms: Plenary Talk](https://ieeexplore.ieee.org/document/10619882)
12. [Early Fault-Tolerant Quantum Algorithms in Practice: Application to Ground-State Energy Estimation](https://quantum-journal.org/papers/q-2025-04-01-1682/#)
13. [Variational Quantum Algorithms for Chemical Simulation and Drug Discovery](https://ieeexplore.ieee.org/document/10041453)
14. [Empirical Analysis of Classical and Quantum Algorithms for Portfolio Optimization: Enhancing Financial Decision-Making Through Quantum Computing](https://ieeexplore.ieee.org/document/10864082)
15. [Distributed exact quantum algorithms for Deutsch-Jozsa problem](https://api.semanticscholar.org/CorpusID:257632235)
16. [Strength and Weakness in Grover’s Quantum Search Algorithm](https://arxiv.org/pdf/0811.4481)
