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


