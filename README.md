<!-- hide -->
# Exploratory data analysis in Python - Step by step guide
<!-- endhide -->

- Download New York Airbnb data from Kaggle.com.
- Perform a complete EDA, including all steps of the process.
- Write down the conclusions of each step and analyze the results based on the relationships between the variables.

<how-to-start>
  
## 🌱 How to start this project

Follow the instructions below:

1. Create a new repository based on our [machine learning project](https://github.com/4GeeksAcademy/machine-learning-python-template/) or [by clicking here](https://github.com/4GeeksAcademy/machine-learning-python-template/generate).
2. Open the newly created repository in Codespace using the [Codespace button extension](https://docs.github.com/en/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace-for-a-repository).
3. Once the Codespace VSCode has finished opening, start your project by following the instructions below.

</how-to-start>

## 🚛 How to deliver this project

Once you have finished solving the exercises, be sure to commit your changes, push them to your repository, and go to 4Geeks.com to upload the repository link.

## 📝 Instructions

### Airbnb in New York

A company has collected New York housing rental data from the Airbnb app during 2019. This dataset was used to train Machine Learning models during that year, in an open competition.

We will now use it to conduct a study about the variables that make up the dataset in order to understand it and draw conclusions about it.

#### Step 1: Loading the dataset

You can download the dataset directly from Kaggle.com or from the following link: `https://raw.githubusercontent.com/4GeeksAcademy/data-preprocessing-project-tutorial/main/AB_NYC_2019.csv`. Store the raw data in the `./data/raw` folder.

#### Step 2: Perform a complete EDA

This step is vital to ensure that we keep the variables that are strictly necessary and eliminate those that are not relevant or do not provide information. Use the example Notebook we worked on and adapt it to this use case.

Be sure to conveniently divide the data set into `train` and `test` as we have seen in the lesson.

#### Step 3: Save the processed dataset

After the EDA you can save the data in the `./data/processed` folder. Make sure to add the data folder in the `.gitignore`. The data as well as the models should not be uploaded to git.

> Note: We also incorporated the solution samples on `./solution.ipynb` that we strongly suggest you only use if you are stuck for more than 30 min or if you have already finished and want to compare it with your approach.
