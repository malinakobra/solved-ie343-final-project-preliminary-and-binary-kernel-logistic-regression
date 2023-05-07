Download Link: https://assignmentchef.com/product/solved-ie343-final-project-preliminary-and-binary-kernel-logistic-regression
<br>
<h1>1              Preliminary and Binary Kernel Logistic Regression</h1>

We implemented the logistic regression in the binary and multiple labels classification at the midterm project. In the final project, we will extend the logistic regression to the kernel logistic regression.

Let’s <em>N </em>and <em>d </em>denote the total number of the training data points and dimension of each data input’s dimension, respectively.

And let {(<em>X</em><sup>(<em>i</em>)</sup><em>,y</em><sup>(<em>i</em>)</sup>)}<em><sub>i</sub></em><sub>=1<em>,</em>2<em>,</em>···<em>,N </em></sub>be the training data sets. At the binary logistic regression, we train the parameter <em>θ </em>where the model was

<ol start="2">

 <li>P<em>. </em>(2.1)</li>

</ol>

Here, <em>concatenate</em>(1<em>,X</em>) := (1<em>,X</em><sub>1</sub><em>,X</em><sub>2</sub><em>,</em>···<em>X<sub>d</sub></em>) and <em>&lt; </em>·<em>,</em>· <em>&gt; </em>indicates the inner product.

Let’s review the SVM. To escape the non-linear separable situation, the mapping function <em>φ </em>was defined which increase the dimension of the data’s input space. For the hyper-plane <em>β</em><sub>0</sub>+ <em>&lt; β,φ</em><em><sup>~ </sup></em>(<em>X</em>) <em>&gt;</em>, the optimal <em>β</em><em><sup>~</sup></em><sup>∗ </sup>= <sup>P<em>N</em></sup><em><sub>j</sub></em><sub>=1 </sub><em>α<sub>j</sub>y</em><sup>(<em>j</em>)</sup><em>φ</em>(<em>X</em><sup>(<em>j</em>)</sup>).

From that <em>β</em><em><sup>~</sup></em><sup>∗</sup>, we obtain the optimal dual variable {<em>α<sub>j</sub></em><sup>∗</sup>}<em><sub>j</sub></em><sub>=1<em>,</em>2<em>,</em>···<em>,N </em></sub>by solving quadratic programming.

And from that mapping function <em>φ</em>, the kernel function <em>K </em>was defined by

<em>K</em>(<em>X</em><sup>(<em>i</em>)</sup><em>,X</em><sup>(<em>j</em>)</sup>) =<em>&lt; φ</em>(<em>X</em><sup>(<em>i</em>)</sup>)<em>,φ</em>(<em>X</em><sup>(<em>j</em>)</sup>) <em>&gt; .                                                                             </em>(2.2)

Now, let’s deal with the kernel logistic regression from these backgrounds. For binary kernel logistic regression, the model can be constructed by

1

P(<em>y </em>= 1|<em>X </em>= (<em>X</em><sub>1</sub><em>,X</em><sub>2</sub><em>,</em>···<em>X<sub>d</sub></em>)) =                                                           (2.3)

1 + <em>exp</em>(<em>&lt; </em>(<em>β</em><sub>0</sub><em>,β</em><em><sup>~</sup></em>)<em>,concatenate</em>(1<em>,φ</em>(<em>X</em>)) <em>&gt;</em>

(2.4)

(2.5)

(2.6)

1

(2.4) was derived by using). And at the (2.5), we redefine the <em>β</em><sub>0 </sub>to <em>α</em><sub>0</sub>.

In short, you need to implement the binary kernel logistic regression model

P                             (2.7)

by training parameter <em>α</em>.

<h1>2           TODO for Code Implementation</h1>

There are 2 tasks for the code implementation. ‘task 1’ and ‘task2’ are for binary logistic regression and binary kernel logistic regression, respectively. ‘task1’ and ‘task2’ files are attached and they are almost same from midterm project’s ‘mid_task2_titanic’ folder. The different things is that I provide additional files ‘./App/Pre_processing/kernel.py’ and ‘./App/rbf.py’. These are from the assignment 4 and will be helpful for the final project. Unlike midterm project, I already filled the ‘getData()’ method in the ‘.main.py’. And you need to complete followings for the code implementation.

<ul>

 <li>(task1)</li>

</ul>

It is similar to the midterm project. You need to fill out the ‘./App/logistic_regressor.py’. The code should be implemented in the minus-log-likelihood loss function, epoch_num=5000 and lr=0.00005 settings. And ‘main.py’ needs to print the 50 train accuracy results(print the test accuracy for every 100 epoch) and one test accuracy. Lastly, you need to use the bias term <em>θ</em><sub>0 </sub>of (2.1).

<ul>

 <li>(task2)</li>

</ul>

You need to fill out the ‘./App/logistic_regressor.py’ and ‘./main.py’ . The code should be implemented in the minus-log-likelihood loss function, RBF kernels, epoch_num=5000 and lr=0.005 settings. RBF kernels should use the hyperparameter (1,1,1,1,…1). And ‘main.py’ needs to print the 50 train accuracy results(print the test accuracy for every 100 epoch) and one test accuracy. Lastly, you need to use the bias term <em>α</em><sub>0 </sub>of (2.7).

<table width="516">

 <tbody>

  <tr>

   <td width="361"><em>– Final Porject</em></td>

   <td width="155">2</td>

  </tr>

 </tbody>

</table>

<h1>3           TODO for Report</h1>

<ul>

 <li>Write the kernel logistic regression model and logistic regression model for the binary labels data. For those models, which parameter we have to train? State the parameter’s dimension precisely.</li>

 <li>What’s the needs of the kernel logistic regression? i.e. from kernel logistic regression, what we can recover the issue that original logistic regression can’t solve and state the reason precisely.</li>

 <li>State the advantages and disadvantages of kernel logistic regression and original logistic regression.</li>

 <li>State how the weight update should happen for the original logistic regression and kernel logistic regression at the binary version. You need to write precisely how the gradient is induced also.</li>

 <li>Construct the model for the original logistic regression and kernel logistic regression at the multiple labels(<em>K </em>: number of labels <em>&gt; </em>2). You need to clarify the parameters.</li>

 <li>For the model you construct at the (5) and minus-log-likelihood loss function, write the pseudo code about each weight update situation. You also need to state the reason and input value in the method function precisely.</li>

 <li>Describe the method about your logistic regression model with the code at the task1 line by line.</li>

 <li>Describe the method about your kernel logistic regression model and py with the code at the task2 line by line.</li>

</ul>