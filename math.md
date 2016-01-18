---
layout: page
title: Math Cheatsheet
permalink: /math/
excerpt: Math cheatsheet for all the math-related rules and formulas I can't seem to remember off the top of my head
---
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    },
    displayAlign: "left"
  });
</script>
<script type="text/javascript" async
  src="//cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML&displayAlign=left">
</script>
## Trigonometry

* * *

### Law of Cosines

The **Law of Cosines** is a generalization of the right triangle-specific **Pythagorean Theorem**.  The Law of Cosines is useful in finding a missing angle measure, given all the sides of a triangle, or in finding a missing side length, provided you know measure of the angle opposite the missing side as well as the length of the other two sides.  Simply put, the **Law of Cosines** extends the usefulness of the **Pythagorean Theorem**.

* #### Find a missing side 
$c^2= a^2+b^2-2ab\cos(\angle{C})$, if you were missing the side $c$, but knew the angle measure of $\angle{C}$.

* #### Find a missing angle
$\cos(\angle{C}) = \frac{a^2+b^2-c^2}{2ab}$, this assumes that you know the lengths of all the sides and are looking for the measure of the angle opposite of side $c$.  *Note:* Converting the result to degress will require use of the inverse $cos$ function: $arccos$.

## Algebra II

* * *

### Geometric Series (Finite Sum)

$S_n = \frac{a_1(1-r^n)}{1-r}, r \neq 1$  where $n$ is the number of terms, $a_1$ is the first term and $r$ is the **common ratio**.  
For geometric sequences, the **common ratio** is the constant multiplier used to derive each successive number.

### Arithmetic Series (Finite Sum)

$S_n = \frac{n(a_1 + a_n)}{2}$  where $n$ is the number of terms, $a_1$ is the first term, and $a_n$ is the last term.

### Arithmetic Sequence (Find any Term)

$a_n = a_1 + (n-1)d$  where $n$ is the number of the term you are trying to find, $a_n$ is its value, $a_1$ is the first term (of the sequence), and $d$ is the **common difference**, i.e., the constant difference between each successive term.