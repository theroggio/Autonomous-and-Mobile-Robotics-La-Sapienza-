# Exercises from Chapter 11 

## Problem 11.1

First we think about the tricycle, it needs 4 generalized coordinates: x-position, y-position, angle wrt x axis of the chassis, angle of the steerable wheel wrt chassis orientation.

Then for each of the N trailers, we can establish the position of the center between the wheels from the x and y position of the chassis, knowing the orientation of the wheels wrt the orientation of the wheels / chassis of the tricycle. 

So for each one of the N trailers we just need the orientation coordinate. 

This means the final set of generalized coordinates is <img src="http://bit.ly/2VYODuU" align="center" border="0" alt="q= \begin{bmatrix}x & y & \phi & \theta_0 & ... & \theta_N \end{bmatrix} ^T" width="150" height="20" />.

## Problem 11.2

We can easily build the matrix for the Pfaffian constraints which is

<a href="https://www.codecogs.com/eqnedit.php?latex=A^T&space;=&space;\begin{bmatrix}&space;0.5(\sqrt{3}c_3&space;-s_3)&space;&&space;0.5(c_3&space;&plus;&space;\sqrt{3}s_3)&space;&&space;l&space;&&space;r&space;&&space;0&space;&&space;0\\&space;s_3&space;&&space;-c_3&space;&&space;l&space;&&space;0&space;&&space;r&space;&&space;0\\&space;-0.5(\sqrt{3}c_3&plus;s_3)&space;&&space;0.5(c_3&space;-&space;\sqrt{3}s_3)&space;&&space;l&space;&&space;0&space;&&space;0&space;&&space;r&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?A^T&space;=&space;\begin{bmatrix}&space;0.5(\sqrt{3}c_3&space;-s_3)&space;&&space;0.5(c_3&space;&plus;&space;\sqrt{3}s_3)&space;&&space;l&space;&&space;r&space;&&space;0&space;&&space;0\\&space;s_3&space;&&space;-c_3&space;&&space;l&space;&&space;0&space;&&space;r&space;&&space;0\\&space;-0.5(\sqrt{3}c_3&plus;s_3)&space;&&space;0.5(c_3&space;-&space;\sqrt{3}s_3)&space;&&space;l&space;&&space;0&space;&&space;0&space;&&space;r&space;\end{bmatrix}" title="A^T = \begin{bmatrix} 0.5(\sqrt{3}c_3 -s_3) & 0.5(c_3 + \sqrt{3}s_3) & l & r & 0 & 0\\ s_3 & -c_3 & l & 0 & r & 0\\ -0.5(\sqrt{3}c_3+s_3) & 0.5(c_3 - \sqrt{3}s_3) & l & 0 & 0 & r \end{bmatrix}" /></a>

Now we do not consider the first two columns, which are very likely not integrable due to the presence of cosine and sine. Restricting ourselves to the situation where the center of the robot is not moving (first two velocities are zero) we can sum up the three rows and obtain:

<a href="https://www.codecogs.com/eqnedit.php?latex=3l\dot{q_3}&space;&plus;&space;r(\dot{q_4}&space;&plus;&space;\dot{q_5}&space;&plus;&space;\dot{q_6})&space;=&space;0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?3l\dot{q_3}&space;&plus;&space;r(\dot{q_4}&space;&plus;&space;\dot{q_5}&space;&plus;&space;\dot{q_6})&space;=&space;0" title="3l\dot{q_3} + r(\dot{q_4} + \dot{q_5} + \dot{q_6}) = 0" /></a>

From here we can easily re-order the equation and prove together that the constraint is integrable (so the system is partially integrable) and that the orientation of the vehicle (q3) is a linear function of the rotational angles of the wheels.

