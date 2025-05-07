# Distribusi Probabilitas Diskrit dan Kontinu

## Distribusi Diskrit

### 1. Bernoulli
**Notasi**: $X \sim \text{Bern}(p)$  
**PMF**: $P(X = x) = p^x (1 - p)^{1 - x}, \quad x \in \{0,1\}$  
**CDF**:  
- $P(X \leq 0) = 1 - p$  
- $P(X \leq 1) = 1$  
**Mean**: $\mathbb{E}[X] = p$  
**Variance**: $\text{Var}(X) = p(1 - p)$  
**Interval**: $[0, 1]$  
**Batas Nilai $x$**: $x = 0$ atau $1$  
**Eksponensial**: Tidak ada  

---

### 2. Binomial
**Notasi**: $X \sim \text{Bin}(n, p)$  
**PMF**: $P(X = x) = \binom{n}{x} p^x (1 - p)^{n - x}$  
**CDF**: $\sum_{k=0}^{\lfloor x \rfloor} \binom{n}{k} p^k (1 - p)^{n - k}$  
**Mean**: $\mathbb{E}[X] = np$  
**Variance**: $\text{Var}(X) = np(1 - p)$  
**Interval**: $[0, n]$  
**Batas Nilai $x$**: $x \in \{0,1,\dots,n\}$  
**Eksponensial**: Tidak ada  

---

### 3. Geometric
**Notasi**: $X \sim \text{Geom}(p)$  
**PMF**: $P(X = x) = (1 - p)^{x - 1} p, \quad x \geq 1$  
**CDF**: $P(X \leq x) = 1 - (1 - p)^{\lfloor x \rfloor}$  
**Mean**: $\mathbb{E}[X] = \frac{1}{p}$  
**Variance**: $\text{Var}(X) = \frac{1 - p}{p^2}$  
**Interval**: $[1, \infty)$  
**Batas Nilai $x$**: $x \in \mathbb{N}, x \geq 1$  
**Eksponensial**: Tidak ada  

---

### 4. Negative Binomial
**Notasi**: $X \sim \text{NB}(r, p)$  
**PMF**: $P(X = x) = \binom{x - 1}{r - 1} p^r (1 - p)^{x - r}$  
**CDF**: $\sum_{k=r}^{\lfloor x \rfloor} \binom{k - 1}{r - 1} p^r (1 - p)^{k - r}$  
**Mean**: $\mathbb{E}[X] = \frac{r}{p}$  
**Variance**: $\text{Var}(X) = \frac{r(1 - p)}{p^2}$  
**Interval**: $[r, \infty)$  
**Batas Nilai $x$**: $x \in \mathbb{N}, x \geq r$  
**Eksponensial**: Tidak ada  

---

### 5. Poisson
**Notasi**: $X \sim \text{Poisson}(\lambda)$  
**PMF**: $P(X = x) = \frac{\lambda^x e^{-\lambda}}{x!}$  
**CDF**: $e^{-\lambda} \sum_{k=0}^{\lfloor x \rfloor} \frac{\lambda^k}{k!}$  
**Mean**: $\mathbb{E}[X] = \lambda$  
**Variance**: $\text{Var}(X) = \lambda$  
**Interval**: $[0, \infty)$  
**Batas Nilai $x$**: $x \in \mathbb{N}$  
**Eksponensial**: Ya ($e^{-\lambda}$)  

---

### 6. Hypergeometric
**Notasi**: $X \sim \text{H}(N, K, n)$  
**PMF**: $P(X = x) = \frac{\binom{K}{x} \binom{N - K}{n - x}}{\binom{N}{n}}$  
**CDF**: $\sum_{k=0}^{\lfloor x \rfloor} \frac{\binom{K}{k} \binom{N - K}{n - k}}{\binom{N}{n}}$  
**Mean**: $\mathbb{E}[X] = n \left( \frac{K}{N} \right)$  
**Variance**: $\text{Var}(X) = n \left( \frac{K}{N} \right) \left( 1 - \frac{K}{N} \right) \left( \frac{N - n}{N - 1} \right)$  
**Interval**: $[\max(0, n - (N - K)), \min(n, K)]$  
**Batas Nilai $x$**: $x$ integer dalam interval  
**Eksponensial**: Tidak ada  

