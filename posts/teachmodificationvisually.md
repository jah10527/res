### Teach pose modification visually

#### Eye in hand

In the teach procedure, I set a capturing pose for DG1, annotated $P$, then we can get the pose of DG1, annotated $D_{c}$, in camera coordinates. Then it is easy to get the pose of DG1 in base coordinates $D_b$.
$$
D_{b}=PHD_{c}
$$
where the $H$ is the eye in hand calibration results.

After moved CT, the new pose of DG1 in base is $D_{b}^{new}$
$$
D_{b}^{new}=P^{new}HD_{c}^{new}
$$
The modifier $\Delta$ can be got according to:
$$
\Delta=D_{b}^{new}D_{b}^{-1}
$$
When putting the grasped DG1 to CT, we record the TCP as grasped pose, annotated $T$, which we modify so that the robot can reach to the very point regardless the CT and the camera moved or not, and the new tcp pose $T^{new}$ is 
$$
T^{new}= \Delta T
$$



#### Eye to hand

Just remove the $P$ and $P^{new}$ above.
$$
D_{b}=HD_{c} \\
D_{b}^{new}=HD_{c}^{new}
$$
where the $H$ is the eye to hand calibration results, and the rest are the same.

Feb. 2024
