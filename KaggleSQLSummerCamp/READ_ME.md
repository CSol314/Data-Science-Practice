
## SQL Notes

* The most basic SQL query selects a single column from a single table. Specify the column you want after the word SELECT (or use * to select all columns), and then the table after the word FROM.

* WHERE is used to filter for certain conditions.

For example:  
```sql
SELECT Name  
FROM `bigquery-public-data.pets`  
WHERE Animal = 'Cat'  
```

* If you're not working in a program like Sequel Pro, you can:   
   * Create a client objective   
   * Constructe a reference to the dataset   
   * Use the reference to the dataset in list(client.list_tables(datasetRef))   
   * Use the reference to the dataset to get a refernce to the table   
   * Use the table reference to get access to the table object, then list the rows.  


* If we want to add queries, that requires some setup, such as:

```python
query_job = client.query(query)     
/# API request - run the query, and return a pandas DataFrame    
<name> = query_job.to_dataframe()   
````



* Triple quotation marks tell Python that everything inside them is a single string even though it has line breaks.


