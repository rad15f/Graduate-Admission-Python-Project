# FINAL-PROJECT-GROUP4

## Steps to Run
1. Clone this repo
2. Install the necesary packages  (Check Requirements)
3. Open Code No GUI or Code PYQT5 for the Graphical User Interface
4. Run and Enjoy!


## Predictive Modeling using Regression Model for Change of Admission

The Main PYQT5.py shows graphics for an EDA Analysis, as well as the results of three machine learning algorithms based on the chance of admission data set. The research's aim is to build a regression model that best predicts the chance of admission for graduate students and obtain feature importance.

Code Order: The code is built from bottom to top for a more efficient GUI code readability. 

## Data set structure:

Independent Variable -- X  
GRE Score
TOEFL Score
SOP  (Statement of Purpose)
LOR (Letter of Recommendation)
CGPA(Cumulative GPA)
University Rating
Research 

Target/ Dependant Variable -- Y
Chance of Admission


## Machine Learning algorithms:

Decision Tree Regression
Random Tree Regression
Logistic Regression

## Requirements:
Before running this Main pyqt5.py file, you need the following installed on your python environment:

Pip install numpy

Pip install pandas

Pip install matplotlib

Pip install seaborn

Pip install scikit-learn

Pip install pydotplus*

Pip install kaggle*

https://graphviz.org/download/ install any version and replace the path to your path
Code No GUI (line 217) example: 'C:\\Program Files (x86)\\graphviz-2.38\\release\\bin' <- this is my path replace with yours
os.environ["PATH"] += os.pathsep + 'C:/Program Files (x86)/Graphviz/bin'  
Code PYQT5: If you have it installed in another path, change this path at the top of the Main.py file (line 52). Check Technical Consideration for further details


Note: Using Anaconda environment saves the stress of the above apart from those in asterisk and the link. The link above is an application which works with pydotplus to plot decision trees.


## Description of files:


Code PYQT5.py is the python file that contains all the code for the demo including the GUI.(GUI = Graphical user intertace/ Dashboard)

Code No GUi is the python file which contains all the code with more data visualization and more models but no GUI included.

Pty.png , enter.png, racoon.png are icons that are used in the menu items in the application.

All the files need to be located in the same directory

## Technical considerations:

Main is PYQ5 application, thus, pyq5 needs to be installed in the computer in order to execute this app.


The application also uses graphviz-2.38 but can use any version, to be user to have it installed in the computer

The directory that uses this application for graphviz-2.38 is:

'C:\\Program Files (x86)\\graphviz-2.38\\release\\bin'
If you have it installed in another path, change this path at the top of the Main.py file.

The application also uses a font_size_window = 'font-size:15px' at the top of the Main.py file, if you switch , it can be changed, just be sure to use the correct syntax for your stylesheet font size.

## Description of the application:

The purpose of the application is to present a basic EDA analysis of the processed dataset and three dashboards with the results of the algorithms where the user can manipulate the features and the test/train size of the model. The algorithms used are Logistic Regression, Random Forest Regression and Decision Tree Regression. These three models can be run separately, but Random Forest Regression and Logistic Regression complement each other since both give information that is relevant for making recommendations.

## The structure of the application is as follows

File
Exit : it quits the application
E.D.A Analysis
Distribution : This option presents a frequency histogram. It shows the distribution of ou Y variable (Change of Admission)
Features vs Admit Chance : This option presents a scatter plot that shows the relation of each feature in the datasets with Change of Admission. A line can be drawn optionally to represent the tendency of the data.
Heatmap : This option presents a correlation plot for all the features in the dataset. The features can be added or deleted from the plot. Each time that a modification is made the button Create Plot should be pressed.
Boxplot: This option shows a box plot which shows the range and possible outliers of the selected features




## Machine Learning MODELS

Cross Validation:
The dashboard for cross validation displays first hand test scores on the data set with several regression models. This gives us a view on what model works best for our data set.

Decision Tree Regression:
The dashboard shows the input section and output section for the decision tree regressor algorithm provided by sci-kit learn.
The features to be included in the algorithm are chosen. However, you can choose how many features by manipulating the checkboxes on the screen.
The application also presents the percentage of the data set used for training and the random state. These parameters can also be changed.
Click Execute DTR to populate the dashboard with the data.
You can execute the algorithms as many times as you wish. The dashboard will erase the previous results and present the new ones with a feature importance graph of the model.
To view the tree generated by the algorithm you will need to press the button View Tree. This button will open an additional window showing the pdf with the tree. This pdf is saved in the directory of your application with the name decision_tree_regressor.pdf

Random Forest Regression:
The dashboard shows the input section and output section for the Random Forest Regression algorithm provided by sci-kit learn.
The features to be included in the algorithm are checked. However, you can manipulate how many features by changing the checkboxes on the screen.
The application also presents the percentage of the data set used for training, N Estimators, min sample split, min sample leaf, max depth . These parameters can be changed, as well.
Once you are comfortable with the chosen features and parameters you can click Execute RF to populate the dashboard with the data.
You can execute the algorithms as many times as you wish. The dashboard will erase the previous results and present the new ones.

Linear Regression:

The dashboard shows the input section and output section for the linear regression algorithm provided by sci-kit learn.
The features to be included in the algorithm are chosen. However, you can choose how many features by manipulating the checkboxes on the screen.
The application also presents the percentage of the data set used for training and the random state. These parameters can also be changed.
Click Execute LR to populate the dashboard with the data.
You can execute the algorithms as many times as you wish. The dashboard will erase the previous results and present the new ones with a graph of the distribution of the Predict Values vs Actual Values. 
