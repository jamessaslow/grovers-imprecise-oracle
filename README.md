# An Error Analysis of Grover's Search Algorithm with a Faulty Oracle

<b> Return to [Full Project Portfolio](https://github.com/jamessaslow/portfolio) </b>

A quantum error correction project involving recovering the solutions to Grover's search algorithm with an imprecise oracle.


<h2> Grover's Search Algorithm and Accuracy Issues at Large Qubit Sizes</h2>

In this research project, we obtain solutions to Grover's algorithm with an 'imprecise' Oracle while still maintaining the quantum advantage guaranteed by Grover's Algorithm. Grover's algorithm is a search algorithm that takes advantage of quantum superposition to perform a parallelized search in $O(\sqrt{t})$ times. Grover's Algorithm is structured by a two-step process: an oracle call followed by a Diffusion Operation. The Oracle call marks the desired item in the search with a pi-phase, and the Diffusion operator boosts the probability of measuring that marked item. In contrast to traditional Grover's search, we implement a multi-control phase gate that takes on any arbitrary angle $CP(\theta)$ to deviate away from the peak of the probabilistic gain curve at $\theta = \pi$. However, in the lab, there is no guarantee we can implement an infinite precision $3.1415926...$ pi-pulse that would yield an exact multi-control pi phase gate. Therefore, $\theta$ may not be exactly $\pi$, but bounded by some error $\theta = \pi \pm \epsilon$ that still gives probability $> \frac{1}{2}$ such that an imprecise oracle still maintains a quantum advantage. It can be shown that the necessary oracle phase precision scales exponentially by the number of qubits, which sets experimental limitations defined by the laser pulse coherence.



<h2> Results </h2>

We define the range of $\theta$ values where the probability is greater than $0.5$ on the probability distribution function as $\epsilon_{0.5}$ (This is the distance between the 2 purple x's on the graphs below.)

![image](https://github.com/jamessaslow/grovers-imprecise-oracle/assets/22723891/fa13c47a-cd7a-4209-874a-93aee41535b4)


As we increase the qubit size $n$, the range of useful $\theta$ values $\epsilon_{0.5}$ gets smaller and smaller, indicating that more precise oracles are needed at higher qubit sizes.

We observe $\epsilon_{0.5}$ shrink exponentially according to the results below that depict a log scale of $\epsilon_{0.5}$ as a function of qubit size.

![image](https://github.com/jamessaslow/grovers-imprecise-oracle/assets/22723891/66aaaba6-44a6-4034-a36c-2435431face4)

 
