# # My Eighth Code Review: Data Modeling

## Alex Wallace

## Description
For this project, I was tasked to create a new dataset in bigquery called 'air_travel', and create numerous tables within that dataset. I had to create three dimension tables: 'airlines', 'airports' and 'passengers'. The 'passengers' table had to be classified as SCD Type II. I also had to create a fact table called 'tickets'. I created the dataset and all of the tables using an ETL pipeline I created in python. The ERD for the dataset looks like this:

![Image](./img/air_travel_erd.png)

The pipeline can be found in the jupyter notebook here [ETL pipeline]. I plan on creating a main.py file with the whole pipeline that anyone can access and use, but haven't done that yet. 

The 'tickets' fact table is linked to each dimension table via:

-UUID for the 'passengers' dimension
-airline iata code for the 'airlines' dimension
-airport iata code for the 'airports' dimension

I had to use a lookup to link the 'tickets' fact table to the 'passengers' type II dimension. This is also done in the ETL pipeline created. I finished the project by establishing the primary keys for each table in SQL. 
 
## Setup/Installation Requirements
In order to set this up, you will need to make a directory for your file and then switch over to that directory. Then, create a virtual environment for python 3 to work in. Change into your virtual environment using source venv/bin/activate. You will need to install the requirements.txt file (pip install -r requirements.txt).

You should be able to run the whole pipeline after installing these requirements. You can run the final SQL code in bigquery if you want to establish the primary keys.

## Known Bugs
No known bugs

## License
Copyright 2023 Alex Wallace

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.