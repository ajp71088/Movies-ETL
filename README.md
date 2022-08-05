# Movies-ETL

### Project Overview
Using Python to create an automated pipeline that will Extract, Transform, & Load data which builds a database of movies. Data is collected from multiple sources: Wikipedia, Kaggle, and MovieLens ratings. It is then read and transformed before being loaded into a PostgreSQL database.

#### Deliverable 1 - Write an ETL Function to Read Three Data Files
![image](https://user-images.githubusercontent.com/107162310/182993588-0439b43d-e0b6-40d9-9677-a8c689c0b3bc.png)
The function takes the JSON file, Kaggle metadata, and MovieLens ratings and turns them into dataframes.

![image](https://user-images.githubusercontent.com/107162310/182993748-85b99713-1830-4cf6-b2b7-e637c4aa1101.png)

![image](https://user-images.githubusercontent.com/107162310/182993772-2c801d48-ff95-464f-9e98-321dc137467a.png)

![image](https://user-images.githubusercontent.com/107162310/182993797-b58f9a12-a1df-478e-812b-fdd85c9fddc2.png)

#### Deliverable 2 - Extract and Transform the Wikipedia Data
The Wikipedia data is cleaned and prepped so that it can be merged with the Kaggle metadata. First the data is cleaned for movies only, and the columns are merged for easier use.

![image](https://user-images.githubusercontent.com/107162310/182994121-b2bd9448-5cde-406e-8d4e-a5d4a6846663.png)

The data is further cleaned based on a number of factors, using regular expression strings.

![image](https://user-images.githubusercontent.com/107162310/182994215-11285714-e7dd-4196-96cd-568f6b9d4fd1.png)

![image](https://user-images.githubusercontent.com/107162310/182994247-16200db5-4d59-4594-ba2c-5c68e5e33f5d.png)

![image](https://user-images.githubusercontent.com/107162310/182994355-d8a71d94-5b15-426f-acad-3ed2a26c9285.png)

The cleaned dataframe now awaits a clean Kaggle dataframe:

![image](https://user-images.githubusercontent.com/107162310/182994465-066f9a2b-824c-4582-9a00-000f9df0cfb4.png)

#### Deliverable 3 - Extract and Transform the Kaggle Data
Following a similar process, the Kaggle metadata and MovieLens ratings data are cleaned and turned into their own dataframes.

![image](https://user-images.githubusercontent.com/107162310/182994630-605ea5ab-a889-4a6c-a8d8-a54f4e7e2ab3.png)

![image](https://user-images.githubusercontent.com/107162310/182994669-116da56e-6b30-418c-aac4-76fa5f66a7de.png)

The Kaggle and Wikipedia dataframes are merged into the movies dataframe, and then the ratings data is cleaned and merged with the movies dataframe.

![image](https://user-images.githubusercontent.com/107162310/182994730-6bdc3da4-34e1-4aeb-b01c-0cde429c1fdc.png)

#### Deliverable 4 - Create the Movie Database
The function is created into a pipeline that loads the databases through this piece of code:

![image](https://user-images.githubusercontent.com/107162310/182995210-773d7a32-aa4b-4363-8f0f-d00c33b0e5da.png)

The process takes a bit of time...

![image](https://user-images.githubusercontent.com/107162310/182995340-4590a973-4040-4dc4-969e-1352da621c51.png)

But now the pipeline is ready to be used to maintain the continuously updating database.

#### Challenges
I was repeatedly thrown off course by the warnings seen in the last screenshot. I mistook them for errors and spent far too long repeating the challenge in different ways to get them to go away. 
