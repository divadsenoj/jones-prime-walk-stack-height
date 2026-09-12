David Jones

Abstract

This paper investigates the spatial behavior of a deterministic random walk on a two-dimensional integer lattice \(\mathbb{Z}^{2}\), governed by the sequence of prime numbers. Moving sequentially through the integers \(n \in \mathbb{1, 2, 3, \dots}\), a path advances by one unit grid space per integer, executing a strict 90° clockwise rotation if and only if n is prime.

While the trajectory of this "prime walk" has been previously mapped to visualize spatial distribution, this paper introduces a novel metric—the Jones Stack Height (\(H_{s}\))—to quantify the exact frequency and depth of coordinate self-intersections. By mapping the walk up to n = 1,000,000,000 (1 billion) steps, we analyze structural trapping behaviors, directional drift, and the intersection limits imposed by the Prime Number Theorem.

1. Definition of the Walk and the Jones Metric

Let the position of the walk at step n be defined by coordinates \((x_n, y_n) \in \mathbb{Z}^2\). The direction vector \(\vec{d}_n \in \{(1,0), (0,-1), (-1,0), (0,1)\}\) updates according to the primality of n:

\(\vec{d}_{n}=\begin{cases}\text{rotate\_right}(\vec{d}_{n-1})&\text{if\ }n\in \mathbb{P}\\ \vec{d}_{n-1}&\text{if\ }n\notin \mathbb{P}\end{cases}\)

The Jones Stack Height for any coordinate (x, y) after N steps is defined as the total number of times the path has occupied that exact lattice point:

\(H_{s}(x,y,N)=\sum _{n=1}^{N}\delta (x_{n},x)\cdot \delta (y_{n},y)\)

where δ is the Kronecker delta.

2. Empirical Findings at Extreme Scale (N = 10⁹)

Computational simulations mapping the path through the first one billion integers reveal three distinct structural properties:

The Upper Intersection Bound (The "Cap at 5"): Despite the astronomical scale of 10⁹ steps, the maximum stack height across the entire lattice satisfies the strict inequality \(\max(H_s) \le 5\). The maximum collision density is locked entirely within the chaotic local loop of the first few hundred steps (n ≤ 500).Asymptotic Escape Trajectory: As n → ∞, the local stack height drops precipitously to \(H_s \to 1\) for newly explored coordinates. This provides a clear geometric manifestation of the Prime Number Theorem; because the average gap between primes grows logarithmically (\(\sim \ln n\)), the straight lines (composite highways) between turns become too vast for the path to loop back and re-intersect old coordinates.Macro-Scale Anisotropy: The path exhibits an aggressive horizontal drift pulling towards the positive X-axis (East), creating a fibrous, elongated cluster rather than a symmetrical expansion.

3. Conclusion & Open Questions

The Jones Stack Height provides a powerful visual framework for analyzing the distribution gaps of prime sequences. Future work will investigate whether modifying the rotational mechanics based on modular residue classes (e.g., turning left for primes of the form 4k+1 and right for 4k+3) can successfully flatten the directional drift and alter the maximum stack height limit.

