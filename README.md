 # Extended Kalman Filter

## Scope and Objectives
Since the normal Kalman filter can only deal with linear dynamics problems, extended Kalman filter(EKF) is the nonlinear version of the Kalman filter which linearizes about an estimate of the current mean and covariance. 

In this note, I intend to provide a brief introduction to EKF, specifying EKF problems, and explaining its relevance to control theories. After reading this note, readers will understand the basic concepts and motivations with EKF.  

## Introduction
The extended Kalman filter(EKF) is a very useful tool in control theory and estimation. It is widely used for nonlinear control systems. As an extension of traditional Kalman filter, EKF addresses the challenges of nonlinearity, making it be more extensively used in control theory. 

In real world systems, such as autonomous vehicles and aircrafts, exhibit nonlinear behaviors. The EKF provides a systematic approach to estimate the states of those nonlinear systems with noisy environment. Also, in robotics, for localization and mapping(SLAM), where a robot must estimate its position and orientation within an environment. 

The papers related to mathematical foundations of Kalman filter were firstly established between 1959 and 1961. Kalman filter is an optimal way to deal with linear system with noise. However, most of the engineering problems are nonlinear. So attempts are made to solve those nonlinear problems. The EKF used calculus multivariating Taylor Series to linearize a model of a working point. If a system is not well known, praticle filters(PF) are used for estimation. 

## Preliminaries
In EKF, the state transition and observation models do not need to be linear, but just differentiable. 

$$ \mathbf{x_k} = f (\mathbf{x_{k-1}}, \mathbf{u_{k-1}}) + \mathbf{w_k} $$

$$ \mathbf{z_k} = h (\mathbf{x_k}) + \mathbf{v_k} $$

where $\mathbf{w_k}$ and $\mathbf{v_k}$ are the process and observation noises, $\mathbf{x_k}$ is the state, $\mathbf{u_{k-1}}$ is the control input vector of the previous state. $\mathbf{z_k}$ is the measurement vector at time step k, f is a nonlinear function describing state transition, and h is a nonlinear function relating the state to the measurements. 

$$ \mathbf{P}^T = \tilde{\mathbf{R}} \mid Q$$

$$ \mathbf{delP/delx} $$

$$ \frac{\partial P}{\partial X} $$

<p align="center">
  <img width="400" height="400" >
</p>

[Barrier functions] ,
