## Prequisites:
* Python 3

## Instruction to run on Jupyter notebook:

* Clone the repository 
* Download the dataset from drive : [Dataset](https://drive.google.com/uc?export=download&id=1YLTwJY8zvwMgJJ4YWhXkn-CXC2TlJ6zE)
* Unzip and place inside GalaChallenge folder.
* Open Terminal and navigate till the GalaChallenge folder. 
* Create virtual Directory inside Galachallenge folder  using following link : [Link](https://docs.python.org/3/tutorial/venv.html)
* Run following commands based on OS platform to activate the virtual directory:
    NOTE : change <vir_dir_name> with the virtual directory name given in above step.
    IOS/Linux : ```source <vir_dir_name>/bin/activate```
    Windows :```<vir_dir_name>\Scripts\activate.bat```
* Run the following command, in order to install all libraries needed to run jupyter notebook :
    ```pip install -r requirements.txt ```
* Run the following command to launch jupyter notebook : ```jupyter notebook```
* Jupyter Notebook will be launched on localhost:8888 in default browser.
 


## Approach followed:

* __Data Preprocessing__ - Data Augmentatiion is done as Overfitting generally occurs when there are a small number of training examples, one way to fix this problem is to augment the dataset so that it has a sufficient number of training examples. 

* __CNN with activation function , loss function, optimizer__ - Chose VGG16 predefined model for achieving higher accuracy, in addition with two sequential layers with relu and softmax as activation function. ReduceLROnPlateau function is used to reduce learning rate when a metric has stopped improving. Here metric selected is accuracy and optimizer selected is Adam.


* __Cross validation__ - With a small sample size like our current situation, it’s especially important to perform cross validation to get a better estimate on accuracy. 

* __Predicting Test data__ - After predicting across test data set of n (here n=4) probabalities are predicted. Max probability of each instance decides the resultant class.


