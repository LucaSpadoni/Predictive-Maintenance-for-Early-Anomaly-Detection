# 📊 predictive_maintenance 🛠️
<h2>A project for the Artificial Intelligence course part of the Master Degree in Computer Science at the University of Bologna.</h2>
<br>Specific analysis of the data collected by sensors of industrial machines for the development of a Machine Learning application which exploits the correlations between various features discovered in the dataset we used, in order to provide a sufficiently valid and correct prediction model regarding a probable failure of a machine.

<br>Dataset used: “AI4I Predictive Maintenance Dataset”.
<br>Link: https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset
<br>The version of the dataset we used can be found in this github repository under the name "predictive_maintenance.csv".

<br><h3>🎯 Objectives:</h3>
1. Refinement and pre-processing of the dataset used in order to keep the useful data for our purpose and discard everything else;
2. Exploratory Data Analysis (EDA), an in-depth study of the dataset aimed at discovering its main characteristics and searching for possible patterns, using statistical analysis tools;
3. Application of certain classification algorithms to see which one can do the job most accurately.

<h3>Example of dataset samples after pre-processing </h3>
For informations on the characteristics of the dataset please refer to the link at the top of the page.

![exampledataser](https://github.com/michele-abruzzese/predictive_maintenance/blob/main/img/esempio%20dataset.png)

<h3>EDA (Exploratory Data Analysis)</h3>
The output shows the type of failure and its absolute frequency. A quick glance at the table below immediately shows that the number of failures detected is extremely low compared to the cases labelled as "No Failure".

![frequency](https://github.com/michele-abruzzese/predictive_maintenance/blob/main/img/frequenza.png)

<h3>Correlation matrixes </h3>
In the first picture, we can observe the correlation between the various features, while in the second one the correlation between the various types of failure. Analysing them, we can see for example a significant positive correlation of 0.88 between air temperature and process temperature, while there is a significant negative correlation of -0.88 between rotation speed and torque.

![correlation](https://github.com/michele-abruzzese/predictive_maintenance/blob/main/img/correlazione1.png)
![correlation](https://github.com/michele-abruzzese/predictive_maintenance/blob/main/img/correlazione2.png)


<h3>Data visualization </h3>
An imbalance was found in the dataset as the number of machine failures were found to be 3.39%.

![sbilanciamento](https://github.com/michele-abruzzese/predictive_maintenance/blob/main/img/sbilanciamento.png)
![failures](https://github.com/LucaSpadoni/predictive_maintenance/blob/main/img/fallimenti.png)

<h3>Classification models used</h3>

- Logistic regression
- KNN
- Support Vector Machine
- Random Forest
- Ada Boost
- XG Boost
- Naive Bayes
- Decision Tree Classifier
- Multi Layer Perceptron

<h3>Comparison of different configurations and solutions</h3>
The parameters used to evaluate the model are accuracy and total running time, although the latter turns out to be quite irrelevant for ranking them. As can be seen from the image below, all the algorithms applied to the designated model turn out to have a more than remarkable accuracy, being for all of them between 96% and 98%. What varies considerably however is the execution time, ranging from the order of thousandths of a second for Naive Bayes to almost 10 seconds for the Multi Layer Perceptron. In retrospective, another parameter we could have used is recall since it tells more useful informations about the classification model rather than running time (and perhaps accuracy).

![results](https://github.com/michele-abruzzese/predictive_maintenance/blob/main/img/results.png)

The 'XGB Classifier' algorithm returned an accuracy of 98% and an execution time of 0.4/0.5s. For a more in-depth study, we show below the scores XGB returned on the classification of records on the target attributes (precision, recall, f-1 score and support).

![xgb](https://github.com/michele-abruzzese/predictive_maintenance/blob/main/img/xgb.png)
