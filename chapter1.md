##### \(B2\) Assuming that the firm’s objective is maximizing the present value of its profits and there is no final period.

##### Its optimization problem is:

##### $$max_{k(t),I(t)}\int_0^\infty e^{-rt} [p(t)f(k(t)) - c(I(t))]dt , s.t. \tag{7}$$

##### $$\dot{k(t)} = I(t) - \delta k(t),\tag{-}$$

##### $$k(0) = \bar{k},\tag{-}$$

##### where k\(.\) and I\(.\) stand for the capital path and the investment path respectively;

##### f\(.\) is the production function while c\(.\) is the investment cost function.

**\(a\) Find the F.O.C.**

$$\mathcal{L} = \int_0^\infty e^{-rt}[p(t)f(k(t))-c(I(t))]dt + \int_0^\infty \mu(t)\{[I(t)-\delta k(t)]-\dot{k}(t)\}dt + \lambda(\bar{k}-k(0)) $$

$$\\ = \int_0^\infty \{ e^{-rt}[p(t)f(k(t))-c(I(t))]dt + \mu(t)[I(t)-\delta k(t)]dt \} -\int_0^\infty \mu(t)\dot{k}(t) dt + \lambda(\bar{k}-k(0)) $$

$$\\ =  \int_0^\infty \{ e^{-rt}[p(t)f(k(t))-c(I(t))]dt + \mu (t)[I(t)-\delta k(t)]dt\} + \\ \quad \int_0^\infty \mu(t)k(t)dt + \mu(0)k(0) - \mu(\infty)k(\infty)+ \lambda(\bar{k} - k(0))$$

Hamiltonian Function

$$H(k(t),I(t),t,\mu(t)) \\ = e^{-rt}[p(t)f(k(t))-c(I(t))] + \mu(t)[I(t)-\delta k(t)]$$

F.O.C

$$\dfrac{\partial H}{\partial I(t)} = 0 \;\; \Rightarrow \;\; -[e^{-rt}c'(I(t))] + \mu(t) = 0 \;\;\;\;\;\tag{*}$$

$$\dfrac{\partial H}{\partial k(t)} + \dot{\mu} = 0 \;\; \Rightarrow \;\; e^{-rt}p(t)f'(k(t)) - \delta \mu(t) + \dot{\mu} = 0 \;\;\;\tag{**}$$

$$\bar{k} = k(0) \tag{-}$$

**\(b\) Discuss the condition\(s\) on f\(.\) and c\(.\). The condition\(s\) may or may not related to the necessary and/or sufficient conditions.**

$$f'(.)>0 \quad f''(.)<0 \tag{-}$$

當生產要素增加，產量也會增加，但生產要素增加會使邊際產量遞減。

**\(c\) Show that, if **$$c(I(t)) = qI(t)$$**,**

$$p(t)f'(k(t)) = (r + \delta)q. \tag{8}$$

**Interpret Equation \(8\).**

**\(d\) Show that, if c ” \(.\) &gt; 0, the optimal paths are characterized by the following pair 3 of differential equations:**

$$\dot{k(t)} = I(t) - \delta k(t), \tag{9}$$

$$\dot{I(t)} =\dfrac{ p(t)f'(k(t)) - (r + \delta)c'(I(t)) }{c '' (I(t)) }. \tag{10}$$

**Interpret Equations \(9\)-\(10\).**

By   $$(\ast)$$

$$\mu(t) = e^{-rt}c'(I(t)) \;\;\; (\ast\ast\ast)$$

By  $$(\ast\ast)$$

$$\dot{\mu(t)} = -e^{-rt}p(t)f'(k(t)) + \delta \mu(t)$$

Put  $$(\ast\ast\ast)$$ into the above equation

$$\dot{\mu(t)} = -e^{-rt}p(t)f'(k(t)) + \delta [e^{-rt}c'(I(t))]$$

However , if we differentiate \(w.r.t. t\) the equation   $$(\ast\ast\ast)$$  directly

$$\dot{\mu(t)} = e^{-rt}(-r)c'(I(t)) + e^{-rt}c''(I(t))\dot{I(t)}$$

Therefore , eliminating  $$\dot{\mu(t)}$$   and   $$e^{-rt}$$

$$-p(t)f'(k(t)) + \delta c'(I(t)) = (-r)c'(I(t)) + c''(I(t))\dot{I(t)} \quad\quad (****)$$

If  $$c(I(t)) = qI(t) \quad, \quad $$

then   $$c'(I(t)) = q \quad , \quad c''(I(t)) = 0$$

By $$(\ast\ast\ast\ast)$$

$$\Rightarrow\quad      -p(t)f'(k(t)) + \delta q = (-r)q $$

