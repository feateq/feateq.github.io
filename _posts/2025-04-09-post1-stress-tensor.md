---
layout: page-fullwidth
title:  "Stress Tensor"
subheadline:  "Cauchy's Stress Theorem"
teaser: "The stress tensor and its properties provide an ideal starting point for an engineering blog focused on solid mechanics. A solid understanding of this tensor facilitates comprehension of concepts such as coordinate transformation, principal stress, and yield criteria."
image:
    thumb:  post1_thumb.png
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

*Ref: Khennane A., Introduction to Finite Element Analysis Using Matlab and Abaqus*{: .right}<br> 

Due to static equilibrium conditions and the absence of body torques, the stress tensor is both real-symmetric. This symmetry ensures that the moments acting on an infinitesimal element are balanced.

![blog_post_images](/post_imgs/post1_img2.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

According to Cauchy's stress theorem, if the stress tensor field at a point is known, its stress vector in a plane defined by normal vector {n} can be calculated with the projection of tensor field on the plane.

![blog_post_images](/post_imgs/post1_img3.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

*Ref: Khennane A., Introduction to Finite Element Analysis Using Matlab and Abaqus*{: .right}<br> 

The stress vector on a cross-section is referred to as the traction vector, {T}. It is defined as the force vector acting on a cross-section divided by the area. The traction vector generally has both normal and tangential components with respect to the plane; in other words, it is not necessarily aligned with the normal vector.

![blog_post_images](/post_imgs/post1_img4.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Principal Stress
---------------------
It is possible to select a plane where the traction vector is parallel to the surface normal, meaning that only normal stresses act on the plane. This condition is described by the following relationship:

![blog_post_images](/post_imgs/post1_img5.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This is an eigenvalue problem. Since the stress tensor is real and symmetric, it has real eigenvalues and orthogonal eigenvectors. To express the solution, two matrices can be defined:
+ \[V\]: a matrix whose columns are the eigenvectors
+ \[Λ\]: a diagonal matrix containing the eigenvalues

The eigenvectors indicate the principal directions, while the eigenvalues represent the principal stresses. In the principal basis, the stress tensor is diagonal and represents pure normal stresses without any shear components.

![blog_post_images](/post_imgs/post1_img6.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Orthogonality of Eigenvectors
---------------------
It is worth emphasizing the orthogonality of the eigenvectors of real-symmetric matrices, as this property is fundamental to many other applications, such as modal analysis and mode superposition. In fact, finite element analysts frequently work with real-symmetric mass and stiffness matrices that exhibit the same behavior.

Consider two eigenvectors of the stress tensor:

![blog_post_images](/post_imgs/post1_img7.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Taking the dot product of the second eigenvector with the first equation:

![blog_post_images](/post_imgs/post1_img8.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Since \[σ\] is symmetric:

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

![blog_post_images](/post_imgs/post1_img16.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Eigenvector matrix \[V\] acts as a transformation matrix from eigenbasis to standard coordinate basis, while its transpose performs the reverse transformation. This eigenbasis transformation is a special case of the more general coordinate basis transformation. Mode superposition is an application of this same concept to multidimensional dynamic systems.

Coordinate Transformation
---------------------
Let us assume that the standard basis vectors are {e1, e2, e3} and we want to express vectors and tensors in another coordinate system defined by {e1’, e2’, e3’}. The rotation matrix between these two bases is defined by using directional cosines between unit vectors as shown in \[Q\]. Alternatively, a sequence of rotations about yaw, pitch, and roll axes can also be used to define a general 3D rotation. Rotation matrices are orthogonal.

![blog_post_images](/post_imgs/post1_img17.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

In Cartesian coordinates, the standard basis \[E\] is simply the identity matrix:

![blog_post_images](/post_imgs/post1_img18.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Unit vectors of transformed basis can be arranged in matrix form as:

![blog_post_images](/post_imgs/post1_img19.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Transformation matrix can also be expressed using these unit vectors:

![blog_post_images](/post_imgs/post1_img20.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Now, consider a vector {u} defined in the standard coordinate system. Its representation in the new coordinate system is:

![blog_post_images](/post_imgs/post1_img21.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

The transformation of a second-order tensor, such as the stress tensor, into the new coordinate system is given by:

![blog_post_images](/post_imgs/post1_img22.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This is the same equation used during transformation into the eigenbasis.

Stress Invariants
---------------------
The characteristic equation of the tensor is used in the solution of eigenvalue problem.

![blog_post_images](/post_imgs/post1_img23.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

The invariants of the stress tensor in index notation are defined as follows:

![blog_post_images](/post_imgs/post1_img24.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Stress invariants are invariant under a change of coordinate basis. They can also be computed using the principal stresses:

![blog_post_images](/post_imgs/post1_img25.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

I1 is related to hydrostatic stress. A key property of I1 is:

![blog_post_images](/post_imgs/post1_img26.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

On the other hand, I2 is associated with the deviatoric part of the stress tensor. The hydrostatic stress tensor represents a mean stress that tends to change the volume of the stressed body, while the stress deviator tensor contributes to the distortion (shearing) of the body.

Deviatoric Stress
---------------------
The deviatoric stress tensor is obtained by removing the mean hydrostatic stress from the stress tensor. It represents the pure shear behavior of a stress field.

![blog_post_images](/post_imgs/post1_img27.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

The invariants of the deviatoric stress tensor \[S\] are:

![blog_post_images](/post_imgs/post1_img28.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Von Misses Equivalent Stress
---------------------
J2 is particularly important because it is used in the definition of Von Misses equivalent stress, which is a scalar value of stress that can be computed from the stress tensor. The Von Mises Yield Criterion, also known as the J2 Yield Criterion, states that a material begins to yield when the von Mises stress reaches the material's yield strength. It is used to relate a general stress field to the material data obtained from uniaxial tensile tests.

The expression for J2 in terms of the standard stress components is:

![blog_post_images](/post_imgs/post1_img29.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

In terms of the principal stresses, J2 can be written as:

![blog_post_images](/post_imgs/post1_img30.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Finally, the von Misses Equivalent Stress is:

![blog_post_images](/post_imgs/post1_img31.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

Alternatively, in terms of the stress components:

![blog_post_images](/post_imgs/post1_img32.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

In terms of the principal stresses:

![blog_post_images](/post_imgs/post1_img33.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

An important observation can be made by comparing the conditions of pure uniaxial tension and shear. For these conditions:

![blog_post_images](/post_imgs/post1_img34.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

When the same magnitude of stress is applied in both conditions, the shear specimen will yield earlier. The ratio of the yield strengths of the material under these two load conditions is:

![blog_post_images](/post_imgs/post1_img35.jpg){:style="display:block; margin-left:auto; margin-right:auto"}

This indicates that a material can carry nearly half the shear load compared to the tension load before yielding. A comparison of material tests using different yield criteria is shown in the graph below.

![blog_post_images](/post_imgs/post1_img36.jpg){:style="display:block; margin-left:auto; margin-right:auto"}
*Ref: Dowling, N.E., Mechanical Behavior of Materials*{: .right}<br> 

Example Calculations
---------------------
Below is an example of a MATLAB/Octave code that performs the necessary calculations for Von Mises stress and the invariants of the stress tensor.

<pre><code>
clc
%define a stress tensor
S=[100 50 30; 50 150 40; 30 40 120]

%calculate principal stresses and directions
[V,L]=eig(S);
%sort eigenvalues
B=diag(L);
[C,I] = sort(B,'descend');
Prin_Stress=diag(C)
Prin_Direct=V(:,I)

%calculate I1
I1=sum(diag(L))

%Calculate J2
J2=1/6*((L(1,1)-L(2,2))^2+(L(2,2)-L(3,3))^2+(L(1,1)-L(3,3))^2)

%Calculate Von Misses Stress
Von_Miss_Stress=sqrt(3*J2)
</code></pre>

The output of the code would be:

![blog_post_images](/post_imgs/post1_img38.jpg){:style="display:block; margin-left:auto; margin-right:auto"}




