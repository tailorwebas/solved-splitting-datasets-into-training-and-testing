Download Link: https://assignmentchef.com/product/solved-splitting-datasets-into-training-and-testing
<br>
<h1>2           Splitting Datasets into Training and Testing [10 points]</h1>

A common task in ML is to divide a dataset of independent instances into a ”training” set and a ”test” set. These two sets can then be used to measure how well an ML method generalizes to data it hasn’t seen before: we fit the method to the training set, then evaluate the trained method on the test set.

In this problem, you’ll demonstrate basic understanding of NumPy array indexing and random number generation by writing a procedure to divide an input dataset of <em>L </em>instances into a training set (of size <em>M</em>) and a test set (of size <em>N</em>). Each row of the original dataset should be exclusively assigned to either train or test.

How do we set the values of M and N? Your function will take a keyword argument <em>frac test </em>that specifies the number of test examples (<em>N</em>) as a fraction of the overall dataset size. To compute N, we always want to round up to the nearest whole number: <em>N </em>= <em>ceil</em>(<em>frac </em><em>test </em>× <em>L</em>)

We want the test set to be a uniform at random subset. You should look at the NumPy API for Random Sampling. Functions like <em>shuffle </em>or <em>permutation </em>might be helpful.

We also want the test set to be reproducible by specifying particular random seed. That is, if I run the code now to extract a train/test set, if I need to rerun the code later I’d like to be able to recover the exact same train/test assignments if needed. With <em>NumPy</em>, the common way to do this is by specifying a <em>random state </em>keyword argument that can either take an integer seed (0, 42, 1337, etc.) or an instance of the <em>RandomState </em>class. Specifying the same <em>random state </em>should deliver the same pseudo-randomness across multiple calls to a function.

Use the starter code in <em>spitDataset.py </em>for function definition and a detailed specification. You need to fill in the missing code. Remember, use exclusively <em>NumPy </em>functions. No calls to any functions in <em>sklearn </em>or other libraries.