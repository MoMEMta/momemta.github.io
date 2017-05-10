The strenght of MoMEMta is the user's freedom to define the phase-space parameterisation most suitable to his problem. Starting from the general parameterisation for $n$ final-state particles (with $\sqrt{s}$ the hadronic centre-of-mass energy, $p_i$ the final-state particles and $P_{\text{ini}}$ the total initial-state momentum):

\[
  \text{d} \Phi(y) \frac{\text{d} x_1 \text{d} x_2}{x_1 x_2 s} =
    \left(
      \prod_{i=1}^n \underbrace{ \frac{|p_i|^2 \, sin(\theta_i)}{(2\pi)^3 2 E_i} }_{A_i} \underbrace{ \text{d} p_i \, \text{d} \theta_i \, \text{d} \phi_i}_{\text{d} A_i}
    \right)
    \underbrace{ \delta \left( \sum_{i=1}^n p_i - P_{\text{ini}} \right)}_{D}
    \underbrace{ \frac{\text{d} x_1 \text{d} x_2}{x_1 x_2 s} }_{F}
\]

One sees immediately that this parameterisation cannot be used directly to compute numerical integrals: it features a Delta function, and some sharp peaks in the function to be integrated (see [introduction](introduction)) are not aligned with the integration variables.

In MoMEMta, the parameterisation above can be broken down into several parts, each of which is taken care of by a module. MoMEMta ships with several pre-defined modules designed to handle common use-cases:


## Main Blocks

(Main) Blocks are designed to handle the Delta function ($D$), the integration over initial-state partons and initial flux factor ($F$), and several final-state variables (parts of the $\text{d}A_i$ and $A_i$). The removal of the Delta function reduces the dimensionality of the integration by four. Furthermore, the remaining variables covered by the Block are re-organised to be more adapted to problem at hand: angular and/or momentum variables are transformed into invariant masses of intermediate particles. The procedure aligns those peaks due to propagators in the matrix element with the integration grid. Note that depending on the Block chosen, **some** of the variables in $\text{d}A_i$&$A_i$ might not be affected.

## Secondary Blocks

Secondary Blocks can be chained with a Main Block to handle (some of) the remaining variables in $\text{d}A_i$&$A_i$ (if still present), if some propagator enhancements have not been aligned by the Main Block.

## Transfer Functions

Assuming the transfer function can be factorised for the final state particles, and for the different variables, i.e.:
$$