---

### 7. Discrete Uniform
**Notasi**: $X \sim \text{DU}(a, b)$  
**PMF**: $P(X = x) = \frac{1}{b - a + 1}$  
**CDF**: $P(X \leq x) = \frac{\lfloor x \rfloor - a + 1}{b - a + 1}$  
**Mean**: $\mathbb{E}[X] = \frac{a + b}{2}$  
**Variance**: $\text{Var}(X) = \frac{(b - a + 1)^2 - 1}{12}$  
**Interval**: $[a, b]$  
**Batas Nilai $x$**: $x \in \mathbb{Z}, a \leq x \leq b$  
**Eksponensial**: Tidak ada  

---

## Distribusi Kontinu

### 1. Uniform
**Notasi**: $X \sim \text{U}(a, b)$  
**PDF**: $f(x) = \begin{cases} 
\frac{1}{b - a} & \text{untuk } a \leq x \leq b \\
0 & \text{lainnya}
\end{cases}$  
**CDF**: $F(x) = \begin{cases} 
0 & x < a \\
\frac{x - a}{b - a} & a \leq x \leq b \\
1 & x > b
\end{cases}$  
**Mean**: $\mathbb{E}[X] = \frac{a + b}{2}$  
**Variance**: $\text{Var}(X) = \frac{(b - a)^2}{12}$  
**Interval**: $[a, b]$  
**Batas Nilai $x$**: $a \leq x \leq b$  
**Eksponensial**: Tidak ada  

---

### 2. Normal
**Notasi**: $X \sim \mathcal{N}(\mu, \sigma^2)$  
**PDF**: $f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left( -\frac{(x - \mu)^2}{2\sigma^2} \right)$  
**CDF**: $\Phi(x) = \frac{1}{2} \left[ 1 + \text{erf} \left( \frac{x - \mu}{\sigma \sqrt{2}} \right) \right]$  
**Mean**: $\mathbb{E}[X] = \mu$  
**Variance**: $\text{Var}(X) = \sigma^2$  
**Interval**: $(-\infty, \infty)$  
**Batas Nilai $x$**: $x \in \mathbb{R}$  
**Eksponensial**: Ya  

---

### 3. Exponential
**Notasi**: $X \sim \text{Exp}(\lambda)$  
**PDF**: $f(x) = \lambda e^{-\lambda x}, \quad x \geq 0$  
**CDF**: $F(x) = 1 - e^{-\lambda x}, \quad x \geq 0$  
**Mean**: $\mathbb{E}[X] = \frac{1}{\lambda}$  
**Variance**: $\text{Var}(X) = \frac{1}{\lambda^2}$  
**Interval**: $[0, \infty)$  
**Batas Nilai $x$**: $x \geq 0$  
**Eksponensial**: Ya  

---

### 4. Gamma
**Notasi**: $X \sim \text{Gamma}(\alpha, \beta)$  
**PDF**: $f(x) = \frac{x^{\alpha - 1} e^{-x/\beta}}{\beta^\alpha \Gamma(\alpha)}, \quad x > 0$  
**CDF**: Tidak ada bentuk tertutup  
**Mean**: $\mathbb{E}[X] = \alpha \beta$  
**Variance**: $\text{Var}(X) = \alpha \beta^2$  
**Interval**: $[0, \infty)$  
**Batas Nilai $x$**: $x > 0$  
**Eksponensial**: Ya  

---

### 5. Chi-Square
**Notasi**: $X \sim \chi^2(k)$  
**PDF**: $f(x) = \frac{x^{k/2 - 1} e^{-x/2}}{2^{k/2} \Gamma(k/2)}, \quad x > 0$  
**CDF**: Tidak ada bentuk tertutup  
**Mean**: $\mathbb{E}[X] = k$  
**Variance**: $\text{Var}(X) = 2k$  
**Interval**: $[0, \infty)$  
**Batas Nilai $x$**: $x \geq 0$  
**Eksponensial**: Ya  

