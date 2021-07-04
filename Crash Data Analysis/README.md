## Crash Data Analysis
### Project Overview
This projects aims to analysis vehicle crash data using PySpark. RDD, Dataframe, and Spark SQL were used and a comparision between 3 types of data process method were implemented.

Details of queries can be seen in following sections.

### Dataset Info
The data used here is the Road Crash Data from 2015-2019 for South Australia prepared by the Department of Planning, Transport and Infrastructure ( DPTI ) . The data is available on the website https://data.sa.gov.au .

The datasets contain various details about the crash events including the vehicle and the people involved in the crash. In this assignment, only two datasets i.e. Crash and Units are considered. For more detailed information on the dataset, please refer to the Metadata file included in the assignment dataset or from the given website .

Note: In the dataset, the exact day of the crash is not released by the data provider, being considered as sensitive information. When displaying dates, please use the format ( Year-Month-Dayofweek ) E.g.(2017-January-Sunday).

### Project Contents

#### RDD

**Data Preparation and Loading**

1. Write the code to create a SparkContext object using SparkSession, which tells Spark how to access a cluster. To create a SparkSession you first need to build a SparkConf object that contains information about your application. Give an appropriate name for your application and run Spark locally with as many working processors as logical cores on your machine .

2. Import all the “Units” csv files from 2015-2019 into a single RDD.

3. Import all the “Crashes” csv files from 2015-2019 into a single RDD.

4. For each Units and Crashes RDDs, remove the header rows and display the total count and first 10 records .

**Data Partitioning in RDD**

1. Analysis of numer of partitions the RDDs have, the default partition method of RDD. 

2. Manully set the partition strategy to keep all "SA-related data" in one partition and keeps other data in another partition.

   <p>2.1. Create a Key Value Pair RDD with Lic State as the key and rest of the other columns as value.</p>

   <p>2.2. Write the code to implement this partitioning in RDD using appropriate partitioning functions.</p>

   <p>2.3. Write the code to print the number of records in each partition. What does it
   tell about the data skewness?</p>

**RDD Queries**

1. Find the average age of male and female drivers separately.

2. What is the oldest and the newest vehicle year involved in the accident? Display the
Registration State, Year and Unit type of the vehicle.

#### DataFrames

**Data Preparation and Loading**

1. Load all units and crash data into two separate dataframes.

2. Display the schema of the final two dataframes.

**Query/Analysis**

1. Find all the crash events in Adelaide where the total number of casualties in the event
is more than 3.

2. Display 10 crash events with highest casualties .

3. Find the total number of fatalities for each crash type.

4. Find the total number of casualties for each suburb when the vehicle was driven by an
unlicensed driver. You are required to display the name of the suburb and the total number of casualties.

#### Severity Analysis
In this section, we wanted to analyze whether severity of accidents is higher when the driver is on drugs or alcohol compared to when the driver is normal. The severity of the crash is given by the column “CSEF Severity”, the three levels of severity is given below (also included in the
Metadata file). Similarly the columns “DUI Involved” and “Drugs Involved” tell whether the
driver has been detected with blood alcohol and drugs respectively.

**Queries include:**

1. Find the total number of crash events for each severity level. Which severity level is the
most common?

2. Compute the total number of crash events for each severity level and the percentage
for the four different scenarios.

#### Comparison between RDDs, DataFrame and Spark SQL
Implement the following queries using RDDs, DataFrames and SparkSQL separately. Log the
time taken for each query in each approach using the “%%time” built-in magic command in
Jupyter Notebook and discuss the performance difference of these 3 approaches.

1. Find the Date1 and Time of Crash, Number of Casualties in each unit and the Gender,
Age, License Type of the unit driver for the suburb "Adelaide".

2. Find the total number of casualties for each suburb when the vehicle was driven by an
unlicensed driver. You are required to display the name of the suburb and the total
number of casualties.

