# Project Explore Berkshire Data


## Project Description

This project includes reading and exploring the data without using pandas, numpy or any other advance library of data analysis.

Berkshire bike share data has been used for this project. Data has been included within the repository.


## Environment and Programming Language

* Python 2.7.14 has been used.
* Miniconda framework has been used which can be downloaded from this [link](https://repo.continuum.io/miniconda/).
* Once installed, open conda prompt.
* Create virtual environment by using `conda env create -f environment.yaml`. **environment.yaml** has been included in the repository.
* Jupyter notebook has been used for interactively analyzing and exploring the data.


## Data Description

* Data has been saved in `./jupyterwork/data/` directory.
* Data from 3 states of US (Chicago, NYC and Washington DC) has been given.
* Files are in CSV format.
* Original data is given in following links.
  * [Chicago](https://www.divvybikes.com/system-data)
  * [NYC](https://www.divvybikes.com/system-data)
  * [Washington, DC](https://www.capitalbikeshare.com/system-data)
* Data has already been collected for year 2016 and some data wrangling for inconsistent date format has already been and saved in previously mentioned link.


## Data Exploration steps

Data exploration consists of following steps.

1. **Data reading**

  First task is to read the data. For this **DictReader()** from **csv** library has been used.
  _Dictreader_ reads the file line by line. Function `print_first_point(filename)` takes the **filename** as input and **prints the first trip** from the file and also **returns city and first_trip**. This function split out the city name from the filename.

2. **Data Cleaning**

  Each city has different column names with different formats and extra information as well. Details of the same has been given in iPython Notebook. So we need to clean the data with uniform formatting across the cities and also extract out the information which is required for analysis.

  The helper functions `duration_in_mins(datum, city)`, `time_of_trip(datum, city)` and `type_of_user(datum, city)` were created and used in function `condense_data(in_file, out_file, city)` which is the main function to generate the cleaned and formatted data.

  Data after cleaning has been saved to the **Summary** files given in the data folder. **DictWriter()** from the **csv** library was used to write the cleaned data to the **Summary** files for each city.

3. 
