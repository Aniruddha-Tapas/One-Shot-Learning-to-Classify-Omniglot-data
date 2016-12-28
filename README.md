Overview
============
This is a One-Shot Learning Handwritten Character Classifer written in Python using the SciPy library. The code trains against a few examples of handwritten characters and then tries to classify characters correctly. The error rate is around 38%. If you want to try a state-of-the-art, better-than-human, one-shot learning library that you can apply to all sorts of data, check out [this](https://github.com/MaxwellRebo/PyBPL) repo. 

One-Shot Learning
=============

One-shot learning refers to the process of learn features from datasets containing few training samples. This is in contrast to some machine learning techniques like CNN which require large datasets in order to perform the learning task effectively.

Humans have the ability to learn categories using very few examples and can match features and perform pattern recognition effectively well despite of less data available. If I was to provide you a reference card of an unfamiliar alphabet and show you a series of hand written variants of that alphabet, chances are you'd be able to match a high percentage of this test set with the reference alphabet -- perhaps misclassifying a few exotic variations. The current state-of-the-art for visual pattern recognition are convolutional neural nets. The problem with convolutional neural nets, and with neural networks to begin with, is that they require massive amounts of labeled data to train on and resources to do so. The key motivation for the one-shot learning technique is that systems, like humans, can use prior knowledge about object categories to classify new objects.


Dependencies
============

* Python - (https://www.python.org/downloads/)
* scipy - `pip install scipy`
* numpy `pip install numpy`

Use [pip](https://pypi.python.org/pypi/pip) to install any missing dependencies


Basic Usage
===========
Step 1 - Run the code! It'll train against the handwritten character samples in the `all_runs` folder and then test it's classification ability.
It should output an average error rate of around 38%.
```shell
python demo_classification.py
```

Output
===========

<code>
One-shot classification demo with Modified Hausdorff Distance
 run 00 (error 45.0%)
 run 01 (error 35.0%)
 run 02 (error 40.0%)
 run 03 (error 25.0%)
 run 04 (error 30.0%)
 run 05 (error 15.0%)
 run 06 (error 60.0%)
 run 07 (error 35.0%)
 run 08 (error 40.0%)
 run 09 (error 55.0%)
 run 10 (error 15.0%)
 run 11 (error 70.0%)
 run 12 (error 65.0%)
 run 13 (error 35.0%)
 run 14 (error 15.0%)
 run 15 (error 25.0%)
 run 16 (error 30.0%)
 run 17 (error 40.0%)
 run 18 (error 70.0%)
 run 19 (error 30.0%)
Average error 38.8%
</code>

References
===========
Credit for this demo code goes to the authors of the original BPL paper, this was the baseline demo code they used to compare their novel (much better) Matlab results against. 

# Omniglot data set for one-shot learning

This dataset contains 1623 different handwritten characters from 50 different alphabets.   
Each of the 1623 characters was drawn online via Amazon's Mechanical Turk by 20 different people.   
The Omniglot data set contains 50 alphabets total. These are split into a background set of 30 alphabets and an evaluation set of 20 alphabets.  

The data is stored in the `all_runs` folder which contain the testing set, training set and the class labels in each of the 20 runs subfolders.


[Lake, B. M., Salakhutdinov, R., and Tenenbaum, J. B. (2015). Human-level concept learning through probabilistic program induction.](http://www.sciencemag.org/content/350/6266/1332.short) _Science_, 350(6266), 1332-1338.


We are grateful for the [Omniglot](http://www.omniglot.com/) encyclopedia of writing systems for helping to make this data set possible, and for [Jason Gross](https://people.csail.mit.edu/jgross/) who was essential to the development and collection of this data set.

<hr>