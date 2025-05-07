| Distribusi          | Notasi               | PMF (Fungsi Massa)                          | Mean ($\mu$)       | Varians ($\sigma^2$)   | Parameter                     |
|---------------------|----------------------|---------------------------------------------|-------------------|------------------------|-------------------------------|
| **Bernoulli**       | $X \sim Ber(p)$      | $P(X=x) = p^x(1-p)^{1-x}$                  | $p$               | $p(1-p)$               | $p$ (prob. sukses)            |
| **Binomial**        | $X \sim Bin(n,p)$    | $P(X=k) = \binom{n}{k}p^k(1-p)^{n-k}$      | $np$              | $np(1-p)$              | $n$ (percobaan), $p$ (sukses) |
| **Negative Binomial** | $X \sim NB(r,p)$   | $P(X=k) = \binom{k-1}{r-1}p^r(1-p)^{k-r}$  | $\frac{r}{p}$     | $\frac{r(1-p)}{p^2}$   | $r$ (sukses target), $p$      |
| **Geometrik**       | $X \sim Geom(p)$     | $P(X=k) = (1-p)^{k-1}p$                    | $\frac{1}{p}$     | $\frac{1-p}{p^2}$      | $p$ (prob. sukses)            |
| **Poisson**         | $X \sim Pois(\lambda)$ | $P(X=k) = \frac{e^{-\lambda}\lambda^k}{k!}$ | $\lambda$         | $\lambda$              | $\lambda$ (rataan kejadian)   |
| **Hipergeometrik**  | $X \sim H(N,K,n)$    | $P(X=k) = \frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}$ | $n\frac{K}{N}$ | $n\frac{K}{N}\frac{N-K}{N}\frac{N-n}{N-1}$ | $N$ (populasi), $K$ (sukses), $n$ (sampel) |
| **Multinomial**     | $X \sim Mult(n,\mathbf{p})$ | $P(X_1=k_1,...,X_m=k_m) = \frac{n!}{k_1!\cdots k_m!}p_1^{k_1}\cdots p_m^{k_m}$ | $n\mathbf{p}$ | $n\text{diag}(\mathbf{p}) - n\mathbf{p}\mathbf{p}^T$ | $n$ (percobaan), $\mathbf{p}$ (vektor prob.) |
| **Uniform Diskrit** | $X \sim Unif\{a,...,b\}$ | $P(X=x) = \frac{1}{b-a+1}$              | $\frac{a+b}{2}$   | $\frac{(b-a+1)^2-1}{12}$ | $a$ (min), $b$ (max)          |
