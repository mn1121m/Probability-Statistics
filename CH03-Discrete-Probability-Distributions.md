# CH03. Discrete Probability Distributions

---


## Contents

- 3.1 The Binomial Distribution
- 3.2 The Geometric and Negative Binomial Distributions
- 3.3 The Hypergeometric Distribution
- 3.4 The Poisson Distribution
- 3.5 The Multinomial Distribution

---

## 3.1.2 Definition of the Binomial Distribution

- A binomial distribution(이항 분포) with parameter $n$ and $p$
    - The random variable is defined by the parameter $p$, 0 ≤ p ≤ 1 , which is the probability that the outcome is 1
    - The number of successes within a fixed number of trials $n$
    
    - n independent Bernoulli trials $X_{1}, … , X_{n}$
        - $X = X_{1} + . . . + X_{n}$
    
    - $X \sim B(n, p)$
        - $P( X = x) = {n \choose x} p^{x} (1 - p)^{n-x}$
        - ${n \choose x} ==  \frac{n!}{x!(n - x)!}$
        

---

- Consider an experiment consisting of $**n$**  Bernoulli trials with a constant probability $**p**$ of success

- **A random varialbe** $X$: the total number of successes
    - A binomial distribution with parameter $n$ and $p$
    - $X \sim B(n, p)$ → 성공 확률이 p인 실험을 n번 실행하였을 때, 성공 횟수의 분포 ⇒ 이항 분포
    
- The **probability mass function** of a $B( n, p )$
    - $P( X = x) = {n \choose x} p^{x} (1 - p)^{n-x}$, for $x = 0, 1, 2, …, n$
    - the expectation and the variance
        - $E(X) = np$ and $Var(X) = np(1-p)$
        
- The **cumulative distribution function** of a $B(n, p)$
    - $P( X ≤ x ) = \sum_{j = 0}^{i} P( X ≤ x_{j} )$

---

## 3.2.1 Definition of the Geometric Distribution → 첫 성공

- **The Geometric Distribution(기하 분포) with Parameter p**
    - A probability mass function
        - $P( X = x) = (1 - p)^{x-1}p$, for $x = 1, 2, 3, 4, …$
        - $(1 - p)^{x-1}$ → The probability value of x - 1 failures
        - $p$ → The probability value of $x{th}$ success
        - 베르누이 시행이 처음 성공할 때까지의 시행횟수를 확률변수 X라고 했을 때, 이 확률변수 X의 분포를 말한다.
        - 최초로 발생한 것 (처음 성공할 확률)
    - The cumulative distribution function
        - $P( X ≤ x) = \sum_{i = 1}^{x} P( X = i ) = 1 - ( 1 - p)^{x}$
        - ⇒ 의미: $x$ 번을 시도했을 때 다 실패하지 않은 값 ( ⇒ $x$번째까지 성공한 것을 다 더한 값)
        

---

## 3.2.2 Definition of the nagative binomial distribution

- **Definition of the nagative binomial distribution < 중요 > → x번 시도해서 r번 성공할 확률**
    - The number of trials up to and including the $r^{th}$ success
        - $P( X = x) = {x - 1 \choose r - 1} p^{r-1} (1 - p)^{(x-1)-(r-1)} \times p = {x - 1 \choose r - 1} (1 - p)^{x-r} p^{r}$, for $x = r, r + 1, r + 2, r + 3, …$
            - x - 1 번 시도해서 r - 1번 성공할 확률 X(곱하기) r번째 성공할 확률
        
        - The expectation of $X$ and the variance
            - $E(X) = \frac{r}{p}$
            - $Var(X) = \frac{r(1-p)}{p^{2}}$
            

---

## 3.3.1 Definition of the Hypergeometric Distribution

- **The hypergeometric distribution**
    - $P(X = x)$: (전제: N개 중에서 r개가 특정 조건을 만족) N개 중에서 n개 를 골랐는데, 그 중 x개가 r과 같은 조건에 포함된 경우에 대한 분포
    - The pmf $P( X = x) = \frac{{r \choose x} \times {N - r \choose n - x}}{{N \choose n}}$ ,  for $max( 0, n + r - N ) ≤ x ≤ min( n, r )$
    - Expectation and Variance: $E(X) = \frac{nr}{N}, Var(X) = \frac{N - n}{N - 1} \times n \times \frac{r}{N} \times ( 1 - \frac{r}{N})$
    
- **Ex. 2 Defective Computer Chips**
    - There are 500 computer chips in a box, in which 9 defective chips.
    Let’s randomly choose 3 chips without replacement.
        - $N = 500$, $r = 9$, and $n = 3$
        - The total number of possible samples, ${500 \choose 3}$
        - The number of sample containing exactly one defective chip, ${9 \choose 1} \times {491 \choose 2}$ → 3개중 한개가 defective chip인 경우의 확률 값 계산
            - $P( X = 1) = \frac{{r \choose x} \times {N - r \choose n - x}}{{N \choose n}} = \frac{{9 \choose 1} \times {491 \choose 2}}{{500 \choose 3}} \cong 0.0523$

---

## 3.4.1 Definition of the Poisson Distribution <중요>

- **A random variable that counts the number of “events” that
occur within certain specified boundaries**
- **A probability mass function for a random variable
Poisson distribution**
    - $X \sim P(\lambda)$
    - $P( X = x ) = \frac{e^{-\lambda}\lambda^{x}}{x!}$ , for $x = 0, 1, 2, 3, …$ 해석) $x$ 개 이벤트가 발생할 확률

- The Poisson distribution can be used to approximate the $B(n, p)$ distribution
    
    <img width="500" alt="스크린샷_2022-06-24_오전_1 02 39" src="https://user-images.githubusercontent.com/83820185/175346964-568691c6-b69e-4158-b92c-11a0aa61ac02.png">

    - when 1) $n$ is very large (larger than 150, say) and 2) the success probability $p$ is very small (smaller than 0.01, say).
    - A parameter value of $\lambda = np$ should be used for the Poisson distribution, so that it has the same expected value as the binomial distribution.
    

---

## 3.5.1 Definition of the Multinomial Distribution <중요>

- **The Multinomial Distribution** 
    - Consider a sequence of $n$ independent trials where each individual trial can have $k$ outcomes that occur with constant probability values
    $p_{1}, …, p_{k}$ with $\sum_{i = 1}^{k} p_{i} = 1$
    - The random variables $X_{1}, …, X_{k}$ that count the number of occurrences
    of each outcome are said to have a multinomial distribution, and their joint pmf,
    $P( X_{1} = x_{1}, …, X_{k} = x_{k} ) = \frac{n!}{x_{1}! … x_{k}!} \times p_{1}^{x_{1}} \times … \times p_{k}^{x_{k}}$, for nonnegative integer values of the $x_{i}$ satisfying $x_{1} + … + x_{k} = n$
    - The expectation of the variance of each random variable $X_{i}$
        - $E(X_{i}) = np_{i} , Var(X_{i}) = np_{i}(1 - p_{i})$
        - The random variables $X_{1}, …, X_{k}$ are not independet
