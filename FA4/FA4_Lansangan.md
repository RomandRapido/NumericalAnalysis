Okay, here is the approximation of $\int_0^1 x^2 e^x dx$ using Gaussian quadrature with $n=2$.

### Transpose Interval

Since the Guassian quarature rules are defined on the interval $[-1,1]$, we ought to transpose the interval of integration. 

$$x(t) = \frac{(b-a)t + (b+a)}{2} = \frac{(1-0)t + (1+0)}{2} = \frac{t+1}{2}$$
    
Then, $dx = \frac{b-a}{2} dt = \frac{1}{2} dt$.

Consquentyly, $f(x) = x^2 e^x$ becomes $f\left(\frac{t+1}{2}\right) = \left(\frac{t+1}{2}\right)^2 e^{\frac{t+1}{2}}$.

$$\int_0^1 x^2 e^x dx = \int_{-1}^1 f\left(\frac{t+1}{2}\right) \frac{1}{2} dt = \int_{-1}^1 \frac{1}{2} \left(\frac{t+1}{2}\right)^2 e^{\frac{t+1}{2}} dt$$

Let $g(t) = \frac{1}{2} \left(\frac{t+1}{2}\right)^2 e^{\frac{t+1}{2}}$.

Let us now find the nodes and the wieghts for $n=2$.

From the slide (Page 36), the nodes ($t_i$) and weights ($c_i$) needed for Guassian Quarature are:

$t_1 = -0.5773502692$, $c_1 = 1.0$

$t_2 = 0.5773502692$, $c_2 = 1.0$

Recall that the formula for Guassian Quarature rule is:

$$\int_{-1}^1 g(t) dt \approx \sum_{i=1}^n c_i g(t_i)$$

For $n=2$:
$$\int_{-1}^1 g(t) dt \approx c_1 g(t_1) + c_2 g(t_2)$$