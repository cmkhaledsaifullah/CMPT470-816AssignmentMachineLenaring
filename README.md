# CMPT470-816AssignmentMachineLearning
This Repository contains the code for the machine learning assignment of CMPT 470/816.


## Getting Started

The assignment will give you a basic understanding of how deep neural networks can be used for source code.
Here I use the source code as a feature and feed them into the neural network.

By this assignment, you will solve the following Software engineering problem:

```
Method Call Recommendation using Reccurent Neural Network(RNN) and Long Short Term Memory(LSTM) Based neural network.
```


There are three parts of this assignment:

1. Run the existing code: The Java code in the repository collects the dataset from any number of java projects. Then you use the dataset and run the python written machine learning code situated at [scripts](scripts) folder. It will train a recurrent neural network based model, evaluate the top-1 recommendation and return the accuracy value. Neural Network is developed using [Keras](https://keras.io/) library.

2. Train and test with the LSTM model: In this task, you need to change the machine learning code in such a way that it will train an LSTM model and test using the same. To do that, you need to first understand the code, locate where the change is required (concept location), determine the lines of code that are going to be affected due to the change (effect analysis), and update the code accordingly.

3. Write the machine learning code using DeepLearning4j: Now you need to write the whole machine learning code using the DeepLearning4j library in Java. [DeepLearning4J](https://deeplearning4j.org/) is a java based library maintained by Eclipse foundation used primarily for deep learning tasks. The architecture of the library is very similar to Keras. Therefore the coding style will be similar. 


### Prerequisites

Before running the code, you must have the following packages installed on your computer:

```
java 8
maven
python 3.x
pip
```

### TASK 1

A step by step instruction is given in the following

* Step 1: Use any editor to import the java project. I will recommend [IntelliJ](https://www.jetbrains.com/idea/) editor. To import the project, click File-> Open. In the pop up dialogue, choose the [pom.xml](pom.xml) file and click open. Another pop up window will appear and choose open as project option.
  IntelliJ will open the project as maven project and install all the dependencies automatically.
  
*  Step 2: 
    ```
    Open src/main/java/config/Config.java
    change the following global variable
    public static final String LOG_PATH = ROOT_PATH+"cms500_codeparser.log";
    ```
    Put your NSID in the logfile name. Otherwise, you will not get any marks.

* Step 3: If any .log file exit, delete them.

* Step 4: 
    ```
    Open src/main/java/extraction/MethodCallCollector.java
    Run the main function
    ```
    If the main method is run properly, you will see 10 CSV files is written in "./data/dataset/" folder. Moreover **your_nsid_codeparser.log** will be created. It will store all log statements regarding code extraction.


* Step 5: Now, you need to run the machine learning code written in python. To do that go to [Scripts](scripts) folder and open the [README.MD](scripts/README.MD) file. All instructions of running the machine learning code are given there. Follow them and you will able to run the machine learning code.
  After the successful run, you will be done with the Task 1. 

### TASK 2
Task 2 is more like building an LSTM based neural network instead of RNN. 
Before doing any change in the machine learning part, update the following global variable:
```
log_file_path = root_folder+'your_nsid_keras_rnn.log'
to
log_file_path = root_folder+'your_nsid_keras_lstm.log'
```

Next, you can follow the following steps to complete the task:

* Understand the code: First, you need to understand how the current machine learning code is working. I tried to write the code as readable as I can. Moreover, the code is also checked by some experts and revised. So I hope, you will not find any difficulty to understand it.

* Concept location: Next, try to find the location of the code where the change is required to fulfill the task. You might need to do some online search about how LSTM is implemented through Keras. Since Keras is a very popular framework in the machine learning community, you will find a lot of discussion, blogs, tutorial and so on. Then detect the area where you need to change.

* Impact analysis: Before changing the code, try to find the code where the change will be impacted. The impacts are but not limited to parameters, data types of the contexts and labels, any functions and so on. Hint: think simple and straight.

* Update: Finally, update the code and run it. If you find any error solve it because once you are able to run the RNN code, I am not going to touch your code. It is your responsibility to make the code runnable. 

After the successful run, you will find **your_nsid_keras_lstm.log** file in the project directory. It will keep all the log statements along with the accuracy of the model.

### TASK 3
This is a bit tricky because you need to learn how DeepLearning4J works. However, the working mechanism of Keras and deeplearning4j are almost the same. 

However, if you understand the machine learning code, you will find the following five sections there:
1. Data Collection
2. Data Prepossessing
3. Neural Network Configuration
4. Training
5. Testing

DeepLearning4j will come to the play from third. Before that, you need to do the data collection and prepossessing. You should do these two steps by yourself.

For neural network configuration, training and testing you can look at the following code examples: 

[RNN Example using DeepLearning4j](https://github.com/khaledkucse/methodRec/blob/master/src/main/java/Classification.java)

[Another Example](http://github.com/eclipse/deeplearning4j-examples/blob/master/dl4j-examples/src/main/java/org/deeplearning4j/examples/recurrent/basic/BasicRNNExample.java)

DeepLearning4j is created based on the concept of Keras library. Therefore, you just need to relate the code I provided for Keras and the above code examples. 

First, try for yourself. If you fail then come to me. I will not help you if you don't anything.

Hint: In the [pom.xml](pom.xml) file, I included all the libraries required for the machine learning code in Java. Therefore, you can use the current project for writing machine learning code or you can create a new maven project.


One last thing: You need to create a log file for the machine learning task. You can see how I have done logging while parsing the code and follow that. But your completion of Task 3 will depends on whether you provide a log file or not.
Therefore, after a successful run of your machine learning code, **your_nsid_deeplearning4j_rnn/lstm.log** file needs to be generated.

### What to hand in
1. your_nsid_codeparser.log

2. For each of the task provide the following three files:
    * Zip file of the full project
    * your_nsid_keras/deeplearning4j_rnn/lstm.log


3. Lastly one file name as README.txt file that will have the followings:
    * Status of all three tasks.
    * How to run each of your project(s): requirements, steps to run
    * Changes in python script for completing task 2. 
    * Overall what you learn from the assignment out of 10 in three categories: 1. Usability(10 as in very useful, 0 as in not required for future), 2. Complexity(10 as in very hard, 0 as in very easy), 3. New learning(10 as in everything were new, 0 as in nothing learned)
    * Any additional comment.
Your assessment will not be considered for marking and will be helpful for the future.


### Marking
1. Dataset Creation: 5 (will be considered as complete if your_nsid_codeparser.log file is provided with all log statements)
2. Task 1: 10 (will be considered as complete if your_nsid_keras_rnn.log file and the zip file of the project are provided)
3. Task 2: 20 (will be considered as complete if your_nsid_keras_lstm.log file, the zip file of the project and the README.txt file are provided. For task 2, the main important line in README.txt is "4. Changes in python script for completing task 2.")
4. Task 3: 40 (will be considered as complete if your_nsid_deeplearning4j_rnn/lstm.log file and the zip file of the project are provided)
5. README.txt: 5 (will be considered as complete if the descriptions of first two points are provided and Task 1 is complete. Even if you write you cant finish Task 2 or 3, you will get full marks for README.txt file)


Total Marks: 80

### Issues

If  you have any problem with the code provided in the repository. Please create an issue. I will try to solve it as soon as possible.

## Authors

* **C M Khaled Saifullah** - *Initial work* - [khaledkucse](https://github.com/khaledkucse)

See also the list of [contributors](https://github.com/khaledkucse/CMPT470-816AssignmentMachineLenaring/graphs/contributors) who participated in this project.

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details


