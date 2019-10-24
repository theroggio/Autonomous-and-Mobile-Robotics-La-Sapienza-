# Chapter 12

## Problem 12.1

First we know that a unicycle needs three coordinates, two for its position and one for the orientation. 
Then on top of the unicycle we must address the coordinates for the manipulator with 6 dof. Remembering from the theory we know that 
a manipulator in 3D with n dof needs **n** coordinates, we can say the exactly same thing here.

The final vector for the genralized coordinates is 

<a href="https://www.codecogs.com/eqnedit.php?latex=q&space;=&space;\begin{bmatrix}&space;x_u&space;&&space;y_u&space;&&space;\theta_u&space;&&space;\theta_0&space;&&space;...&space;&&space;\theta_N&space;\end{bmatrix}^T" target="_blank"><img src="https://latex.codecogs.com/gif.latex?q&space;=&space;\begin{bmatrix}&space;x_u&space;&&space;y_u&space;&&space;\theta_u&space;&&space;\theta_0&space;&&space;...&space;&&space;\theta_N&space;\end{bmatrix}^T" title="q = \begin{bmatrix} x_u & y_u & \theta_u & \theta_0 & ... & \theta_N \end{bmatrix}^T" /></a>

The configuration space is 

<a href="https://www.codecogs.com/eqnedit.php?latex=\mathit{C}&space;=&space;\mathbb{R}^2&space;\times&space;SO(2)&space;\times&space;(SO(3))^6" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mathit{C}&space;=&space;\mathbb{R}^2&space;\times&space;SO(2)&space;\times&space;(SO(3))^6" title="\mathit{C} = \mathbb{R}^2 \times SO(2) \times (SO(3))^6" /></a>

Where the first two compoenents are the ones of the unicycle (which moves and rotates in the 2D space) the others are from the manipulator in the 3D space. 

## Problem 12.2

We need to keep in mind that after 2pi it's like we're starting back from zero. The two configuration vectors have components 1 and 2 with this property so we could say that, for them the distance should be computed as

<a href="https://www.codecogs.com/eqnedit.php?latex=d_2&space;(q_A,q_B)_i&space;=&space;\left&space;\|mod(q_A(i),2\pi)&space;-&space;mod(q_B(i),2\pi)&space;\right&space;\|" target="_blank"><img src="https://latex.codecogs.com/gif.latex?d_2&space;(q_A,q_B)_i&space;=&space;\left&space;\|mod(q_A(i),2\pi)&space;-&space;mod(q_B(i),2\pi)&space;\right&space;\|" title="d_2 (q_A,q_B)_i = \left \|mod(q_A(i),2\pi) - mod(q_B(i),2\pi) \right \|" /></a>

where i is the index of the component, and **mod** is the function computing the rest of the euclidean division, so it's a number always minor of 2pi.

## Problem 12.3

We want to prove that with different obstacles and robots, we can have the same C-shape for the obstacle. 

Let's start from a triangular robot and a squared obstacle, the C-obstalce will have a difference on one of the sides creating a sort of trapezoid attached to the basis.

The same shape can be obtained using the C-shape just obtained as shape of the obstacle and a squared robot. Being careful with the sized of robots and obstacles we can easily visualize that the final C-obstacles will be the same.

## Problem 12.4

First of all our configuration vectors have two components for the two angles of the links of the robot. The center is indeed fixed in the center of the image. 
To have a batter idea of which parts of the free space are connected we could just copy and paste the square of the C space in all possible directions.

Obtaining three configuration from this is super easy, we just need to pick a point and see its q1 and q2 values from the axes. 

For example (0,0) is in the same connected space to (2pi - epislon, 2pi - epislon) and (pi, pi/2) even if in the first image we have it's not like that. 
