# Midterm 2017 / 2018

## Problem 1

### Controllability of the system

We can study the controllability using the theorem on the Lie Brackets, so we need to compute the null space of the constraints matrix. It's easy to see from the kinematic model that 

<img src="https://latex.codecogs.com/gif.latex?g_1&space;=&space;\begin{pmatrix}&space;q_2&space;\\&space;-q_1&space;\\&space;0&space;\end{pmatrix}\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;q_3&space;\\0&space;\\&space;-q_1&space;\end{pmatrix}" title="g_1 = \begin{pmatrix} q_2 \\ -q_1 \\ 0 \end{pmatrix}\hspace{0.5cm} g_2 = \begin{pmatrix} q_3 \\0 \\ -q_1 \end{pmatrix}" />

so we just need to compute the first Lie Bracket, if it's linearly independent from g1 and g2 the system is controllable, otherwise is not.

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;[g1,g2]&space;=&space;\frac{\partial&space;g_2}{\partial&space;q}&space;g_1&space;-&space;\frac{\partial&space;g_1}{\partial&space;q}&space;g_2&space;=&space;\\&space;=&space;\begin{bmatrix}&space;0&space;&&space;1&space;&&space;0&space;\\&space;-1&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;\end{bmatrix}&space;\begin{pmatrix}&space;q_2&space;\\&space;-q_1&space;\\&space;0&space;\end{pmatrix}&space;-&space;\begin{bmatrix}&space;0&space;&&space;0&space;&&space;1&space;\\&space;0&space;&&space;0&space;&&space;0&space;\\&space;-1&space;&&space;0&space;&&space;0&space;\end{bmatrix}&space;\begin{pmatrix}&space;q_3&space;\\0&space;\\&space;-q_1&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;0&space;\\&space;-q_2&space;\\&space;q_3&space;\end{pmatrix}" title="[g1,g2] = \frac{\partial g_2}{\partial q} g_1 - \frac{\partial g_1}{\partial q} g_2 = \\ = \begin{bmatrix} 0 & 1 & 0 \\ -1 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} \begin{pmatrix} q_2 \\ -q_1 \\ 0 \end{pmatrix} - \begin{bmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ -1 & 0 & 0 \end{bmatrix} \begin{pmatrix} q_3 \\0 \\ -q_1 \end{pmatrix} = \begin{pmatrix} 0 \\ -q_2 \\ q_3 \end{pmatrix}" />

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;\left&space;|&space;\begin{matrix}&space;0&space;&&space;-q_2&space;&&space;q_3&space;\\q_3&space;&&space;0&space;&&space;-q_1&space;\\&space;q_2&space;&&space;-q_1&space;&&space;0&space;\end{matrix}&space;\right&space;|&space;=&space;0" title="\left | \begin{matrix} 0 & -q_2 & q_3 \\q_3 & 0 & -q_1 \\ q_2 & -q_1 & 0 \end{matrix} \right | = 0" />

This means the system is **not controllable**. 

### Differential constraint and holonomy

First, from the previous point we know the system is not controllable so the constraint is integrable and holonomic.

From the kinematic model we can isolate the inputs **u** and put them in the first equation which becomes

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;q_1&space;\dot{q_1}&space;&plus;&space;q_2&space;\dot{q_2}&space;&plus;&space;q_3&space;\dot{q_3}&space;=&space;0" title="q_1 \dot{q_1} + q_2 \dot{q_2} + q_3 \dot{q_3} = 0" />

Which is indeed integrable as

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;q_1^2&space;&plus;&space;q_2^2&space;&plus;&space;q_3^2&space;=&space;c" title="q_1^2 + q_2^2 + q_3^2 = c" />

where **c** is the summation of the squared initial values of the three variables. In fact integrating between 0 - T we have that that the squared qi are the initial constant values.

### Geometric description of the mobility

Globally we're constrained to move on a sphere with center in the origin and passing through the initial configuration. Locally, writing the constraint in Pfaffian form, it's easy to see the velocities live in a plane tangent the sphere in the specific configuration point for every point.

## Problem 2

### Plan a trajectory

We know the geometric model of the unicycle, we can use more than one approach to solve the problem. One of them is using flat outputs which we know are x and y. 

So we use a cubic polynomial for x(s) and y(s), using the boundaries conditions:

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;\\x(0)&space;=&space;0&space;\hspace{2.25cm}&space;y(0)&space;=&space;0&space;\\&space;x(1)&space;=&space;1&space;\hspace{2.25cm}&space;y(1)&space;=&space;1&space;\\&space;\dot{x}(0)&space;=&space;v_i&space;cos\theta_i&space;=&space;v_i&space;\hspace{0.5cm}&space;\dot{y}(0)&space;=&space;v_i&space;sen\theta_i&space;=&space;0&space;\\&space;\dot{x}(1)&space;=&space;v_f&space;cos\theta_f&space;=&space;0&space;\hspace{0.5cm}&space;\dot{y}(1)&space;=&space;v_f&space;sen\theta_f&space;=&space;v_f" title="\\x(0) = 0 \hspace{2.25cm} y(0) = 0 \\ x(1) = 1 \hspace{2.25cm} y(1) = 1 \\ \dot{x}(0) = v_i cos\theta_i = v_i \hspace{0.5cm} \dot{y}(0) = v_i sen\theta_i = 0 \\ \dot{x}(1) = v_f cos\theta_f = 0 \hspace{0.5cm} \dot{y}(1) = v_f sen\theta_f = v_f" />

The initial and ending velocities must be with the same sign, but have no other limits. For now let's say they're equal to each other with value **k**. Imposing the boundary conditions we obtain

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;\\&space;x(s)=&space;(k-2)s^3&space;&plus;&space;(3-2k)s^2&space;&plus;&space;ks&space;\hspace{0.5cm}&space;y(s)=&space;(k-2)s^3&space;&plus;&space;(3-k)s^2&space;\\&space;\dot{x}(s)=&space;3(k-2)s^2&space;&plus;&space;2(3-2k)s&space;&plus;&space;k&space;\hspace{0.46cm}&space;\dot{y}(s)=&space;3(k-2)s^2&space;&plus;&space;2(3-k)s&space;\\&space;\ddot{x}(s)=&space;6(k-2)s&space;&plus;&space;2(3-2k)&space;\hspace{1.5cm}&space;\ddot{y}(s)=&space;6(k-2)s&space;&plus;&space;2(3-k)" title="\\ x(s)= (k-2)s^3 + (3-2k)s^2 + ks \hspace{0.5cm} y(s)= (k-2)s^3 + (3-k)s^2 \\ \dot{x}(s)= 3(k-2)s^2 + 2(3-2k)s + k \hspace{0.46cm} \dot{y}(s)= 3(k-2)s^2 + 2(3-k)s \\ \ddot{x}(s)= 6(k-2)s + 2(3-2k) \hspace{1.5cm} \ddot{y}(s)= 6(k-2)s + 2(3-k)" />

And being x and y flat outputs we can recover all the other information of the state and input

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;\\&space;\theta&space;=&space;Atan2({\dot{y},\dot{x}})&space;\\&space;v(s)&space;=&space;\pm&space;\sqrt{\dot{x}^2&space;&plus;&space;\dot{y}^2}&space;\\&space;w(s)&space;=&space;\dot{\theta}&space;=&space;\frac{\ddot{y}\dot{x}&space;-&space;\ddot{x}\dot{y}}{\dot{x}^2&space;&plus;&space;\dot{y}^2}" title="\\ \theta = Atan2({\dot{y},\dot{x}}) \\ v(s) = \pm \sqrt{\dot{x}^2 + \dot{y}^2} \\ w(s) = \dot{\theta} = \frac{\ddot{y}\dot{x} - \ddot{x}\dot{y}}{\dot{x}^2 + \dot{y}^2}" />

### Find a timing law

The easiest choice for a timing law is <img src="https://latex.codecogs.com/svg.latex?\inline&space;\dpi{100}&space;s&space;=&space;s(t)&space;=&space;\alpha&space;t" title="s = s(t) = \alpha t" />.

The alpha is useful to scale uniformly the planning if a velocity bound is not satisfied, otherwise it can be set to 1 and nothing is lost. 

To check if we need this alpha we must compute the maximum value of both **v** and **w**, this can be done with a fine discrete approximation or using the function to compute the maxima. 

Having the 'max values' we can see if they are over the bounds or not, if one of both of them are over the soglia we use alpha = 1/m where m is the biggest ratio among { vmax / v_bound , wmax / w_bound }.

## Problem 3 

### Kinematic Model

We can write first the kinematic model for the differential drive robot (in the right inputs), then we augment it considering that our actual inputs are at acceleration level which is the derivative of the velocities.

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;\dot{x}&space;=&space;\frac{R}{2}(w_r&space;&plus;&space;w_l)&space;cos(\theta)&space;\\&space;\dot{y}&space;=&space;\frac{R}{2}(w_r&space;&plus;&space;w_l)&space;sen(\theta)&space;\\&space;\dot{\theta}&space;=&space;\frac{R}{d}(w_r&space;-&space;w_l)&space;\\&space;\dot{w_r}&space;=&space;a_r&space;\\&space;\dot{w_l}&space;=&space;a_l&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}&space;=&space;\frac{R}{2}(w_r&space;&plus;&space;w_l)&space;cos(\theta)&space;\\&space;\dot{y}&space;=&space;\frac{R}{2}(w_r&space;&plus;&space;w_l)&space;sen(\theta)&space;\\&space;\dot{\theta}&space;=&space;\frac{R}{d}(w_r&space;-&space;w_l)&space;\\&space;\dot{w_r}&space;=&space;a_r&space;\\&space;\dot{w_l}&space;=&space;a_l&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x} = \frac{R}{2}(w_r + w_l) cos(\theta) \\ \dot{y} = \frac{R}{2}(w_r + w_l) sen(\theta) \\ \dot{\theta} = \frac{R}{d}(w_r - w_l) \\ \dot{w_r} = a_r \\ \dot{w_l} = a_l \end{matrix}\right." /></a>

### Discrete time model

