# mars-impact-hydrothermal

iSALE-2D input files for the impact simulations in **Zorzi, A., Tikoo, S. M., Sori, M. M., & Bramson, A. M., "Lifetime of Impact-Induced Subglacial Hydrothermal Systems on Mars,"** submitted to *Geophysical Research Letters*.

## The question

An impact deposits enough heat to melt subsurface ice and create a transient hydrothermal system — potentially a habitable one. How long does that liquid water last on Mars, and how much is its lifetime extended by ice that accumulates in the crater afterwards, as seen in the crater-filling ice mounds at high latitudes?

## What's in this repository

| Path | Contents |
|---|---|
| `30-km/` | iSALE-2D inputs for the impact forming a 30 km diameter crater |
| `110-km/` | iSALE-2D inputs for the impact forming a 110 km diameter crater |
| `asteroid.inp` | Impactor definition shared by both scenarios |
| `material.inp` | Target material and equation-of-state parameters |

iSALE itself is distributed separately, with registration, at <https://isale-code.github.io>. It is not redistributed here.

## Method

The simulations configured here produce the post-impact temperature field. That field is then the initial condition for a finite-difference heat-diffusion model — not included in this repository — which tracks cooling of the crust over millions of years while ice accumulates on the crater floor, and reports where and for how long liquid water is present.

## Result

Craters 30 km across sustain liquid water for more than 0.5 Myr. Craters 110 km across sustain it for up to 5 Myr. Higher ice deposition rates, greater crustal porosity and a steeper geothermal gradient each extend the lifetime.

## Reproducing

Requires a working iSALE-2D installation. Run each scenario directory separately; `asteroid.inp` and `material.inp` apply to both.
