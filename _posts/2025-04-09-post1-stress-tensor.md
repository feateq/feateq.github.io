---
layout: page
title:  "Stress Tensor"
subheadline:  "Cauchy's Stress Theorem"
teaser: "The stress tensor and its properties provide an ideal starting point for an engineering blog focused on solid mechanics. A solid understanding of this tensor facilitates comprehension of concepts such as coordinate transformation, principal stress, and yield criteria."
tags:
    - mechanics
    - analysis
---
Stress Vector
---------------------
Most readers are already familiar with the well-known cube that illustrates the stress components. However, this cube is not a physical block of material extracted from the body; rather, it is a convenient representation of the stress field at a point, depicted using three mutually perpendicular planes defined by the base vectors (e1, e2, e3).

![blog_post_images](/post_imgs/post1_img1.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Due to static equilibrium conditions and the absence of body torques, the stress tensor is both real-symmetric. This symmetry ensures that the moments acting on an infinitesimal element are balanced.

$$
\sigma_{ij} = \sigma_{ji}
$$

According to Cauchy's stress theorem, if the stress tensor field at a point is known, its stress vector in a plane defined by normal vector {n} can be calculated with the projection of tensor field on the plane.

![blog_post_images](/post_imgs/post1_img3.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

The stress vector on a cross-section is referred to as the traction vector, {T}. It is defined as the force vector acting on a cross-section divided by the area. The traction vector generally has both normal and tangential components with respect to the plane; in other words, it is not necessarily aligned with the normal vector.

$$
\mathbf{T} = [\boldsymbol{\sigma}]^T \mathbf{n} = [\boldsymbol{\sigma}] \mathbf{n}
$$

Principal Stress
---------------------
It is possible to select a plane where the traction vector is parallel to the surface normal, meaning that only normal stresses act on the plane. This condition is described by the following relationship:

![blog_post_images](/post_imgs/post1_img5.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This is an eigenvalue problem. Since the stress tensor is real and symmetric, it has real eigenvalues and orthogonal eigenvectors. To express the solution, two matrices can be defined:
* [V]: a matrix whose columns are the eigenvectors
* [Λ]: a diagonal matrix containing the eigenvalues
The eigenvectors indicate the principal directions, while the eigenvalues represent the principal stresses. In the principal basis, the stress tensor is diagonal and represents pure normal stresses without any shear components.

![blog_post_images](/post_imgs/post1_img6.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

