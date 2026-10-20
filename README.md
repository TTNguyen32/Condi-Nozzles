# Convergent nozzle: back pressure and choking

An interactive simulation of isentropic flow through a convergent nozzle (air, γ = 1.4), built for Cambridge Engineering IIA compressible flow revision.

Drag the back-pressure slider to see how exit pressure, exit Mach number and the mass flow function respond across the four handout cases:

1. p_B = p_0: no flow.
2. p_B > 0.528 p_0: subsonic exit, p_E = p_B.
3. p_B = 0.528 p_0: exit just sonic, maximum mass flow (ṁ√(c_p T_0)/(A p_0) = 1.281).
4. p_B < 0.528 p_0: choked. p_E stays at 0.528 p_0 and the remaining expansion happens outside the nozzle.

The animated pulses show pressure signals travelling upstream at a − u, which stall at the exit once M_E = 1. That is the physical reason the flow upstream can no longer respond to the back pressure.

## Run it

Open `index.html` in any browser. No build step or dependencies.

To host it with GitHub Pages: repo Settings → Pages → deploy from the `main` branch root.

## Model

- Area distribution: A/A_E = 1 + 2(1 − x)², with the exit at x = 1 as the minimum area.
- Mass flow function: f(M) = γ/√(γ−1) · M (1 + (γ−1)M²/2)^(−(γ+1)/(2(γ−1))).
- Local Mach number from A(x) f(M(x)) = A_E f(M_E), taking the subsonic root.
