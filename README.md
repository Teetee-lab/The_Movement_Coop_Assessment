# The_Movement_Coop_Assessment

## Below are my approaches in matching the input dataset with the county txt files:

- Created a data folder
- Downloaded each txt file and store them into the data folder
- Use pandas library to join, gather, normalize and retrieve the output.

### Process:
After reading each data into a dataframe, I had to concatenate all the files in order to have a master dataset. This result in a total of *8,042,945* rows and *117* columns. Then, I concatenate the firstname, middlename and lastname into one single column 'name' so that I can have similar records when I match the input data. Aside from that, I changed the date of birth column into python date format so that I can retrieve the year. Also, I change the residential zip from a float data type to int data type for similar data accross all records. Then I dropped the duplicate columns since I have new columns that stored the new data. After all the columns are dropped, I rename the relevant columns then move ahead and capitalize all the Initials of the 'name' , 'city' and 'address' so that I can normaize the strings.  
Finally, I read the input dataset into a dataframe, convert the zip from a float data type into int data type then save it into a new csv with name match_input. Then I finally use the pandas function .merge() to match the input dataset from the master dataset.

### Challenges:
At first I wanted to use a database to store my data but most of them required that I pay for GPU in order to host the dataset in the cloud since it is a large dataset. Also, I have so many runtime error while working on this data, which I overcame by being patiently waiting for the output. Aside from that it took several hours to work on this locally which is not advised.

### Next Steps:
Even though this is not the best option for matching the input data with the county dataset, In the future I plan to create a table in the database and host it using the cloud then use SQL join to merge all county dataset using their unique ids and then match the input data to get the output. 


