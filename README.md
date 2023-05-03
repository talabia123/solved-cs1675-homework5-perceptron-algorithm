Download Link: https://assignmentchef.com/product/solved-cs1675-homework5-perceptron-algorithm
<br>
You will trace through a run of the perceptron algorithm.

You have the following two-dimensional data: {(-1,-4), (-3,-1), (-3,-2), (-2,1), (-1,-1), (4,5), (1,3), (4,0), (3,2), (5,3)}. The first five data points belong to the positive class, and the second set of five to the negative class. This data is linearly separable and can be plotted in 2D using its two feature dimensions. Your goal is to create figures similar to Figure 4.7 in Bishop.

Instead of a basis function, you will just use <b>x</b>, i.e. φ(<b>x</b>) = <b>x</b>.

In a script <span style="font-family: courier new;">perceptron.m</span>, implement the perceptron algorithm and use it, along with some provided plotting code, to trace through several iterations of the method:

<ol>

 <li> First, represent the data and labels, with samples as the rows and features (coordinates) as the columns. Use all the data for training since we won’t test but will only visualize what the method is learning. Set the learning rate <i>η</i> to 0.1. Initialize the weight vector to a vector of random numbers.</li>

 <li> Compute the predicted label vector <span style="font-family: courier new;">Y_pred</span> by multiplying the weights and features, and checking the sign of the result. Use the Matlab function <span style="font-family: courier new;">sign</span>. If the predicted label is 0, set it to 1.</li>

 <li>Compute the accuracy of the current prediction for each training sample. While the accuracy for some sample is not 1, loop as follows.</li>

 <li> Find a sample whose label isn’t accurately predicted. If there are multiple such samples, choose at random. Compute the weight update for that misclassified sample. Then predict all labels again using the new weights, and check the accuracy.</li>

 <li> Use the provided <span style="font-family: courier new;"><a href="https://people.cs.pitt.edu/~kovashka/cs1675_fa18/plot_points_w.m">plot_points_w.m</a></span> function to plot the data points and the direction of the weight vector. This function shows positive samples as open circles, and negative samples as filled circles. It shows correctly classified samples in green, and misclassified samples in red. It also outputs the iteration ID and the two feature dimensions for the misclassified example that is being used to correct <b>w</b>. This script requires that you keep an iteration counter <span style="font-family: courier new;">ct</span> and an index for which misclassified point was selected in a given iteration as <span style="font-family: courier new;">sel</span>. Name your weights vector variable <span style="font-family: courier new;">w</span>, your data matrix <span style="font-family: courier new;">X</span> (with samples as the rows), your vector of true labels <span style="font-family: courier new;">Y</span>, and your predicted labels <span style="font-family: courier new;">Y_pred</span>.</li>

 <li>In a file <span style="font-family: courier new;">report.pdf/docx</span>, show the process for three consecutive iterations of the method, i.e. include three figures output by the plotting function provided. If too many (or too few) iterations are taking place, terminate the run and start another run.</li>

</ol>

<b>Submission:</b> Please include the following files:

<ul>

 <li><span style="font-family: courier new;">perceptron.m</span></li>

 <li><span style="font-family: courier new;">report.pdf/docx</span></li>

</ul>