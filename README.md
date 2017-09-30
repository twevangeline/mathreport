#### **Group B: Classmate Chen, Classmate Cheng and Classmate Wu**

##### \(B1\) Consider the following problem in undergraduate classes.

##### Suppose$$x_1,x_2,\cdots,x_n$$ are i.i.d. with certain distribution F in which the \(population\) mean/expectation is denoted by µ and the \(population\) variance is denoted by $$\sigma^2 , 0<\sigma^2<\infty$$.

##### To test the null hypothesis:

$$H_0 : \mu \le 0 \quad v.s \quad H_a : \mu> 0 \quad \tag{5}$$

As usual, we use the following so-called ”t-statistic”:

##### $$\displaystyle\frac{\bar{x}\sqrt{n}}{\mathcal{s}} \tag{6}$$

##### where $$\;\; \bar{x} =\displaystyle\frac{1}{n} \sum_{t=1}^nX_t \;\;$$ , and $$\;\; s^2 =\displaystyle\frac{1}{n - 1}\sum_{t=1}^n(x_t- \bar{x})^2$$ ,

##### that is, the sample mean and the sample variance respectively.

##### Figure out the critical value of the so-called ”t-statistic” in \(6\) under the following cases:

**\(a\) F is normal and n is small.**

**\(b\) F is normal and n is large.**

t-statistic $$\;\; \dfrac{\sqrt{n}\bar{x}}{s} = \dfrac{\sqrt{n}(\bar{x}-\mu)}{s} = \dfrac{(\bar{x}-\mu)}{\sqrt{\dfrac{s^2}{n}}} = \dfrac{\dfrac{(\bar{x}-\mu)}{\sqrt{\dfrac{\sigma^2}{n}}}}{\sqrt{\dfrac{\dfrac{(n-1)s^2}{\sigma^2}}{n-1}}}$$

已知$$\;\;\; \dfrac{(\bar{x}-\mu)}{\sqrt{\dfrac{\sigma^2}{n}}} \sim N(0,1)$$          且$$\;\;\;\dfrac{(n-1)s^2}{\sigma^2} \sim \mathcal{X^2}(n-1)$$

$$\Rightarrow\;\;
\dfrac{\sqrt{n}\bar{x}}{s} \stackrel{d}{=} \dfrac{N(0,1)}{\sqrt{\dfrac{\mathcal{X^2}(n-1)}{n-1}}} \stackrel{d}{=} t(n-1)$$

當知道其分配後，不論是多少信心水準的 critical value 皆可求得。

當n很大的時候，透過 CLT 可知其會趨近常態分配。

**\(c\)F is **$$t_v$$**, 1/ν **$$\in$$** \[0.072, 0.161\] , and n is small.**

$$\mathcal{x_i}\sim^{i.i.d.}\mathcal{t_v}$$

$$\bar{x} = \dfrac{1}{n}\sum_{i=1}^n \mathcal{x_i}$$

$$\mathcal{s} = \sqrt{\mathcal{s^2}} = \sqrt{\dfrac{1}{n-1} \sum_{t=1}^n (\mathcal{x_t}-\bar{x})^2}$$

$$\dfrac{\sqrt{n}\bar{x}}{\mathcal{s}} = \dfrac{\dfrac{1}{\sqrt{n}}\sum_{i=1}^n \mathcal{x_i}}{\sqrt{\dfrac{1}{n-1}\sum_{t=1}^n (\mathcal{x_t}-\bar{x})^2}}$$

以下做個簡單的模擬來觀察

```r
> n=5  #一次抽5個
> df=6
> N=1000  # 抽1000遍
> x=vector(mode = "numeric", length = N  )  #length is 1000,initial 0
> #rt(n, df, ncp)
> #n number of observations
> #df  degrees of freedom (> 0, maybe non-integer). df = Inf is allowed.
> #The t distribution with df = n degrees of freedom has density
> #f(x) = Γ((n+1)/2) / (√(n π) Γ(n/2)) (1 + x^2/n)^-((n+1)/2)
> # sqrt(n)*mu/sd
> for(i in 1:N   ){
+   xt = rt(n,df)
+   x[i]=n^0.5*(mean(xt)/sd(xt))
+ }
> #print(x)
> hist(x)
```

                     ![](/assets/b1-1.png)

![](/assets/b1-2.png)可看出其未完全符合常態分配。

**\(d\) F is **$$t_v$$** , 1/ν **$$\in$$** \[0.072, 0.161\], and n is large.**

當母體標準差$$\sigma$$為未知時,以樣本標準差$$s$$代入,由中央極限定理得知

$$\dfrac{(\bar{x}-\mu)}{\dfrac{\sigma}{\sqrt{n}}} = \dfrac{\sqrt{n}(\bar{x}-\mu)}{\sigma} \; \xrightarrow[\text{CLT}]{\text{d}} N(0,1)$$

又由樣本標準差$$s$$為母體標準差$$\sigma$$之一致估計量,知$$\;\;s\;\stackrel{p}{\rightarrow}\;\sigma$$,可推出$$\;\dfrac{\sigma}{s}\;\stackrel{p}{\rightarrow} 1$$

By Slutsky's theorem

$$\dfrac{(\bar{x}-\mu)}{\dfrac{s}{\sqrt{n}}} = \dfrac{\sqrt{n}(\bar{x}-\mu)}{s} = \dfrac{\sigma}{s}\dfrac{\sqrt{n}(\bar{x}-\mu)}{\sigma} \; \stackrel{d}{\rightarrow} N(0,1)$$



