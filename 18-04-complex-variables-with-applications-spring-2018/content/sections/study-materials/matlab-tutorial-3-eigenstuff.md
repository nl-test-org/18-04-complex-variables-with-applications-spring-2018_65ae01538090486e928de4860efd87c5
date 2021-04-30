---
course_id: 18-04-complex-variables-with-applications-spring-2018
layout: course_section
menu:
  leftnav:
    identifier: ab7a0e0875fca007c7b375e6fba2af72
    name: 'MATLAB Tutorial 3: Eigenstuff'
    parent: 895a48216cfecadfafd6973524d079f5
    weight: 90
parent_title: Study Materials
title: 'MATLAB Tutorial 3: Eigenstuff'
type: course
uid: ab7a0e0875fca007c7b375e6fba2af72

---

Time
----

We estimate this tutorial will take 10 minutes. That includes time for a bit of playing around with the commands.

Conventions
-----------

% This is an edited transcript of a MATLAB session.  
% We've inserted comment lines, which begin with a '%'.

_Command lines_ begin with a '>'. When copying a command you should enter everything after the '>' and hit return. MATLAB's response will be shown in the line or lines below the command.

**Trick:** you can use the up arrow to find previous commands. If you type the first letter of the command then the up arrow will only show previous commands that start with that letter.

Finding eigenstuff: the eig function
------------------------------------

Given a square matrix the eig function returns eigenstuff.

`% Our favorite 2 x 2 matrix`

> `> A = [6 5; 1 2]  
> A =  
>     6   5  
>     1   2`

`% The eig function returns the eigenvalues:`

> `> eig(A)  
> ans =  
>       7  
>       1`

`% To get the eigenvectors and eigenvalues use the following syntax:`

> `> [S,D] = eig(A)  
> S =  
>     0.98058   -0.70711  
>     0.19612   0.70711  
> D =  
>     Diagonal Matrix  
>     7   0  
>     0   1`

`% Matlab put the eigenvectors as the columns of S and the eigenvalues in the diagonal matrix D. Notice that S is not guaranteed to have nice (to humans) columns like [5 1]' or [1 -1]'`

`% You can check the diagonalization formula:`

> `> S*D*S^(-1)  
> ans =  
>       6   5  
>       1   2`