# Project Title - Crypto Investments

## Introduction
As a financial advisor to the top financial companies, the primary objective of our team is to employ unsupervised machine learning in order to seek out the optimal performances of crypto financial investment portfolios.   

## Technologies
**Python Libraries**

`python 3.9.12`<br>
`pandas 1.4.2`<br>
`Path`<br>
`hvplot 0.73`<br>
`scikit-learn 1.0.2`

## Installation Guide

[Install Anaconda](https://www.anaconda.com/download/)

To clone and run this application, you'll need Git installed on your computer.
From your command line:
```
#Create a new conda environment
conda create -n dev python=3.7 anaconda

#Activate the new environment with the following command
conda activate dev

# Install dependencies in the new conda environment
pip install jupyter lab
pip install -U scikit-learn
conda install -c pyviz hvplot

# Clone this repository on your local machine
git clone https://github.com/AlexanderValenzuela/crypto_investments

# Activate conda environment
conda activate dev

# In the conda environment, run Jupyter Lab
jupyter lab 

# Browse to the crypto_investments directory and launch `crypto_investments.ipynb`
```
---

## Usage

The steps for this challenge are broken out into the following sections:

1.) Import the the CSV file, `crypto_market_data.csv`<br>

2.) Prepare the Data - Use `StandardScaler` and the `fit_transform` function to scale and normalize the DataFrame columns.<br>

3.) Find the Best Value for k Using the Original Data<br>
a.)Use the `Elbow Method`.<br>
b.)Plot the `Elbow Curve`.<br>
![Screenshot 2023-05-22 at 3 11 18 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/0cce3f83-5d44-4f1a-88eb-589f1bbf3bbd)

4.) Cluster Cryptocurrencies with K-means Using the Original Data<br>
a.)Initialize the K-Means model.<br> 
b.)Fit the K-Means model.<br> 
c.)Predict the clusters and view the array of cluster values.<br> 
d.)Copy the original dataframe.<br> 
e.)Add a new column to the DataFrame for the predicted clusters.<br>
f.)Create a scatter plot.<br>
![Screenshot 2023-05-22 at 3 23 35 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/7d68e830-540c-496f-a896-f5cd4e8fd7a1)

5.) Optimize Clusters with Principal Component Analysis<br>
a.)Create a PCA model.<br>
b.)use `fit_transform` to reduce the number features.<br>
c.)retrieve the explained variance.<br>
d.)create a new dataframe with the PCA data.<br> 
e.)copy the crypto names and set that column as the index.<br>
![Screenshot 2023-05-22 at 3 30 58 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/fd19cc9c-b55a-4f5a-852c-fb2f6ae7736d)

6.) Find the Best Value for k Using the PCA Data<br>
a.)Create a list for the k-values.<br>
b.)Create an empty list to store the k-values.<br>
c.)Create a loop to compute the inertia with each possible value of k and view the inertia list.<br>
d.)Create a dictionary of the inertia list and then create the DataFrame for the `Elbow Curve`.<br>
e.)Plot the `Elbow Curve`.<br>
![Screenshot 2023-05-22 at 3 58 08 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/15f74f8c-1ace-49fd-a85b-16e7685727d6)

7.) Cluster the Cryptocurrencies with K-means Using the PCA Data<br>
a.)Initialize the K-Means model.<br> 
b.)Fit the K-Means model.<br> 
c.)Predict the clusters and view the array of cluster values.<br> 
![Screenshot 2023-05-22 at 4 02 43 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/dbf68f1e-021d-41fb-9035-2d38deea48e1)<br>
d.)Copy the DataFrame with the PCA data.<br> 
e.)Add a new column, Customer Segment, to the DataFrame for the predicted clusters.<br>
![Screenshot 2023-05-22 at 4 03 58 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/50873145-3fca-4261-a9a3-a6cc7a28aafc)<br>
f.)Create a scatter plot.<br>
![Screenshot 2023-05-22 at 4 05 07 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/5619393d-9f55-4994-b7fb-d465332e6600)

8.) Visualize and Compare the Results<br>
a.) Create a composite plot using hvPlot and the plus (+) operator to contrast the Elbow Curve that you created to find the best value for k with the original and the PCA data.
![Screenshot 2023-05-22 at 4 10 28 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/af2bba9f-c171-43a7-8934-9b06549a52c3)
b.) Create a composite plot using hvPlot and the plus (+) operator to contrast the cryptocurrencies clusters using the original and the PCA data.
![Screenshot 2023-05-22 at 4 10 44 PM](https://github.com/AlexanderValenzuela/crypto_investments/assets/111409358/6c8ef20b-564d-42fe-9a3a-e50a13111925)

## Contributors
- Firas Obeid, UC Berkeley FinTech Instructor
[GitHub](<https://github.com/firobeid>)
- Lucas Manning, UC Berkeley FinTech Tutoring Team
[LinkedIn Profile](<https://www.linkedin.com/in/lucas-manning-b44760206/>)
- Dylan Johnston, UC Berkeley FinTech Classmate
[GitHub](<https://github.com/djohnst914>)
- Alexander Valenzuela<br>
[LinkedIn Profile](<https://www.linkedin.com/in/alex-valenzuela-97826842/>)


## License
Licensed under the MIT License

