---
layout: post
title:  "Crystal Lattices"
date:   2015-09-02 6:01:38
categories: lattices structures
---


Now, on to Ashcroft & Mermin Chapter 4


## Starting off

Many materials forms crystals, including metals (despite the appearances you may be used to). All it takes to be a crystal is for the microscopic arrangement of the ions is in a periodic array (or in a series of such arrays, in a polycrystalline state).

We'll consider here purely geometric properties of periodic in 3-D space.

## Bravais Lattice (pg. 64)
The **Bravais lattice** of a crystalline solid specifies the periodic array in which the repeated units of the crystal are arranged.

* The units may be single atoms, groups of atoms, molecules, ions, etc.
* The Bravais lattice summarizes only the geometry of the underlying periodic structure (regardless of what the actual units are)


Here are two definitions given

1. A Bravais lattice is an infinite array of discrete points with an arragement and orientation that appears *exactly* the same, from whichever of the points the array is viewed
2. A (three-dimensional) Bravais lattice consists of all points with position vectors $$R$$ of the form  $$ R = n_1 a_1 + n_2a_2+n_3a_3$$ where $$a_1$$, $$a_2$$, and $$a_3$$ are any three vectors not all in the same plane, and $$n_1$$, $$n_2$$, and $$n_3$$ range through all integral values. Thus the point $$\sum n_i a_i$$ is reached by moving $$n_i$$ steps of length $$a_i$$ in the direction of $$a_i$$ for i = 1,2, and 3.

The vectors in the second definition are the *primitive vectors* and they "generate" or "span" the lattice.

Note that it isn't just the arrangement but also the orientation that is important. 

## Infinite Lattices and Finite Crystals (pg. 66)

By the definition of the Bravais lattice, the lattice must be inifinite - it must appear identical *from all points*. This isn't a huge problem for most real crystals, since the number of points within the bulk of the crystal is so large that most points are far from the surface. The infinite crystal idealization is very useful

Finite crystals are also considered, sometimes for surface effects, sometimes for the convenience of having something smaller than an infite object.


## Further examples and illustrations
While the second definition of the Bravais lattice is more matheamtically rigorous, it has some "minor shortcomings"

* For a given lattice, the set of primitive vectors is non-unique - there are infinitely moany non-equivalent choices
* It is difficult to know or prove that the definition is true

The rest of this sections explains the basics of *how this definition is true*, more or less.

## A note on usage
While the term *Bravais Lattice* is used to describe the set of all points, it is also used to describe the set of vectors joining any of these points to all the others.

An additional use of the term is the set of all translations or displacements that can be described by such vectors.

It is apparently always clear from context what is meant.


## Coordination number
The points in a Bravais lattice closest to a given point are that point's *nearest neighbors*. Clearly, due to the periodic nature of the lattice, each point must have the same number of nearest neighbors. This number is a lattice property, and is known as the **coordination number** of the lattice. 

* A simple cubic lattice has coordination number 6
* A BCC lattice has coordination number 8
* A FCC lattice has coordination number 12

This idea can be extended to other, non Bravais lattices as long as there is sufficient symmetry such that each point still has the same number of nearest neighbors.


## Primitive Unit Cell
**Primitive cell** (or primitive unit cell) - A volume of space that, when translated through all the vectors in a Bravais lattice, just fills all of space without either overlapping itself or leaving voids.

There is no unique way of choosing a prmitive cell for a given Bravais lattice.

A primitive cell must contain precisely one lattice point, though it may be positioned to have points on its surface).

It is often important to work with cells that have the full symmetry of their Bravais lattice, and ther eare two widely used solutions to this problem, which will be disussed:

* Conventional unit cell
* Wigner-Seitz Primitive Cell



## (Conventional) Unit Cell (pg 73)
**Unit Cell** a region that just fills space without any overlapping when translated through a subset of the vectors in the Bravais lattice.

The conventional unit cell is generally larger than the primitive cell, and is chosen to have the appropriate symmetry.


## Wigner-Seitz Primitive Cell

An alternative is to choose a primitive cell with the full symmetry of the Bravais lattice. The most common way of doing this is with a [**Wigner-Seitz Cell**](https://en.wikipedia.org/wiki/Wigner%E2%80%93Seitz_cell). It is the region of space that is closer to a given lattice point than any other point (and will naturally take the shape of the lattive).


## Crystal Structure; Lattice with a Basis

An actual physical crystal has not just an associated Bravais lattice, but also a particular arrangement of atoms, molecules, ions, etc. within a primitive cell. 



## Important Examples of Crystal Structures

A nice resource to look at a variety of examples is on the [Wolfram Demonstrations Project](http://demonstrations.wolfram.com/CubicCrystalLattices/).


### Diamond structure
The [diamond lattice](https://en.wikipedia.org/wiki/Diamond_cubic) consists of the interpenetrating FCC Bravais lattices displaced along the body diagonal of the cubic cell by one quarter the length of the diagonal. There is a nice demo of this available [here](http://demonstrations.wolfram.com/TheStructureOfDiamond/).

A few different elements can crystallize in a diamond structure: carbon, silicon, germanium, $$\alpha$$-tin, and probably others. The difference in these materials is in the cube side length, the lattice parameter.

<!--
({{site.base_url}}/{{site.url}}/{% post_url 2015-08-28-Why-is-it-solid %})

[overview]({{site.base_url}}{% post_url 2015-08-27-Overview-what-is-a-solid %})
-->

## Concluding thoughts
This chapter looked at the translational symmetries of lattices. In the next post, we'll look at rotational symmetries.


