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

  ```latex
    x \epsilon \mathbb{R}^{N_{x}}
  ```
