## Dynamic Systems, Stability  and Normalizing Flows
### _Introduction to ImitationFlows_

![Image](/Figures/RSHAPE.png)

Dynamic Systems represent the time evolution of a point in a  geometrical space. Dynamic Systems can model apple's motion falling from a tree, the heat diffusion in a room or a robot's motion playing table tennis.

An Important property of Dynamic Systems is the Stability. The Stability Theory studies how the motion in a dynamic system changes under some perturbation. Given a point running

In this article we will introduce how we can build stable stochastic nonlinear dynamics by the combination of Linear Dynamics and Normalizing Flows. For more information you can go to our paper  (add citation)


## Linear Stochastic Dynamics & Stability

Linear Dynamic Systems consider a linear function between the state and the time derivative of the state

\begin{equation}
\dot{x} = A x
\end{equation}

Linear Dynamics has been further studied. Thanks to their simplicity, there has been plenty of mathematical research on them.

### Stability
Stability analysis can be clearly study from Poincare Diagrams

![Image](/Figures/Stability_Diagram.png) (add reference to the figure)


### Stochasticity and density evolution

GIF on which we can observe how a gaussian distribution mean and variance is morphed moving through a stable linear vector field.

Graphical model to explain the message passing of the noise.


## Normalizing Flows & Nonlinear Stable Flows

Introduce a GIF showing the morphing through a Normalizing Flow(use FFJORD case, for some dynamics)

### Diffeormorphism

Explain what diffeomorphism is, add a graphical model explaining my dynamical systems evolution in latent space vs observation space

### The importance of the bijective mappings

Add a figure showing the bijective mapping versus the injective mapping and surjective mappings

![Image](/Figures/injective_bijective.png) (add reference to the figure)


Explain the problem of encoder-decoder structure.
