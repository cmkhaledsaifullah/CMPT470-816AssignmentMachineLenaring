# CMPT470-816AssignmentMachineLenaring
This Repository contains the code for the machine learning assignment of CMPT 470/816.


## Getting Started

The assignemnt will give you a basic understanding of how deep neural network can be used for source code. Here we use the source code as a feature.

By this assignment we will try to solve the following Software engineering problem:

```
Method Call Recommendation using Reccurent Neural Network(RNN) and Long Short Term Memory(LSTM) Based neural network.
```

There are three parts of this assignment:

1. Run the existing code: The code in the repository collect the dataset from any number of java projects. Then you use the dataset and run the python written machine learning code. It will train a reccurent neural network based model, evaluate the top-1 reccomendation and return the accuracy value. Neural Network is developed using [Keras](https://keras.io/) library.
2. Train and test with LSTM model: In this task, you need to change the machine learning code in such a way that it will train a LSTM model and test using the same. To do that you need to first do understand the code -> concept location -> effect analysis -> update code. Hint: The change is very small
3. Write the machine learning code using DeepLearning4j: Now do the whole machine learning task using DeepLearning4j library. [DeepLearning4J](https://deeplearning4j.org/) is a java based deep learning library maintained by Eclipse foundation. The architecture of the library is very similar to Keras. Therefore the tasks will be similar. 

### Prerequisites

Before running the code, you must have following packages installed in your computer:

```
java8 or later
maven
python3
pip
```

### TASK 1

A step by step instruction is given in the following

Step 1
Import all dependencies of maven first.
```
Open src/main/java/config/Config.java
change the following global variables
public static final String LOG_PATH = ROOT_PATH+"cms500_codeparser.log";
```
Put your NSID in logfile name. Otherwise you will not get any marks.

Step 2: 
Delete all .log files. 

Step 3: 
```
Open src/main/java/extraction/MethodCallCollector.java
Run main function
```
If the main method is run properly, you will see 10 csv files is written in "./data/dataset/" folder. These will be used for the machine learning script. So dont change anything.


Step 4: 
Run the following comamnd:
```
pip install -r requirements.txt
```
This will install all the required library for the machine learning tasks.


Step 4: 
```
open config.py
change the following global variables
log_file_path = root_folder+'cms500_keras_rnn.log'
```

next either run __main__.py file using IDE or run the following command:
```
python __main__.py
```
This will train the RNN based model on nine folds and will test with the remaining one fold of the dataset colelcted form step 3.


### TASK 2
Understand the code written in the __main__.py file. Find where you need to change to support LSTM training and testing (concept location). Try to analynis the effect of change of the code (effect analysis) and then update the code. 

Hint: You dont need to install any new library. Just a very small change will do the work

### TASK 3
This is a but tough because you need to learn how DeepLearning4J work. However, the working mechanism of kepler and deeplearning4j is almost same. But you need do data collecttiona data data preprocessing in java too.

To learn how RNN please look the follwing code example:
[RNN Example](http://github.com/eclipse/deeplearning4j-examples/blob/master/dl4j-examples/src/main/java/org/deeplearning4j/examples/recurrent/basic/BasicRNNExample.java)
[Another RNN Example](https://github.com/khaledkucse/methodRec/blob/master/src/main/java/Classification.java)

First try by yourself. If you fail then come to me. I will not help you if you dont anything.




## Authors

* **C M Khaled Saifullah** - *Initial work* - [khaledkucse](https://github.com/khaledkucse)

See also the list of [contributors](https://github.com/khaledkucse/DeepAPIMethodCallReccomendation/graphs/contributorss) who participated in this project.

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details


