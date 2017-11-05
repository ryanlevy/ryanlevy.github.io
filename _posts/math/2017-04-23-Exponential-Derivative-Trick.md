---
layout: single
title:  "Exponential Derivative Trick"
toc: true
categories: 
  - math
tags: 
  - derivative
  - numpy
excerpt: A cool numerical derivative for the matrix exponential
---
The matrix exponential can appear in a variety of computational problems. Unfortunately the standard finite difference routine to obtain its derivative is often inaccurate. Using complex numbers we can do better!
## Complex Step
<small>From Ref. [\[1\]](#references)</small>  
For normal finite difference schemes we can approximate a derivative with

$$ F^\prime(x) = \frac{F(x+h)-F(x)}{h}+O(h^2)$$ 

with \\( h\ll 1 \\) . When \\( F(x+h)\approx F(x)\\) we run into subtraction errors. 
A useful trick to mitigate this, when dealing with analytic functions, is to use the ***complex step*** which is

$$ \boxed{ F^\prime (x) = \frac{\text{Im}\left[F(x+ih)\right]}{h}} +O(h^2)$$  

### Short proof:
----
Expand \\(F(x+ih)\\) about \\(x\\) using a taylor expansion

$$F(x+ih) = F(x)+ihF^\prime(x) +O(h^2) $$  

Asking what the imaginary part is to first order yields the derivative. Note that \\(\text{Re}\left[F(x+ih)\right]=F(x)\\), so we can obtain the function at a point and its derivative in one calculation. 

---
## Exponential Complex Step
<small>From Ref. [\[2\]](#references)</small>  
The same trick can be applied for matrices, particularly the exponential matrix function \\(\exp(A)\\). 
Consider the Fréchet derivative (really a directional derivative) of a function \\(f(A)=\exp(A)\\). The derivative of \\(f\\) can be approxmated as

$$\frac{df}{dA_{ij}}=\frac{\text{Im}\left[ \exp(A+ihE_{ij}) \right]}{h} $$

where \\( (E\_{ij})\_{kl}=\delta\_{ik}\delta\_{jl} \\) is the single-entry matrix. 
Note: Other matrices can be used for \\(E\\). 

## Python Example
Here is an example for getting the derivative at the identity. The derivative is analytic here, and is simply \\(\delta\_{ij}\\)

```python
import scipy.linalg as spsl
```

```python
A = np.zeros([4,4],dtype=np.complex)
#derivative at i,j 
i = 1
j = 2
h = 1e-6

Ah = A.copy()
Ah[i,j]+=1j*h
mA = spsl.expm(Ah)
print("exp(A)=\n",np.real(mA),"\n d/dA_ij exp(A)=\n",np.imag(mA)/h)
#normal finite difference
Ah =A.copy()
Ah[i,j]+=h
finiteDiff = np.real(spsl.expm(Ah)-spsl.expm(A))/h
print("Finite differences:\n",finiteDiff)
```
Output:  

    exp(A)=
     [[ 1.  0.  0.  0.]
     [ 0.  1.  0.  0.]
     [ 0.  0.  1.  0.]
     [ 0.  0.  0.  1.]] 
     d/dA_ij exp(A)=
     [[ 0.  0.  0.  0.]
     [ 0.  0.  1.  0.]
     [ 0.  0.  0.  0.]
     [ 0.  0.  0.  0.]]
    Finite differences:
     [[ 0.  0.  0.  0.]
     [ 0.  0.  1.  0.]
     [ 0.  0.  0.  0.]
     [ 0.  0.  0.  0.]]

While the finite difference scheme here worked, it required two matrix exponential calculations rather than one; in terms of operations the complex step method is better for larger matrices. See Ref [2] for cases in which the complex step has a lower relative error than finite difference schemes. 
 
# References 

[1] Squire, William, and Trapp, George, Using complex variables to estimate derivatives of real functions, *SIAM Review 40*, 1998, pp. 110-112. [DOI:10.1137/S003614459631241X](http://dx.doi.org/10.1137/S003614459631241X)  

[2] Al-Mohy, Awad H., and Higham, Nicholas J., The complex step approximation to the Fréchet
derivative of a matrix function, *Numer Algor* (2010) 53:133–148 [DOI:10.1007/s11075-009-9323-y](http://dx.doi.org/10.1007/s11075-009-9323-y)