---

### 6. Beta
**Notasi**: $X \sim \text{Beta}(\alpha, \beta)$  
**PDF**: $f(x) = \frac{x^{\alpha - 1} (1 - x)^{\beta - 1}}{B(\alpha, \beta)}, \quad 0 \leq x \leq 1$  
**CDF**: Tidak ada bentuk tertutup  
**Mean**: $\mathbb{E}[X] = \frac{\alpha}{\alpha + \beta}$  
**Variance**: $\text{Var}(X) = \frac{\alpha \beta}{(\alpha + \beta)^2 (\alpha + \beta + 1)}$  
**Interval**: $[0, 1]$  
**Batas Nilai $x$**: $0 \leq x \leq 1$  
**Eksponensial**: Tidak ada  

---

### 7. Log-Normal
**Notasi**: $X \sim \text{LogN}(\mu, \sigma^2)$  
**PDF**: $f(x) = \frac{1}{x \sigma \sqrt{2\pi}} \exp\left( -\frac{(\ln x - \mu)^2}{2\sigma^2} \right), \quad x > 0$  
**CDF**: $\Phi\left( \frac{\ln x - \mu}{\sigma} \right)$  
**Mean**: $\mathbb{E}[X] = e^{\mu + \sigma^2/2}$  
**Variance**: $\text{Var}(X) = (e^{\sigma^2} - 1) e^{2\mu + \sigma^2}$  
**Interval**: $(0, \infty)$  
**Batas Nilai $x$**: $x > 0$  
**Eksponensial**: Ya  

---

### 8. Weibull
**Notasi**: $X \sim \text{Weibull}(\lambda, k)$  
**PDF**: $f(x) = \frac{k}{\lambda} \left( \frac{x}{\lambda} \right)^{k - 1} e^{-(x/\lambda)^k}, \quad x \geq 0$  
**CDF**: $F(x) = 1 - e^{-(x/\lambda)^k}, \quad x \geq 0$  
**Mean**: $\mathbb{E}[X] = \lambda \Gamma\left(1 + \frac{1}{k}\right)$  
**Variance**: $\text{Var}(X) = \lambda^2 \left[ \Gamma\left(1 + \frac{2}{k}\right) - \left( \Gamma\left(1 + \frac{1}{k}\right) \right)^2 \right]$  
**Interval**: $[0, \infty)$  
**Batas Nilai $x$**: $x \geq 0$  
**Eksponensial**: Ya  

---

### 9. Pareto
**Notasi**: $X \sim \text{Pareto}(x_m, \alpha)$  
**PDF**: $f(x) = \frac{\alpha x_m^\alpha}{x^{\alpha + 1}}, \quad x \geq x_m$  
**CDF**: $F(x) = 1 - \left( \frac{x_m}{x} \right)^\alpha, \quad x \geq x_m$  
**Mean**: $\mathbb{E}[X] = \frac{\alpha x_m}{\alpha - 1}, \quad \alpha > 1$  
**Variance**: $\text{Var}(X) = \frac{x_m^2 \alpha}{(\alpha - 1)^2 (\alpha - 2)}, \quad \alpha > 2$  
**Interval**: $[x_m, \infty)$  
**Batas Nilai $x$**: $x \geq x_m$  
**Eksponensial**: Ya  

---

### 10. Cauchy
**Notasi**: $X \sim \text{Cauchy}(x_0, \gamma)$  
**PDF**: $f(x) = \frac{1}{\pi \gamma} \left[ \frac{\gamma^2}{(x - x_0)^2 + \gamma^2} \right]$  
**CDF**: $F(x) = \frac{1}{\pi} \arctan\left( \frac{x - x_0}{\gamma} \right) + \frac{1}{2}$  
**Mean**: Tidak terdefinisi  
**Variance**: Tidak terdefinisi  
**Interval**: $(-\infty, \infty)$  
**Batas Nilai $x$**: $x \in \mathbb{R}$  
**Eksponensial**: Tidak ada  
