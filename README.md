# SVMwithTruncatedPinballLoss
1,
This solver is a modified version of LIBSVM 3.2.1:
Citation:
Chih-Chung Chang and Chih-Jen Lin, LIBSVM : a library for support vector machines. ACM Transactions on Intelligent Systems and Technology, 2:27:1--27:27, 2011. Software available at http://www.csie.ntu.edu.tw/~cjlin/libsvm
and it is used for experiments in our paper:
"Support Vector Machine Classifier with Truncated Pinball Loss"

2,
All of our modifications are annotated in the code.

3,
Most command line options are the same with LIBSVM 3.2.1, except the following ones: 
-y: Set hyper-parameter s in the paper;
-i: Set hyper-parameter $\tau$ in the paper;
-o: Set the termination accuracy of CCCP iterations;
-e: Set the termination accuracy of inner decomposition method;
Example:
==============================================================
./svm-train -s 5 -h 0 -c 16 -g 0.03125 -y 0.01 -i 0.5 australian
CCCP outer optimization finished, #number of outer iters = 3
Percentage of SVs:48.000000  
The training time is 0.011260s
./svm-predict australian.t australian.model australian.t.predict
Accuracy = 86.9388% (426/490) (classification)
==============================================================
