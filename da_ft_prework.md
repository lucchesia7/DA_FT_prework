# **Coding Temple's Data Analytics Program PreWork**
---
## **Getting Started**
---
Before you begin the exercises, please ensure the following:

- You have created an account with [Kaggle](https://www.kaggle.com/), [Tableau](https://public.tableau.com/app/discover), [GitHub](https://github.com/)

- You have downloaded [MySQL Installer](https://dev.mysql.com/downloads/windows/installer/8.0.html), [pgadmin4](https://www.pgadmin.org/download/), [R](https://cran.r-project.org/mirrors.html), [R Studio](https://posit.co/download/rstudio-desktop/), [Tableau Public](https://public.tableau.com/app/discover), and [GitHub Desktop](https://desktop.github.com/)

- You have access to Microsoft Excel, whether [locally](https://www.microsoft.com/en-us/microsoft-365/p/excel/CFQ7TTC0HR4R?ef_id=_k_6c21ac55d67a147acce5c81734cef983_k_&OCID=AIDcmm409lj8ne_SEM__k_6c21ac55d67a147acce5c81734cef983_k_&msclkid=6c21ac55d67a147acce5c81734cef983&activetab=pivot:overviewtab) or [online](https://www.office.com/launch/excel?ui=en-US&rs=US&auth=1). Excel requires a subscription on your local machine, but offers a free month trial! Online, access to Excel is free.

- You have created a GitHub Repository for all your precourse work to go into.
## **Excel**
---
### Walk-Through

Excel can be used to load in data from a lot of different sources and makes doing so very easy and intuitive. After launching Excel, we are greeted by the `Home` screen. In this screen, we will see three different panes off to the left hand side. `Home`, `New`, and `Open`. 

Once we select the open button, we will want to click on `Browse` option and select the file we want to open in Excel.

With csv files, Excel will infer the format it imports in. You can verify that the data has been loaded correctly by seeing the column names in the top row followed by data in each other row. Each row should have a value and each column should be a variable.


### **Exercises**
- Complete the following exercises in an `.xlsx` file. 
- Upload the file to github.com and submit the link to the Git Repository to the Google Classroom Assignment.

#### **Exercise 1**:

Using Excel, load in the dataset located [here](https://www.kaggle.com/datasets/takahirokubo0/annual-financial-data-for-hybrid-cdp-kpi).


#### **Exercise 2**:

Create a bar chart of the `Fiscal Year` and `Revenue` columns.

## **MySQL**
---
### **Walk-Through**

#### **Create a Database**
After installation of MySQL, we can open the Workbench, our GUI (Graphic User Interface) for MySQL operations. When opened, we are greeted by the MySQL welcome screen. Don't worry too much about the GUI yet, we will be covering over it in class. 

On the screen in bold letters is MySQL Connections. Next to this, is a small `+` button. This is how we will set up our new connection. Once we click on this, we will focus on the `Stored Connection` and the `Test Connection` variables. Click on `Connection Name` and name your connection `test`. After that, click on the `Test Connection` button to verify that you have a connection to your database you are trying to create. In the event that the connection fails, you may want to double check your firewall or antivirus. You may also need to open the port on your computer to accept connections!

Once we test the connection and have verified that it works, click the `OK` button to create your first database. Then we can click on the connection name and open our database.

#### **Create a Table**

Structured Query Language(SQL) is how we interact with a MySQL database. 

To create a table, we specify use SQL keywords `CREATE` and `TABLE`, giving a table name and the names of columns we wish to add to the table. 

For example:
```
CREATE TABLE IF NOT EXISTS <table_name>(
    id INT,
    product VARCHAR(50),
    quantity INT,

)
```
You can read more about creating a table in SQL [here](https://www.w3schools.com/mysql/mysql_create_table.asp). 

#### **Inserting Data**
Now that we have created a table, we will need to add data to it. This is done in SQL using the `INSERT` keyword. 

For example:

```
INSERT INTO <table_name>
VALUES(
    value1,
    value2,
    value3
)
```

For more on how to utilize the INSERT statement in MySQL, check out [this](https://www.w3schools.com/mysql/mysql_insert.asp) resource.

#### Querying Data
Now that we have a table and data inside that table, what if I wanted to view my data? This is where queries come in. Queries are how we access and return data from a table. A query utilizes the SQL keyword `SELECT`.

For example:
```
SELECT * FROM <table_name>
```
`*` in SQL means everything, so when this query is run, we should be returned all the data available within our table!

### **Exercises**
- Complete the following exercises in MySQL
- Save your code for all exercises to a single .sql file and upload the file to GitHub.

#### **Exercise 1:**
Create a table in MySQL named `customers`. This table should include three columns:

- cust_id
- cust_name
- address


#### **Exercise 2:**
Insert 3 rows of data into your table. You are free to write the data to be whatever you would like to insert into the table you created above. 

#### **Exercise 3:**
Query all the data in your database

## **R**
---
### **Walk-Through**
After installing R and R Studio, we will launch R Studio. R Studio has a lot in it's GUI, all which we will be covering during the course. Today, we will focus on the `new file` button, located in the top left corner of R Studio. We will click on this button and create a new R Script. Now that we have a new file, we can begin to work with R!

#### **Variable Assignment**
Once you have your new file open in front of you, we will begin with variable assignment. In R, variable assignment uses `<-` to assign a variable name to a value. 

For example, let's say I wanted to create a variable `x` and save the value `3` to it:

```
x <- 3
```
What if I wanted to create two character strings and save them to the variables `my_first_name` and `my_last_name`?

```
my_first_name <- "Alex"
my_last_name <- "Lucchesi"
```
Now that I have both these names, how can I change it into a single name instead? In R, we would utilize the `paste` function. `paste` concatenates values given, separating them by a `sep` argument. 

For Example:

```
my_full_name <- paste(my_first_name, my_last_name, sep = ' ')
```
#### **Vectors**
In R, we will work a lot with vectors. A vector is like a list in Python, but it can only hold a single type of data. Vectors are highly functional and very important in Data Analysis.

To create a vector, we use the `c()` function in R, passing in the values we wish to assign to our vector.

For example:
```
my_vec <- c(1,2,3,4,5,6,7,8,9)
```

Numerical vectors support element-wise operations, meaning we can add, subtract, multiply, and divide vectors across each item in each vector. 

For example:

```
my_vec2 <- c(9,8,7,6,5,4,3,2,1)

my_added_vec <- my_vec + my_vec2
```
### **Exercises**
- Complete the following exercises in an `.r` file. 
- Upload the file to github.com and submit the link to the Git Repository to the Google Classroom Assignment.

#### **Exercise 1:**
Create three variables; x, y, and z. Assign each of these variables a numerical value, then perform each of the operands you have learned about so far to all three variables.


#### **Exercise 2:**

Create two strings with your first and last name, respectively. Then concatenate them, and print the new value as "My name is `your newly created concatenated variable will go here`".

#### **Exercise 3:**

Create two numerical vectors of equal length. Multiply these vectors together and save the resulting vector to the variable `mult_vect`.