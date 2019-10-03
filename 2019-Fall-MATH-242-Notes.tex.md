# 2019-10-02 Lecture

## Properties of the absolute value
$|a| \le |b| \iff -|b| \le a \le |b|$

### The triangle inequality- Sum
$|a| + |b| \le |a + b| \le |a| + |b|$. (3)

### Proof for the triangle inequality- Sum
$|a| \le |a| \implies -|a| \le a \le |a|$
$|b| \le |b| \implies -|b| \le b \le |b|$

*Sum the two inequalities*

$- (|a| + |b|) \le a + b \le |a| + |b|$

$\implies |a + b| \le |a| + |b|$.

### The triangle inequality- Difference
$||a| - |b|| \le |a - b| \le |a| + |b|$

### Proof- first inequality

"Important trick": **Add and subtract the same number to construct a "triangle."**

$|a| = |(a - b) + b|$

Apply the triangle sum inequality.

$|a| = |(a - b) + b| \le |a - b| + |b|$

Substract $|b|$ from both sides of this equation:

$|a| - |b| \le |a - b|$.

That's not sufficient for an absolute value on the left-hand-side. Interchange $a$ and $b$ to obtain a similar expression:

$|b| - |a| \le |b - a| = |a - b|$

Multiple both side by $(-1)$:

$|a| - |b| \ge - |a - b|$.

In other words,

$-|a - b| \le |a| - |b| \le |a - b|$.

Apply property (3) to obtain

$||a| - |b|| \le |a - b|$.

### Proof- second Inequality
Apply the triangle sum inequality:
$|a - b| = |a + (-b)| \le |a| + |(-b)| = |a| + |b|$.

### General Triangle Inequality: three or more terms in the center absolute value
$||a_1| + |a_ 2| + \cdots |a_n|| \le |a_1 + a_2 + \cdots a_n| \le |a_1| + |a_ 2| + \cdots |a_n|$.

### Proof 
Apply mathematical induction on $n$ with the help of triangle inequality for the difference of two terms.

### Definition 
For every $\epsilon > 0$ and $a \in \mathbb{R}$, we call $\epsilon$-neighborhood of $a$ the set $V_\epsilon(a) = \{x\in \mathbb{R}: |x - a| <\epsilon\}$. Note that the two endpoints are not included.

That's all the points in the interval of radius $\epsilon$ and $a$ as the center.

$|x - a| <\epsilon$ can be expressed as two inequalities:

$x - a <\epsilon$ and $x - a > -\epsilon$. (Diagram 0x01)

### Proposition
Let $x \in \mathbb{R}$. Assume that $x \in V_\epsilon(a)$ for all $\epsilon >0$. Then $x = a$.

### Proof by contradiction
Assume by contradiction that $x \neq a$.

*Take anything that is between $0$ and $|x - a|$ to create a contradiction.*.

Take $\displaystyle \epsilon = \frac{|x - a|}{2}$. 

$x \neq a \implies \epsilon \neq 0$.

Since $x \in V_\epsilon(a)$, 

$|x - a| \le \displaystyle \frac{|x - a|}{2}$

Subtract $\displaystyle \frac{|x - a|}{2}$ from both sides of the inequality.

$\displaystyle \frac{|x - a|}{2} \le 0$.

$x \neq a \implies |x - a| \neq 0$.

$|x - a| < 0$. Contradiction.


# 2019-10-02 (WED) Lecture
## Upper and Lower Bounds
### Definition- Upper Bounds
A subset $S$ of $\mathbb{R}$ is **bounded above** if $\exist u\in \mathbb{R}$ such that $\forall s \in S$, $s \le u$. As long as this condition is satisfied, this $u$ is an **upper bound** of set $S$.

$u$ is a $\verb!supremum!$ (**least upper bound**) of $S$ if
1. $u$ is an upper bound of $S$, and
2. $u \le v$ for all upper bounds $v$ of $S$.

Notations: $\displaystyle u = \sup{S} = \sup_{s\in S} s$

Note that $u$ isn't necessarily a member of the set $S$. For example, $S$ is an interval defined with an open upper bound.

Additionally, $u$ is the **maximum** of $S$ if $u$ is a $\verb!supremum!$ (**least upper bound**) of $S$, and 
3. $u \in S$.

Notations: $\displaystyle u = \max{S} = \max_{s \in S} s$

### Definition- Lower Bounds
A subset $S$ of $\mathbb{R}$ is **bounded below** if $\exist u \in \mathbb{R}$ such that $\forall s \in S$, $s \ge u$. As long as this condition is satisfied, this $u$ is a **lower bound** of set $S$.

$u$ is a $\verb!infimum!$ (**greatest upper bound**) of $S$ if
1. $u$ is a lower bound of $S$, and
2. $u \ge v$ for all lower bounds $v$ of $S$.

Notations: $\displaystyle u = \inf{S} = \inf_{s\in S} s$

Additionally, $u$ is the **minimum** of $S$ if $u$ is a $\verb!infimum!$ (**greatest upper bound**) of $S$, and 
3. $u \in S$.

Notations: $\displaystyle u = \min{S} = \min_{s \in S} s$

### Definition- Bounded Sets
A set $S$ is **bounded** if it is bounded both above and below.

### Proposition- Uniqueness of Supremum and Infimum
The supremum and infimum of a set are unique provided that they exist.

### Proof for the Uniqueness of Supremum and Infimum
*Assume by contradiction that there are more than one suprema and infima that are different from each other.*

Assume that $u_1$ is a supremum of and $u_2$ be an upper bound of $S \subseteq \mathbb{R}$. Assume that $u_1 \neq u_2$.

By definition,

- $u_1 \le u_2$, and
- $u_2 \le u_1$.

In other words, $u_1 = u_2$. Contradiction. Hence the supremum of a set is unique.

*The proof for the uniqueness of the infimum of a set is similar.*

### Proposition
Let $u \in \mathbb{R}$ be an upper bound of $S$.
1. If $u \in S$, $u = \max{S}$ by definition.
2. $u = \sup{S} \iff \forall \epsilon >0$, $\exist s_{\epsilon} \in S$ such that $s_\epsilon > u - \epsilon$.

*The subscript $\epsilon$ next to the member of $S$, $s_{\epsilon}$ indicates that the exact set of $s$ that is chosen **depends** on the value of $\epsilon$.* 
