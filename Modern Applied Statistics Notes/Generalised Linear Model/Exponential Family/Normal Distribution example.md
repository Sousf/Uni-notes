Let $Y = N(\mu,\sigma^2)$

The pdf is:
$f(y) = \frac{1}{\sqrt{2\pi\sigma^2}}exp(-\frac{1}{2}\frac{(y-\mu)^2}{\sigma^2})$

We want to get this pdf into the form that the [[Exponential Family]] requires

Changing into an exponential form:
$f(y) = exp[log(2\pi\sigma^2)^{-1/2}-\frac{1}{2}\frac{y^2-2{\mu}y+\mu^2}{\sigma^2}]$

Collecting the ${\mu}y$ term and the $\mu^2$ term to the left side
$f(y) = exp[\frac{y{\mu}-\mu^2/2}{\sigma^2} - \frac{y^2}{2\sigma^2}-\frac{1}{2}log(2\pi\sigma^2)]$

Here we can see that the equation for the pdf $f(y)$ is in the [[Exponential Family]] form
$\theta = \mu$
$b(\theta)=\theta^2/2 \rightarrow \mu^2/2$
$a(\phi) = \sigma^2$
$c(y,\phi) = - \frac{y^2}{2\sigma^2}-\frac{1}{2}log(2\pi\sigma^2)$



















