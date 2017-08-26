# Week 2

## Binary Classification

Logistic regression is an algorithm for binary classification.

 0 or 1 - depending of the answer (ie. image contains cat or not)

In an image we should roll out all our inputs into a `Feature Vector`

Take the matrices that correspond to the RGB pixel inputs.
In a 64x64 pixel inputs there would be 12288 (64x64x3) entries into the feature verctor.

  ```
    x =  [255, 231 ... , 255, 234 ... , 255, 145 ]
           ---RED---   ---GREEN---   ---BLUE---
  ```

  Nx or n  -> repesents the size of the dimension of this input feature vector

The goal is to classify wether each input of the feature vector is `0` or  `1`

### Notation:

  (x,y) -> single training example

  Where `x` is ![x](http://chart.apis.google.com/chart?cht=tx&chs=30&chl=x%20%5Cepsilon%20%5Cmathbb%7BR%7D%5E%7BN_%7Bx%7D%7D)
 <!-- x \epsilon \mathbb{R}^{N_{x}} -->

  And `y` is  ![y](http://chart.apis.google.com/chart?cht=tx&chs=30&chl=y%20%5Cepsilon%20%5Cbig%5C%7B0%20%2C%201%5Cbig%5C%7D)

<!-- y \epsilon \big\{0 , 1\big\} -->

Training sets would be:

 `m` -> training examples

 the training set would be represented as follows:

![](http://chart.apis.google.com/chart?cht=tx&chs=30&chl=%5C%7B%5Cleft(%20x%5E%7B(1)%7D%2C%20y%5E%7B(1)%7D%20%5Cright%20)%2C%20%5Cleft(%20x%5E%7B(2)%7D%2C%20y%5E%7B(2)%7D%20%5Cright%20)%2C%5Cldots%2C%20%5Cleft(%20x%5E%7B(n)%7D%2C%20y%5E%7B(n)%7D%20%5Cright%20)%5C%7D)

<!--\{\left( x^{(1)}, y^{(1)} \right ), \left( x^{(2)}, y^{(2)} \right ),\ldots, \left( x^{(n)}, y^{(n)} \right )\}-->

There would be a difference on M(training) and M(test) when refering to the number or training/test examples.
Also the training set would be represented by a matrix:

![matrix](http://chart.apis.google.com/chart?cht=tx&chs=51&chl=x%3D%20%5Cbegin%7Bbmatrix%7D%0A%7C%20%26%20%7C%20%26%20%7C%20%26%20%7C%20%5C%5C%20%0Ax%5E%7B(1)%7D%20%26%20x%5E%7B(2)%7D%26%20%5Cldots%20%26x%5E%7B(m)%7D%20%5C%5C%20%0A%7C%20%26%20%7C%20%26%20%7C%20%26%20%7C%20%5C%5C%20%0A%5Cend%7Bbmatrix%7D)

Where Nx (height of the matrix) is the number of rows. And M is the number of examples.
<!-- x= \begin{bmatrix}
| & | & | & | \\
x^{(1)} & x^{(2)}& \ldots &x^{(m)} \\
| & | & | & | \\
\end{bmatrix}-->

There are other ways to implement the matrix (ie. the number of training examples as rows). The convention before is much easier to implement.

So this would be: ![matrixrep](http://chart.apis.google.com/chart?cht=tx&chs=30&chl=x%20%5Cepsilon%20%5Cmathbb%7BR%7D%5E%7BN_%7Bx%7D%20%5Ccdot%20m%7D)
 <!-- x \epsilon \mathbb{R}^{N_{x} \cdot m} -->

 or in python: 

```python
  x.shape(Nx, m)
```