<a href="https://www.codecogs.com/eqnedit.php?latex=\dot{q_3}&space;=&space;-&space;\frac{r}{3l}(\dot{q_4}&space;&plus;&space;\dot{q_5}&space;&plus;&space;\dot{q_6})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dot{q_3}&space;=&space;-&space;\frac{r}{3l}(\dot{q_4}&space;&plus;&space;\dot{q_5}&space;&plus;&space;\dot{q_6})" title="\dot{q_3} = - \frac{r}{3l}(\dot{q_4} + \dot{q_5} + \dot{q_6})" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=q_3&space;=&space;-&space;\frac{r}{3l}(q_4&space;&plus;&space;q_5&space;&plus;&space;q_6)&space;&plus;&space;c" target="_blank"><img src="https://latex.codecogs.com/gif.latex?q_3&space;=&space;-&space;\frac{r}{3l}(q_4&space;&plus;&space;q_5&space;&plus;&space;q_6)&space;&plus;&space;c" title="q_3 = - \frac{r}{3l}(q_4 + q_5 + q_6) + c" /></a>

## Problem 11.3

We need to remember that every component of the time derivative of q can be wrriten as the summation of a product between g_i * u_i. 

Considering the integrability condition we can assume that the n-1 vectors of the vector field are in the form

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}&space;-\gamma(q)a_2(q)\\&space;\gamma(q)a_1(q)\\&space;0\\&space;...\\&space;0&space;\\&space;\end{pmatrix}&space;\begin{pmatrix}&space;-\gamma(q)a_3(q)\\&space;0\\&space;\gamma(q)a_1(q)\\&space;...\\&space;0&space;\\&space;\end{pmatrix}&space;\begin{pmatrix}&space;-\gamma(q)a_n(q)\\&space;0\\&space;0\\&space;...\\&space;\gamma(q)a_1(q)&space;\\&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;-\gamma(q)a_2(q)\\&space;\gamma(q)a_1(q)\\&space;0\\&space;...\\&space;0&space;\\&space;\end{pmatrix}&space;\begin{pmatrix}&space;-\gamma(q)a_3(q)\\&space;0\\&space;\gamma(q)a_1(q)\\&space;...\\&space;0&space;\\&space;\end{pmatrix}&space;\begin{pmatrix}&space;-\gamma(q)a_n(q)\\&space;0\\&space;0\\&space;...\\&space;\gamma(q)a_1(q)&space;\\&space;\end{pmatrix}" title="\begin{pmatrix} -\gamma(q)a_2(q)\\ \gamma(q)a_1(q)\\ 0\\ ...\\ 0 \\ \end{pmatrix} \begin{pmatrix} -\gamma(q)a_3(q)\\ 0\\ \gamma(q)a_1(q)\\ ...\\ 0 \\ \end{pmatrix} \begin{pmatrix} -\gamma(q)a_n(q)\\ 0\\ 0\\ ...\\ \gamma(q)a_1(q) \\ \end{pmatrix}" /></a>

The involutiveness is true if any Lie Bracket between any couple of vectors can be expressed as linear combination of the input vectors as well. Usin the integrability condition is easy to prove that any possible Lie Bracket will respect that having only partial derivative of gamma multiplied by a_i. 

## Problem 11.4

Without a mathematical prove, it's an easy intuition to say that if the Pfaffian matrix does not depend on the generalized coordinates it means that for our purpose it's a constant matrix. This matrix multiply the generalized velocities and as we know the result is a set of linear equation in the generalized velocities. 

If the constraint does not depends on the generalized coordinates, we have just coefficients multiplying the generalized velocities and this is always integrable. 

## Problem 11.5

