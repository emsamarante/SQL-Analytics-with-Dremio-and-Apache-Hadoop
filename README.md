# SQL Analytic wit Dremio and Apache Hadoop
**This project is a data archictect project using the Dremio to analyze data with SQL language. A Hadoop DataLake was set up to storage the datasets. The ratings dataset has over 20M of records.**
<br>
<br>
## Datasets source

MovieLens 20M movie ratings. Stable benchmark dataset. 20 million ratings and 465,000 tag applications applied to 27,000 movies by 138,000 users. Includes tag genome data with 12 million relevance scores across 1,100 tags.
To more details of the datasets, please check out this [link](https://files.grouplens.org/datasets/movielens/ml-20m-README.html). 
The datasets of **MovieLens 20M Dataset** are available [here](https://grouplens.org/datasets/movielens/).
<br>
<br>
## Tools:

To develop this project, a datalake was set up in single node using **Apache Hadoop** technology in Linux environment.
The picture below shows the datasets in a datalake folder:

![Figure 1: Files within in the datalake folder.](https://user-images.githubusercontent.com/45640708/208963018-583a7544-850b-4f8f-950a-d82489744919.png)

In order to do the analysis, a connection between the **Dremio** (in Docker) and Hadoop DataLake was stablished in localhost. The next picture shows the DataLake contents through the Dremio and its physical datasets. 

![Figure 2: Physical datasets.](https://user-images.githubusercontent.com/45640708/208965889-4048ef97-3122-489d-a96c-8f3a61a46f32.png)

The figures below depict the **metadados managment in Dremio** by _Tags_ and _Wiki documentation_.

![image](https://user-images.githubusercontent.com/45640708/208975145-ecc7446d-1cac-43e5-ac48-8f9ace232089.png)


![image](https://user-images.githubusercontent.com/45640708/208975224-00e69f38-94d2-41bc-ab8c-992f639791fe.png)
<br>
<br>
## Results:

In total, three queries were made to get some answers.

**To calculate the moving average over year of ratings to each movie**

![image](https://user-images.githubusercontent.com/45640708/208976890-79dc6209-f923-4703-92ff-e3deb9917820.png)

**From movies which were starred in 2006, which are the top five the most rated?**

![image](https://user-images.githubusercontent.com/45640708/208979483-0e1edcb3-4f7b-421b-bfec-3064f2bc01bd.png)

**Which are the title movies of romance and genre "Drama" which were rated as "Satisfied" in the 2003? Use theses ratings labels to rating scale:**

    * from 1 to 1.9 = Very Dissatisfied
    * from 2 to 2.9 = Dissatisfied
    * from 3 to 3.9 = Neutral
    * from 4 to 4.9 = Satisfied
    * rating equal to 5 = Very Satisfied

![image](https://user-images.githubusercontent.com/45640708/208978665-278aa12e-c18f-42d7-a5d2-d7716f728948.png)






