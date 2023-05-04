Download Link: https://assignmentchef.com/product/solved-cs7643-homework-1
<br>
<h1>1           Multiple Choice Questions</h1>

<ol>

 <li>true/false We are machine learners with a slight gambling problem (very different from gamblers with a machine learning problem!). Our friend, Bob, is proposing the following payout on the roll of a dice:</li>

</ol>

payout                                                                  (1)

where <em>x </em>∈ {1<em>,</em>2<em>,</em>3<em>,</em>4<em>,</em>5<em>,</em>6} is the outcome of the roll, (+) means payout to us and (−) means payout to Bob. Is this a good bet i.e are we expected to make money?

True              False

<ol start="2">

 <li>(1 point) <em>X </em>is a continuous random variable with the probability density function:</li>

</ol>

(2)

Which of the following statements are true about equation for the corresponding cumulative density function (cdf) <em>C</em>(<em>x</em>)?

[<em>Hint: </em>Recall that CDF is defined as <em>C</em>(<em>x</em>) = <em>Pr</em>(<em>X </em>≤ <em>x</em>).]

All of the above

None of the above

<ol start="3">

 <li>(2 point) A random variable x in standard normal distribution has following probability density</li>

</ol>

(3)

Evaluate following integral

(4)

[<em>Hint: </em>We are not sadistic (okay, we’re a little sadistic, but not for this question). This is not a calculus question.]

a + b + c                c               a + c                b + c

<ol start="4">

 <li>(2 points) Consider the following function of <strong>x </strong>= (<em>x</em><sub>1</sub><em>,x</em><sub>2</sub><em>,x</em><sub>3</sub><em>,x</em><sub>4</sub><em>,x</em><sub>5</sub><em>,x</em><sub>6</sub>):</li>

</ol>

(5)

where <em>σ </em>is the sigmoid function

(6)

Compute the gradient ∇<strong><sub>x</sub></strong><em>f</em>(·) and evaluate it at at <strong>x</strong>ˆ = (5<em>,</em>−1<em>,</em>6<em>,</em>12<em>,</em>7<em>,</em>−5).

<ol start="5">

 <li>(2 points) Which of the following functions are convex?</li>

</ol>

<strong>x </strong>for <strong>x </strong>∈ R<em><sup>n </sup></em> for <strong>w </strong>∈ R<em><sup>d</sup></em>

All of the above

<ol start="6">

 <li>(2 points) Suppose you want to predict an unknown value <em>Y </em>∈ R, but you are only given a sequence of noisy observations <em>x</em><sub>1</sub><em>…x<sub>n </sub></em>of <em>Y </em>with i.i.d. noise ().. If we assume the noise is I.I.D. Gaussian (), the maximum likelihood estimate (<em>y</em>ˆ) for <em>Y </em>can be given by:</li>

</ol>

= argmin

= argmin

Both A &amp; C

Both B &amp; C

<h1>2           Proofs</h1>

<ol start="7">

 <li> Prove that</li>

</ol>

log<em><sub>e </sub>x </em>≤ <em>x </em>− 1<em>,             </em>∀<em>x &gt; </em>0                                                                 (7)

with equality if and only if <em>x </em>= 1.

[<em>Hint: </em>Consider differentiation of log(<em>x</em>) − (<em>x </em>− 1) and think about concavity/convexity and second derivatives.]

<ol start="8">

 <li>(6 points) Consider two discrete probability distributions <em>p </em>and <em>q </em>over <em>k </em>outcomes:</li>

</ol>

<em>k     k </em>X X

<em>p<sub>i </sub></em>=           <em>q<sub>i </sub></em>= 1                                                          (8a)

<em>i</em>=1                    <em>i</em>=1

<em>p<sub>i </sub>&gt; </em>0<em>,q<sub>i </sub>&gt; </em>0<em>,            </em>∀<em>i </em>∈ {1<em>,…,k</em>}                                                             (8b)

The Kullback-Leibler (KL) divergence (also known as the <em>relative entropy</em>) between these distributions is given by:

(9) It is common to refer to <em>KL</em>(<em>p,q</em>) as a measure of distance (even though it is not a proper metric). Many algorithms in machine learning are based on minimizing KL divergence between two probability distributions. In this question, we will show why this might be a sensible thing to do.

[<em>Hint: </em>This question doesn’t require you to know anything more than the definition of <em>KL</em>(<em>p,q</em>) and the identity in Q7]

<ul>

 <li>Using the results from Q7, show that <em>KL</em>(<em>p,q</em>) is always non-negative.</li>

 <li>When is <em>KL</em>(<em>p,q</em>) = 0?</li>

 <li>Provide a counterexample to show that the KL divergence is not a symmetric function of its arguments: <em>KL</em>(<em>p,q</em>) 6= <em>KL</em>(<em>q,p</em>)</li>

</ul>

<ol start="9">

 <li>(6 points) In this question, you will prove that cross-entropy loss for a softmax classifier is convex in the model parameters, thus gradient descent is guaranteed to find the optimal parameters. Formally, consider a single training example (<strong>x</strong><em>,y</em>). Simplifying the notation slightly from the implementation writeup, let</li>

</ol>

<strong>z </strong>= <em>W</em><strong>x </strong>+ <strong>b</strong><em>,                                                                              </em>(10)

(11)

(12)

Prove that <em>L</em>(·) is convex in W.

[<em>Hint: </em>One way of solving this problem is “brute force” with first principles and Hessians.

There are more elegant solutions.]