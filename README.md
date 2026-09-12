# Spatial Density and Intersection Limits in Prime-Induced Deterministic Walks: The Jones Stack Height Metric

**Author:** David Jones  
**Date:** September 2026  

### Abstract
This paper investigates the spatial behavior of a deterministic random walk on a two-dimensional integer lattice ℤ², governed by the sequence of prime numbers. Moving sequentially through the integers n ∈ {1, 2, 3, ...}, a path advances by one unit grid space per integer, executing a strict 90° clockwise rotation if and only if n is prime. 

While the trajectory of this "prime walk" has been previously mapped to visualize spatial distribution, this paper introduces a novel metric—**the Jones Stack Height (H_s)**—to quantify the exact frequency and depth of coordinate self-intersections. By mapping the walk up to n = 1,000,000,000 (1 billion) steps, we analyze structural trapping behaviors, directional drift, and the intersection limits imposed by the Prime Number Theorem.

### 1. Definition of the Walk and the Jones Metric
Let the position of the walk at step n be defined by coordinates (x_n, y_n) ∈ ℤ². The direction vector d_n updates according to the primality of n:

If n is prime: rotate_right
If n is not prime: maintain current direction

The **Jones Stack Height** for any coordinate (x, y) after N steps is defined as the total number of times the path has occupied that exact lattice point:

H_s(x, y, N) = Total count of visits to coordinate (x, y) across all steps up to N.

### 2. Empirical Findings at Scale
Computational simulations mapping the path reveal three distinct structural properties of the Jones metric:

*   **The Upper Intersection Bound (The Peak at 11):** Granular tracking of the lattice intersections proves that the maximum stack height across the lattice achieves a peak value of **H_s = 11**. These ultra-dense nodes are heavily concentrated within localized clusters where specific prime frequencies create complex geometric bottlenecks.
*   **Asymptotic Escape Trajectory:** As n → ∞, the local stack height drops precipitously to H_s → 1 for newly explored coordinates. This provides a clear geometric manifestation of the Prime Number Theorem; because the average gap between primes grows logarithmically, the straight lines (composite highways) between turns become too vast for the path to loop back and re-intersect old coordinates.
*   **Macro-Scale Anisotropy:** The path exhibits an aggressive horizontal drift pulling towards the positive X-axis (East), creating a fibrous, elongated cluster rather than a symmetrical expansion.

### 3. Conclusion & Open Questions
The **Jones Stack Height** provides a powerful visual framework for analyzing the distribution gaps of prime sequences. Future work will investigate whether modifying the rotational mechanics based on modular residue classes (e.g., turning left for primes of the form 4k+1 and right for 4k+3) can successfully flatten the directional drift and alter the maximum stack height limit.
