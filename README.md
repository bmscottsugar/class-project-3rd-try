# class-project-3rd-try
Project Title: Autism Prevalence vs Country Population

Class project for Code KY/Louisville Class: My goal is to compare population sizes of various countries with their related rate of autism, per capita, respectively. From kaggle.com , I was able to locate a study that lists the countries, in order that have the highest prevalence of autism, per 10K people. By combing this data with a file I created using the population (using worldbankdata.com) of the countries listed in the first study, I am able to compare the two sets of data. I theorize that the larger the population, the higher the rate of autism (per 10K) will be. Possible causes may include such things as over population, pollution, etc..  If the graph and data show an increased prevalence of autism correlates with larger population,  I would suggest future studies to determine the potential cauases of the increased rate of autism in countries with larger populations, ie) over population, increased pollution, higher vaccination rates, genetically modified food/organisms, etc..


File to be downloaded from github.com to be viewed in Jupyter notebook: https://github.com/bmscottsugar/class-project-3rd-try/commit/e00942e628fe09a7f42c5c9b65a645316a5467d0



Relevant packages that need to be installed to run the project:


* [Python 3.0 or higher](https://www.python.org)
* [Jupyter Notebook](https://jupyter.org)
* [pandas](https://pandas.pydata.org/pandas-docs/stable/index.html)
* [NumPy](https://numpy.org/doc/)
* [Matplotlib](https://matplotlib.org)

To install these with PIP, install the following:

pip install notebook
pip install pandas
pip install numpy
python -m pip install -U pip
python -m pip install -U matplotlib

To run the this program in a Jupyter Notebook:


1. Clone the repository on git hub. 
2. Save this repository on your local machine, in a new folder. 
3. Open Jupyter notebook from command line or from Anaconda.
4. From home page of Jupyter, click "upload"
5. Navigate to the location where you save the cloned repo from step 2. 
6. Click on File named "Autism prevalance vs country population.ipynb". 
7. Click on "Run", the scroll down and select  "Run All"


Requirements met for Code Louisville:

1. Create a dictionary or list, populate it with several values, retrieve at least one value, and use it in your program.
Created CSV file(Corresponding Country Population 2020 CSV) using Google Sheets that listed the countries listed in the study "Autism by Country 2022 CSV" that was downloaded from Kaggle.com. The data  for the populations of the corresponding countries CSV file was downloaded and created via the website: worldbankgroup.org where a folder was created in which, the population of each country, in order corresponding order of the Autism by Country,  was created. 

1. Read in data from a local csv, excel file, json, or any other file type. There are many ways to do this, but using Pandas read_ functions is pretty easy

Used Pandas in Jupyter to read in several files, including : 'Autism Prevalence & Population 2020 combined CSV _4 - Autism by Country 2022.csv'. Also, read in the individual CSV files that were used to create "Autism Prevalence & Population 2020 combined CSV _4 - Autism by Country 2022.csv"

2. Manipulate and clean your data:

Used the following to better visualize all data in all CSV files:
pd.set_option('display.max_rows', 500)
pd.set_option('display.max_columns', 500)
pd.set_option('display.width', 1000)

Also, used the following in order to convert data into same format (int and float):

Autism_by_country_and_population['2020 Country Population'] = pd.to_numeric(Autism_by_country_and_population['2020 Country Population'], downcast='float')

3. 
Analyze your data! This is usually the more fun part and probably has more approaches than I can write here.
Used the following built in functions to analyze data.
 a.  len(Country_Population) - -used twice
 b. type(Autism_by_country_and_population)
 c. Autism_by_country_and_population["2020 Country Population"].mean()calculated twice. Once for each column of data used

 d. Autism_by_country_and_population['prevalencePer10K'].median() calculated twice. Once for each column of data used
 e. Printed Top 4 rows and all columns using "data_top = Autism_by_country_and_population.head()


 4. Visualize your data. The standard choice here is just making a couple visualizations then interpreting them to say something about your data.

 a. created 3 graphs (plot, scatter and line) using plt and plot methods. In line graph, increased the y limit using:
"Autism_by_country_and_population.plot(ylim=(0,200))"

5. Used markdown in Jupyter file to explain methods used and why they were used. Also, listed theory and hypothesis in README.md file. 

In Conclusion, the graphs that were created from the data obtained and merged into one document did not show the correlation that I expected to see. However, 
I do believe that this too, is useful as it may help determine what factors may lead to an increased (ie, lack of vaccines, limited access to medical providers, etc..) or decreased prevalence (ie, access to vaccinations,  better diet, etc.) of autism in our society. 

