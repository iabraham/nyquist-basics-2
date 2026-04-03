# nyquist-basics-2: Generalized Argument Principle Visualizer

A [Pluto.jl](https://plutojl.org/) notebook for visualizing the **Argument Principle** and the relation

$$N = Z - P$$

for clockwise contours, where:
- $N$ = clockwise encirclements of the origin by $H(C)$,
- $Z$ = zeros of $H(s)$ inside $C$,
- $P$ = poles of $H(s)$ inside $C$.

## Transfer function

$$H(s) = \frac{s - 3}{s^2 + 4s + 8}, \quad z_1 = 3, \quad p_{1,2} = -2 \pm 2i$$

## Interactive cases in the notebook

| Case | Contour encloses | Predicted $N=Z-P$ | Expected $H(C)$ behavior |
|------|-------------------|-------------------|---------------------------|
| 1 | Both poles $p_1, p_2$ | $0-2=-2$ | Two counter-clockwise encirclements |
| 2 | One zero + one pole ($z_1, p_1$) | $1-1=0$ | No net encirclement (cancellation) |
| 3 | All singularities ($z_1, p_1, p_2$) | $1-2=-1$ | One counter-clockwise encirclement |

Each case keeps the same Pluto structure as the original notebook:
- *s*-plane contour with singularities and current traversal point,
- mapped *H(s)*-plane trajectory,
- net angle build-up,
- individual unwrapped angle traces for each singularity.

## Run

1. Install Julia 1.x.
2. In Julia:
   ```julia
   import Pkg; Pkg.add("Pluto")
   import Pluto; Pluto.run()
   ```
3. Open `nyquist_visualization.jl` in Pluto.
