---
layout: post
title:  "The Reciprocal Lattice"
date:   2015-09-06 12:00:01
categories: lattice
---

**Reciprocal lattices** are an important concept that come up quite a lot in solid state, and having a good understanding of it is important. 

This concept is covered in Chapter 5 of Ashcroft and Mermin.

This concept is apparently confusing to many students, but deep down, it's really a pretty simple idea requiring only some knowledge of Fourier transforms.

## The concept
To start off, it's worth it to watch this short video:

[![IMAGE ALT TEXT](http://img.youtube.com/vi/DFFU39A3fPY/0.jpg)](http://www.youtube.com/watch?v=DFFU39A3fPY "Crystallograph and Reciprocal Space")

An additional way to buld some intuition is to try this out:
[2D Reciprocal Lattice on Wolfram Demonstrations](http://demonstrations.wolfram.com/ReciprocalLattice2D/).

<script type='text/javascript' src='http://demonstrations.wolfram.com/javascript/embed.js' ></script><script type='text/javascript'>var demoObj = new DEMOEMBED(); demoObj.run('ReciprocalLattice2D', '', '473', '595');</script><div id='DEMO_ReciprocalLattice2D'><a class='demonstrationHyperlink' href='http://demonstrations.wolfram.com/ReciprocalLattice2D/' target='_blank'>Reciprocal Lattice 2D</a> from the <a class='demonstrationHyperlink' href='http://demonstrations.wolfram.com/' target='_blank'>Wolfram Demonstrations Project</a> by P. Fraundorf</div><br />

It does most of the same things that were shown in the video, but it gives you the ability to control it, which can be nice.


Maybe watch it a few times, but the idea is pretty straightforward - the *reciprocal lattice* is an additional lattice which contains the information of the real lattice, with point spacing in the reciprocal space directly related to the spacing in real physical space. More specifically, the reciprocal lattice is the fourier transform of the direct lattice, though this doesn't seem to be the "standard" way of introducing the idea. An interesting [AJP article](http://dx.doi.org/10.1119/1.18243) argues for teaching it in this way. I will closely follow the method of this paper in my attempt to explain the reciprocal lattice.



So why is this a useful idea? It comes up in a significant way in x-ray diffraction of crystals, where you are usually working to guess what the real physical lattice is like based on what the "shadow" of it looks like. 





## The definition

We'll follow a relatively formal calculation here, but the general idea is that, we know a lattice is periodic, so it's a natural thing to take the Fourier transform. You know it has some structure in space, and a fourier transform will tell you something about what that structure is - in particular, we already know that the Fourier transform will give us information about the 


#### The Fourier Transform

Recall the [Fourier transform](https://en.wikipedia.org/wiki/Fourier_transform). 
\begin{equation}
	\mathscr{F} [ f(x) ] = \int f(x) e^{i k x } dx
\end{equation}

We'll make use of the slightly more general vector form
\begin{equation}
	\mathscr{F} [ f(\vec r) ] = F(\vec k) = \int\limits_{\infty} f(\vec r) e^{i \vec k\cdot \vec r } d^{N}\vec r
\end{equation}
This definition is harder than it should be to Google/wiki your way into, for some reason (if you disprove me, please, share). There are some vexatious factors of $$(2\pi)^{N}$$ that get added for normalization - some people put them in the definition of the transform, some divide it out in the inverse transform. I choose to divide it out in the inverse, but it's all the same, as long as you're consistent.


#### Applying this to a lattice

Our lattice is an array of atoms, which we can treat as being spatially located at points - effectively delta functions. 
For an array of delta functions separated by length $$a$$, we have
\begin{equation}
	\mathscr{F} \left[ \sum\limits_{n=-\infty}^{\infty} \delta(x-na) \right] = \sum\limits_{n=-\infty}^{\infty} \delta(k-\frac{2\pi n}{a})
\end{equation}

The Fourier transformed array is itself an array of delta functions, but with a different spacing ($$2\pi/a$$ in fourier/reciprocal space, instead of $$a$$ in direct space). It is clear from this why we would call this a "reciprocal" lattice, since the spacing is just reciprocally related to the direct-space particle spacing.

Recall also the *shift theorem*. It says that when we shift a function by some amount $$x_0$$, we multiply the transform by a phase factor $$e^{i k x_0}$$. Let's say it mathematically as
\begin{equation}
	\mathscr{F} [ f(x + x_0) ] = 	\mathscr{F} [ f(x) ] e^{i k x_0 }
\end{equation}
So we pick up a constant phase factor $$e^{ikx_0}$$ if we spatially shift the function by $$x_0$$.

If we use the primitive vectors $$a$$, $$b$$, and $$c$$ of the Bravais lattice as a basis, we can write any vector $$r$$ as
\begin{equation}
	r = r_a \vec a + r_b \vec b + r_c \vec c.
\end{equation} 
which makes the 3D **Bravais lattice** describable by 

\begin{equation}
Bravais: \sum\limits_{n_a,n_b,n_c}\delta^3(\vec r - n_a \vec a - n_b \vec b - n_c \vec c) 
= \sum\limits_{n_a}\delta(r_a - n_a \vec a)
\sum\limits_{n_b}\delta(r_b - n_b \vec b)
\sum\limits_{n_c}\delta(r_c - n_c \vec c)
\end{equation}

That's a mathematical convenience, that we can split the 3-dimensional delta function into a product of 3 1-dimensional delta functions. 

To take the Fourier transform of this, we we'll need the scalar product $$ k\cdot r$$. For additional convenience, we'l write $$\vec k$$ in terms of three undefined vectors $$\vec A$$, $$\vec B$$, and $$\vec C$$.
\begin{equation}
	\vec k = k_A \vec A + k_B \vec B  + k_C \vec C.
\end{equation}

It is then possible to calculate $$ k\cdot r$$ without much trouble. See the [Thompson AJP paper](http://dx.doi.org/10.1119/1.18243) equation 10 for the full expression, or [work it out yourself](https://en.wikipedia.org/wiki/Dot_product). If we make the requirement that $$\vec  A$$ be perpendicular to both $$\vec b$$ and $$\vec c$$, and also the other 2 obvious permutations ($$\vec B\perp \vec a, \vec c$$ and $$\vec C \perp \vec a, \vec b$$), the full $$ k\cdot r$$ boils down to

\begin{equation}
	\vec k \cdot \vec r = \vec A \cdot \vec a k_a r_a + \vec B \cdot \vec b k_b r_b  + \vec C \cdot \vec c k_c r_c 
\end{equation}


The Fourier transform of the Bravais lattice defined above then is 

\begin{equation}
	\mathscr{F} [ \sum\limits_{n_a,n_b,n_c}\delta^3(\vec r - n_a \vec a - n_b \vec b - n_c \vec c)  ] 
	= \sum\limits_{n_a}\delta\left(k_A - \frac{2\pi n_a}{a}\right)
	\sum\limits_{n_b}\delta\left(k_B - \frac{2\pi n_b}{b}\right)
	\sum\limits_{n_c}\delta\left(k_C - \frac{2\pi n_c}{c}\right)
\end{equation}

This also a Bravais lattice. Instead of having the points separated by distances $$a$$, $$b$$, and $$c$$, however, this lattice has point separation of $$2\pi/a$$, $$2\pi/b$$, and $$2\pi/c$$ in the directions of $$\vec A$$, $$\vec B$$, and $$\vec C$$, respectively.

We still haven't explicitly said what $$\vec A$$, $$\vec B$$, and $$\vec C$$ actually are though. 
We have enough information now to find them, though! 
We required that they have some mutual perpendicularity, described above. 
Additionally, we know that they must have lengths of the lattice separations ($$2\pi/x$$), so we can say
\begin{equation}
	\vec A = \frac{2\pi \vec b \times \vec c}{\vec a \cdot \vec b \times \vec c}
\end{equation}
The other two vectors come by the obvious permutations. 
If it isn't clear exactly which direction this is supposed to be pointing, it's in the $$\vec b \times \vec c$$ direction, and the rest is all scaling the size of it. 
If the vectors were all unit in length, for example, it would be $$2\pi$$ in length.
{% include image.html url="throwin.png" description="Classic wikipedia gang signs" %}
{% include space.html %}

So now we have a set of reciprocal lattice vectors, and all we need is the direct-space lattice vectors. 
If you had looked it up on wikipedia (or in Ashcroft and Mermin), these vectors are somewhat magically just given to you. 
Don't allow this to convince you that these are more complicated or axiomatic!


#### Some thoughts

A (very mildly) interesting thing here is that the fourier transform is defined for an infinitely repeating lattice, but of course no lattice is infinitely large. 
So, this is a slightly idealized situation, though practically every real solid is large enough to not be able to differentiate between these cases.

