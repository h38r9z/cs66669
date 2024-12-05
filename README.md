java c
Machine   Learning:   Fall   Exam 
IEOR E4525   Spring   2020, 
May   8th,   2020
1. Classiﬁer Boundaries [20   pts]
Given   the   following   classiﬁers:
1 A   logistic   regression   classiﬁer.
2 A logistic regression classiﬁer trained on the input   features x1   ,   x2   ,   x1(2),   x2(2).
3 A   nearest   neighbors   classiﬁer.
4 A   SVM   with   linear   kernel.
5 A   SVM   with   a   polynomial   kernel   of degree   d =   2.
K(x,   x') =   (1   + xx')2                                                                                                                                                      (1)
6 A   SVM   with   a   Gaussian   kernelK(x, x0 ) = e−γ|x−x'|2                                                                                                   (2)
with   and   intermediate   (neither   too   large,   not   too   small)   value   of the   √   parameter.
7 A   linear   SVM   classiﬁer trained with the   input   features   x1   ,   x2   ,   x1(2),   x2(2).
8 A   SVM   with   a   Gaussian   kernel   and   a   very   small   value   of √   .
9 A   LDA   classiﬁer
10 A   QDA   classiﬁer
11 A   Classiﬁcation   Tree.
12 A   Gaussian   Naive   Bayes   classiﬁer.
Indicate with classification boundary in Figure (1) was most likely gener-ated   by   each   one   of the   classiﬁers   above.
Note   that   more   that   one   of the   classiﬁers   might   have   generated   the   same   boundary.
If   not   indicated   otherwise   assume   the   classiﬁers   were   trained   on   the   raw   input   features   x   =   (x1,   x2)   ∈ R2.

Figure   1:      Classiﬁcation   boundaries   for   Problem 1
2. Polynomial Kernel [20   points]
Given   by   x   =   (xA   ;   xB   )   ∈ R2      and   x'    =   (xA(');   xB('))   ∈   R2    describe   the   feature
mapping   Φ(儿)   that   generates   the   kernel:
K(x; x')   =   (1   + √xT x')3    =    (1   + √ (xA xA(')   + xB xB(')))3                                                            (3)
3. Dense Neural Network [30   points]
We   have   a   dense   neural   network   with   two   hidden   layers   deﬁned   by   the   following   graph:

Figure   2:      Network   Architecture   for   Problem   5
where
• The   two   hidden   layers   have   ReLU   activation.
•   the   connection   between   the   input   an   the   ﬁrst   hidden   layer   is   given   by

and

•      The   connection   between   the   ﬁrst   and   second   hidden   layers   is   given   by

and

•   the   connection   between the   second   hidden   layer   and the   output   unit   η   is   given   by
W2      =   (1            2            -1)                                                                                                            (8)
and
b2      =   (-3)                                                                                                                                 (9)
• the   last   layer   has   logistic   activation   so   that

• The   network   perfo代 写IEOR E4525 Spring 2020, Machine Learning: Fall ExamJava
代做程序编程语言rmance   is   assessed   using   the   logistic   loss
l(y,   η)   = log   (1 + eη )   -   yη                                                                         (11)
Given   one   input   sample      (x1   ,   x2   ,   x3   ,   x4   )   =      (0,   -2,   1,   1)   and   the   network’s   output   label   y =   1   compute:
(a)    The ﬁrst hidden   layer   activations   (a1(1),   a2(1)).
(b)    The   second   hidden   layer   activations   (a1(2),   a2(2),   a3(2)).
(c)      The   output   ˆ(y)(x)
With   that   we   have

(d)    Back   propagate   the   errors   δα through   the   network   layers
(e)    Compute the gradients ∂W2/∂ L and ∂b2/∂L for the   learnable parameters   W2   ,   b2    of   the   output   layer.
(f)   Compute   the   gradient   to   the   learnable   parameters   W1   ,   b1       of   the   second hidden   layer
(g)   Compute the gradient to the learnable parameters W0   , b0    of   the ﬁrst   hidden layer
4. Tweedie Distribution:    Generalized Linear Model [30 points]
The Tweedie distribution is frequently use to model the distribution of   in-   surance losses.   This distribution belongs to an exponential family deﬁned by   the   probability   density   function
where   the   parameter   μ    >    0   is   unknown,   the   parameter   1   < p < 2 is assumed to be known, and the function h(y; p) is the base measure that does not depend on μ .
(a)   Write   an   expression   for   the   sufficient   statistic   T   (y)   of   the   tweedie distribution:
(b)   Write an expression for the canonical parameter η   as a function of μ   and   p.
(c)   Find   the   expression   for   the   cumulant   function   A(η)
(d)   Derive an expression for the expected valueˆ(y)   of   the random variable   y   in terms of the parameters p   and μ:
(e)   Derive an expression for the variance of   y in terms of   the distribution   parameters p   and μ
(f)   Assume   we   have   training   observations   {xi   ,   yi   } for   i   = 1, . . . ,   N   where we wish to assume   that
•    yi      > 0 is   an   observed,   positive   valued   labels.
•      xi      ∈ RD      is   our   input   data.
•   p(yi   jxi   ) has   a   tweedie   distribution   with ﬁxed, known   parameter p   but unknown parameter μ   that depends on   x.
•      The   canonical   parameter   ηi      is   linear   in   xi
η(xi   ) = xi(T)w   +   b                                                                                          (14)
Write   the   loss   function   L(w,   b;   {xi   ,   yi   }   of   the   generalized   tweedie   re-   gression model
(g)   Write the gradient of the loss L with   respect   to   w   and   b.
(h)   What   does   the   constrain   μ    >    0   implies   for   the   allowed   values   of   the   canonical   parameter?      How   would   this   afect   the   optimization problem   of   learning   the   parameters   w   ,b?.    Explain   brieﬁy      what   you would do to resolve   this   issue.






         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