First of all we need to remember the kinematic model of the unicycle, which is 

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;\dot{x}&space;=&space;v&space;cos(\theta)\\&space;\dot{y}&space;=&space;v&space;sin(\theta)\\&space;\dot{\theta}&space;=&space;w&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;\dot{x}&space;=&space;v&space;cos(\theta)\\&space;\dot{y}&space;=&space;v&space;sin(\theta)\\&space;\dot{\theta}&space;=&space;w&space;\end{matrix}\right." title="\left\{\begin{matrix} \dot{x} = v cos(\theta)\\ \dot{y} = v sin(\theta)\\ \dot{\theta} = w \end{matrix}\right." /></a>

And we know that our input are **v** and **w**. We can compute now the Lie Bracket, because we already know the vectors of the vector field (just compute the A matrix from the above model and find its null space). 

<a href="https://www.codecogs.com/eqnedit.php?latex=[g_1,g_2]&space;=&space;\begin{pmatrix}&space;sin(\theta)\\&space;-cos(\theta)\\&space;0&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?[g_1,g_2]&space;=&space;\begin{pmatrix}&space;sin(\theta)\\&space;-cos(\theta)\\&space;0&space;\end{pmatrix}" title="[g_1,g_2] = \begin{pmatrix} sin(\theta)\\ -cos(\theta)\\ 0 \end{pmatrix}" /></a>

Now we can think about the movememnt of the robot split into the four steps. For every step we have a set of input that is fixed for time = epsilon and from that we can reconstruct the increments or decrements of **q**.

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;x(\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))\\&space;y(\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))\\&space;\theta(\epsilon)&space;=&space;\theta(0)&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;x(\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))\\&space;y(\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))\\&space;\theta(\epsilon)&space;=&space;\theta(0)&space;\end{matrix}\right." title="\left\{\begin{matrix} x(\epsilon) = x(0) + \epsilon cos(\theta(0))\\ y(\epsilon) = y(0) + \epsilon sin(\theta(0))\\ \theta(\epsilon) = \theta(0) \end{matrix}\right." /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;x(2\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))\\&space;y(2\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))\\&space;\theta(2\epsilon)&space;=&space;\theta(0)&space;&plus;&space;\epsilon&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;x(2\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))\\&space;y(2\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))\\&space;\theta(2\epsilon)&space;=&space;\theta(0)&space;&plus;&space;\epsilon&space;\end{matrix}\right." title="\left\{\begin{matrix} x(2\epsilon) = x(0) + \epsilon cos(\theta(0))\\ y(2\epsilon) = y(0) + \epsilon sin(\theta(0))\\ \theta(2\epsilon) = \theta(0) + \epsilon \end{matrix}\right." /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;x(3\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))&space;-&space;\epsilon&space;cos(\theta(0)&space;&plus;&space;\epsilon)\\&space;y(3\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))&space;-&space;\epsilon&space;sin(\theta(0)&space;&plus;&space;\epsilon)\\&space;\theta(3\epsilon)&space;=&space;\theta(0)&space;&plus;&space;\epsilon&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;x(3\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))&space;-&space;\epsilon&space;cos(\theta(0)&space;&plus;&space;\epsilon)\\&space;y(3\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))&space;-&space;\epsilon&space;sin(\theta(0)&space;&plus;&space;\epsilon)\\&space;\theta(3\epsilon)&space;=&space;\theta(0)&space;&plus;&space;\epsilon&space;\end{matrix}\right." title="\left\{\begin{matrix} x(3\epsilon) = x(0) + \epsilon cos(\theta(0)) - \epsilon cos(\theta(0) + \epsilon)\\ y(3\epsilon) = y(0) + \epsilon sin(\theta(0)) - \epsilon sin(\theta(0) + \epsilon)\\ \theta(3\epsilon) = \theta(0) + \epsilon \end{matrix}\right." /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;x(4\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))&space;-&space;\epsilon&space;cos(\theta(0)&space;&plus;&space;\epsilon)\\&space;y(4\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))&space;-&space;\epsilon&space;sin(\theta(0)&space;&plus;&space;\epsilon)\\&space;\theta(4\epsilon)&space;=&space;\theta(0)&space;&plus;&space;\epsilon&space;-&space;\epsilon&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;x(4\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon&space;cos(\theta(0))&space;-&space;\epsilon&space;cos(\theta(0)&space;&plus;&space;\epsilon)\\&space;y(4\epsilon)&space;=&space;y(0)&space;&plus;&space;\epsilon&space;sin(\theta(0))&space;-&space;\epsilon&space;sin(\theta(0)&space;&plus;&space;\epsilon)\\&space;\theta(4\epsilon)&space;=&space;\theta(0)&space;&plus;&space;\epsilon&space;-&space;\epsilon&space;\end{matrix}\right." title="\left\{\begin{matrix} x(4\epsilon) = x(0) + \epsilon cos(\theta(0)) - \epsilon cos(\theta(0) + \epsilon)\\ y(4\epsilon) = y(0) + \epsilon sin(\theta(0)) - \epsilon sin(\theta(0) + \epsilon)\\ \theta(4\epsilon) = \theta(0) + \epsilon - \epsilon \end{matrix}\right." /></a>

For readability we can use the formulas for cosine and sine addiction to decompose the terms in the equation of x and y. Then for epsilon very small, its sine is exactly epsilon while its cosine is 1. Doing this substitution we find.

<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{\begin{matrix}&space;x(4\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon^2&space;sin(\theta(0))&space;\\&space;y(4\epsilon)&space;=&space;y(0)&space;-&space;\epsilon^2&space;cos(\theta(0))&space;\\&space;\theta(4\epsilon)&space;=&space;\theta(0)&space;\end{matrix}\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{\begin{matrix}&space;x(4\epsilon)&space;=&space;x(0)&space;&plus;&space;\epsilon^2&space;sin(\theta(0))&space;\\&space;y(4\epsilon)&space;=&space;y(0)&space;-&space;\epsilon^2&space;cos(\theta(0))&space;\\&space;\theta(4\epsilon)&space;=&space;\theta(0)&space;\end{matrix}\right." title="\left\{\begin{matrix} x(4\epsilon) = x(0) + \epsilon^2 sin(\theta(0)) \\ y(4\epsilon) = y(0) - \epsilon^2 cos(\theta(0)) \\ \theta(4\epsilon) = \theta(0) \end{matrix}\right." /></a>

So the total net displacement, which is obtained subtracting the configuration at time zero is:

<a href="https://www.codecogs.com/eqnedit.php?latex=\epsilon^2\begin{pmatrix}&space;sin(\theta(0))\\&space;-cos(\theta(0))\\&space;0&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\epsilon^2\begin{pmatrix}&space;sin(\theta(0))\\&space;-cos(\theta(0))\\&space;0&space;\end{pmatrix}" title="\epsilon^2\begin{pmatrix} sin(\theta(0))\\ -cos(\theta(0))\\ 0 \end{pmatrix}" /></a>

Which is an infinitesimal movement in the direction of the Lie Bracket. 

## Problem 11.6

If we have a differential drive, it means we have two set of (x,y) coordinates for the positions of the two wheels and their derivate wrt time can be written as

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}&space;\dot{x_i}&space;=&space;rw_icos(\theta)\\&space;\dot{y_i}&space;=&space;rw_isin(\theta)&space;\end{pmatrix}&space;i&space;=&space;R,L" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;\dot{x_i}&space;=&space;rw_icos(\theta)\\&space;\dot{y_i}&space;=&space;rw_isin(\theta)&space;\end{pmatrix}&space;i&space;=&space;R,L" title="\begin{pmatrix} \dot{x_i} = rw_icos(\theta)\\ \dot{y_i} = rw_isin(\theta) \end{pmatrix} i = R,L" /></a>

Now the speed of the center between the two wheels is just an average 

<a href="https://www.codecogs.com/eqnedit.php?latex=v_i&space;=&space;\sqrt(\dot{x_i}^2&space;&plus;&space;\dot{y_i}^2)&space;=&space;\sqrt(r^2w_i^2cos^2(\theta)&space;&plus;&space;r^2w_i^2sin^2(\theta))&space;=&space;rw_i" target="_blank"><img src="https://latex.codecogs.com/gif.latex?v_i&space;=&space;\sqrt(\dot{x_i}^2&space;&plus;&space;\dot{y_i}^2)&space;=&space;\sqrt(r^2w_i^2cos^2(\theta)&space;&plus;&space;r^2w_i^2sin^2(\theta))&space;=&space;rw_i" title="v_i = \sqrt(\dot{x_i}^2 + \dot{y_i}^2) = \sqrt(r^2w_i^2cos^2(\theta) + r^2w_i^2sin^2(\theta)) = rw_i" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=v_M&space;=&space;\frac{v_R&space;&plus;&space;v_L}{2}&space;=&space;\frac{r}{2}(w_R&space;&plus;&space;w_L))" target="_blank"><img src="https://latex.codecogs.com/gif.latex?v_M&space;=&space;\frac{v_R&space;&plus;&space;v_L}{2}&space;=&space;\frac{r}{2}(w_R&space;&plus;&space;w_L))" title="v_M = \frac{v_R + v_L}{2} = \frac{r}{2}(w_R + w_L))" /></a>

For the angular velocity we use the velocity composition rule which says that

<a href="https://www.codecogs.com/eqnedit.php?latex=\dot{p_R}&space;=&space;\dot{p_L}&space;&plus;&space;S(w)(p_r&space;-&space;p_L)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dot{p_R}&space;=&space;\dot{p_L}&space;&plus;&space;S(w)(p_r&space;-&space;p_L)" title="\dot{p_R} = \dot{p_L} + S(w)(p_r - p_L)" /></a>

where S(w) is a skew symmetric matrix. The difference between the positions of the two wheels can be easily computed in dependence of the distance between them and the orientation of the robot. The velocities are the ones above from which we computed the velocity of the 'unicycle'. 

Squaring and summing the terms of the equations we obtain a second grade equation in **w** with result 

<a href="https://www.codecogs.com/eqnedit.php?latex=w=&space;\frac{r}{d}(w_R&space;-&space;w_L)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w=&space;\frac{r}{d}(w_R&space;-&space;w_L)" title="w= \frac{r}{d}(w_R - w_L)" /></a>

## Problem 11.7

The first thing required is to compute the position of the center of rotation of the robot. To make it simpler let's consider a moving frame whose center is the midpoint of the rear wheels and whose axes are the onde indicating the orientation of the robot and the no-motion line for the rear wheels.

In this frame the **center of roation** is on one of the axis, so the other component is zero. The component > 0 can be computed using some geometry property building the triangle (with a 90° angle) with the no motion lines from the wheels and the rear wheel axis. Attention, this create a triangle whose sides are along the axis of the 'moving frame'. With the congruency theorem we can find the angles of the triangle and use the triangle rectus formulas to write that the side (midpoint of rear wheels to center of rotation) is l / tg(phi).

Now, we want to put all of this in the reference frame so we need to translate with respect to the midpoint of the rear wheels and to rotate back from the theta angle.

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}&space;x_c\\&space;y_c&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x\\&space;y&space;\end{pmatrix}&space;&plus;&space;R(\theta)&space;\begin{pmatrix}&space;0&space;\\&space;l&space;/&space;tg(\phi)\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;x_c\\&space;y_c&space;\end{pmatrix}&space;=&space;\begin{pmatrix}&space;x\\&space;y&space;\end{pmatrix}&space;&plus;&space;R(\theta)&space;\begin{pmatrix}&space;0&space;\\&space;l&space;/&space;tg(\phi)\end{pmatrix}" title="\begin{pmatrix} x_c\\ y_c \end{pmatrix} = \begin{pmatrix} x\\ y \end{pmatrix} + R(\theta) \begin{pmatrix} 0 \\ l / tg(\phi)\end{pmatrix}" /></a>

The angular velocity of any generic point P on the body can be computed as w = vp / Rp where vp is the velocity of that point and Rp is the radius of the trajectory, so to say.

The radius of the trajectory in our case is the distance between the center of rotation and the midpoint of the rear wheels that we'be just computed above. So we find that w = v * tg(phi) / l which is exactly what we have in the kinematic model of the bicycle. 

Then the velocity of the point v we can plug in the w just found in the relation w = vp / Rp. 

## Problem 11.8

