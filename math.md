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
## STATISTICS

* * *

### Mean
The **mean** (or arithmetic mean) is what most of us think of as the **average**, i.e., add up all the numbers and divide by the number of numbers
  
### Mode
The **mode** is the number that occurs the most frequently
   
### Median
The **median** is the "middle" number, i.e., if you were to order the numbers and take the middle one.  In the event that there are an even number of numbers, then you take the middle two numbers and compute the average (traditional mean) for those.

### Range
The **range** is the difference between the highest and lowest numbers

### Standard Deviation
The **standard deviation** is the measure of how "spread out" numbers are.
Determining the standard deviation for a population can be done following this sequence of steps:
    
  * **Step 1**: Work out the mean (average)
  * **Step 2**: For each number, subtract the mean and square the resulting differences
  * **Step 3**: Determine the mean of the above (a.k.a. **the variance**), i.e., sum the squared differences (from Step 2) and divide by how many there are
  * **Step 4**: Take the square root of Step 3
 
### Variance
The **variance** is the average of the squared differences from the mean.  It is what you have after Step 3 of the above is completed.  After all, **the standard deviation is simply the square root of the variance**.

### Sample Populations
When dealing with **sample populations** in which all data could not be gathered or considered, you need to calculate the variance differently: instead of summing the squared differences and then dividing by the number of numbers, $n$, divide by $n-1$.  This should always be done when dealing with so-called **sample data**.
    
### Combinations
**Combinations** refer to groupings in which **order is not important**.  Determining the number of possibilities in a combination that is unordered is similar to what we do with permutations, but you have to reduce the number of possiblities that are introduced by requiring order.

  * A combination that **allows for repetition** is calculated using **$\frac{(n+r-1)!}{(n-r)!} * \frac{1}{r!}$** or simply **$\frac{(n+r-1)!}{r!(n-r)!}$** where $n$ is the number of choices and $r$ is the number we are picking.

  * A combination that **does not allow for repetition** is calculated using **$\frac{n!}{(n-r)!} * \frac{1}{r!}$** where $n$ is the number of choices and $r$ is the number of them that we are picking.
    Essentially, it is a permutation in which we subtract the number of possibilities added by requiring order.  The formula is often simplied to **$\frac{n!}{r!(n-r)!} = \binom{n}{r}$** and is often said as "n choose r" (a.k.a. The Binomial Coefficient).
    
### Permutations
A **permuation** is an **ordered** combination.  There are two basic kinds of permutations: those that allow repetition and those that do not.  

 * If a permutation allows for repetition, then calculating the number of possible outcomes is as simple as **$n^r$** in which $n$ is the number of choices and $r$ is the number of items we are picking; this formula is for when repetition is permitted and order matters.

 * If a permutation **does not allow** for repetition, then **$\frac{!n}{(n-r)!}$** in which $n$ is the number of choices and $r$ is the number of items we are picking; this formula is for when repetition is not allowed and order matters.

### Z-Score
A **z-score** (a.k.a. a standard score) indicates how many standard deviations an element is from the mean.

### The Empirical Rule
**The empirical rule** is a rough gauge of normality.  It is also known as the **three-sigma rule** or the 68-95-99.7 rule. It provides a **quick estimate of the spread of data in a normal distribution given the mean and standard deviation**. 
When a number of data points fall outside the three standard deviation range, it can indicate a non-normal distribution.

 * 68% of the data will fall within one standard deviation of the mean
 * 95% of the data will fall within two standard deviations of the mean
 * Almost all (99.7%) of the data will fall within three standard deviations of the mean

## GEOMETRY

* * *

### Equation of Circles
Equations of circles are normally expressed in either:

  * #### Standard Form 
  The equation of a circle in **standard form** is $(x-h)^2+(y-k)^2 = r^2$ where the circle's center is at point $(h,k)$ with a radius of $r$.
  
  * #### General Form
  The equation of a circle in **general form** is $x^2+y^2+Dx+Ey+F=0$ and will require that you **complete the square** in order to convert the equation to the much easier to understand standard form.

## TRIGONOMETRY

* * *

### 30-60-90 Triangles
**30-60-90 triangles** are a special variant of right triangle.  Sides of 30-60-90 triangles are referred to using the following shorthand: **SL** (across from $30\unicode{xb0}$) is the "short leg", **LL** (across from $60\unicode{xb0}$) is the "long leg", and **H** refers to the hypotenuse (across from $90\unicode{xb0}$).

  * #### Side Ratios
  $1:\sqrt 3:2$, which corresponds to $SL:LL:H$
  
  * #### Side Formulas
  The above ratios, yield the following shortcut formulas for determining the side lengths:
    * $$SL = \frac{1}{2}H$$
    * $$LL = \frac{1}{2}H \sqrt 3$$ or simply $$SL\sqrt 3$$

### Law of Sines
The **Law of Sines** is an equation relating the lengths of the sides of any shaped triangle to the sines of its angles.  The law is normally stated using the reciprocals: $\frac{\sin(\angle{A})}{a} = \frac{\sin(\angle{B})}{b} = \frac{\sin(\angle{C})}{c}$. It can be used to compute the remaining sides of a triangle when two angles and a side are known; it can also be used when two sides and one of the non-enclosed angles are known.

### Law of Cosines
The **Law of Cosines** is a generalization of the right triangle-specific **Pythagorean Theorem**.  The Law of Cosines is useful in finding a missing angle measure, given all the sides of a triangle, or in finding a missing side length, provided you know measure of the angle opposite the missing side as well as the length of the other two sides.  Simply put, the **Law of Cosines** extends the usefulness of the **Pythagorean Theorem**.

  * #### Find a missing side
  $c^2= a^2+b^2-2ab\cos(\angle{C})$, if you were missing the side $c$, but knew the angle measure of $\angle{C}$.

  * #### Find a missing angle
  $\cos(\angle{C}) = \frac{a^2+b^2-c^2}{2ab}$, this assumes that you know the lengths of all the sides and are looking for the measure of the angle opposite of side $c$.  *Note:* Converting the result to degress will require use of the inverse $cos$ function: $arccos$.

## ALGEBRA II

* * *

### Geometric Series (Finite Sum)
$S_n = \frac{a_1(1-r^n)}{1-r}, r \neq 1$  where $n$ is the number of terms, $a_1$ is the first term and $r$ is the **common ratio**.  
For geometric sequences, the **common ratio** is the constant multiplier used to derive each successive number.

### Arithmetic Series (Finite Sum)
$S_n = \frac{n(a_1 + a_n)}{2}$  where $n$ is the number of terms, $a_1$ is the first term, and $a_n$ is the last term.

### Arithmetic Sequence (Find any Term)
$a_n = a_1 + (n-1)d$  where $n$ is the number of the term you are trying to find, $a_n$ is its value, $a_1$ is the first term (of the sequence), and $d$ is the **common difference**, i.e., the constant difference between each successive term.