We just need to integrate the equations considering also a process noise.

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;x_{k&plus;1}&space;=&space;x_k&space;&plus;&space;\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})&space;cos(\theta_k)&space;&plus;&space;\textbf{v}_{1,k}&space;\\&space;y_{k&plus;1}&space;=&space;y_k&space;\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})&space;sen(\theta)&space;&plus;&space;\textbf{v}_{2,k}&space;\\&space;\theta_{k&plus;1}&space;=&space;\theta_k&space;&plus;&space;\frac{R&space;T_s}{d}&space;(w_{r,k}&space;-&space;w_{l,k})&space;&plus;&space;\textbf{v}_{3,k}&space;\\&space;w_{r,k&plus;1}&space;=&space;w_{r,k}&space;&plus;&space;a_rT_s&space;&plus;&space;\textbf{v}_{4,k}&space;\\&space;w_{l,k&plus;1}&space;=&space;w_{l,k}&space;&plus;&space;a_lT_s&space;&plus;&space;\textbf{v}_{5,k}&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;x_{k&plus;1}&space;=&space;x_k&space;&plus;&space;\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})&space;cos(\theta_k)&space;&plus;&space;\textbf{v}_{1,k}&space;\\&space;y_{k&plus;1}&space;=&space;y_k&space;\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})&space;sen(\theta)&space;&plus;&space;\textbf{v}_{2,k}&space;\\&space;\theta_{k&plus;1}&space;=&space;\theta_k&space;&plus;&space;\frac{R&space;T_s}{d}&space;(w_{r,k}&space;-&space;w_{l,k})&space;&plus;&space;\textbf{v}_{3,k}&space;\\&space;w_{r,k&plus;1}&space;=&space;w_{r,k}&space;&plus;&space;a_rT_s&space;&plus;&space;\textbf{v}_{4,k}&space;\\&space;w_{l,k&plus;1}&space;=&space;w_{l,k}&space;&plus;&space;a_lT_s&space;&plus;&space;\textbf{v}_{5,k}&space;\end{matrix}\right." title="\left\{\begin{matrix} x_{k+1} = x_k + \frac{R T_s}{2}(w_{r,k} + w_{l,k}) cos(\theta_k) + \textbf{v}_{1,k} \\ y_{k+1} = y_k \frac{R T_s}{2}(w_{r,k} + w_{l,k}) sen(\theta) + \textbf{v}_{2,k} \\ \theta_{k+1} = \theta_k + \frac{R T_s}{d} (w_{r,k} - w_{l,k}) + \textbf{v}_{3,k} \\ w_{r,k+1} = w_{r,k} + a_rT_s + \textbf{v}_{4,k} \\ w_{l,k+1} = w_{l,k} + a_lT_s + \textbf{v}_{5,k} \end{matrix}\right." /></a>

### EKF

We already have the time discrete system, due to the presence of sen and cos it's non linear so we need to build the F matrix to linearize the model. We also need to augment the coordinates with the landmark position, which needs to be estimated. 

In the meantime we can see what are our observations and check if we also need to linearize the observation model. We observe the angular and linear velocities, plus the bearing angle with respect to the robot of the landmark, which is at an unknown fixed position. 

<a href="https://www.codecogs.com/eqnedit.php?latex=h_k&space;=&space;\begin{pmatrix}&space;\frac{R}{2}(w_{r,k}&space;&plus;&space;w_{l,k})&space;\\&space;\frac{R}{d}(w_{r,k}&space;-&space;w_{l,k})&space;\\&space;Atan2(y_{L,k}&space;-&space;y_k,&space;x_{L,k}&space;-&space;x_k&space;)&space;-&space;\theta_k&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?h_k&space;=&space;\begin{pmatrix}&space;\frac{R}{2}(w_{r,k}&space;&plus;&space;w_{l,k})&space;\\&space;\frac{R}{d}(w_{r,k}&space;-&space;w_{l,k})&space;\\&space;Atan2(y_{L,k}&space;-&space;y_k,&space;x_{L,k}&space;-&space;x_k&space;)&space;-&space;\theta_k&space;\end{pmatrix}" title="h_k = \begin{pmatrix} \frac{R}{2}(w_{r,k} + w_{l,k}) \\ \frac{R}{d}(w_{r,k} - w_{l,k}) \\ Atan2(y_{L,k} - y_k, x_{L,k} - x_k ) - \theta_k \end{pmatrix}" /></a>

We can see the third row is non linear so we need to linearize both models.

<a href="https://www.codecogs.com/eqnedit.php?latex=F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})sen(\theta_k)&space;&&space;\frac{R&space;T_s}{2}cos(\theta_k)&space;&&space;\frac{R&space;T_s}{2}cos(\theta_k)&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;1&space;&&space;\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})cos(\theta_k)&space;&&space;\frac{R&space;T_s}{2}sen(\theta_k)&space;&&space;\frac{R&space;T_s}{2}sen(\theta_k)&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;\frac{R&space;T_s}{d}&space;&&space;-\frac{R&space;T_s}{d}&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})sen(\theta_k)&space;&&space;\frac{R&space;T_s}{2}cos(\theta_k)&space;&&space;\frac{R&space;T_s}{2}cos(\theta_k)&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;1&space;&&space;\frac{R&space;T_s}{2}(w_{r,k}&space;&plus;&space;w_{l,k})cos(\theta_k)&space;&&space;\frac{R&space;T_s}{2}sen(\theta_k)&space;&&space;\frac{R&space;T_s}{2}sen(\theta_k)&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;\frac{R&space;T_s}{d}&space;&&space;-\frac{R&space;T_s}{d}&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;\end{pmatrix}" title="F_k = \begin{pmatrix} 1 & 0 & -\frac{R T_s}{2}(w_{r,k} + w_{l,k})sen(\theta_k) & \frac{R T_s}{2}cos(\theta_k) & \frac{R T_s}{2}cos(\theta_k) & 0 & 0 \\ 0 & 1 & \frac{R T_s}{2}(w_{r,k} + w_{l,k})cos(\theta_k) & \frac{R T_s}{2}sen(\theta_k) & \frac{R T_s}{2}sen(\theta_k) & 0 & 0 \\ 0 & 0 & 1 & \frac{R T_s}{d} & -\frac{R T_s}{d} & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & 1 \end{pmatrix}" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;0&space;&&space;0&space;&&space;0&space;&&space;\frac{R}{2}&space;&&space;\frac{R}{2}&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;\frac{R}{d}&space;&&space;-\frac{R}{d}&space;&&space;0&space;&&space;0&space;\\&space;\frac{y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;&&space;-\frac{x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;-\frac{y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;&\frac{x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;0&space;&&space;0&space;&&space;0&space;&&space;\frac{R}{2}&space;&&space;\frac{R}{2}&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;\frac{R}{d}&space;&&space;-\frac{R}{d}&space;&&space;0&space;&&space;0&space;\\&space;\frac{y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;&&space;-\frac{x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;-\frac{y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;&\frac{x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{(x_{L,k&plus;1|k}&space;-&space;x_{k&plus;1|k})^2&space;&plus;&space;(y_{L,k&plus;1|k}&space;-&space;y_{k&plus;1|k})^2}&space;\end{pmatrix}" title="H_{k+1} = \begin{pmatrix} 0 & 0 & 0 & \frac{R}{2} & \frac{R}{2} & 0 & 0 \\ 0 & 0 & 0 & \frac{R}{d} & -\frac{R}{d} & 0 & 0 \\ \frac{y_{L,k+1|k} - y_{k+1|k}}{(x_{L,k+1|k} - x_{k+1|k})^2 + (y_{L,k+1|k} - y_{k+1|k})^2} & -\frac{x_{L,k+1|k} - x_{k+1|k}}{(x_{L,k+1|k} - x_{k+1|k})^2 + (y_{L,k+1|k} - y_{k+1|k})^2} & 0 & 0 & 0 & -\frac{y_{L,k+1|k} - y_{k+1|k}}{(x_{L,k+1|k} - x_{k+1|k})^2 + (y_{L,k+1|k} - y_{k+1|k})^2} &\frac{x_{L,k+1|k} - x_{k+1|k}}{(x_{L,k+1|k} - x_{k+1|k})^2 + (y_{L,k+1|k} - y_{k+1|k})^2} \end{pmatrix}" /></a>

Now using these matrices we just need to 'build the Kalman machine':

<a href="https://www.codecogs.com/eqnedit.php?latex=\hat{q}_{k&plus;1|k}&space;=&space;f(\hat{q}_k&space;,&space;u_k)&space;\\&space;P_{k&plus;1|k}&space;=&space;F_k&space;P_k&space;F_k^T&space;&plus;&space;V_k&space;\\&space;\\&space;\hat{q}_{k&plus;1}&space;=&space;\hat{q}_{k&plus;1|k}&space;&plus;&space;K_{k&plus;1}&space;\nu_{k&plus;1}&space;\\&space;P_{k&plus;1}&space;=&space;P_{k&plus;1|k}&space;-&space;K_{k&plus;1}H_{k&plus;1}P_{k&plus;1|k}&space;\\&space;\\&space;K_{k&plus;1}&space;=&space;P_{k&plus;1|k}H_{k&plus;1}^T(H_{k&plus;1}&space;P_{k&plus;1|k}&space;H_{k&plus;1}^T&space;&plus;&space;W_{k&plus;1})^{-1}&space;\\&space;\nu_{k&plus;1}&space;=&space;h_{k&plus;1}-&space;h(\hat{q}_{k&plus;1|k})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\hat{q}_{k&plus;1|k}&space;=&space;f(\hat{q}_k&space;,&space;u_k)&space;\\&space;P_{k&plus;1|k}&space;=&space;F_k&space;P_k&space;F_k^T&space;&plus;&space;V_k&space;\\&space;\\&space;\hat{q}_{k&plus;1}&space;=&space;\hat{q}_{k&plus;1|k}&space;&plus;&space;K_{k&plus;1}&space;\nu_{k&plus;1}&space;\\&space;P_{k&plus;1}&space;=&space;P_{k&plus;1|k}&space;-&space;K_{k&plus;1}H_{k&plus;1}P_{k&plus;1|k}&space;\\&space;\\&space;K_{k&plus;1}&space;=&space;P_{k&plus;1|k}H_{k&plus;1}^T(H_{k&plus;1}&space;P_{k&plus;1|k}&space;H_{k&plus;1}^T&space;&plus;&space;W_{k&plus;1})^{-1}&space;\\&space;\nu_{k&plus;1}&space;=&space;h_{k&plus;1}-&space;h(\hat{q}_{k&plus;1|k})" title="\hat{q}_{k+1|k} = f(\hat{q}_k , u_k) \\ P_{k+1|k} = F_k P_k F_k^T + V_k \\ \\ \hat{q}_{k+1} = \hat{q}_{k+1|k} + K_{k+1} \nu_{k+1} \\ P_{k+1} = P_{k+1|k} - K_{k+1}H_{k+1}P_{k+1|k} \\ \\ K_{k+1} = P_{k+1|k}H_{k+1}^T(H_{k+1} P_{k+1|k} H_{k+1}^T + W_{k+1})^{-1} \\ \nu_{k+1} = h_{k+1}- h(\hat{q}_{k+1|k})" /></a>

A scheme for the EKF is below, we omitted the formulas because are the ones presented above. At every step we use the last estimation as input, together with the readings from the sensors. In this specific case, the **h** we use as observation contains the readings of angular and linear velocities, this mens that the **proprioceptive sensors are also inputs of the UPDATE block**.

<img src='https://github.com/theroggio/Autonomous-and-Mobile-Robotics-La-Sapienza-/blob/master/images/blockscheme_ekf.JPG'/>

# Midterm 2016/2017

## Problem 1

### Augmented Configuration Space

We can start from the basis: a unicycle without the wheel angle has three coordinates: one for x-position of its center, one for y-position and one for the orientation.

To consider also the wheel angle we must include it in the state, which become a 4 element vector. 

The configuration space, of dimension 4, is the cartesian product of (R\*R) for the position of the center, ( SO(2) ) for the orientation and ( SO(2) ) for the orientation of the wheel. 

### Kinematic Augmented Model

Starting from the kinematic model of the unicycle we can try to augment it. We just need to consider this information connecting the former input **v** to a new input related to the wheel's orientation.

<img src="https://latex.codecogs.com/gif.latex?v&space;=&space;w_{wheel}&space;R" title="v = w_{wheel} R" />

Replacing this information inside the model and adding the information about the phi angle we have

<img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}&space;=&space;w_{\phi}&space;R&space;cos(\theta)&space;\\&space;\dot{y}&space;=&space;w_{\phi}&space;R&space;sen(\theta)&space;\\&space;\dot{\theta}&space;=&space;w&space;\\&space;\dot{\phi}&space;=&space;w_{\phi}&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x} = w_{\phi} R cos(\theta) \\ \dot{y} = w_{\phi} R sen(\theta) \\ \dot{\theta} = w \\ \dot{\phi} = w_{\phi} \end{matrix}\right." />

### Controllability

From the kinematic model above we have already two vector of the vector field:
<img src="https://latex.codecogs.com/gif.latex?\\&space;g_1&space;=&space;\begin{pmatrix}&space;R&space;cos(\theta)&space;\\&space;R&space;sen(\theta)&space;\\&space;0&space;\\&space;1&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;0&space;\\&space;0&space;\\&space;1&space;\\&space;0&space;\end{pmatrix}" title="\\ g_1 = \begin{pmatrix} R cos(\theta) \\ R sen(\theta) \\ 0 \\ 1 \end{pmatrix} \hspace{0.5cm} g_2 = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix}" />

To prove controllability we need to find other two vectors (because configuration space has dimension 4) using the Lie Brackets.
<img src="https://latex.codecogs.com/gif.latex?\\&space;\begin{bmatrix}&space;g_1,g_2&space;\end{bmatrix}&space;=&space;\begin{pmatrix}&space;R&space;sen(\theta)&space;\\&space;-&space;R&space;cos(\theta)&space;\\&space;0&space;\\&space;0&space;\end{pmatrix}&space;=&space;g_3&space;\\&space;\begin{bmatrix}&space;g_1,g_3&space;\end{bmatrix}&space;=&space;\begin{pmatrix}&space;0&space;\\&space;0&space;\\&space;0&space;\\&space;0&space;\end{pmatrix}&space;\\&space;\begin{bmatrix}&space;g_2,g_3&space;\end{bmatrix}&space;=&space;\begin{pmatrix}&space;R&space;cos(\theta)&space;\\&space;R&space;sen(\theta)&space;\\&space;0&space;\\&space;0&space;\end{pmatrix}&space;=&space;g_4" title="\\ \begin{bmatrix} g_1,g_2 \end{bmatrix} = \begin{pmatrix} R sen(\theta) \\ - R cos(\theta) \\ 0 \\ 0 \end{pmatrix} = g_3 \\ \begin{bmatrix} g_1,g_3 \end{bmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \\ 0 \end{pmatrix} \\ \begin{bmatrix} g_2,g_3 \end{bmatrix} = \begin{pmatrix} R cos(\theta) \\ R sen(\theta) \\ 0 \\ 0 \end{pmatrix} = g_4" />

We can easily compute the rank of the matrix composed by all the g vectors, it's 4, because the determinant of the matrix is -R\*R. So the system is controllable.

### Maneuver between two configurations

A possible maneuver between any initial configuration and any final one can be augmented from the maneuver of the uncycle. 

- we orientate the robot in the direction of the center point of the final configuration
- we move the robot on this direction until the current center is the same of the final one
- we orientate the robot direction as the final desired orientation

Now we just need to have the wheel orientation as the one we desire, we just need to notice that to change it we must move the robot. Knowing of how much we need to change the wheel orientation we can compute the radius of the circle with that length as the circonference, than

- we move the robot on a circle, with radius diff\*pi/2, at the end we'll be in the same position, with same orientation but desired wheel angle

## Problem 2

We have the initial and final configuration, we can use more than one way to compute the planning. Let's try with the polynomial interpolation, using the flat outputs of the (2,3) chain form which are z1 and z3.

The number of boundary conditions we have is 6: 2 for the initial values of FO, 2 for their final values and 2 for the initial and final value of z2, which depends on their derivatives. 

So we need 6 parameters, a good way is using a first order polynomial and a third order polynomial respectively for z1 and z3. 

Solving with the conditions we get 

<img src="https://latex.codecogs.com/gif.latex?\\&space;z_1&space;(s)&space;=&space;s&space;\\&space;z_3&space;(s)&space;=&space;-s^3&space;&plus;&space;2s^2&space;\\&space;\\&space;z_2(s)&space;=\frac{z_3'(s)}{z_1'(s)}&space;=&space;-3s^2&space;&plus;4s" title="\\ z_1 (s) = s \\ z_3 (s) = -s^3 + 2s^2 \\ \\ z_2(s) =\frac{z_3'(s)}{z_1'(s)} = -3s^2 +4s" />

## Problem 3

### Feedback Control Law of x

If the y coordinate is not of interest we can just take it out for now and try with an input-output linearization. The x is our desired output and we already know from the kinematic model that 

<img src="https://latex.codecogs.com/gif.latex?\dot{x}&space;=&space;v&space;cos(\theta)" title="\dot{x} = v cos(\theta)" />

So it depends only on one input **v** in a linear way, we can just invert the formula (it's a 1-by-1 matrix basically) to find the **T** transformation.

<img src="https://latex.codecogs.com/gif.latex?\\T&space;=&space;cos(\theta)&space;\\&space;v&space;=&space;T^{-1}&space;u&space;=&space;\frac{u}{cos(\theta)}&space;\\&space;\dot{x}&space;=&space;u" title="\\T = cos(\theta) \\ v = T^{-1} u = \frac{u}{cos(\theta)} \\ \dot{x} = u" />

This means our feedback control to drive the robot from its position to the deisred x is below, using T we can also retrieve the feedback for the v input.

<img src="https://latex.codecogs.com/gif.latex?\\&space;u&space;=&space;k_1&space;(x_d&space;-&space;x)&space;\\&space;v&space;=&space;\frac{k_1}{cos(\theta)}&space;(x_d&space;-&space;x)" title="\\ u = k_1 (x_d - x) \\ v = \frac{k_1}{cos(\theta)} (x_d - x)" />

We still need to avoid the collision with the walls, but we still have a second input we're not using for controlling the position on x axis. We can add a second control over the **w** input to keep the orientation fixed so that the robot follow a straight path without colliding with the walls, the law would be just a proportional one.

### Localization System

Our controller needs estimation of theta (orientation, to correct it) and x (to drive it towards the desired position). So out state for the Kalman Filter will be just ( x theta ). Due to the presence of the cos(theta) in the equation of the **x** we will need to linearize the dynamic model.

The observations we get are (1) theta, from a compass, and (2) the distance from the end of the wall. The measurement (2) must be expressed in our set of coordinates, in this specific case d = l - x.
The observation model is affine (not strictly linear), but it does not need linearization: intuitively, the only term which is not a linear combination of the parameters is **l** but it's a constant term which would disappear in the derivations. 

<a href="https://www.codecogs.com/eqnedit.php?latex=F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;-v_k&space;T_s&space;sen(\theta_k)&space;\\&space;0&space;&&space;1&space;\end{pmatrix}&space;\hspace{0.5cm}&space;y_k&space;=&space;C_k&space;x_k&space;&plus;&space;w_k&space;,&space;C_k&space;=&space;\begin{pmatrix}&space;0&space;&&space;1&space;\\&space;-1&space;&&space;0&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;-v_k&space;T_s&space;sen(\theta_k)&space;\\&space;0&space;&&space;1&space;\end{pmatrix}&space;\hspace{0.5cm}&space;y_k&space;=&space;C_k&space;x_k&space;&plus;&space;w_k&space;,&space;C_k&space;=&space;\begin{pmatrix}&space;0&space;&&space;1&space;\\&space;-1&space;&&space;0&space;\end{pmatrix}" title="F_k = \begin{pmatrix} 1 & -v_k T_s sen(\theta_k) \\ 0 & 1 \end{pmatrix} \hspace{0.5cm} y_k = C_k x_k + w_k , C_k = \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix}" /></a>

The equations of the Kalman Filter are:
<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;\hat{q}_{k&plus;1|k}&space;=&space;f(\hat{q}_k,&space;u_k)&space;\\&space;P_{k&plus;1|k}&space;=&space;F_k&space;P_k&space;F_k&space;^T&space;&plus;&space;V_k" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;\hat{q}_{k&plus;1|k}&space;=&space;f(\hat{q}_k,&space;u_k)&space;\\&space;P_{k&plus;1|k}&space;=&space;F_k&space;P_k&space;F_k&space;^T&space;&plus;&space;V_k" title="\\ \hat{q}_{k+1|k} = f(\hat{q}_k, u_k) \\ P_{k+1|k} = F_k P_k F_k ^T + V_k" /></a>

These did not change because we linearized the model, V is the variance of the white, zero-mean gaussian process noise (diagonal matrix). 

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;\hat{q}_{k&plus;1}&space;=&space;\hat{q}_{k&plus;1|k}&space;&plus;&space;K_{k&plus;1}\nu_{k&plus;1}&space;\\&space;\\&space;K_{k&plus;1}&space;=&space;P_{k&plus;1|k}C_{k&plus;1}^T&space;(C_{k&plus;1}&space;P_{k&plus;1|k}&space;C_{k&plus;1}^T&space;&plus;&space;W_{k&plus;1})^{-1}&space;\\&space;\nu_{k&plus;1}&space;=&space;h_{k&plus;1}&space;-&space;h(\hat{q}_{k&plus;1|k})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;\hat{q}_{k&plus;1}&space;=&space;\hat{q}_{k&plus;1|k}&space;&plus;&space;K_{k&plus;1}\nu_{k&plus;1}&space;\\&space;\\&space;K_{k&plus;1}&space;=&space;P_{k&plus;1|k}C_{k&plus;1}^T&space;(C_{k&plus;1}&space;P_{k&plus;1|k}&space;C_{k&plus;1}^T&space;&plus;&space;W_{k&plus;1})^{-1}&space;\\&space;\nu_{k&plus;1}&space;=&space;h_{k&plus;1}&space;-&space;h(\hat{q}_{k&plus;1|k})" title="\\ \hat{q}_{k+1} = \hat{q}_{k+1|k} + K_{k+1}\nu_{k+1} \\ \\ K_{k+1} = P_{k+1|k}C_{k+1}^T (C_{k+1} P_{k+1|k} C_{k+1}^T + W_{k+1})^{-1} \\ \nu_{k+1} = h_{k+1} - h(\hat{q}_{k+1|k})" /></a>

In the update of the state we use C instead of H (because the observation model was already linear) and where W is the diagonal matrix of the white gaussian noise, with zero mean, for the measurements. 

<a href="https://www.codecogs.com/eqnedit.php?latex=P_{k&plus;1}&space;=&space;P_{k&plus;1|k}&space;-&space;K_{k&plus;1}&space;C_{k&plus;1}&space;P_{k&plus;1|k}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?P_{k&plus;1}&space;=&space;P_{k&plus;1|k}&space;-&space;K_{k&plus;1}&space;C_{k&plus;1}&space;P_{k&plus;1|k}" title="P_{k+1} = P_{k+1|k} - K_{k+1} C_{k+1} P_{k+1|k}" /></a>

Also here we have C instead of H. The value of the matrix K (kalman gain) is the same of the formula above.

From the image in the first midterm (or in the image folder) we can see the 'common' block scheme for the EKF. In this case the scheme does not need to be modified. The theta measurement we get from the exteroceptive sensor is indeed not used as it is, but always compared to the estimation to get a better result (better than only the sensing, better than an estimation without sensing). Nothing from the extercopetive is used as it is in the **predict** module. 

We could include the controller in the scheme, these estimations would be the input of the controller which produces the **v** and **w** inputs of the kinmeatic model which are commanded to the actuators. 

# Midterm 2015/2016

## Problem 1

### Kinematic Model for the Cycab with rear-wheel drive

First of all, the Cycab is a car-like vehicle with an additional possibility to orient the rear wheels, so its configuration can be expressed as (x,y) position of the middle point of the rear wheel axis, orientation of the chassis, orientation of the rear wheels and orientation of the front wheels. This is a 5 dimensional vector linked to a configuration space like R*\R x (SO(2))^3.

We can derive the model from its constraints that are the same of the car-like robot, just we need to pay attention to the angles of the constraint which are always vehicle orientation + wheel orientation, for both front and rear wheels.

<img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}&space;sin(\theta&space;&plus;&space;\gamma)&space;-&space;\dot{y}&space;cos(\theta&space;&plus;&space;\gamma)&space;=&space;0&space;\\&space;\dot{x_f}&space;sin(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y_f}&space;cos(\theta&space;&plus;&space;\phi)&space;=&space;0&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x} sin(\theta + \gamma) - \dot{y} cos(\theta + \gamma) = 0 \\ \dot{x_f} cos(\theta + \phi) - \dot{y_f} sin(\theta + \phi) = 0 \end{matrix}\right." />

Now we need to express the middle point of the front wheel axis as dependent on the other measures we have, we do not need other two coordinates for that point.

<img src="https://latex.codecogs.com/gif.latex?\\&space;\begin{pmatrix}&space;x_f&space;\\&space;y_f&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;&plus;&space;lcos(\theta)&space;\\&space;y&space;&plus;&space;lsin(\theta)&space;\end{pmatrix}&space;\\&space;\begin{pmatrix}&space;\dot{x_f}&space;\\&space;\dot{y_f}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;-&space;l\dot{\theta}sin(\theta)&space;\\&space;\dot{y}&space;&plus;&space;l\dot{\theta}cos(\theta)&space;\end{pmatrix}" title="\\ \begin{pmatrix} x_f \\ y_f \end{pmatrix} = \begin{pmatrix} x + lcos(\theta) \\ y + lsin(\theta) \end{pmatrix} \\ \begin{pmatrix} \dot{x_f} \\ \dot{y_f} \end{pmatrix} = \begin{pmatrix} \dot{x} - l\dot{\theta}sin(\theta) \\ \dot{y} + l\dot{\theta}cos(\theta) \end{pmatrix}" />

Plugging this in the previous constraints we obtain our kinematic model:

<img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}&space;sin(\theta&space;&plus;&space;\gamma)&space;-&space;\dot{y}cos(\theta&space;&plus;&space;\gamma)&space;=&space;0&space;\\&space;\dot{x}&space;sin(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y}&space;cos(\theta&space;&plus;&space;\phi)&space;-&space;l&space;\dot{\theta}&space;cos(\phi)&space;=&space;0&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x} sin(\theta + \gamma) - \dot{y}cos(\theta + \gamma) = 0 \\ \dot{x} sin(\theta + \phi) - \dot{y} cos(\theta + \phi) - l \dot{\theta} cos(\phi) = 0 \end{matrix}\right." />

That now can be written in Pfaffian form depending on the generalized velocities of x y theta phi gamma. We need to find the vector field to write the kinematic model, first of all we already see the last two columns are all zeros so we already have two vector from there; the first vector can be chosen augmenting the vector for the unicycle with cos and sin of the main angle (theta + gamma) and solving for the third coordinate. 

We get

<img src="https://latex.codecogs.com/gif.latex?\\&space;g_1&space;=&space;\begin{pmatrix}&space;cos(\theta&space;&plus;&space;\gamma)&space;\\&space;sin(\theta&space;&plus;&space;\gamma)&space;\\&space;\frac{sin(\phi&space;-&space;\gamma)}{l&space;cos(\phi)}&space;\\&space;0&space;\\&space;0&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;0\\&space;0&space;\\&space;0&space;\\&space;1&space;\\&space;0&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;0\\&space;0&space;\\&space;0&space;\\&space;0&space;\\&space;1&space;\end{pmatrix}" title="\\ g_1 = \begin{pmatrix} cos(\theta + \gamma) \\ sin(\theta + \gamma) \\ \frac{sin(\phi - \gamma)}{l cos(\phi)} \\ 0 \\ 0 \end{pmatrix} \hspace{0.5cm} g_2 = \begin{pmatrix} 0\\ 0 \\ 0 \\ 1 \\ 0 \end{pmatrix} \hspace{0.5cm} g_2 = \begin{pmatrix} 0\\ 0 \\ 0 \\ 0 \\ 1 \end{pmatrix}" />

So the final model can be written using as inputs v, steering of the rear and of the front wheels, as 

<img src="https://latex.codecogs.com/gif.latex?\\&space;\dot{x}&space;=&space;v&space;cos(\theta&space;&plus;&space;\gamma)&space;\\&space;\dot{y}&space;=&space;v&space;sin(\theta&space;&plus;&space;\gamma)&space;\\&space;\dot{\theta}&space;=&space;v&space;\frac{sin(\phi&space;-&space;\gamma)}{lcos(\phi)}&space;\\&space;\dot{\gamma}&space;=&space;w_{r}&space;\\&space;\dot{\phi}&space;=&space;w_{f}" title="\\ \dot{x} = v cos(\theta + \gamma) \\ \dot{y} = v sin(\theta + \gamma) \\ \dot{\theta} = v \frac{sin(\phi - \gamma)}{lcos(\phi)} \\ \dot{\gamma} = w_{r} \\ \dot{\phi} = w_{f}" />

### Prove the controllability of the system

We can see this as the augmentation of the car-like robot, because of the heavy computations of the Lie Bracket in a 5 dimensional space we can try to find the maneuver which brings the robot from any initial configuration to any final configuration. 

- we set the rear wheel orientation to zero using only the wr input
- we bring the robot from this configuration to the final configuration for the first four coordinates, this is possible because the car like robot is controllable, we're not using the wr input now
- we use only the wr input to change the rear wheel orientation to match the desired one

## Problem 2

We want to control only the chassis orientation, from the former exercise we can see that we have a realtionship between the derivative and just the **v** input, which can be easily inverted. 

<img src="https://latex.codecogs.com/gif.latex?\\&space;T&space;=&space;\frac{sin(\phi&space;-&space;\gamma)}{l&space;cos(\phi)}&space;\\&space;T^{-1}&space;=&space;\frac{l&space;cos(\phi)}{sin(\phi&space;-&space;\gamma)}&space;\\&space;v&space;=&space;T^{-1}u&space;\\&space;\dot{\theta}&space;=&space;u" title="\\ T = \frac{sin(\phi - \gamma)}{l cos(\phi)} \\ T^{-1} = \frac{l cos(\phi)}{sin(\phi - \gamma)} \\ v = T^{-1}u \\ \dot{\theta} = u" />

So the control law is now trivial 

<img src="https://latex.codecogs.com/gif.latex?\\&space;u&space;=&space;k_v&space;(\theta_d&space;-&space;\theta)&space;&plus;&space;\dot{\theta_d}" title="\\ u = k_v (\theta_d - \theta) + \dot{\theta_d}" />

What about its problems? We can see that our **T** has some problems when the phi and gamma angle are equal to each other, so when the rear and front wheels have the same orientation. We have any way two other inputs we're not using for the control that we can set to avoid this singularity. 

If the initial configuration is not a singular one we can just set both of them to zero, if the initial configuration is singular we need to move outside of it (epsilon burst of one of the wheels velocity) and when they are different we can go back to the previous case.

## Problem 3

We already have the system dynamics, we need to put it in time-discrete form, but we can already see it's non-linear.  The observation is just the distance from the charging station, which is non linear (it's the square root of two differences to the power of two).

<a href="https://www.codecogs.com/eqnedit.php?latex=F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\theta_k&space;&plus;&space;\gamma_k)&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\theta_k&space;&plus;&space;\gamma_k)&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\theta_k&space;&plus;&space;\gamma_k)&space;&&space;0&space;&&space;v_k&space;T_s&space;cos(\theta_k&space;&plus;&space;\gamma_k)&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;\frac{v_k&space;T_s&space;cos(\gamma_k)}{l&space;cos^2(\phi_k)}&space;&&space;-&space;\frac{v_k&space;T_s&space;cos(\phi_k&space;-&space;\gamma_k)}{l&space;cos(\phi_k)}&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&1&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\theta_k&space;&plus;&space;\gamma_k)&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\theta_k&space;&plus;&space;\gamma_k)&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\theta_k&space;&plus;&space;\gamma_k)&space;&&space;0&space;&&space;v_k&space;T_s&space;cos(\theta_k&space;&plus;&space;\gamma_k)&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;\frac{v_k&space;T_s&space;cos(\gamma_k)}{l&space;cos^2(\phi_k)}&space;&&space;-&space;\frac{v_k&space;T_s&space;cos(\phi_k&space;-&space;\gamma_k)}{l&space;cos(\phi_k)}&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&1&space;\end{pmatrix}" title="F_k = \begin{pmatrix} 1 & 0 & - v_k T_s sen(\theta_k + \gamma_k) & 0 & - v_k T_s sen(\theta_k + \gamma_k) \\ 0 & 1 & v_k T_s cos(\theta_k + \gamma_k) & 0 & v_k T_s cos(\theta_k + \gamma_k) \\ 0 & 0 & 1 & \frac{v_k T_s cos(\gamma_k)}{l cos^2(\phi_k)} & - \frac{v_k T_s cos(\phi_k - \gamma_k)}{l cos(\phi_k)} \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 &1 \end{pmatrix}" /></a>

Because the charging station location is known we can just express its position as (x , y)c. This variable is not in the state, we do not derive with respect to it and it's not estimated at every step, is a constant value.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;h_k&space;=&space;\sqrt{(x_k&space;-&space;x_c)^2&space;&plus;&space;(y_k&space;-&space;y_c)^2}&space;\\&space;\\&space;H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;\frac{x_{k&plus;1|k}&space;-&space;x_c}{\sqrt{(x_{k&plus;1|k}&space;-&space;x_c)^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_c)^2}}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_c}{\sqrt{(x_{k&plus;1|k}&space;-&space;x_c)^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_c)^2}}&space;&&space;0&space;&&space;0&space;&&space;0&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;h_k&space;=&space;\sqrt{(x_k&space;-&space;x_c)^2&space;&plus;&space;(y_k&space;-&space;y_c)^2}&space;\\&space;\\&space;H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;\frac{x_{k&plus;1|k}&space;-&space;x_c}{\sqrt{(x_{k&plus;1|k}&space;-&space;x_c)^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_c)^2}}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_c}{\sqrt{(x_{k&plus;1|k}&space;-&space;x_c)^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_c)^2}}&space;&&space;0&space;&&space;0&space;&&space;0&space;\end{pmatrix}" title="\\ h_k = \sqrt{(x_k - x_c)^2 + (y_k - y_c)^2} \\ \\ H_{k+1} = \begin{pmatrix} \frac{x_{k+1|k} - x_c}{\sqrt{(x_{k+1|k} - x_c)^2 + (y_{k+1|k} - y_c)^2}} & \frac{y_{k+1|k} - y_c}{\sqrt{(x_{k+1|k} - x_c)^2 + (y_{k+1|k} - y_c)^2}} & 0 & 0 & 0 \end{pmatrix}" /></a>

From here we use the common EKF equations. The scheme is a little bit different: we have a further information, which is used only in the H matrix: the position of the charging station. That info is not in the state and is not predicted, is an information, given at **update** together with the measurements. 

# Class Test 2014/2015

## Problem 1

### Kinematic Model 

Starting from the unicycle model and knowing the input trasformations we can write the kinematic model of the differential drive robot in no time. 

<img src="https://latex.codecogs.com/gif.latex?\begin{Bmatrix}&space;\dot{x}&space;=&space;\frac{R}{2}&space;(w_R&space;&plus;&space;w_L)&space;cos(\theta)&space;\\&space;\dot{y}&space;=&space;\frac{R}{2}&space;(w_R&space;&plus;&space;w_L)&space;sin(\theta)&space;\\&space;\dot{\theta}&space;=&space;\frac{R}{d}&space;(w_R&space;-&space;w_L)&space;\end{Bmatrix}" title="\begin{Bmatrix} \dot{x} = \frac{R}{2} (w_R + w_L) cos(\theta) \\ \dot{y} = \frac{R}{2} (w_R + w_L) sin(\theta) \\ \dot{\theta} = \frac{R}{d} (w_R - w_L) \end{Bmatrix}" />

### Controllability

From the above model we can find the firsts vector of the vector field, then we need to compute the third one using the Lie Bracket.

<img src="https://latex.codecogs.com/gif.latex?\\&space;g_1&space;=&space;\begin{pmatrix}&space;\frac{R}{2}&space;cos(\theta)&space;\\&space;\frac{R}{2}&space;sin(\theta)&space;\\&space;\frac{R}{d}&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;\frac{R}{2}&space;cos(\theta)&space;\\&space;\frac{R}{2}&space;sin(\theta)&space;\\&space;-\frac{R}{d}&space;\end{pmatrix}" title="\\ g_1 = \begin{pmatrix} \frac{R}{2} cos(\theta) \\ \frac{R}{2} sin(\theta) \\ \frac{R}{d} \end{pmatrix} \hspace{0.5cm} g_2 = \begin{pmatrix} \frac{R}{2} cos(\theta) \\ \frac{R}{2} sin(\theta) \\ -\frac{R}{d} \end{pmatrix}" />

<img src="https://latex.codecogs.com/gif.latex?\\&space;\begin{bmatrix}&space;g_1,g_2&space;\end{bmatrix}&space;=&space;\begin{bmatrix}&space;0&space;&&space;0&space;&&space;-\frac{R}{2}&space;sin(\theta)&space;\\&space;0&space;&&space;0&space;&&space;\frac{R}{2}&space;cos(\theta)&space;\\&space;0&space;&&space;0&space;&&space;0&space;\end{bmatrix}&space;\begin{pmatrix}&space;\frac{R}{2}&space;cos(\theta)&space;\\&space;\frac{R}{2}&space;sin(\theta)&space;\\&space;\frac{R}{d}&space;\end{pmatrix}&space;-&space;\begin{bmatrix}&space;0&space;&&space;0&space;&&space;-\frac{R}{2}&space;sin(\theta)&space;\\&space;0&space;&&space;0&space;&&space;\frac{R}{2}&space;cos(\theta)&space;\\&space;0&space;&&space;0&space;&&space;0&space;\end{bmatrix}&space;\begin{pmatrix}&space;\frac{R}{2}&space;cos(\theta)&space;\\&space;\frac{R}{2}&space;sin(\theta)&space;\\&space;-\frac{R}{d}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;-\frac{R^2}{d}sin(\theta)&space;\\&space;\frac{R^2}{d}cos(\theta)&space;\\&space;0&space;\end{pmatrix}&space;=&space;g_3" title="\\ \begin{bmatrix} g_1,g_2 \end{bmatrix} = \begin{bmatrix} 0 & 0 & -\frac{R}{2} sin(\theta) \\ 0 & 0 & \frac{R}{2} cos(\theta) \\ 0 & 0 & 0 \end{bmatrix} \begin{pmatrix} \frac{R}{2} cos(\theta) \\ \frac{R}{2} sin(\theta) \\ \frac{R}{d} \end{pmatrix} - \begin{bmatrix} 0 & 0 & -\frac{R}{2} sin(\theta) \\ 0 & 0 & \frac{R}{2} cos(\theta) \\ 0 & 0 & 0 \end{bmatrix} \begin{pmatrix} \frac{R}{2} cos(\theta) \\ \frac{R}{2} sin(\theta) \\ -\frac{R}{d} \end{pmatrix} = \begin{pmatrix} -\frac{R^2}{d}sin(\theta) \\ \frac{R^2}{d}cos(\theta) \\ 0 \end{pmatrix} = g_3" />

It's easy to see they're independent from each other and the matrix they form has determinant R^4 / d^2.

### Sketch of the LB maneuver

A LB maneuver uses 2\*#input step to see the infinitesimal error committed by the model during the motion. IN this case our inputs are the right and left angular velocity for the wheels.

This means tha during the first step the robot's wheel A will move along an arc of circumference (of radius d, center the position of wheel B). 
During the second step the wheel B will do the same. At the end we will be in front of the previous position titled in the direction of the B wheel. 
During the third step we'll do the contrary of the first one, so we'll go back with another arc of circumference; same for the fourth step.

Because of the 'arc' movement of the first wheel is influenced by the B position, we'll end up basically a little more on the B direction wrt to the initial position.

## Problem 2

TODO

## Problem 3

We already know the kinematic model for the differential drive robot, anyway we need to augment the state of the Kalman Filter to estimate also the positions of the L landmarks. This means our final state will be ( x y theta x1 y1 ... ... xL yL ) because for every landmark we want the coordinates x,y. 

The discrete-time model can be easily build from the discrete-time model of the differential drive robot: the first three equations do not depend on the landmark position and all the landmarks position do not change due to any robot input. Anyway because the differential-drive robot has a non-linear kinematic model we need to compute the F matrix. 

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\theta_k)&space;&&space;0&space;&&space;...&space;&&space;0&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\theta_k)&space;&&space;0&space;&&space;...&space;&&space;0&space;\\&space;&&space;0_{2L&space;\times&space;3&space;}&space;&&space;&&space;&&space;I_{2L&space;\times&space;2L}&space;&&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\theta_k)&space;&&space;0&space;&&space;...&space;&&space;0&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\theta_k)&space;&&space;0&space;&&space;...&space;&&space;0&space;\\&space;&&space;0_{2L&space;\times&space;3&space;}&space;&&space;&&space;&&space;I_{2L&space;\times&space;2L}&space;&&space;\end{pmatrix}" title="\\ F_k = \begin{pmatrix} 1 & 0 & - v_k T_s sen(\theta_k) & 0 & ... & 0 \\ 0 & 1 & v_k T_s cos(\theta_k) & 0 & ... & 0 \\ & 0_{2L \times 3 } & & & I_{2L \times 2L} & \end{pmatrix}" /></a>

