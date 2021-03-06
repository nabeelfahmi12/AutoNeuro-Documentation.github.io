## **_Data Ingestion_**


**Data ingestion** is the transportation of data from assorted sources to a storage medium where it can be accessed, used, and and analyzed by the application.
    
![tsd](../img/image003.png)

 

upload file formats allowed    |   
------------------------ |
csv files|
Excel file(xlsx) |
HTML|
JSON|
txt files|
MongoDB |
MySql |


## Methods to upload Data


### Read from CSV
Method Name    |read_data_from_csv|   |
------------ | ------------- | -----|
| | Method Description |This method will be used to read data from a csv file or a flat file
 | |Input parameter  names |self,file_name, header,names, use_cols, separator 
 | |Input Parameter Description|   file_name: name of the file to be read header: Row number(s) to be used as column names names : array-like, optional List of column names to use. If file contains no header row, then you should explicitly pass ``header=None``. Use_cols:  To load a subset of columns Separator: Delimiter to use 
 | |ouptput    |A pandas Dataframe 
 | |On Exception|  Write the exception in the log file. Raise an exception with the appropriate error message 

### Read from Excel
Method Name    |read_data_from_excel  | |
------------ | ------------- | ---|
| |Method Description| This method will be used to read data from an MS Excel File
| |Input parameter  names| self,file_name,sheet_name, header,names, use_cols, separator
| |    Input Parameter Description    |file_name: name of the file to be read sheet_name: Lists of strings/integers are used to request multiple sheets. Specify None to get all sheets. header: Row number(s) to be used as column names names : array-like, optional List of column names to use. If file contains no header row, then you should explicitly pass ``header=None``. Use_cols:  To load a subset of columns Separator: Delimiter to use
| | ouptput    |A pandas Dataframe
| |On Exception    |Write the exception in the log file. Raise an exception with the appropriate error message

### Read from HTML
Method Name    |read_data_from_html | |
------------ | ------------- | -----|
| |Method Description  |This method will be used to read data from an HTML web page Input parameter  names    self,url
| |Input Parameter Description|    url: URL of the HTML page to be read. 
| |ouptput |A pandas Dataframe
| |On Exception    |Write the exception in the log file. Raise an exception with the appropriate error message


### Read from JSON
Method Name  |   read_data_from_json|  |
------------ | ------------- | -----|
| |Method Description  |This method will be used to read data from a json file.
| |Input parameter  names| self,file_name
| |Input Parameter Description |file_name: name of the file to be read
| |ouptput|    A pandas Dataframe
| |On Exception| Write the exception in the log file. Raise an exception with the appropriate error message


### Read from text
Method Name    |read_data_from_text|   |
------------ | ------------- | -----|
| | Method Description |This method will be used to read data from a text file.
 | |Input parameter  names |self,file_name, delimiter
 | |Input Parameter Description|   file_name: name of the file to be read header: Row number(s) to be used as column names names : array-like, optional List of column names to use. If file contains no header row, then you should explicitly pass ``header=None``. Use_cols:  To load a subset of columns Separator: Delimiter to use 
 | |ouptput    |A pandas Dataframe 
 | |On Exception|  Write the exception in the log file. Raise an exception with the appropriate error message 


### Connecting to SQLDB
Method Name    |Connect_to_sqldb  | |
------------ | ------------- | -----|
| |Method Description| This method will be used to connect to a SQL Databases
| |Input parameter  names| self,host,port, username, password
   | |Input Parameter Description|    host: the server hostname/IP where the DB server is hosted Port: the port at which the DB Server is running username: The username to connect to the DB server password: The password to connect to the DB server
| |ouptput|    A DB connection object
| |    On Exception   |Write the exception in the log file. Raise an exception with the appropriate error message


### Read from SQLDB
Method Name    |read_data_from_sqldb| |
------------ | ------------- | -----|
| |Method Description  |This method will be used to read data from SQL Databases
| |Input parameter  names  |self,db_name,host,port, username, password, schema_name,query_string
   | |Input Parameter Description|    db_name: For example, SQL, MySQL, SQLLite etc. host: the server hostname/IP where the DB server is hosted Port: the port at which the DB Server is running username: The username to connect to the DB server password: The password to connect to the DB server schema_name: The name of the DB schema the user wants to connect to. query_string: the query to be executed to load the data
| |ouptput |A Pandas Dataframe
| |    On Exception   |Write the exception in the log file. Raise an exception with the appropriate error message 

### Read from MONGODB
Method Name    |read_data_from_mongdb  | |
------------ | ------------- | -----|
| |Method Description| This method will be used to read data from Mongo DB
| |Input parameter  names  |self,host,port, username, password, db_name,collection_name, query_string. Input Parameter Description    |host: the server hostname/IP where the DB server is hosted Port: the port at which the DB Server is running username: The username to connect to the DB server password: The password to connect to the DB server db_name: The name of the database collection_name: The name of the collection the user wants to connect to. query_string: the query to be executed to load the data
   | |output| A Pandas Dataframe
   | |On Exception    |Write the exception in the log file. Raise an exception with the appropriate error message


## Exceptions Scenarios

|Step  |Exception |Mitigation|
--------|----------|----|
User gives Wrong Data Source|  Give proper error message| Ask the user to re-enter the details
User gives corrupted data |    Give proper error message  



