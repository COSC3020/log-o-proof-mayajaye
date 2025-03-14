# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

### Proof

$T(n) \in O(f(n)) \iff  \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

= $T(n) \in O(log{_2}{n}) \iff  \exists c, n_0: T(n) \leq c \cdot log{_2}{n} \forall n \geq n_0$ {definition of $O(log{_2}{n})$}

= $T(n) \in O(log{_2}{n}) \iff  \exists n_0: T(n) \leq  \frac{1}{log{_2}{5}} \cdot log{_2}{n} \forall n \geq n_0$ {replace $\exists$ c → $\frac{1}{log{_2}{5}}$}

= $T(n) \in O(log{_2}{n}) \iff  \exists n_0: T(n) \leq  1  \cdot log{_5}{n} \forall n \geq n_0$ {change of base formula}

= $T(n) \in O(log{_2}{n}) \iff  \exists c, n_0: T(n) \leq c \cdot log{_5}{n} \forall n \geq n_0$ {replace $1 → \exists c, c$}

= $T(n) \in O(log{_5}{n}) \iff  \exists c, n_0: T(n) \leq c \cdot log{_5}{n} \forall n \geq n_0$ {definition of $O(log{_5}{n})$}

= $T(n) \in O(log{_5}{n}) \iff  \exists n_0: T(n) \leq  \frac{1}{log{_5}{2}} \cdot log{_5}{n} \forall n \geq n_0$ {replace $\exists$ c → $\frac{1}{log{_5}{2}}$}

= $T(n) \in O(log{_5}{n}) \iff  \exists n_0: T(n) \leq  1  \cdot log{_2}{n} \forall n \geq n_0$ {change of base formula}

= $T(n) \in O(log{_2}{n}) \iff  \exists c, n_0: T(n) \leq c \cdot log{_2}{n} \forall n \geq n_0$ {replace $1 → \exists c, c$}

= $T(n) \in O(log{_2}{n}) \iff  \exists c, n_0: T(n) \leq c \cdot log{_2}{n} \forall n \geq n_0$ {definition of $O(log{_2}{n})$} 

Q.E.D

"I certify that I have listed all sources used to complete this exercise,
including the use of any Large Language Models. All of the work is my own, except
where stated otherwise. I am aware that plagiarism carries severe penalties and
that if plagiarism is suspected, charges may be filed against me without prior
notice."