# PINNS and iPINNS in Pytorch

Python 3.10.12

PyTorch Version: 2.1.0+cu121

NumPy Version: 1.25.2

Matplotlib Version: 3.7.1


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


