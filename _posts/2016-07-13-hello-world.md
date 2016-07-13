---
title: 'Hello World!'
author: Fixel Algorithms
layout: post
class: news
---
![2016][a]Hello World! This is a test post with some MathJax code as well. 

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$ 

<!-- This is commented out -->

Not being cheap, here's a [link](http://www.google.com) (which can be written also [this way][1]) as well as some `inline code`, and code block

```
let a = "ES2015";
let it = "be";
```

Looking forward to seeing here often!

[a]: {{site.baseurl}}/news/images/2016.png "2016"
[1]: http://www.google.com