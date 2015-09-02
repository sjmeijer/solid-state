---
layout: post
title:  "Classification of Solids"
date:   2015-08-27 16:01:38
categories:  overview solids 
---


Starting off then we'll look at Ashcroft and Mermin, Chapter 19. 


# Classification of Solids
Solids may be classified according to their symmetric geometrical structures, as is most obvious with crystals. It is notable that even within each of the seven basic [crystal systems](https://en.wikipedia.org/wiki/Crystal_system) (think monoclinic, triclinic, cubic, etc.) there are significant *physical* differences; each crystal system contains specimens which have wildly varying electrical, mechanical, and optical properties.

 So, in additional to classifying based on these geometric symmetries, we can choose to look at the physical properties of solids, which is based off of the valence electrons.
 
The primary distinction here is between __metals__ and __insulators__. 

* Metals have partially filled energy bands
* Insulators do not have any partially filled energy bands

It is perhaps worthwhile to clarify what is meant by [energy bands](https://en.wikipedia.org/wiki/Electronic_band_structure) here. Recall when solving for the energy levels of some quantum system, say the  particle in a box/well, that the allowed energys are discrete values, referred to as __energy levels__. In a multi-well system, there are more allowed energies. As the number of wells increases, the number of allowed energies also increases, and has the effect of smearing the discrete energy level into a __band___ of allowed values since they overlap (presumably the width is thermal?). Normally, we consider an infinite number of wells (or atoms), which is reasonably-justified for any macroscopic system. If you lack an intutiion for band structure in this way, I strongly encourage you to try out the [PhET on Band Structure](https://phet.colorado.edu/en/simulation/band-structure).


{% include image.html url="Finite_vs_Infinite_Square_Well_Energies_(75eV,_0.4nm).png" description="The discrete energy levels of a finite and infinite square well, taken from wikipedia. For a solid composed of a bunch of finite wells, each level would be smeared out." %}
{% include space.html %}

The distinction between metals and insulators is not clear merely from the spatial distribution of electrons (that is, in real space). Perhaps vaguely, the distribution of electrons in metals is less concentrated in the "ion cores" as in insulators (electrons are shared), but as A&M point out, this is not a rigorous definition of the difference, and they lead us back to looking at it in k-space, also known as [__reciprocal lattice space__](https://en.wikipedia.org/wiki/Reciprocal_lattice).

The distinction between metals and insulators is in the distribution of electrons in k-space.


## The Classification of insulators

There are, broadly, three kinds of insulators. While for any given material, there is a some fair ability to claim it has aspects of each of these three, we can at least describe the prototypical varieties, and then describe materials in terms of these.

###1. Covalent Crystals
Covalent crystals 

###2. Molecular Crystals
These are not necessarily comprised of "molecules", *per se*. A molecular crystal is just a crystalline substance in which the crystal is pretty much the same as the individual molecules in the crystal. The configuration is only slightly perturbed by being put into a solid. Each molecule has completely filled electronic shells. For this reason, solid noble gases form molecular crystals -- they have filled shells.

###3. Ionic Crystals
Ionic crystals are composed of a metallic and nonmetallic element. Unlike in a molecular crystal, where the electrons are effectively bound to the "molecule", in an ionic crystal, some of the electrons *stray* to the partnering atoms. The local entities are electrically charged ions, and the electrostatic forces between the ions play a large pat in determining the properties of the solid.



## Ionic Crystals
Continuing on, A&M go a bit deeper on ionic crystals, giving a discussion of **alkali halides** (I-VII ionic crystals),  **II-VI Ionic crystals**, and **III-V crystals** (mixed ionic and covalent).

Briefly, alkali halides are relatively ideal ionic crystals, which essentially act like a set of spherical ions packed together.


II-VI Ionic Crystals are composed of doubly-ionized elements from columns II and VI of the periodic table, and are less ideally-ionic that the II-VI crystals.

III-V crystals pair elements from columns III and V of the periodic table, and are even less ideally-ionic. They are mostly semiconductors, rather than insulators (small band gaps).

> They are conventionally described as primarily covalent, with some residual concentration of excess charge about the ion cores.



## Covalent Crystals
Not as good of insulators as ionic crystals, as you might expect from the delocalized charge in a covalent bond. All semiconductors are coalent crystals with some small amount of ionic bonding. 

##Molecular Crystals
Since molecular crystals are electrically neutral and stable, they are held together by *van der Waals* or *fluctuating dipole* forces. 


##Metals
Metals are found to the left of column IV in the periodic table. Here, the covalent bond expands until the electron density is appreciable in the interstitial regions (between atoms/molecules) -- in k-space, this is "appreciable band overlap".

## Hydrogen-bonded crystals
This is sometimes listed as a "fourth category of insulator". Hydrogen has a few properties which make it unique:
1. The ion core is a bare single proton (very small)
2. Hydrogen is only 1 electron away from the stable helum configuration of 2 electrons (not 8)
3. The first ionization potential of atomic H is unusually high compared to other similar atoms

Due ot the high ionization potential, electrons are difficult to remove, so it doesn't behave like the alkali metal ions and form ionic crystals. 

On the other hand, it can't act like acovalent crystal because it can form only one covalent bond through electron sharing (unlike the 4 bonds in most, from a valence shell of 8 electrons).

Finally, the small size of the proton means that

> it can essentially sit on the surface of the large negative ions, resulting in a type of structure unattainable with any other positive ion.




## Conclusion
This is it for now on this topic. Next time we'll look at Chapter 20 of A&M.

