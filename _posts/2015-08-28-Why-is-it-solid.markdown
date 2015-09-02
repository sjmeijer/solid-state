---
layout: post
title:  "Cohesive energy: Why is it solid?"
date:   2015-08-27 16:01:38
categories:  overview solids 
---


Now, on to Ashcroft & Mermin Chapter 20.


## Starting off

**Cohesive energy** - The energy required to disassemble a solid into it's constituent parts (binding energy). Generally, the atoms are considered to be the "constituent parts", but depending on context, other conventions may be used (molecules, or ions, rather than atoms).

Cohesive energy is the ground state energy of a solid. It's sign determines if the solid is stable at all.

Cohesive energy is also referred to as **crystal potential energy**.

The generalization of the *cohesive energy* to nonzero temperatures is the **Helmholtz Free Energy**. If you know the Helmholtz Free energy of a solid as a function of volume and temperature, you know all of the equilibrium themodynamic infoation about the solid. As the field of solid state physics has trended to a growing interest in non-equilibrium thermodynamics (transport and optical properties), the study of cohesion no longer plays as significant of a role.

In this chapter we will:

* Discuss elementary facts about cohesive energy
* Calculate these energies for an externally imposed lattice constant (considering solids under external pressure)
* By calculating the rate of change of cohesive energy with lattice constant, we can find the pressure needed to maintain a given volume (and therefore determine the equilibrium lattice constant as that requiring 0 (i.e. atmospheric) pressure for its mainteneance).
* In the same way, we can calculate the compressibility of the solid (change in colume with pressure).

<a name="localizeParticles"></a>
To do this, we will (incorrectly) treat the ion cores as classical particles which can be perfeclty localized with zero kinetic energy. This simplification violates the uncertainty principle by confining the ion core to a small region, which should increase the particle momentum and the "zero-point kinetic energy". Additionally, the ions are not perfectly localized. These effects are mostly ignored for now.


So then, lets look at the more important factors that contribute to these binding energies. We'll start with the (simple) 

* **Molecular solids** are "treated as atoms held together by short-range fluctuating dipole interactions, and prevented from coming close together by the still shorter-range core-core repulsion."
* **Ionic crystals** are composed of electrically charged ionsk and problems arise connected with the very long range interionic foce. On the other hand, the electrostatic interaction dominates other sources of attraction, making it somewhat simpler.
* **Covalent crystals and metals** prove difficult to construct even a crude theory for. The arrangement of the valence electrons ( whether in the well-localized bonds of good covalent insulators, or the electron gas of the alkali metals) is vastly different from the isolated atom or ions, so we'll only be able to qualitatively discuss this.

<a name="latticeParameter"></a>
To simplify things, we'll discuss cubic crystals, in terms of the unit cell side length $$a$$, which most people just call the [**lattice parameter**](https://en.wikipedia.org/wiki/Lattice_constant). This is the distance between "corner" atoms along the cube edge. Note that non-cubic lattices may requireadditional lattice parameters ([hexagonal close packed](https://en.wikipedia.org/wiki/Hexagonal_crystal_system), for example)




