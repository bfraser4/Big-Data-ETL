# Big Data ETL - Amazon Customer Reviews 

## Background
In this project, I will put my ETL skills to the test. Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. They are quite large and can exceed the capacity of local machines. One dataset alone contains over 1.5 million rows; with over 40 datasets, data analysis can be very demanding on the average local computer. My first goal will be to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance. My second goal will be to use PySpark or SQL to perform a statistical analysis of selected data. 

## Instructions
### Part 1 - Extract two Amazon customer review datasets, transform each dataset into four DataFrames, and load the DataFrames into an RDS instance.
1) Activate Spark, install params, and start a SparkSession.
![carbon (40)](https://user-images.githubusercontent.com/107604123/217335261-9636ed4a-7d4c-4b78-8913-4377be321b91.png)
![carbon (41)](https://user-images.githubusercontent.com/107604123/217335788-19adb0d1-206a-4ccb-b41a-6877b2ce6a34.png)

2) Explore the Amazon Reviews Links to an external site.datasets and pick two datasets to perform ETL.

3) Extract the Data
    - Read in each dataset using the correct header and sep parameters.
    ![carbon (38)](https://user-images.githubusercontent.com/107604123/217334705-a2b362ed-0349-4532-854d-d300a9bd5148.png)
    - Get the number of rows in the dataset.
    ![carbon (39)](https://user-images.githubusercontent.com/107604123/217334830-f177b857-5790-464d-9313-34ef34ded1ee.png) 

4) Transform the Data
![carbon (42)](https://user-images.githubusercontent.com/107604123/217336321-475d52bc-98df-4c56-b5ec-45fe87d6c220.png)
![carbon (43)](https://user-images.githubusercontent.com/107604123/217336443-02f4116a-b86a-4918-9226-2ebcdf6934f9.png)
![carbon (44)](https://user-images.githubusercontent.com/107604123/217336545-9b9d721e-db65-4466-b312-262ae7efcf4f.png)
![carbon (45)](https://user-images.githubusercontent.com/107604123/217336773-c2ac0338-aae1-483c-8863-2a805589822b.png)

5) Load the Data into an RDS Instance

6) Export each DataFrame into the RDS instance to create four tables for each dataset.
![carbon (46)](https://user-images.githubusercontent.com/107604123/217337044-4e89e258-b350-4b50-a9eb-6bdcaee52ed5.png)


### Part 2 - Extract two Amazon customer review datasets and use either SQL or PySpark to analyze whether reviews from Amazon's Vine program are trustworthy.
In Amazon's Vine program, reviewers receive free products in exchange for reviews. Amazon has several policies to reduce the bias of its Vine reviews 

But are Vine reviews truly trustworthy? Your task is to investigate whether Vine reviews are free of bias. Use either PySpark or, for an extra challenge, SQL to analyze the data.

If you choose SQL, first use Spark on Colab to extract and transform the data and then load it into a SQL table on your RDS account. Perform your analysis with SQL queries on RDS.

While there are no strict requirements for the analysis, consider steps you can take to reduce noisy data, such as filtering for reviews that meet a certain number of helpful votes, total votes, or both.

Submit a summary of your findings and analysis.

References
Amazon Customer Reviews Dataset. (n.d.). Retrieved April 08, 2021, from: https://s3.amazonaws.com/amazon-reviews-pds/readme.html
