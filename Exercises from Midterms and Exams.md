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

TODO

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

TODO 

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

If the initial configuration is not a singular one we can just set both of them to zero, if the initial configuration is singular we need to move outside of it (epslon burst of one of the wheels velocity) and when they are different we can go back to the previous case.

## Problem 3

TODO

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

TODO

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

TODO

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

TODO

# Class Test 2011/2012

## Problem 1

### Constraint

It's easy to see that the constraint is Pfaffian, it can be written as a matrix A (composed by a1 and a2) multiplying the generalized velocities, and this matrix depens only on constant parameters and the cofngiuration.

### Kinematic Model

From the constraint we must find the null space of transpose(A).

 
