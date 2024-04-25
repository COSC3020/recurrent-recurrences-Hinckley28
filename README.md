[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/8KYthzwp)
# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

  $T(n) = T(n/13) + 5$\
  $T(n/13) = T(n/169) + 5$\
  $T(n) = T(n/169) + 5 + 5$\
  $= T(n/13^i) + 5i$\
  for i = logn\
  $T(1) + 5log(n) \in \Theta(logn)$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$T(n) = 13T(n/13) + 5$\
$T(n/13) = 13T(n/169) + 5$\
$T(n) = 13(13T(n/169) + 5 + 5$\
$T(n) = 169T(n/169) + 5 + 5$\
$T(n) = 13^iT(n/13^i) + 5i$\
for i = logn\
$nT(1) + 5logn \in \Theta(n)$\

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

$T(n) = 13T(n/13) + 2n$\
$T(n/13) = 13T(n/169) + 2(n/13)$\
$T(n) = 13(13T(n/169) + 2(n/13)) + 2n$\
$T(n) = 13^2T(n/169) + 26n/13 + 2n$\
$T(n) = 13^2T(n/169) + 2n + 2n$\
$T(n/169) = 13T(n/13^3) + 2(n/13^2)$\
$T(n) = 13^2(13T(n/13^3) + 2(n/13^2)) + 2n + 2n$\
$T(n) = 13^3T(n/13^3) + 338n/169 + 2n + 2n$\
$T(n) = 13^3T(n/13^3) + 2n + 2n + 2n$\
$T(n) = 13^iT(n/13^i) + (2n)i$\
for i = log n\
$T(n) = nT(1) + 2n(logn) \in \Theta(nlogn)$\