$$\Rightarrow\quad p(t)f'(k(t)) = (r + \delta)q$$

If   $$c''(I(t))>0 \quad , \quad$$

By $$(\ast\ast\ast\ast)$$

$$\Rightarrow \quad \dot{I(t)} =\dfrac{ p(t)f'(k(t)) - (r + \delta)c'(I(t)) }{c '' (I(t)) }$$

![](/assets/b2-1.png)

當投資的邊際報酬大於投資的邊際成本時，會繼續增加投資，而當投資的邊際成本大於投資的邊際報酬時，會減少投資，經過不斷調整，最後達到均衡的狀態。

**\(e\) Interpret your results in \(a\)-\(d\) with a Cobb-Douglas production function and a quadratic cost function.**

Suppose   $$f(k(t)) = Ak(t)^{\alpha}$$     and         $$c(I(t)) = aI(t)^2 + bI(t) + c$$

$$max_{k(t),I(t)}\int_0^\infty e^{-rt} [p(t)f(k(t)) - c(I(t))]dt = max_{k(t),I(t)}\int_0^\infty e^{-rt} [p(t)Ak(t)^{\alpha} - (aI(t)^2 + bI(t) + c)]dt,\tag{-}$$

$$\dot{k(t)} = I(t) - \delta k(t),\tag{-}$$

$$k(0) = \bar{k},\tag{-}$$

$$\mathcal{L} = \int_0^\infty e^{-rt}[p(t)Ak(t)^{\alpha}-(aI(t)^2 + bI(t) + c)]dt + \int_0^\infty \mu(t)\{[I(t)-\delta k(t)]-\dot{k}(t)\}dt + \lambda(\bar{k}-k(0)) $$

$$\quad = \int_0^\infty \{ e^{-rt}[p(t)Ak(t)^{\alpha}-(aI(t)^2 + bI(t) + c)]dt + \mu(t)[I(t)-\delta k(t)]dt \} -\int_0^\infty \mu(t)\dot{k}(t) dt + \lambda(\bar{k}-k(0)) $$

$$\quad =  \int_0^\infty \{ e^{-rt}[p(t)Ak(t)^{\alpha}-(aI(t)^2 + bI(t) + c)]dt + \mu (t)[I(t)-\delta k(t)]dt\} + \\ \quad \int_0^\infty \mu(t)k(t)dt + \mu(0)k(0) - \mu(\infty)k(\infty)+ \lambda(\bar{k} - k(0))$$

Hamiltonian Function

$$H(k(t),I(t),t,\mu(t)) \\ = e^{-rt}[p(t)Ak(t)^{\alpha}-(aI(t)^2 + bI(t) + c)] + \mu(t)[I(t)-\delta k(t)]$$

F.O.C

$$\dfrac{\partial H}{\partial I(t)} = 0 \;\; \Rightarrow \;\; -[e^{-rt}(2aI(t) + b)] + \mu(t) = 0 \;\;\;\;\;\tag{*}$$

$$\dfrac{\partial H}{\partial k(t)} + \dot{\mu} = 0 \;\; \Rightarrow \;\; e^{-rt}p(t)(A \alpha k(t)^{\alpha -1} ) - \delta \mu(t) + \dot{\mu} = 0 \;\;\;\tag{**}$$

$$\bar{k} = k(0) \tag{-}$$

By   $$(\ast)$$

$$\mu(t) = e^{-rt}(2aI(t) + b) \;\;\; (\ast\ast\ast)$$

By  $$(\ast\ast)$$

$$\dot{\mu(t)} = -e^{-rt}p(t)(A \alpha k(t)^{\alpha -1} ) + \delta \mu(t)$$

Put  $$(\ast\ast\ast)$$ into the above equation

$$\dot{\mu(t)} = -e^{-rt}p(t)(A \alpha k(t)^{\alpha -1} ) + \delta [e^{-rt}(2aI(t) + b)]$$

However , if we differentiate \(w.r.t. t\) the equation   $$(\ast\ast\ast)$$  directly

$$\dot{\mu(t)} = e^{-rt}(-r)(2aI(t) + b) + e^{-rt}2a\dot{I(t)}$$

Therefore , eliminating  $$\dot{\mu(t)}$$   and   $$e^{-rt}$$

$$p(t)f'(k(t)) - \delta (2aI(t) + b) = r(2aI(t) + b) + 2a\dot{I(t)} \quad\quad (****)$$

By\(\*\*\*\*\)

$$\Rightarrow \quad \dot{I(t)} =\dfrac{ p(t)(A \alpha k(t)^{\alpha -1} ) - (r + \delta)(2aI(t) + b) }{2a }$$



