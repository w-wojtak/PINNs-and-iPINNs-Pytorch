# PINNS and iPINNS in Pytorch

This repository hosts my PyTorch implementations of PINN (Physics-Informed Neural Network) and iPINN (inverse Physics-Informed Neural Network) from the tutorial https://towardsdatascience.com/inverse-physics-informed-neural-net-3b636efeb37e

The original implementations were crafted using TensorFlow and can be accessed at https://github.com/jmorrow1000/PINN-iPINN


Python 3.10.12  
PyTorch Version: 2.1.0+cu121  
NumPy Version: 1.25.2  
Matplotlib Version: 3.7.1  


The current implementation concentrates on a PINN and iPINN for the second-order differential equation governing an RLC circuit:

$$
L \frac{d^2 i}{dt^2} + R \frac{di}{dt} + \frac{1}{C} i = 0.
$$

Here, $R$, $L$, and $C$ denote the circuit's resistance, inductance, and capacitance, respectively. The variable $i$ represents the current in the circuit, while $t$ signifies time.


### PINN results

Below are the results from training a PINN on three test cases: under-damped, critically-damped, and over-damped. For definitions of each scenario, please refer to the original tutorial. Each plot presents a comparison between the analytical solution and the response output from the trained PINN.

<p align="center">
  <img src="https://github.com/w-wojtak/PINNs-and-iPINNs-Pytorch/assets/19287772/6002ff45-ed3c-48c2-a740-062db158f1ac" alt="image1" width="376" height="303" style="margin-right: 10px;"/>
  <img src="https://github.com/w-wojtak/PINNs-and-iPINNs-Pytorch/assets/19287772/bf8f3145-a059-458f-9cfe-4bc7966718d9" alt="image2" width="376" height="303" style="margin-right: 10px;"/>
  <img src="https://github.com/w-wojtak/PINNs-and-iPINNs-Pytorch/assets/19287772/9677a15a-69a3-4a2c-9911-70638f0066a8" alt="image3" width="376" height="303"/>
</p>


### iPINN results

Below are the results of applying an iPINN to determine three unknown parameters—R, L, and C—in three different scenarios: under-damped, critically-damped, and over-damped. The tables juxtapose the parameters used to generate the test responses with those inferred by the iPINN. The plots provide a comparison of the analytical solutions and the predictions made by the trained iPINN.


#### Under-damped scenario:

| Circuit Parameter | Generating Value | iPINN Value |
|-------------------|------------------|-------------|
| R (ohms)          | 1.20             | 1.201        |
| L (henries)       | 1.50             | 1.499        |
| C (farads)        | 0.30             | 0.300        |

<img src="https://github.com/w-wojtak/PINNs-and-iPINNs-Pytorch/assets/19287772/157d8187-af26-4319-b010-0e02c28c7fc9" width="376" height="303" alt="image">


#### Critically-damped scenario:

| Circuit Parameter | Generating Value | iPINN Value |
|-------------------|------------------|-------------|
| R (ohms)          | 4.47             | 4.472        |
| L (henries)       | 1.50             | 1.503        |
| C (farads)        | 0.30             | 0.299        |

<img src="https://github.com/w-wojtak/PINNs-and-iPINNs-Pytorch/assets/19287772/25f651e7-ef24-42d0-8c13-0428cb2a5393" width="376" height="303" alt="image">


#### Over-damped scenario:

| Circuit Parameter | Generating Value | iPINN Value |
|-------------------|------------------|-------------|
| R (ohms)          | 6.00             | 6.005        |
| L (henries)       | 1.50             | 1.500        |
| C (farads)        | 0.30             | 0.299        |

<img src="https://github.com/w-wojtak/PINNs-and-iPINNs-Pytorch/assets/19287772/85ccbef5-7206-4ac7-a2c2-a16bb6402e74" width="376" height="303" alt="image">




@software{wojtak_pinn_ipinn_2024,  
title = {PINN and iPINN for RLC Circuit Equation in Pytorch},  
author = {Weronika Wojtak},  
month = feb,  
year = 2024,  
version = {1.0},  
publisher = {GitHub},  
repository = {https://github.com/w-wojtak/PINNs-and-iPINNs-Pytorch},  
}  