The sensor is located exactly in the 'center point' we use for localizing the robot, so there is no offset. It can identify the landmarks and sense always all of them, so at every time step for every landmark **i** we get two observations:

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;h_{i,k}&space;=&space;\begin{pmatrix}&space;\sqrt{(&space;x_k-&space;x_{i,k})^2&space;&plus;&space;(y_k&space;-&space;y_{i,k})^2}&space;\\&space;Atan2(&space;y_k&space;-&space;y_{i,k},&space;x_k&space;-&space;x_{i,k}&space;)&space;-&space;\theta_k&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;h_{i,k}&space;=&space;\begin{pmatrix}&space;\sqrt{(&space;x_k-&space;x_{i,k})^2&space;&plus;&space;(y_k&space;-&space;y_{i,k})^2}&space;\\&space;Atan2(&space;y_k&space;-&space;y_{i,k},&space;x_k&space;-&space;x_{i,k}&space;)&space;-&space;\theta_k&space;\end{pmatrix}" title="\\ h_{i,k} = \begin{pmatrix} \sqrt{( x_k- x_{i,k})^2 + (y_k - y_{i,k})^2} \\ Atan2( y_k - y_{i,k}, x_k - x_{i,k} ) - \theta_k \end{pmatrix}" /></a>

The real **h** we get at every time step is just a big column vector, with all the single observations stacked one above the other. Same for its linearization H - because obviously both the atan2 and the square root are non linear.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;H_{i,k&plus;1}&space;=&space;\begin{pmatrix}&space;\frac{x_{k&plus;1|k}&space;-&space;x_{i,k&plus;1|k}}{\sqrt{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k}}{\sqrt{(x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2)^2}}&space;&&space;0_{1&space;\times&space;2i&plus;1}&space;&&space;\frac{x_{i,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{\sqrt{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}}&space;&&space;\frac{y_{i,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{\sqrt{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}}&space;&&space;0_{1&space;\times&space;2L-2i}&space;\\&space;\frac{y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;-\frac{x_{k&plus;1|k}&space;-&space;x_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;-1&space;&&space;0_{1&space;\times&space;2i}&space;&&space;-\frac{y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;\frac{x_{k&plus;1|k}&space;-&space;x_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;0_{1&space;\times&space;L-&space;2i}&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;H_{i,k&plus;1}&space;=&space;\begin{pmatrix}&space;\frac{x_{k&plus;1|k}&space;-&space;x_{i,k&plus;1|k}}{\sqrt{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k}}{\sqrt{(x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2)^2}}&space;&&space;0_{1&space;\times&space;2i&plus;1}&space;&&space;\frac{x_{i,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{\sqrt{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}}&space;&&space;\frac{y_{i,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{\sqrt{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}}&space;&&space;0_{1&space;\times&space;2L-2i}&space;\\&space;\frac{y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;-\frac{x_{k&plus;1|k}&space;-&space;x_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;-1&space;&&space;0_{1&space;\times&space;2i}&space;&&space;-\frac{y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;\frac{x_{k&plus;1|k}&space;-&space;x_{i,k&plus;1|k}}{(&space;x_{k&plus;1|k}-&space;x_{i,k&plus;1|k})^2&space;&plus;&space;(y_{k&plus;1|k}&space;-&space;y_{i,k&plus;1|k})^2}&space;&&space;0_{1&space;\times&space;L-&space;2i}&space;\end{pmatrix}" title="\\ H_{i,k+1} = \begin{pmatrix} \frac{x_{k+1|k} - x_{i,k+1|k}}{\sqrt{( x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2}} & \frac{y_{k+1|k} - y_{i,k+1|k}}{\sqrt{(x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2)^2}} & 0_{1 \times 2i+1} & \frac{x_{i,k+1|k} - x_{k+1|k}}{\sqrt{( x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2}} & \frac{y_{i,k+1|k} - y_{k+1|k}}{\sqrt{( x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2}} & 0_{1 \times 2L-2i} \\ \frac{y_{k+1|k} - y_{i,k+1|k}}{( x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2} & -\frac{x_{k+1|k} - x_{i,k+1|k}}{( x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2} & -1 & 0_{1 \times 2i} & -\frac{y_{k+1|k} - y_{i,k+1|k}}{( x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2} & \frac{x_{k+1|k} - x_{i,k+1|k}}{( x_{k+1|k}- x_{i,k+1|k})^2 + (y_{k+1|k} - y_{i,k+1|k})^2} & 0_{1 \times L- 2i} \end{pmatrix}" /></a>

From here we use the common EKF formulas. The block scheme is the usual one. If the sensor cannot identify the landamrks means that we have observations in the 'wrong order' (measurement *i* could not belong to landmark *i*). We need to build an association map (something like a(i) = j) which maximize the probability that the observation j comes from landmark i which is the same that saying j minimize x(ij) = innovation(ij) * inv(Sij) * innovation(ij). 

Innovation(ij) is just the 'correction' of the error committed considering this association from the previous step. Sij is a weight matrix depending on the uncertainty of the prediction and the noise of the measurements.

# Class Test 2013/2014

## Problem 1

### Write the diffferential constraint.

We just need to substitute the first two expressions in the third one and bring all the terms to one side.

<a href="https://www.codecogs.com/eqnedit.php?latex=x_1&space;\dot{x_2}&space;-&space;x_2&space;\dot{x_1}&space;-&space;\dot{x_3}&space;=&space;0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_1&space;\dot{x_2}&space;-&space;x_2&space;\dot{x_1}&space;-&space;\dot{x_3}&space;=&space;0" title="x_1 \dot{x_2} - x_2 \dot{x_1} - \dot{x_3} = 0" /></a>

### Prove that the constraint is non holonomic nad the system controllability

The two thingas to check are the same, if the system is controllable than the constraint is non holonomic. To study the controllability we need to find the vector field.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;g_1&space;=&space;\begin{pmatrix}&space;1&space;\\&space;0&space;\\&space;-x_2&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;0&space;\\&space;1&space;\\&space;x_1&space;\end{pmatrix}&space;\\&space;\begin{bmatrix}&space;g_1,g_2&space;\end{bmatrix}&space;=&space;g_3=&space;\begin{pmatrix}&space;0&space;\\&space;0&space;\\&space;2&space;\end{pmatrix}&space;\hspace{0.5cm}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;g_1&space;=&space;\begin{pmatrix}&space;1&space;\\&space;0&space;\\&space;-x_2&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;0&space;\\&space;1&space;\\&space;x_1&space;\end{pmatrix}&space;\\&space;\begin{bmatrix}&space;g_1,g_2&space;\end{bmatrix}&space;=&space;g_3=&space;\begin{pmatrix}&space;0&space;\\&space;0&space;\\&space;2&space;\end{pmatrix}&space;\hspace{0.5cm}" title="\\ g_1 = \begin{pmatrix} 1 \\ 0 \\ -x_2 \end{pmatrix} \hspace{0.5cm} g_2 = \begin{pmatrix} 0 \\ 1 \\ x_1 \end{pmatrix} \\ \begin{bmatrix} g_1,g_2 \end{bmatrix} = g_3= \begin{pmatrix} 0 \\ 0 \\ 2 \end{pmatrix} \hspace{0.5cm}" /></a>

The determinand of the matrix composed by the g vectors is 2, so it's full rank and the system is controllable with non holonomic constraints.

### Compute the final state displacement after LB maneuver

We need to compute four steps when the inputs are put to +1 alternatively and then to -1 in the same order, then compute the displacement between the initial and final configuration. We shoul end up with an  infinitesimal displacement in the direction of the LB.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;\left\{\begin{matrix}&space;x_1(\epsilon)&space;=&space;x_{10}&space;&plus;&space;\epsilon&space;\\&space;x_2(\epsilon)&space;=&space;x_{20}&space;\\&space;x_3(\epsilon)&space;=&space;x_{30}&space;-&space;x_{20}\epsilon&space;\end{matrix}\right&space;\\&space;\\&space;\\&space;\left\{\begin{matrix}&space;x_1(2\epsilon)&space;=&space;x_{10}&space;&plus;&space;\epsilon&space;\\&space;x_2(2\epsilon)&space;=&space;x_{20}&space;&plus;\epsilon&space;\\&space;x_3(2\epsilon)&space;=&space;x_{30}&space;-&space;x_{20}\epsilon&space;&plus;&space;(x_{10}&space;&plus;&space;\epsilon)\epsilon&space;\end{matrix}\right&space;\\&space;\\&space;\\&space;\left\{\begin{matrix}&space;x_1(3\epsilon)&space;=&space;x_{10}&space;\\&space;x_2(3\epsilon)&space;=&space;x_{20}&space;&plus;&space;\epsilon&space;\\&space;x_3(3\epsilon)&space;=&space;x_{30}&space;-&space;x_{20}\epsilon&space;&plus;&space;(x_{10}&space;&plus;&space;\epsilon)\epsilon&space;&plus;&space;(x_{20}&space;&plus;&space;\epsilon)\epsilon&space;\end{matrix}\right&space;\\&space;\\&space;\\&space;\left\{\begin{matrix}&space;x_1(4\epsilon)&space;=&space;x_{10}&space;\\&space;x_2(4\epsilon)&space;=&space;x_{20}&space;\\&space;x_3(4\epsilon)&space;=&space;x_{30}&space;-&space;2\epsilon^2&space;\end{matrix}\right" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;\left\{\begin{matrix}&space;x_1(\epsilon)&space;=&space;x_{10}&space;&plus;&space;\epsilon&space;\\&space;x_2(\epsilon)&space;=&space;x_{20}&space;\\&space;x_3(\epsilon)&space;=&space;x_{30}&space;-&space;x_{20}\epsilon&space;\end{matrix}\right&space;\\&space;\\&space;\\&space;\left\{\begin{matrix}&space;x_1(2\epsilon)&space;=&space;x_{10}&space;&plus;&space;\epsilon&space;\\&space;x_2(2\epsilon)&space;=&space;x_{20}&space;&plus;\epsilon&space;\\&space;x_3(2\epsilon)&space;=&space;x_{30}&space;-&space;x_{20}\epsilon&space;&plus;&space;(x_{10}&space;&plus;&space;\epsilon)\epsilon&space;\end{matrix}\right&space;\\&space;\\&space;\\&space;\left\{\begin{matrix}&space;x_1(3\epsilon)&space;=&space;x_{10}&space;\\&space;x_2(3\epsilon)&space;=&space;x_{20}&space;&plus;&space;\epsilon&space;\\&space;x_3(3\epsilon)&space;=&space;x_{30}&space;-&space;x_{20}\epsilon&space;&plus;&space;(x_{10}&space;&plus;&space;\epsilon)\epsilon&space;&plus;&space;(x_{20}&space;&plus;&space;\epsilon)\epsilon&space;\end{matrix}\right&space;\\&space;\\&space;\\&space;\left\{\begin{matrix}&space;x_1(4\epsilon)&space;=&space;x_{10}&space;\\&space;x_2(4\epsilon)&space;=&space;x_{20}&space;\\&space;x_3(4\epsilon)&space;=&space;x_{30}&space;-&space;2\epsilon^2&space;\end{matrix}\right" title="\\ \left\{\begin{matrix} x_1(\epsilon) = x_{10} + \epsilon \\ x_2(\epsilon) = x_{20} \\ x_3(\epsilon) = x_{30} - x_{20}\epsilon \end{matrix}\right \\ \\ \\ \left\{\begin{matrix} x_1(2\epsilon) = x_{10} + \epsilon \\ x_2(2\epsilon) = x_{20} +\epsilon \\ x_3(2\epsilon) = x_{30} - x_{20}\epsilon + (x_{10} + \epsilon)\epsilon \end{matrix}\right \\ \\ \\ \left\{\begin{matrix} x_1(3\epsilon) = x_{10} \\ x_2(3\epsilon) = x_{20} + \epsilon \\ x_3(3\epsilon) = x_{30} - x_{20}\epsilon + (x_{10} + \epsilon)\epsilon + (x_{20} + \epsilon)\epsilon \end{matrix}\right \\ \\ \\ \left\{\begin{matrix} x_1(4\epsilon) = x_{10} \\ x_2(4\epsilon) = x_{20} \\ x_3(4\epsilon) = x_{30} - 2\epsilon^2 \end{matrix}\right" /></a>

In fact the final displacement is a second grade power of epsilon times ( 0 0 2) which is the LB. 

## Problem 2

### A team of two mobile robots that can translate and rotate in the plane

A signle robot with these properties has C = SE(2), having two of them we have a cartesian product S(2) x SE(2) of dimension 6.

### A team of two mobile robots that can translate and rotate in the plane and are connected by a rope

The robe induces one inequality constraint, until the rope is on tension the robots can move freely, when that happens they have a local restriction, but non a global one. The configuration space is a subset of the first one, because in every point they may have this constraint active.

### A team of two mobile robots that can translate and rotate in the plane and are connected by a rigid bar

The rigid bar constraint the robots always, they can move only on circle with the other as center or together concordly but they will not be able to be in every position with any orientation.
We can describe the situation as havinf 3 dimension of SE(2) for the first robot which can be anywhere, then SO(2) for the angle of the bar linkin the two robot and SO(2) for the orientation of the second robot. C dimension is 5.

### A spacecraft with a 6R robot arm

A spacecraft can be positioned and oriented SE(3), then the arm has 6 dof of type SO(2). The C dimension is 6 + 6 = 12.

### The last link of 6R robot arm mounted on a spacecraft

The last link can be positioned and oriented so it has C dimension = 6 and it's SE(3).

## Problem 3 

First let's focus on the state of the Kalman Filter, it needs to be augmented to include the positions of the two landmarks (x1,y1) and (x2,y2). Now, seeing the kinematic model, we need to linearize it.

<a href="https://www.codecogs.com/eqnedit.php?latex=F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-v_k&space;T_s&space;sen(\psi_k)&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&0&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\psi_k)&space;&&space;0&space;&&space;0&space;&0&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;-\frac{g}{v&space;cos^2(\phi_k)}&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;&&space;0_{5&space;\times&space;3}&space;&&space;&&space;&&space;&&space;I_{5&space;\times&space;5}&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/png.latex?F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-v_k&space;T_s&space;sen(\psi_k)&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&0&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\psi_k)&space;&&space;0&space;&&space;0&space;&0&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;-\frac{g}{v&space;cos^2(\phi_k)}&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;&&space;0_{5&space;\times&space;3}&space;&&space;&&space;&&space;&&space;I_{5&space;\times&space;5}&space;\end{pmatrix}" title="F_k = \begin{pmatrix} 1 & 0 & -v_k T_s sen(\psi_k) & 0 & 0 & 0 & 0 &0 \\ 0 & 1 & v_k T_s cos(\psi_k) & 0 & 0 &0 & 0 & 0 \\ 0 & 0 & 1 & -\frac{g}{v cos^2(\phi_k)} & 0 & 0 & 0 & 0 \\ & 0_{5 \times 3} & & & & I_{5 \times 5} \end{pmatrix}" /></a>

The observations we get each time are the distances from the two landmarks, they're obviously non linear because of the square root. The UAV is at z fixed above 0, while the landmarks are at z = 0, so the distances we compute consider this. The z-position is not to estimate so we do not derive wrt it, but it anyway needs to be used during the computations.

<img src="https://latex.codecogs.com/png.latex?h_k&space;=&space;\begin{pmatrix}&space;\sqrt{(x_k&space;-&space;x_{1,k})^2&space;&plus;&space;(y_k&space;-&space;y_{1,k})^2&space;&plus;&space;\bar{z}^2}&space;&plus;&space;w_{1,k}&space;\\&space;\sqrt{(x_k&space;-&space;x_{2,k})^2&space;&plus;&space;(y_k&space;-&space;y_{2,k})^2&space;&plus;&space;\bar{z}^2}&space;&plus;&space;w_{2,k}&space;\end{pmatrix}" title="h_k = \begin{pmatrix} \sqrt{(x_k - x_{1,k})^2 + (y_k - y_{1,k})^2 + \bar{z}^2} + w_{1,k} \\ \sqrt{(x_k - x_{2,k})^2 + (y_k - y_{2,k})^2 + \bar{z}^2} + w_{2,k} \end{pmatrix}" />

Now we need to linearize it.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;\frac{x_{k&plus;1|k}&space;-&space;x_{1,k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_{1,k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;&&space;\frac{x_{1,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;\frac{y_{1,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;\\&space;\frac{x_{k&plus;1|k}&space;-&space;x_{1,k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_{1,k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;\frac{x_{1,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;&&space;\frac{y_{1,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;\\&space;\end{pmatrix}&space;\\&space;\\&space;\\&space;\delta_i(q_k)&space;=&space;\sqrt{(x_k&space;-&space;x_{i,k})^2&space;&plus;&space;(y_k&space;-&space;y_{i,k})^2&space;&plus;&space;\bar{z}^2}" target="_blank"><img src="https://latex.codecogs.com/png.latex?\\&space;H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;\frac{x_{k&plus;1|k}&space;-&space;x_{1,k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_{1,k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;&&space;\frac{x_{1,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;\frac{y_{1,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{\delta_1(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;\\&space;\frac{x_{k&plus;1|k}&space;-&space;x_{1,k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;&&space;\frac{y_{k&plus;1|k}&space;-&space;y_{1,k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;\frac{x_{1,k&plus;1|k}&space;-&space;x_{k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;&&space;\frac{y_{1,k&plus;1|k}&space;-&space;y_{k&plus;1|k}}{\delta_2(q_{k&plus;1|k})}&space;\\&space;\end{pmatrix}&space;\\&space;\\&space;\\&space;\delta_i(q_k)&space;=&space;\sqrt{(x_k&space;-&space;x_{i,k})^2&space;&plus;&space;(y_k&space;-&space;y_{i,k})^2&space;&plus;&space;\bar{z}^2}" title="\\ H_{k+1} = \begin{pmatrix} \frac{x_{k+1|k} - x_{1,k+1|k}}{\delta_1(q_{k+1|k})} & \frac{y_{k+1|k} - y_{1,k+1|k}}{\delta_1(q_{k+1|k})} & 0 & 0 & \frac{x_{1,k+1|k} - x_{k+1|k}}{\delta_1(q_{k+1|k})} & \frac{y_{1,k+1|k} - y_{k+1|k}}{\delta_1(q_{k+1|k})} & 0 & 0 \\ \frac{x_{k+1|k} - x_{1,k+1|k}}{\delta_2(q_{k+1|k})} & \frac{y_{k+1|k} - y_{1,k+1|k}}{\delta_2(q_{k+1|k})} & 0 & 0 & 0 & 0 & \frac{x_{1,k+1|k} - x_{k+1|k}}{\delta_2(q_{k+1|k})} & \frac{y_{1,k+1|k} - y_{k+1|k}}{\delta_2(q_{k+1|k})} \\ \end{pmatrix} \\ \\ \\ \delta_i(q_k) = \sqrt{(x_k - x_{i,k})^2 + (y_k - y_{i,k})^2 + \bar{z}^2}" /></a>

The equations of the EKF are always the same. Let's focus on the scheme: during the **PREDICTION** phase we need the previous **estimation** of both q and P, the **inputs** of v and u which are available (in the text), the **gravity** which is known and the white **noise**. During the **CORRECTION** phase we need the current estimation, which is given by the previous phase, the **z** value which is constant, the results of the **sensors** and the white **noise**. 

# Class Test 2012/2013

## Problem 1

### Configuration vector

Without considering the robotic arm we know the unicycle needs three coordinates: (x,y) for the position of the center and (theta) for its orientation on the plane. The kinematic arm has one degree of freedom which depends on the angle of rotation of the arm with respect to the orientation of the chassis, this adds the fourth coordinate (phi).

### Kinematic Model

We can augment the model of the unicycle considering that the robotic arm needs to be commanded on its own.

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;\dot{x}&space;=&space;v&space;cos(\theta)&space;\\&space;\dot{y}&space;=&space;v&space;sin(\theta)&space;\\&space;\dot{\theta}&space;=&space;w&space;\\&space;\dot{\phi}&space;=&space;u&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}&space;=&space;v&space;cos(\theta)&space;\\&space;\dot{y}&space;=&space;v&space;sin(\theta)&space;\\&space;\dot{\theta}&space;=&space;w&space;\\&space;\dot{\phi}&space;=&space;u&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x} = v cos(\theta) \\ \dot{y} = v sin(\theta) \\ \dot{\theta} = w \\ \dot{\phi} = u \end{matrix}\right." /></a>

### End-Effector 

The end effector position depends on the position of the chassis plus the terms relative to the orientation of the chassis and of the arm.

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}&space;x_{ee}&space;\\&space;y_{ee}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;&plus;&space;dcos(\theta)&space;&plus;&space;lcos(\theta&space;&plus;&space;\phi)&space;\\&space;y&space;&plus;&space;d&space;sin(\theta)&space;&plus;&space;l&space;sin(\theta&space;&plus;&space;\phi)&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;x_{ee}&space;\\&space;y_{ee}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;&plus;&space;dcos(\theta)&space;&plus;&space;lcos(\theta&space;&plus;&space;\phi)&space;\\&space;y&space;&plus;&space;d&space;sin(\theta)&space;&plus;&space;l&space;sin(\theta&space;&plus;&space;\phi)&space;\end{pmatrix}" title="\begin{pmatrix} x_{ee} \\ y_{ee} \end{pmatrix} = \begin{pmatrix} x + dcos(\theta) + lcos(\theta + \phi) \\ y + d sin(\theta) + l sin(\theta + \phi) \end{pmatrix}" /></a>

It's easy to see that this is not a flat output, even differentiating it we have mixed dependencies on the other state variables which do not allow to retrieve all the state from their knowledge.

### Define a control law over a deisred ee trajectory

The hint says to try the input-output linearization, to do so we first need to find the T matrix. We know the desired trajectory so we can also differentiate it.

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}&space;\dot{x_{ee}}&space;\\&space;\dot{y_{ee}}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;-&space;d\dot{\theta}sin(\theta)&space;-&space;l(\dot{\theta}&space;&plus;&space;\dot{\phi})sin(\theta&space;&plus;&space;\phi)&space;\\&space;\dot{y}&space;&plus;&space;d\dot{\theta}cos(\theta)&space;&plus;&space;l(\dot{\theta}&space;&plus;&space;\dot{\phi})cos(\theta&space;&plus;&space;\phi)&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;vcos(\theta)&space;-&space;dwsin(\theta)&space;-&space;l(w&space;&plus;&space;u)sin(\theta&space;&plus;&space;\phi)&space;\\&space;vsin(\theta)&space;&plus;&space;dwcos(\theta)&space;&plus;&space;l(w&space;&plus;&space;u)cos(\theta&space;&plus;&space;\phi)&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;\dot{x_{ee}}&space;\\&space;\dot{y_{ee}}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;-&space;d\dot{\theta}sin(\theta)&space;-&space;l(\dot{\theta}&space;&plus;&space;\dot{\phi})sin(\theta&space;&plus;&space;\phi)&space;\\&space;\dot{y}&space;&plus;&space;d\dot{\theta}cos(\theta)&space;&plus;&space;l(\dot{\theta}&space;&plus;&space;\dot{\phi})cos(\theta&space;&plus;&space;\phi)&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;vcos(\theta)&space;-&space;dwsin(\theta)&space;-&space;l(w&space;&plus;&space;u)sin(\theta&space;&plus;&space;\phi)&space;\\&space;vsin(\theta)&space;&plus;&space;dwcos(\theta)&space;&plus;&space;l(w&space;&plus;&space;u)cos(\theta&space;&plus;&space;\phi)&space;\end{pmatrix}" title="\begin{pmatrix} \dot{x_{ee}} \\ \dot{y_{ee}} \end{pmatrix} = \begin{pmatrix} \dot{x} - d\dot{\theta}sin(\theta) - l(\dot{\theta} + \dot{\phi})sin(\theta + \phi) \\ \dot{y} + d\dot{\theta}cos(\theta) + l(\dot{\theta} + \dot{\phi})cos(\theta + \phi) \end{pmatrix} = \begin{pmatrix} vcos(\theta) - dwsin(\theta) - l(w + u)sin(\theta + \phi) \\ vsin(\theta) + dwcos(\theta) + l(w + u)cos(\theta + \phi) \end{pmatrix}" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=T=&space;\begin{bmatrix}&space;cos(\theta)&space;&&space;-dsin(\theta)-lsin(\theta&space;&plus;&space;\phi)&space;&&space;-lsin(\theta&space;&plus;&space;\phi)&space;\\&space;sin(\theta)&space;&&space;dcos(\theta)&plus;lcos(\theta&space;&plus;&space;\phi)&space;&&space;lcos(\theta&space;&plus;&space;\phi)&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?T=&space;\begin{bmatrix}&space;cos(\theta)&space;&&space;-dsin(\theta)-lsin(\theta&space;&plus;&space;\phi)&space;&&space;-lsin(\theta&space;&plus;&space;\phi)&space;\\&space;sin(\theta)&space;&&space;dcos(\theta)&plus;lcos(\theta&space;&plus;&space;\phi)&space;&&space;lcos(\theta&space;&plus;&space;\phi)&space;\end{bmatrix}" title="T= \begin{bmatrix} cos(\theta) & -dsin(\theta)-lsin(\theta + \phi) & -lsin(\theta + \phi) \\ sin(\theta) & dcos(\theta)+lcos(\theta + \phi) & lcos(\theta + \phi) \end{bmatrix}" /></a>

So we can linearize the input-output relationship using this matrix saying that the vector v, w, u is equal to inv(T)\*(new inputs). This means we can use the control law in the new inputs as:

<a href="https://www.codecogs.com/eqnedit.php?latex=w_i&space;=&space;\dot{x_{ee}}&space;&plus;&space;k_i&space;(x_{ee}&space;-&space;x)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w_i&space;=&space;\dot{x_{ee}}&space;&plus;&space;k_i&space;(x_{ee}&space;-&space;x)" title="w_i = \dot{x_{ee}} + k_i (x_{ee} - x)" /></a>

Equal for the second input on the y coordinate. 

## Problem 2 

TODO

## Problem 3

One omnidirectional point robot has no orientation, it's described just by its position (x,y) and it moves along the two directions following the two different inputs. This means that for both of them the time discrete model is:

<img src="https://latex.codecogs.com/png.latex?\left\{\begin{matrix}&space;x_{k&plus;1}&space;=&space;x_k&space;&plus;&space;u_1&space;T_s&space;\\&space;y_{k&plus;1}&space;=&space;y_k&space;&plus;&space;u_2&space;T_s&space;\end{matrix}\right." title="\left\{\begin{matrix} x_{k+1} = x_k + u_1 T_s \\ y_{k+1} = y_k + u_2 T_s \end{matrix}\right." />

For the landmark we know it does not move, so all the kinematic equations are linear. The system can be written as:

<img src="https://latex.codecogs.com/png.latex?\\&space;\chi_{k&plus;1}&space;=&space;I_{6&space;\times&space;6}\chi_k&space;&plus;&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;1&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;0&space;&0&space;&0&space;&0&space;\end{pmatrix}&space;\begin{pmatrix}&space;u_{1x,k}&space;\\&space;u_{1y,k}&space;\\&space;u_{2x,k}&space;\\&space;u_{2y,k}&space;\end{pmatrix}&space;&plus;&space;\begin{pmatrix}&space;n_{1,k}&space;\\&space;n_{2,k}&space;\\&space;n_{3,k}&space;\\&space;n_{4,k}&space;\\&space;0&space;\\0&space;\end{pmatrix}" title="\\ \chi_{k+1} = I_{6 \times 6}\chi_k + \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 &0 &0 &0 \end{pmatrix} \begin{pmatrix} u_{1x,k} \\ u_{1y,k} \\ u_{2x,k} \\ u_{2y,k} \end{pmatrix} + \begin{pmatrix} n_{1,k} \\ n_{2,k} \\ n_{3,k} \\ n_{4,k} \\ 0 \\0 \end{pmatrix}" />

Now, every robot senses the distance between itself and the other robot plus the distance between itself and the landmark; so we have four observations at each time step. 

<img src="https://latex.codecogs.com/png.latex?\\&space;h_k&space;=&space;\begin{pmatrix}&space;\sqrt{(x_{1,k}&space;-&space;x_{2,k})^2&space;&plus;&space;(y_{1,k}&space;-&space;y_{2,k})^2}&space;&plus;&space;w_{i,k}\\&space;\sqrt{(x_{1,k}&space;-&space;x_{l,k})^2&space;&plus;&space;(y_{1,k}&space;-&space;y_{l,k})^2}&space;&plus;&space;w_{2,k}\\&space;\sqrt{(x_{2,k}&space;-&space;x_{1,k})^2&space;&plus;&space;(y_{2,k}&space;-&space;y_{1,k})^2}&space;&plus;&space;w_{3,k}&space;\\&space;\sqrt{(x_{2,k}&space;-&space;x_{l,k})^2&space;&plus;&space;(y_{2,k}&space;-&space;y_{l,k})^2}&space;&plus;&space;w_{4,k}&space;\end{pmatrix}" title="\\ h_k = \begin{pmatrix} \sqrt{(x_{1,k} - x_{2,k})^2 + (y_{1,k} - y_{2,k})^2} + w_{i,k}\\ \sqrt{(x_{1,k} - x_{l,k})^2 + (y_{1,k} - y_{l,k})^2} + w_{2,k}\\ \sqrt{(x_{2,k} - x_{1,k})^2 + (y_{2,k} - y_{1,k})^2} + w_{3,k} \\ \sqrt{(x_{2,k} - x_{l,k})^2 + (y_{2,k} - y_{l,k})^2} + w_{4,k} \end{pmatrix}" />

The first and third observations should be equal, anyway using them both can improve our result, correcting measurement errors. The observation model is not linear, so we need to lienarize it.

<img src="https://latex.codecogs.com/png.latex?\\&space;H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;\frac{x_{1,k&plus;1|k}&space;-&space;x_{2,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;\frac{y_{1,k&plus;1|k}&space;-&space;y_{2,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;\frac{x_{2,k&plus;1|k}&space;-&space;x_{1,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;\frac{y_{2,k&plus;1|k}&space;-&space;y_{1,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;\\&space;\frac{x_{1,k&plus;1|k}&space;-&space;x_{l,k&plus;1|k}}{\eta_1(q_{k&plus;1|k})}&space;&&space;\frac{y_{1,k&plus;1|k}&space;-&space;y_{l,k&plus;1|k}}{\eta_1(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;&&space;\frac{x_{l,k&plus;1|k}&space;-&space;x_{1,k&plus;1|k}}{\eta_1(q_{k&plus;1|k})}&space;&&space;\frac{y_{l,k&plus;1|k}&space;-&space;y_{1,k&plus;1|k}}{\eta_1(q_{k&plus;1|k})}&space;\\&space;\frac{x_{1,k&plus;1|k}&space;-&space;x_{2,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;\frac{y_{1,k&plus;1|k}&space;-&space;y_{2,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;\frac{x_{2,k&plus;1|k}&space;-&space;x_{1,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;\frac{y_{2,k&plus;1|k}&space;-&space;y_{1,k&plus;1|k}}{\delta(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;\\&space;\frac{x_{2,k&plus;1|k}&space;-&space;x_{l,k&plus;1|k}}{\eta_2(q_{k&plus;1|k})}&space;&&space;\frac{y_{2,k&plus;1|k}&space;-&space;y_{l,k&plus;1|k}}{\eta_2(q_{k&plus;1|k})}&space;&&space;0&space;&&space;0&space;&&space;\frac{x_{l,k&plus;1|k}&space;-&space;x_{2,k&plus;1|k}}{\eta_2(q_{k&plus;1|k})}&space;&&space;\frac{y_{l,k&plus;1|k}&space;-&space;y_{2,k&plus;1|k}}{\eta_2(q_{k&plus;1|k})}&space;\end{pmatrix}" title="\\ H_{k+1} = \begin{pmatrix} \frac{x_{1,k+1|k} - x_{2,k+1|k}}{\delta(q_{k+1|k})} & \frac{y_{1,k+1|k} - y_{2,k+1|k}}{\delta(q_{k+1|k})} & \frac{x_{2,k+1|k} - x_{1,k+1|k}}{\delta(q_{k+1|k})} & \frac{y_{2,k+1|k} - y_{1,k+1|k}}{\delta(q_{k+1|k})} & 0 & 0 \\ \frac{x_{1,k+1|k} - x_{l,k+1|k}}{\eta_1(q_{k+1|k})} & \frac{y_{1,k+1|k} - y_{l,k+1|k}}{\eta_1(q_{k+1|k})} & 0 & 0 & \frac{x_{l,k+1|k} - x_{1,k+1|k}}{\eta_1(q_{k+1|k})} & \frac{y_{l,k+1|k} - y_{1,k+1|k}}{\eta_1(q_{k+1|k})} \\ \frac{x_{1,k+1|k} - x_{2,k+1|k}}{\delta(q_{k+1|k})} & \frac{y_{1,k+1|k} - y_{2,k+1|k}}{\delta(q_{k+1|k})} & \frac{x_{2,k+1|k} - x_{1,k+1|k}}{\delta(q_{k+1|k})} & \frac{y_{2,k+1|k} - y_{1,k+1|k}}{\delta(q_{k+1|k})} & 0 & 0 \\ \frac{x_{2,k+1|k} - x_{l,k+1|k}}{\eta_2(q_{k+1|k})} & \frac{y_{2,k+1|k} - y_{l,k+1|k}}{\eta_2(q_{k+1|k})} & 0 & 0 & \frac{x_{l,k+1|k} - x_{2,k+1|k}}{\eta_2(q_{k+1|k})} & \frac{y_{l,k+1|k} - y_{2,k+1|k}}{\eta_2(q_{k+1|k})} \end{pmatrix}" />

<img src="https://latex.codecogs.com/png.latex?\\&space;\delta(q_k)&space;=&space;\sqrt{(x_{1,k}&space;-&space;x_{2,k})^2&space;&plus;&space;(y_{1,k}&space;-&space;y_{2,k})^2}\\\eta_1(q_k)&space;=&space;\sqrt{(x_{1,k}&space;-&space;x_{l,k})^2&space;&plus;&space;(y_{1,k}&space;-&space;y_{l,k})^2}\\\eta_2(q_k)&space;=&space;\sqrt{(x_{2,k}&space;-&space;x_{l,k})^2&space;&plus;&space;(y_{2,k}&space;-&space;y_{l,k})^2}" title="\\ \delta(q_k) = \sqrt{(x_{1,k} - x_{2,k})^2 + (y_{1,k} - y_{2,k})^2}\\\eta_1(q_k) = \sqrt{(x_{1,k} - x_{l,k})^2 + (y_{1,k} - y_{l,k})^2}\\\eta_2(q_k) = \sqrt{(x_{2,k} - x_{l,k})^2 + (y_{2,k} - y_{l,k})^2}" />

The equations of the EKF are the common ones, just pay attention then we do not have a Fk matrix (because the kinematic model was already linear) and our 'A' matrix in the model is just the identity and can be omitted. The H matrix is the one above, because the observation model has been linearized. 

# Class Test 2011/2012

## Problem 1

### Constraint

It's easy to see that the constraint is Pfaffian, it can be written as a matrix A (composed by a1 and a2) multiplying the generalized velocities, and this matrix depens only on constant parameters and the cofngiuration.

### Kinematic Model

From the constraint we must find the null space of transpose(A). It's easy to see that the vector field is composed by one signle vector ( a1 , -a2 ) which multiplyies one single input of the system.

### Controllability

In this case we have a state of dimension 2 and only one vector of the vector field, so we need another one. Anyway, we cannot derive it from the kinematic model and we cannot use the LB, because we have just one vector so its Lie Bracket with itself would be a null vector. This means the system is not controllable and the constraint is indeed holonomic.

## Problem 2 

TODO

## Problem 3

We need to derive the kinematic model for this 'composited' robot and its time-discrete model. 

<img src="https://latex.codecogs.com/png.latex?\left\{\begin{matrix}&space;\dot{x}&space;=&space;v&space;cos(\theta)&space;\\&space;\dot{y}&space;=&space;v&space;sen(\theta)&space;\\&space;\dot{\theta}&space;=&space;w&space;\\&space;\dot{q_1}&space;=&space;u_1&space;\\&space;\dot{q_2}&space;=&space;u_2&space;\end{matrix}\right&space;\rightarrow&space;\left\{\begin{matrix}&space;x_{k&plus;1}&space;=&space;x_k&space;&plus;&space;v_k&space;T_s&space;cos(\theta_k)&space;&plus;&space;n_{1,k}&space;\\&space;y_{k&plus;1}=&space;y_k&space;&plus;&space;v_k&space;T_s&space;sen(\theta_k)&space;&plus;&space;n_{2,k}&space;\\&space;\theta_{k&plus;1}&space;=&space;\theta_k&space;&plus;&space;w_k&space;T_s&space;&plus;&space;n_{3,k}&space;\\&space;q_{1,k&plus;1}&space;=&space;q_{1,k}&space;&plus;&space;u_{1,k}&space;T_s&space;&plus;&space;n_{4,k}&space;\\&space;q_{2,k&plus;1}&space;=&space;q_{2,k}&space;&plus;&space;u_{2,k}&space;T_s&space;&plus;&space;n_{5,k}&space;\end{matrix}\right" title="\left\{\begin{matrix} \dot{x} = v cos(\theta) \\ \dot{y} = v sen(\theta) \\ \dot{\theta} = w \\ \dot{q_1} = u_1 \\ \dot{q_2} = u_2 \end{matrix}\right \rightarrow \left\{\begin{matrix} x_{k+1} = x_k + v_k T_s cos(\theta_k) + n_{1,k} \\ y_{k+1}= y_k + v_k T_s sen(\theta_k) + n_{2,k} \\ \theta_{k+1} = \theta_k + w_k T_s + n_{3,k} \\ q_{1,k+1} = q_{1,k} + u_{1,k} T_s + n_{4,k} \\ q_{2,k+1} = q_{2,k} + u_{2,k} T_s + n_{5,k} \end{matrix}\right" />

Obviously the system needs to be linearized. In this case the state of the Kalman Filter is exactly the configuration state, because the position of the beacon is known.

<img src="https://latex.codecogs.com/png.latex?F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\theta_k)&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\theta_k)&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&1&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;\end{pmatrix}" title="F_k = \begin{pmatrix} 1 & 0 & - v_k T_s sen(\theta_k) & 0 & 0 \\ 0 & 1 & v_k T_s cos(\theta_k) & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 &1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{pmatrix}" />

Now let's see the observation: the relative distance to the becon's location, which is known. But it's not the distance from (x,y) which is the center of the robot, but from the end effector. 

<img src="https://latex.codecogs.com/png.latex?\\&space;h_k&space;=&space;\sqrt{(x_{e,k}&space;-&space;x_b)^2&space;&plus;&space;(y_{e,k}&space;-&space;y_b)^2}&space;\\&space;\begin{pmatrix}&space;x_{e,k}&space;\\&space;y_{e,k}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x_{k}&space;&plus;&space;dcos(\theta_k)&space;&plus;&space;l_1&space;cos(\theta_k&space;&plus;&space;q_{1,k})&space;&plus;&space;l_2&space;cos(\theta_k&space;&plus;&space;q_{1,k}&space;&plus;&space;q_{2,k})&space;\\&space;y_{k}&space;&plus;&space;dsen(\theta_k)&space;&plus;&space;l_1&space;sen(\theta_k&space;&plus;&space;q_{1,k})&space;&plus;&space;l_2&space;sen(\theta_k&space;&plus;&space;q_{1,k}&space;&plus;&space;q_{2,k})&space;\end{pmatrix}" title="\\ h_k = \sqrt{(x_{e,k} - x_b)^2 + (y_{e,k} - y_b)^2} \\ \begin{pmatrix} x_{e,k} \\ y_{e,k} \end{pmatrix} = \begin{pmatrix} x_{k} + dcos(\theta_k) + l_1 cos(\theta_k + q_{1,k}) + l_2 cos(\theta_k + q_{1,k} + q_{2,k}) \\ y_{k} + dsen(\theta_k) + l_1 sen(\theta_k + q_{1,k}) + l_2 sen(\theta_k + q_{1,k} + q_{2,k}) \end{pmatrix}" />

The presence of sen and cos, the square root = the observation model is non linear. We need to linearize, using the chain form of the derivatives it's easier. 

<img src="https://latex.codecogs.com/gif.latex?\small&space;\\&space;H_{k&plus;1}&space;=&space;\frac{\partial&space;h_k}{\partial&space;p_e}&space;\frac{\partial&space;p_e}{\partial&space;q_{k&plus;1|k}}&space;\\&space;\frac{\partial&space;h_k}{\partial&space;p_e}&space;=&space;\frac{1}{\sqrt{(x_{e,k&plus;1|k}&space;-&space;x_b)^2&space;&plus;&space;(y_{e,k&plus;1|k}&space;-&space;y_b)^2&space;}}&space;\begin{pmatrix}&space;x_{e,k&plus;1|k}&space;-&space;x_b&space;&&space;y_{e,k&plus;1|k}-y_b&space;\end{pmatrix}&space;\\&space;\frac{\partial&space;p_e}{\partial&space;q_{k&plus;1|k}}&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-d&space;sen(\theta_{k&plus;1|k})&space;-l_1&space;sen(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k})&space;-&space;l_2&space;sen(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k}&space;&plus;&space;q_{2,k&plus;1|k})&space;&&space;-l_1&space;sen(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k})&space;-&space;l_2&space;sen(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k}&space;&plus;&space;q_{2,k&plus;1|k})&space;&&space;-&space;l_2&space;sen(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k}&space;&plus;&space;q_{2,k&plus;1|k})&space;\\&space;0&space;&&space;1&space;&&space;d&space;cos(\theta_{k&plus;1|k})&space;&plus;&space;l_1&space;cos(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k})&space;&plus;&space;l_2&space;cos(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k}&space;&plus;&space;q_{2,k&plus;1|k})&space;&&space;l_1&space;cos(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k})&space;&plus;&space;l_2&space;cos(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k}&space;&plus;&space;q_{2,k&plus;1|k})&space;&&space;l_2&space;cos(\theta_{k&plus;1|k}&space;&plus;&space;q_{1,k&plus;1|k}&space;&plus;&space;q_{2,k&plus;1|k})&space;\end{pmatrix}" title="\small \\ H_{k+1} = \frac{\partial h_k}{\partial p_e} \frac{\partial p_e}{\partial q_{k+1|k}} \\ \frac{\partial h_k}{\partial p_e} = \frac{1}{\sqrt{(x_{e,k+1|k} - x_b)^2 + (y_{e,k+1|k} - y_b)^2 }} \begin{pmatrix} x_{e,k+1|k} - x_b & y_{e,k+1|k}-y_b \end{pmatrix} \\ \frac{\partial p_e}{\partial q_{k+1|k}} = \begin{pmatrix} 1 & 0 & -d sen(\theta_{k+1|k}) -l_1 sen(\theta_{k+1|k} + q_{1,k+1|k}) - l_2 sen(\theta_{k+1|k} + q_{1,k+1|k} + q_{2,k+1|k}) & -l_1 sen(\theta_{k+1|k} + q_{1,k+1|k}) - l_2 sen(\theta_{k+1|k} + q_{1,k+1|k} + q_{2,k+1|k}) & - l_2 sen(\theta_{k+1|k} + q_{1,k+1|k} + q_{2,k+1|k}) \\ 0 & 1 & d cos(\theta_{k+1|k}) + l_1 cos(\theta_{k+1|k} + q_{1,k+1|k}) + l_2 cos(\theta_{k+1|k} + q_{1,k+1|k} + q_{2,k+1|k}) & l_1 cos(\theta_{k+1|k} + q_{1,k+1|k}) + l_2 cos(\theta_{k+1|k} + q_{1,k+1|k} + q_{2,k+1|k}) & l_2 cos(\theta_{k+1|k} + q_{1,k+1|k} + q_{2,k+1|k}) \end{pmatrix}" />

From here we have always the same equations of the EKF. The block scheme is also the common one: we use the last estimation with the kinematic model and the wheel encoder readings in the prediction, then we use the result with the sensor readings for the correction. 


# Class Test 2010/2011 A

## Problem 1

### Generalized Coordinates

Starting from the first vehicle we need four coordinates: (x,y) for the position, theta for the orientation of the chassis and phi for the orientation of the wheels. Then we need to add another coordinate for the orientation of the trailer's chassis and for the orientation of its wheels, let's call it theta and phi of the trailer. 

<a href="https://www.codecogs.com/eqnedit.php?latex=q&space;=&space;\begin{bmatrix}x&space;&&space;y&space;&&space;\theta&space;&&space;\phi&space;&&space;\theta_t&space;&&space;\phi_t&space;\end{bmatrix}^T" target="_blank"><img src="https://latex.codecogs.com/gif.latex?q&space;=&space;\begin{bmatrix}x&space;&&space;y&space;&&space;\theta&space;&&space;\phi&space;&&space;\theta_t&space;&&space;\phi_t&space;\end{bmatrix}^T" title="q = \begin{bmatrix}x & y & \theta & \phi & \gamma \end{bmatrix}^T" /></a>

### Pfaffian form of the Constraints

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;\dot{x}sin(\theta)&space;-&space;\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x_f}sin(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y_f}cos(\theta&space;&plus;&space;\phi)&space;=&space;0&space;\\&space;\dot{x_t}sin(\theta_t&space;&plus;&space;\phi_t)&space;-&space;\dot{y_t}cos(\theta_t&space;&plus;&space;\phi_t)&space;=&space;0&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}sin(\theta)&space;-&space;\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x_f}sin(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y_f}cos(\theta&space;&plus;&space;\phi)&space;=&space;0&space;\\&space;\dot{x_t}sin(\theta_t&space;&plus;&space;\phi_t)&space;-&space;\dot{y_t}cos(\theta_t&space;&plus;&space;\phi_t)&space;=&space;0&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x}sin(\theta) - \dot{y}cos(\theta) = 0 \\ \dot{x_f}sin(\theta + \phi) - \dot{y_f}cos(\theta + \phi) = 0 \\ \dot{x_t}sin(\theta_t + \phi_t) - \dot{y_t}cos(\theta_t + \phi_t) = 0 \end{matrix}\right." /></a>

Now we'll derive the formulas for the position of the 'center' of the front wheels and trailer wheels to substitute them inside the equations, so to have everything express only in the correct parameters.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;\begin{pmatrix}&space;x_f&space;\\&space;y_f&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;&plus;&space;lcos(\theta)&space;\\&space;y&space;&plus;&space;lsen(\theta)\end{pmatrix}&space;\rightarrow&space;\begin{pmatrix}&space;\dot{x_f}&space;\\&space;\dot{y_f}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;-&space;l\dot{\theta}sen(\theta)&space;\\&space;\dot{y}&space;&plus;&space;l\dot{\theta}cos(\theta)\end{pmatrix}&space;\\&space;\\&space;\begin{pmatrix}&space;x_t&space;\\&space;y_t&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;-&space;l_tcos(\theta_t)&space;\\&space;y&space;-&space;l_tsen(\theta_t)\end{pmatrix}&space;\rightarrow&space;\begin{pmatrix}&space;\dot{x_t}&space;\\&space;\dot{y_t}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;&plus;&space;l_t\dot{\theta_t}sen(\theta_t)&space;\\&space;\dot{y}&space;-&space;l_t\dot{\theta_t}cos(\theta_t)\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;\begin{pmatrix}&space;x_f&space;\\&space;y_f&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;&plus;&space;lcos(\theta)&space;\\&space;y&space;&plus;&space;lsen(\theta)\end{pmatrix}&space;\rightarrow&space;\begin{pmatrix}&space;\dot{x_f}&space;\\&space;\dot{y_f}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;-&space;l\dot{\theta}sen(\theta)&space;\\&space;\dot{y}&space;&plus;&space;l\dot{\theta}cos(\theta)\end{pmatrix}&space;\\&space;\\&space;\begin{pmatrix}&space;x_t&space;\\&space;y_t&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;-&space;l_tcos(\theta_t)&space;\\&space;y&space;-&space;l_tsen(\theta_t)\end{pmatrix}&space;\rightarrow&space;\begin{pmatrix}&space;\dot{x_t}&space;\\&space;\dot{y_t}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;&plus;&space;l_t\dot{\theta_t}sen(\theta_t)&space;\\&space;\dot{y}&space;-&space;l_t\dot{\theta_t}cos(\theta_t)\end{pmatrix}" title="\\ \begin{pmatrix} x_f \\ y_f \end{pmatrix} = \begin{pmatrix} x + lcos(\theta) \\ y + lsen(\theta)\end{pmatrix} \rightarrow \begin{pmatrix} \dot{x_f} \\ \dot{y_f} \end{pmatrix} = \begin{pmatrix} \dot{x} - l\dot{\theta}sen(\theta) \\ \dot{y} + l\dot{\theta}cos(\theta)\end{pmatrix} \\ \\ \begin{pmatrix} x_t \\ y_t \end{pmatrix} = \begin{pmatrix} x - l_tcos(\theta_t) \\ y - l_tsen(\theta_t)\end{pmatrix} \rightarrow \begin{pmatrix} \dot{x_t} \\ \dot{y_t} \end{pmatrix} = \begin{pmatrix} \dot{x} + l_t\dot{\theta_t}sen(\theta_t) \\ \dot{y} - l_t\dot{\theta_t}cos(\theta_t)\end{pmatrix}" /></a>

So the final constraints can be wrriten in equations and below in matrix form:

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;\dot{x}sen(\theta)-\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x}sen(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y}cos(\theta&space;&plus;&space;\phi)&space;-&space;l\dot{\theta}cos(\phi)&space;=&space;0&space;\\&space;\dot{x}sen(\theta_t&space;&plus;&space;\phi_t)&space;-&space;\dot{y}cos(\theta_t&space;&plus;&space;\phi_t)&space;&plus;l_t\dot{\theta_t}cos(\phi_t)&space;=&space;0&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}sen(\theta)-\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x}sen(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y}cos(\theta&space;&plus;&space;\phi)&space;-&space;l\dot{\theta}cos(\phi)&space;=&space;0&space;\\&space;\dot{x}sen(\theta_t&space;&plus;&space;\phi_t)&space;-&space;\dot{y}cos(\theta_t&space;&plus;&space;\phi_t)&space;&plus;l_t\dot{\theta_t}cos(\phi_t)&space;=&space;0&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x}sen(\theta)-\dot{y}cos(\theta) = 0 \\ \dot{x}sen(\theta + \phi) - \dot{y}cos(\theta + \phi) - l\dot{\theta}cos(\phi) = 0 \\ \dot{x}sen(\theta_t + \phi_t) - \dot{y}cos(\theta_t + \phi_t) +l_t\dot{\theta_t}cos(\phi_t) = 0 \end{matrix}\right." /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}sen(\theta)&space;&&space;-cos(\theta)&space;&&space;0&&space;0&space;&&space;0&space;&&space;0&space;\\&space;sen(\theta&space;&plus;&space;\phi)&space;&&space;-cos(\theta&space;&plus;&space;\phi)&space;&&space;-lcos(\phi)&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;en(\theta_t&space;&plus;&space;\phi_t)&space;&&space;-cos(\theta_t&space;&plus;&space;\phi_t)&space;&&space;0&space;&&space;0&space;&&space;l_t&space;cos(\phi_t)&space;&&space;0&space;\end{pmatrix}&space;\begin{pmatrix}&space;\dot{x}&space;\\&space;\dot{y}&space;\\&space;\dot{\theta}&space;\\&space;\dot{\phi}&space;\\&space;\dot{\theta_t}&space;\\&space;\dot{\phi_t}\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}sen(\theta)&space;&&space;-cos(\theta)&space;&&space;0&&space;0&space;&&space;0&space;&&space;0&space;\\&space;sen(\theta&space;&plus;&space;\phi)&space;&&space;-cos(\theta&space;&plus;&space;\phi)&space;&&space;-lcos(\phi)&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;sen(\theta_t&space;&plus;&space;\phi_t)&space;&&space;-cos(\theta_t&space;&plus;&space;\phi_t)&space;&&space;0&space;&&space;0&space;&&space;l_t&space;cos(\phi_t)&space;&&space;0&space;\end{pmatrix}&space;\begin{pmatrix}&space;\dot{x}&space;\\&space;\dot{y}&space;\\&space;\dot{\theta}&space;\\&space;\dot{\phi}&space;\\&space;\dot{\theta_t}&space;\\&space;\dot{\phi_t}\end{pmatrix}" title="\begin{pmatrix}sen(\theta) & -cos(\theta) & 0& 0 & 0 & 0 \\ sen(\theta + \phi) & -cos(\theta + \phi) & -lcos(\phi) & 0 & 0 & 0 \\ en(\theta_t + \phi_t) & -cos(\theta_t + \phi_t) & 0 & 0 & l_t cos(\phi_t) & 0 \end{pmatrix} \begin{pmatrix} \dot{x} \\ \dot{y} \\ \dot{\theta} \\ \dot{\phi} \\ \dot{\theta_t} \\ \dot{\phi_t}\end{pmatrix}" /></a>

### Kinematic Model

From the matrix above we can derive the vector field for the kinematic model. Being 3x6 the null space has dimension 3, the first two vectors are easy to find and correspond to the all-zeros columns:

<a href="https://www.codecogs.com/eqnedit.php?latex=g_1&space;=&space;\begin{pmatrix}&space;0&space;\\&space;0\\0\\1\\0\\0&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;0\\0\\0\\0\\0\\1&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?g_1&space;=&space;\begin{pmatrix}&space;0&space;\\&space;0\\0\\1\\0\\0&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;0\\0\\0\\0\\0\\1&space;\end{pmatrix}" title="g_1 = \begin{pmatrix} 0 \\ 0\\0\\1\\0\\0 \end{pmatrix} \hspace{0.5cm} g_2 = \begin{pmatrix} 0\\0\\0\\0\\0\\1 \end{pmatrix}" /></a>

The third one we can easily fin solving parametrically the equations and is:

<a href="https://www.codecogs.com/eqnedit.php?latex=g_3&space;=&space;\begin{pmatrix}&space;cos(\theta)&space;\\&space;sen(\theta)\\&space;\frac{tg(\phi)}{l_t}\\0\\-&space;\frac{sen(\theta&space;-&space;\theta_t&space;-&space;\phi_t)}{l_t&space;cos(\phi_t)}\\0&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?g_3&space;=&space;\begin{pmatrix}&space;cos(\theta)&space;\\&space;sen(\theta)\\&space;\frac{tg(\phi)}{l_t}\\0\\-&space;\frac{sen(\theta&space;-&space;\theta_t&space;-&space;\phi_t)}{l_t&space;cos(\phi_t)}\\0&space;\end{pmatrix}" title="g_3 = \begin{pmatrix} cos(\theta) \\ sen(\theta)\\ \frac{tg(\phi)}{l_t}\\0\\- \frac{sen(\theta - \theta_t - \phi_t)}{l_t cos(\phi_t)}\\0 \end{pmatrix}" /></a>

where the inputs are steering velocity of the main vehicle, the steering velocity of the trailer and then the velocity of the rear wheels. 

## Problem 2

First we can derive the position of the caster wheel dependiong on the configuration coordinates:

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;\begin{pmatrix}&space;x_c&space;\\&space;y_c&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;&plus;&space;Lcos(\theta)&space;\\&space;y&space;&plus;&space;Lsen(\theta)&space;\end{pmatrix}&space;\\&space;\begin{pmatrix}&space;\dot{x_c}&space;\\&space;\dot{y_c}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;-&space;L\dot{\theta}sen(\theta)&space;\\&space;\dot{y}&space;&plus;&space;L\dot{\theta}cos(\theta)&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;\begin{pmatrix}&space;x_c&space;\\&space;y_c&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x&space;&plus;&space;Lcos(\theta)&space;\\&space;y&space;&plus;&space;Lsen(\theta)&space;\end{pmatrix}&space;\\&space;\begin{pmatrix}&space;\dot{x_c}&space;\\&space;\dot{y_c}&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;\dot{x}&space;-&space;L\dot{\theta}sen(\theta)&space;\\&space;\dot{y}&space;&plus;&space;L\dot{\theta}cos(\theta)&space;\end{pmatrix}" title="\\ \begin{pmatrix} x_c \\ y_c \end{pmatrix} = \begin{pmatrix} x + Lcos(\theta) \\ y + Lsen(\theta) \end{pmatrix} \\ \begin{pmatrix} \dot{x_c} \\ \dot{y_c} \end{pmatrix} = \begin{pmatrix} \dot{x} - L\dot{\theta}sen(\theta) \\ \dot{y} + L\dot{\theta}cos(\theta) \end{pmatrix}" /></a>

We can easily see that out output, which is the velocity of the caster wheel, is a linear transformation of the inputs.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;T&space;=&space;\begin{bmatrix}&space;cos(\theta)&space;&&space;-Lsen(\theta)&space;\\&space;sen(\theta)&space;&&space;Lcos(\theta)\end{bmatrix}&space;\\&space;T^{-1}&space;=&space;\begin{bmatrix}&space;cos(\theta)&space;&&space;sen(\theta)&space;\\&space;-\frac{sen(\theta)}{L}&space;&&space;\frac{cos(\theta)}{L}\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;T&space;=&space;\begin{bmatrix}&space;cos(\theta)&space;&&space;-Lsen(\theta)&space;\\&space;sen(\theta)&space;&&space;Lcos(\theta)\end{bmatrix}&space;\\&space;T^{-1}&space;=&space;\begin{bmatrix}&space;cos(\theta)&space;&&space;sen(\theta)&space;\\&space;-\frac{sen(\theta)}{L}&space;&&space;\frac{cos(\theta)}{L}\end{bmatrix}" title="\\ T = \begin{bmatrix} cos(\theta) & -Lsen(\theta) \\ sen(\theta) & Lcos(\theta)\end{bmatrix} \\ T^{-1} = \begin{bmatrix} cos(\theta) & sen(\theta) \\ -\frac{sen(\theta)}{L} & \frac{cos(\theta)}{L}\end{bmatrix}" /></a>

Now, using the input-output linearization we have that the input velocities to the system is inv(T) times the velocity of the caster wheel. To express the velocity of the caster wheel in the x,y-frame we can consider that it has a norm Vc times cos or sin of an angle (cos for the x component and sen for the y). 
The angle depends on the orientation of the desired velocity, which for us is theta - alpha. 

Solving the expression we obtain the v, w inputs that we can transform to wr and wl which are the actual input of the differential drive. 

# Class Test 2010/2011 B

## Problem 1

TODO

## Problem 2

We already have the kinematic model, so we can build the time discrete model. The generalized coordinates are the same variables of the state because the two beacons have known positions. 

<img src="https://latex.codecogs.com/gif.latex?\small&space;\left\{\begin{matrix}&space;x_{k&plus;1}&space;=&space;x_k&space;&plus;&space;v_k&space;T_s&space;cos(\psi_k)&space;&plus;&space;n_{1,k}&space;\\&space;y_{k&plus;1}&space;=&space;y_k&space;&plus;&space;v_k&space;T_s&space;sen(\psi_K)&space;&plus;&space;n_{2,k}&space;\\&space;\psi_{k&plus;1}&space;=&space;\psi_k&space;-&space;\frac{g&space;T_s&space;tan(\phi_k)}{&space;v_k}&space;&plus;&space;n_{3,k}&space;\\&space;\phi_{k&plus;1}&space;=&space;\phi_k&space;&plus;&space;u_{\phi,k}&space;T_s&space;&plus;&space;n_{4,k}&space;\end{matrix}\right." title="\small \left\{\begin{matrix} x_{k+1} = x_k + v_k T_s cos(\psi_k) + n_{1,k} \\ y_{k+1} = y_k + v_k T_s sen(\psi_K) + n_{2,k} \\ \psi_{k+1} = \psi_k - \frac{g T_s tan(\phi_k)}{ v_k} + n_{3,k} \\ \phi_{k+1} = \phi_k + u_{\phi,k} T_s + n_{4,k} \end{matrix}\right." />

The observations are the two bearing angles wrt the two radio beacons. 

<img src="https://latex.codecogs.com/gif.latex?\small&space;h_k&space;=&space;\begin{pmatrix}&space;Atan2(y_k&space;-&space;y_1,&space;x_k&space;-&space;x_1)&space;-&space;\psi_k&space;&plus;&space;w_{1,k}\\&space;Atan2(y_k&space;-&space;y_2,&space;x_k&space;-&space;x_2)&space;-&space;\psi_k&space;&plus;&space;w_{2,k}&space;\end{pmatrix}&space;\\" title="\small h_k = \begin{pmatrix} Atan2(y_k - y_1, x_k - x_1) - \psi_k + w_{1,k}\\ Atan2(y_k - y_2, x_k - x_2) - \psi_k + w_{2,k} \end{pmatrix} \\" />

Both the kinematic and observation model are non linear.

<img src="https://latex.codecogs.com/gif.latex?\small&space;F_k&space;=&space;\begin{pmatrix}&space;1&space;&&space;0&space;&&space;-&space;v_k&space;T_s&space;sen(\psi_k)&space;&&space;0&space;\\&space;0&space;&&space;1&space;&&space;v_k&space;T_s&space;cos(\psi_k)&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;1&space;&&space;-\frac{g&space;T_s}{&space;v_k&space;cos^2(\phi_k)}&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;1&space;\end{pmatrix}" title="\small F_k = \begin{pmatrix} 1 & 0 & - v_k T_s sen(\psi_k) & 0 \\ 0 & 1 & v_k T_s cos(\psi_k) & 0 \\ 0 & 0 & 1 & -\frac{g T_s}{ v_k cos^2(\phi_k)} \\ 0 & 0 & 0 & 1 \end{pmatrix}" />

<img src="https://latex.codecogs.com/gif.latex?\small&space;\\&space;H_{k&plus;1}&space;=&space;\begin{pmatrix}&space;-\frac{y_k&space;-&space;y_1}{\delta_1(q_{k&plus;1|k})}&space;&&space;\frac{x_k&space;-&space;x_1}{\delta_1(q_{k&plus;1|k})}&space;&&space;-1&space;&&space;0&space;\\&space;-\frac{y_k&space;-&space;y_2}{\delta_2(q_{k&plus;1|k})}&space;&&space;\frac{x_k&space;-&space;x_2}{\delta_2(q_{k&plus;1|k})}&space;&&space;-1&space;&&space;0&space;\end{pmatrix}&space;\\&space;\\&space;\delta_1(q_k)&space;=&space;(x_k&space;-&space;x_1)^2&space;&plus;&space;(y_k&space;-&space;y_1)^2&space;\\&space;\delta_2(q_k)&space;=&space;(x_k&space;-&space;x_2)^2&space;&plus;&space;(y_k&space;-&space;y_2)^2" title="\small \\ H_{k+1} = \begin{pmatrix} -\frac{y_k - y_1}{\delta_1(q_{k+1|k})} & \frac{x_k - x_1}{\delta_1(q_{k+1|k})} & -1 & 0 \\ -\frac{y_k - y_2}{\delta_2(q_{k+1|k})} & \frac{x_k - x_2}{\delta_2(q_{k+1|k})} & -1 & 0 \end{pmatrix} \\ \\ \delta_1(q_k) = (x_k - x_1)^2 + (y_k - y_1)^2 \\ \delta_2(q_k) = (x_k - x_2)^2 + (y_k - y_2)^2" />

And from here is the same story. 

# Class Test 2009/2010 A

## Problem 1

### Generalized Coordinates

First we think about the coordinates for the tricycle: (x,y) for the position of P, theta for the chassis' orientation and phi for the front wheel's orientation. The trailer position can be recovered using the position of P and the angle of the revolute joint connecting it to the tricycle, so we only need this angle theta_trailer. 

Our final configuration vector is made up by x y theta phi theta_t. 

### Pfaffian Constraint

The constraints of pure rolling are applied to the front and rear wheel of the tricycle and on the wheel of the trailer. 

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;\dot{x}sen(\theta)&space;-&space;\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x_f}sen(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y_f}cos(\theta&space;&plus;&space;\phi)&space;=&space;0&space;\\&space;\dot{x_t}sen(\theta_t)&space;-&space;\dot{y_t}cos(\theta_t)&space;=&space;0&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}sen(\theta)&space;-&space;\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x_f}sen(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y_f}cos(\theta&space;&plus;&space;\phi)&space;=&space;0&space;\\&space;\dot{x_t}sen(\theta_t)&space;-&space;\dot{y_t}cos(\theta_t)&space;=&space;0&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x}sen(\theta) - \dot{y}cos(\theta) = 0 \\ \dot{x_f}sen(\theta + \phi) - \dot{y_f}cos(\theta + \phi) = 0 \\ \dot{x_t}sen(\theta_t) - \dot{y_t}cos(\theta_t) = 0 \end{matrix}\right." /></a>

Expressing the position of the front wheel and of the trailer wheel wrt the configuration variables and deriving them we obtain the full system only in the right coordinates.

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;\dot{x}sen(\theta)&space;-&space;\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x}sen(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y}cos(\theta&space;&plus;&space;\phi)&space;-l\dot{\theta}cos(\phi)&space;=&space;0&space;\\&space;\dot{x}sen(\theta_t)&space;-&space;\dot{y}cos(\theta_t)&space;&plus;&space;l_t&space;\dot{\theta_t}=&space;0&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}sen(\theta)&space;-&space;\dot{y}cos(\theta)&space;=&space;0&space;\\&space;\dot{x}sen(\theta&space;&plus;&space;\phi)&space;-&space;\dot{y}cos(\theta&space;&plus;&space;\phi)&space;-l\dot{\theta}cos(\phi)&space;=&space;0&space;\\&space;\dot{x}sen(\theta_t)&space;-&space;\dot{y}cos(\theta_t)&space;&plus;&space;l_t&space;\dot{\theta_t}=&space;0&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x}sen(\theta) - \dot{y}cos(\theta) = 0 \\ \dot{x}sen(\theta + \phi) - \dot{y}cos(\theta + \phi) -l\dot{\theta}cos(\phi) = 0 \\ \dot{x}sen(\theta_t) - \dot{y}cos(\theta_t) + l_t \dot{\theta_t}= 0 \end{matrix}\right." /></a>

In matrix form:

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;\begin{bmatrix}&space;sen(\theta)&space;&&space;-cos(\theta)&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;sen(\theta&space;&plus;&space;\phi)&space;&&space;-cos(\theta&space;&plus;&space;\phi)&space;&&space;-lcos/\phi&space;&&space;0&space;&&space;0&space;\\&space;sen(\theta_t)&space;&&space;-cos(\theta_t)&space;&&space;0&space;&&space;0&space;&&space;l_t&space;\end{bmatrix}&space;\begin{pmatrix}&space;\dot{x}&space;\\&space;\dot{y}&space;\\&space;\dot{\theta}&space;\\&space;\dot{\phi}&space;\\&space;\dot{\theta_t}&space;\end{pmatrix}&space;=&space;\mathbf{0}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;\begin{bmatrix}&space;sen(\theta)&space;&&space;-cos(\theta)&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;sen(\theta&space;&plus;&space;\phi)&space;&&space;-cos(\theta&space;&plus;&space;\phi)&space;&&space;-lcos/\phi&space;&&space;0&space;&&space;0&space;\\&space;sen(\theta_t)&space;&&space;-cos(\theta_t)&space;&&space;0&space;&&space;0&space;&&space;l_t&space;\end{bmatrix}&space;\begin{pmatrix}&space;\dot{x}&space;\\&space;\dot{y}&space;\\&space;\dot{\theta}&space;\\&space;\dot{\phi}&space;\\&space;\dot{\theta_t}&space;\end{pmatrix}&space;=&space;\mathbf{0}" title="\\ \begin{bmatrix} sen(\theta) & -cos(\theta) & 0 & 0 & 0 \\ sen(\theta + \phi) & -cos(\theta + \phi) & -lcos/\phi & 0 & 0 \\ sen(\theta_t) & -cos(\theta_t) & 0 & 0 & l_t \end{bmatrix} \begin{pmatrix} \dot{x} \\ \dot{y} \\ \dot{\theta} \\ \dot{\phi} \\ \dot{\theta_t} \end{pmatrix} = \mathbf{0}" /></a>


### Kinematic Model
From the matrix we can obtain the kinematic model. The null space of the matrix has dimension 2: one of the vector is easy to find by inspection (the fourth column is all zeros), the other must be adapted from the knowledge of the unicycle.

<a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;g_1&space;=&space;\begin{pmatrix}&space;0&space;\\&space;0&space;\\&space;0&space;\\&space;1&space;\\&space;0&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;cos(\theta)&space;\\&space;sen(\theta)&space;\\&space;\alpha&space;\\&space;0&space;\\&space;\beta&space;\end{pmatrix}&space;\hspace{1cm}&space;\alpha&space;=&space;\frac{tg(\phi)}{l}&space;,&space;\beta&space;=&space;-&space;\frac{sen(\theta_t&space;-&space;\theta)}{l_t}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;g_1&space;=&space;\begin{pmatrix}&space;0&space;\\&space;0&space;\\&space;0&space;\\&space;1&space;\\&space;0&space;\end{pmatrix}&space;\hspace{0.5cm}&space;g_2&space;=&space;\begin{pmatrix}&space;cos(\theta)&space;\\&space;sen(\theta)&space;\\&space;\alpha&space;\\&space;0&space;\\&space;\beta&space;\end{pmatrix}&space;\hspace{1cm}&space;\alpha&space;=&space;\frac{tg(\phi)}{l}&space;,&space;\beta&space;=&space;-&space;\frac{sen(\theta_t&space;-&space;\theta)}{l_t}" title="\\ g_1 = \begin{pmatrix} 0 \\ 0 \\ 0 \\ 1 \\ 0 \end{pmatrix} \hspace{0.5cm} g_2 = \begin{pmatrix} cos(\theta) \\ sen(\theta) \\ \alpha \\ 0 \\ \beta \end{pmatrix} \hspace{1cm} \alpha = \frac{tg(\phi)}{l} , \beta = - \frac{sen(\theta_t - \theta)}{l_t}" /></a>

## Problem 2

A similar exercise can be found <a href='https://github.com/theroggio/Autonomous-and-Mobile-Robotics-La-Sapienza-/blob/master/Chapter%2011.md#problem-1115'> here </a> where it uses a bicycle instead of a car-like vehicle. It's easy to see that the solution is the same, being the car-like model the same of the bicycle. 
 
# Class Test 2009/2010 B

## Problem 1

Firs of all we need to indeitify a set of control points on the robot. It cannot change its orientation so we can easily use just one control point on one corner. 

Here one of the possible solution for the C-obstacles shapes (using a different control point results in a different shape).

<img src='https://github.com/theroggio/Autonomous-and-Mobile-Robotics-La-Sapienza-/blob/master/images/c-obstacles.jpg' />

TODO

## Problem 2

Problem done on paper. Anyway the kinematic model has already been derived, and similar problem have been done previously. This has no other difficulties. 


