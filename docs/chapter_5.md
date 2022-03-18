# Chapter 5

The **gamma function** is defined for all complex numbers except the non-positive integers. For any positive integer $n$, $\Gamma(n) = (n-1)!\quad$.

Derived by Daniel Bernoulli, for complex numbers with a positive real part, the gamma function is defined via a convergent improper integral:

$$\Gamma(z) = \int_0^\infty x^{z-1} e^{-x}\,dx, \ \qquad \Re(z) > 0\ .$$

The notation $\Gamma (z)$ is due to Legendre. If the real part of the complex number $z$ is strictly positive ($\Re (z)>0$), then the integral converges absolutely, and is known as the Euler integral of the second kind. Using integration by parts, one sees that:

$$
\begin{aligned}
   \Gamma(z+1) & = \int_0^\infty x^{z} e^{-x} \, dx \\
&= \Bigl[-x^z e^{-x}\Bigr]_0^\infty + \int_0^\infty z x^{z-1} e^{-x}\, dx \\
&= \lim_{x\to \infty}\left(-x^z e^{-x}\right) - \left(-0^z e^{-0}\right) + z\int_0^\infty x^{z-1} e^{-x}\, dx.
\end{aligned}
$$