## Molecular Crystals: The Noble Gases
We'll look at only the simplest cases, noble gas atoms in molecular crystals. Actually, we'll even omit helium, since there are many quantum effects to worry about (also because it is [not a solid at atmospheric pressure](http://ltl.tkk.fi/research/theory/helium.html)). 

Quickly reviewing solid nobles:

* Atoms in solid noble gases are only slightly distorted from the stable closed-shell configuration that they posses in the free state
* This small distortion can be described by the *fluctuating dipole interaction* and represented as a weak attractive potential which varies as the inverse $$6^{th}$$ power of interatomic separation. 
* This weak attraction is what holds the solid together.

The equilibrium size of the solid is largely determined by the degree of repulsion that ion cores have when atoms approach closely. At short distances, this repulsion must be stronger than the attraction (to prevent them all from condensing in together, which we know doesn't happen), and it is conventional to represent it as a power law (generally a power of 12). Ths potential has the form then

\begin{equation}
	\phi(r) = -\frac{A}{r^6} + \frac{B}{r^{12}}
\end{equation}

 with positive constants A and B, and $$r$$ as the interatomic distance. This is equivalent to the "dimensionally more appealing form"
 
\begin{equation}
	\phi(r) = 4\epsilon \left[ \left(\frac{\sigma}{r}\right)^{12} - \left(\frac{\sigma}{r}\right)^{6}\right]
\end{equation}

for $$\sigma = (B/A)^{1/6}$$ and $$\epsilon = A^2/4B$$. This is the **Lennard-Jones 6-12 potential**. The choice of power 12 in the repulsive term is "arbitrary" in that it is anlaytically simple and must be greater than the 6 power in the attractive term. Despite being somewhat arbitrary, this reproduces the thermodynamic properties of noble gases at low densities well. An example is shown here:

{% include image.html url="LennardJones.png" description="A nice figure of a L-J potential, taken from http://www.cmbi.ru.nl/redock/Glossary.php" %}
{% include space.html %}

Again, the authors point out that the precise form of the Lennard-Jones 6-12 potential is not to be taken too seriously, and that it simply takes the following into account: 

1. Potential is attractive and varies as $$1/r^6$$ at large separations.
2. The potential is strongly repulsive at small separations
3. The parameters $$\epsilon$$ and $$\sigma$$ measure the strength of the attraction and the radius of the repulsive core, as determined by fitting data in the gaseous state.

A typical $$\epsilon$$ is of order 0.01 eV, consistent with the very weak binding energy of the solidified noble gases.

####Matching to data
Let's try to fit some of the observed properties of the *solid* noble gases using only data from the *gaseous state* and the Lennard-Jones potential.

We treat the rare gas solid as a set of classical particle, localized, with negligible kinetic energy at the points of the observed face-centeres cubic Bravais lattice. To compute the total potential energy of the first solid, first note that the interaction energy of the atom at the origin with all of the other atoms is 

\begin{equation}
	\sum\limits_{R\neq0} \phi(R)
\end{equation}

If we were to multiply this by the total number of atoms in the crystal $$N$$, we get twice the total potential energy of the crystal, because we are double-counting the interaction energy of each atom pair (once from each direction). Thus, the energy-per particle, $$u$$, is just:
\begin{equation}
	u = \frac{1}{2}\sum\limits_{R\neq0} \phi(R)
\end{equation}
where we sum over all nonzero vectors in the FCC Bravais lattice.

For convenience, we'll write the length of the Bravais lattice vector $$R$$ as a dimensionless number, $$\alpha(R)$$ times the nearest-neighbor separation $$r$$.
\begin{equation}
	u = 2\epsilon\left[ A_{12}\left(\frac{\sigma}{r}\right)^{12} - A_{6}\left( \frac{\sigma}{r}\right)^{6} \right]
\end{equation}
where we define constants $$ A_n = \sum\limits_{R\neq0}\frac{1}{\alpha(R)^n}$$ -- these constants depend on only the particular crystal structure (FCC, for example) and the number $$n$$. When $$n$$ is very large, only the nearest neighbors of the origin will contribute to the sum in $$A_n$$.

As $$n\to\infty$$, $$A_n$$ approaches the number of nearest neighbors (12 for an FCC Bravais lattice). This is because $$\alpha(R) = 1$$ by definition, and $$R$$ is a vector joining nearest neighbors.



### Equilibrium Density of the Solid Noble Gases.
Th density is effectively the nearest-neighbor separation - it is a statement of how close atoms in the lattice are to one another. To find the nearest-neighbor separation we minimize $$u$$, above, with respect to $$r$$, to find that $$\partial  u/\partial r = 0$$ at
\begin{equation}
r_0^{th} = \left( \frac{2A_{12}}{A_6} \right)^{1/6}\sigma = 1.09\sigma
\end{equation}

Here $$r_0^{th}$$ is the theoretical nearest-nighbor disance. This compares with the experimental value $$r_o^{exp}$$ quite well, though the experimental value becomes comparitively larger for lighter atomic masses. This is because we neglected the zero-point kinetic energy, which becomes greater for smaller volumes ([recall here](#localizeParticles)).


### Equilibrium Cohesive Energy of the Solid Noble Gases
Substituting this theoretical equilibrium nearest-neighbor separation distance into the energy-per-particle $$u$$ determined above, we can find the *equilibrium cohesive energy*
\begin{equation}
	u_o^{th} = - \frac{\epsilon A_6 ^{2}}{2 A_{12}} = -8.6\epsilon
\end{equation}

This also seems to agree well with measured values $$u_0^{exp}$$, though it suffers the same effect due to neglecting the zero-point motion that is significant for smaller ion cores.


### Equilibrium Bulk Modulus of the Solid Noble Gases 
*Starting pg 402*

A substance's [bulk modulus](https://en.wikipedia.org/wiki/Bulk_modulus) measures it's resistance to uniform compression (from all sides). It is defined as the ratio of infinitesimal pressure increase to the resulting relative decrease of the volume.

A bulk modulus can also be calculated for a solid noble gas in equilibrium. $$B = -V \frac{dP}{dV}$$ or $$-V (\partial P/\partial V)_T$$. 

The pressure at $$T=0$$ is given by $$P = -dU/dV$$, where $$U$$ is the total energy. We can write this in terms of energy per particle $$u = U/N$$. This gives us then:
\begin{equation}
	B = v\frac{\partial}{\partial v}\left( \frac{\partial u}{\partial v} \right)
\end{equation}

In a FCC lattice, the volume-per-particle $$v$$ is $$v = a^3/4$$ (where $$a$$ is the usual [lattice parameter](#latticeParameter)). For a FCC lattice, the lattice parameter and nearest-neighbor separation are related as $$a = \sqrt(2)r$$, which allows us to write the volume as $$v = \frac{r^3}{\sqrt(2)}$$, and $$\frac{\partial}{\partial v} = \frac{\sqrt(2)}{3r^2}\frac{\partial}{\partial r}$$. This then allows us to write the bulk modulus as
\begin{equation}
	B = \frac{\sqrt(2)}{9} r \frac{\partial}{\partial r}\frac{1}{r^2}\frac{\partial}{\partial r}u
\end{equation}

The equilibrium separation distance $$r_0$$ is the distance at which the energy per particle $$u$$ is minumized. In equilibrium $$\frac{\partial u}{\partial r}$$ vanishes, which eventually reduces $$B_0^{th}$$ to $$\frac{75\epsilon}{\sigma^3}$$. This is a better fir for the heavier nobles, presumably for the same reasons we've mentioned about the [localization](#localizeParticles).


## Ionic Crystals (pg 402)



## Cohesion in Covalent Crystals and Metals (A&M pg. 409)

### Cohesion in Covalent Crystals (A&M pg 409)

### Cohesion in Free Electron Metals (A&M pg. 410)

## Concluding thoughts


