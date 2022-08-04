
## Overview
- Gradient Descent is a optimisation techinique use to minimise a certain error/loss function of a model so that a model perform to its best with as low of errors as possible


## Explanation using a Supervised Learning Example
- In supervised learning, we are given a training set of different instances
$D = {d_1,d_2,...}$, where each training instance $d$ comprises a vector of inputs (**features**) 
along with the desired output $t$ (**the class label**)
- $d = ⟨f_1,...,f_n,t⟩$ where $f$ is a feature of the instance $d$
- Now we might have an evaluation function $Eval(s)$ that evaluates the performance of the model, where $s$ is a given output of a model. We want $Eval(s)$ to be as close to $Eval(t)$ ( the true ouput ) as possible.
- If we have an evaluation function $Eval(s) = w_1f_1(s) + w_2f_2(s) + ... + w_nf_n(s)$, we would want to choose weights $w_i$ such that $Eval(s)$ is close to $Eval(t)$. This implies we must minimise **error** and thus this becomes an optimisation problem for our current model.
- We must first define the **error** or **error function** mentioned. A typical example of an **error function** is **$E = \frac{1}{2}\Sigma(t-s)^{2}$**  where $t$ is true ouput and $s$ is current output
- So now let's assume that our models only have 2 features and 2 weights associated with it, it has  $Eval(s) = w_1f_1(s) + w_2f_2(s)$, we can visualise our optimisation as follow:
	- ![[Pasted image 20220402184800.png]]
- As we can see, Error ($E$) is minimised when we are at the bottom of this cone, it is at the global minimum. 
- So we find the **global minimum** to find the points of the weights where the Error function is smallest. To find **global minimum, we just need the derivative of the graph to be equal to 0**
- Assuming that we start at some weight $w$, we can find the new weight by having this update rule $w = w - \frac{dE}{dw}$, this function is basically moving our current weight towards the **global minimum** where the Error Function ($E$) is minimised. a general rule for all weights is
	- $w_i = w_i - \frac{dE}{dw_i}$
- Now we have $\frac{dE}{dw} = \frac{dE}{ds}\frac{ds}{dw}$ (**Chain rule**) $= \frac{dE}{ds}(\frac{1}{2}\Sigma(t-s)^{2})\frac{ds}{dw} = (s - t)\frac{ds}{dw}$
- we had $Eval(s)$ as the function of $s$ and $w$, hence $\frac{ds}{dw}(Eval(s)) = f_i(s)$. This is because if we take derivative with respect to any $w_i$, of $Eval(s) = w_1f_1(s) + w_2f_2(s) + ... + w_nf_n(s)$, all other terms without that $w_i$ would disappear, $w_i$ would become 1 and leaving only its coefficient which is $f_i$
- So now we have  $\frac{dE}{dw} = (s - t)f_i(s)$ which means our weight update function becomes
	- $w_i = w_i - (s - t)f_i(s)$
	- A $\eta$ term called the **learning rate** is usually introduced into the function to control the size of each jump when we approach the **global minimum**. The complete function is now
		- **$w_i = w_i - \eta(s - t)f_i(s)$** 
		- We repeatedly update the weights based on each example until the weights converge


	### Explanation with game playing agents and other reinforcement learning model
	- This algorithm extends to game playing with Reinforcement Learning models. Given a state   ($s$), we can have a function $Eval(s)$ to evaluate the score/utility of being in that state. We want to find weights $w_i$ such that $Eval(s)$ can minimises Error ($E$) to be as close to the optimal **Evaluation score** as possible. We basically just keep updating the weights using **$w_i = w_i - \eta(z - t)f_i(s)$**  until $w_i$ converges, where $s = state$, $z = Eval(s;w)$, $t = Utility(s)$ (will need to be able to calculate the desireable value $t$)
	