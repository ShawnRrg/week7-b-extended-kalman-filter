# Extended Kalman Filter

## Scope and Objectives
Since the normal Kalman filter can only deal with linear dynamics problems, extended Kalman filter(EKF) is the nonlinear version of the Kalman filter which linearizes about an estimate of the current mean and covariance. 

In this note, I intend to provide a brief introduction to EKF, specifying EKF problems, and explaining its relevance to control theories. After reading this note, readers will understand the basic concepts and motivations with EKF.  

## Introduction
The extended Kalman filter(EKF) is a very useful tool in control theory and estimation. It is widely used for nonlinear control systems. As an extension of traditional Kalman filter, EKF addresses the challenges of nonlinearity, making it be more extensively used in control theory. 
