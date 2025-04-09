---
layout: page
title:  "Stress Tensor"
subheadline:  "Cauchy's Stress Theorem"
teaser: "The stress tensor and its properties provide an ideal starting point for an engineering blog focused on solid mechanics. A solid understanding of this tensor facilitates comprehension of concepts such as coordinate transformation, principal stress, and yield criteria."
tags:
    - mechanics
    - analysis
---
<div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-4.columns -->



<div class="medium-8 medium-pull-4 columns" markdown="1">

Stress Vector
---------------------
Most readers are already familiar with the well-known cube that illustrates the stress components. However, this cube is not a physical block of material extracted from the body; rather, it is a convenient representation of the stress field at a point, depicted using three mutually perpendicular planes defined by the base vectors (e1, e2, e3).

![blog_post_images](/post_imgs/post1_img1.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Due to static equilibrium conditions and the absence of body torques, the stress tensor is both real-symmetric. This symmetry ensures that the moments acting on an infinitesimal element are balanced.

![blog_post_images](/post_imgs/post1_img2.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

According to Cauchy's stress theorem, if the stress tensor field at a point is known, its stress vector in a plane defined by normal vector {n} can be calculated with the projection of tensor field on the plane.

![blog_post_images](/post_imgs/post1_img3.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

The stress vector on a cross-section is referred to as the traction vector, {T}. It is defined as the force vector acting on a cross-section divided by the area. The traction vector generally has both normal and tangential components with respect to the plane; in other words, it is not necessarily aligned with the normal vector.

![blog_post_images](/post_imgs/post1_img4.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Principal Stress
---------------------
It is possible to select a plane where the traction vector is parallel to the surface normal, meaning that only normal stresses act on the plane. This condition is described by the following relationship:

![blog_post_images](/post_imgs/post1_img5.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This is an eigenvalue problem. Since the stress tensor is real and symmetric, it has real eigenvalues and orthogonal eigenvectors. To express the solution, two matrices can be defined:
+ V: a matrix whose columns are the eigenvectors
+ Λ: a diagonal matrix containing the eigenvalues
The eigenvectors indicate the principal directions, while the eigenvalues represent the principal stresses. In the principal basis, the stress tensor is diagonal and represents pure normal stresses without any shear components.

![blog_post_images](/post_imgs/post1_img6.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Orthogonality of Eigenvectors
---------------------
It is worth emphasizing the orthogonality of the eigenvectors of real-symmetric matrices, as this property is fundamental to many other applications, such as modal analysis and mode superposition. In fact, finite element analysts frequently work with real-symmetric mass and stiffness matrices that exhibit the same behavior.

Consider two eigenvectors of the stress tensor:

![blog_post_images](/post_imgs/post1_img7.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Taking the dot product of the second eigenvector with the first equation:

![blog_post_images](/post_imgs/post1_img8.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Since [σ] is symmetric:

![blog_post_images](/post_imgs/post1_img9.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Substituting from the second eigenvalue equation:

![blog_post_images](/post_imgs/post1_img10.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Since eigenvalues are distinct, the only solution is:

![blog_post_images](/post_imgs/post1_img11.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This shows that the two eigenvectors must be orthogonal. In matrix form, this orthogonality condition is written as:

![blog_post_images](/post_imgs/post1_img12.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This also implies that the transpose of the orthogonal matrix is equal to its inverse:

![blog_post_images](/post_imgs/post1_img13.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

All eigenvalues and eigenvectors can be expressed simultaneously in the following matrix equation:

![blog_post_images](/post_imgs/post1_img14.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Which also requires:

![blog_post_images](/post_imgs/post1_img15.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This equation represents the transformation of the stress tensor into the eigenbasis (principal basis). Conversely, transforming back to the standard coordinate basis:

Eigenvector matrix V acts as a transformation matrix from eigenbasis to standard coordinate basis, while its transpose performs the reverse transformation. This eigenbasis transformation is a special case of the more general coordinate basis transformation. Mode superposition is an application of this same concept to multidimensional dynamic systems.

![blog_post_images](/post_imgs/post1_img16.jpg){:style="display:block; margin-left:auto; margin-right:auto"}