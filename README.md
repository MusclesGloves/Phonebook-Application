# About the project

The PhoneBook Management System has been done using Microsoft Visual Studio with
the platform Windows and language Python. The Primary File used for the project
is 'data.csv'. The Project mainly focuses on the computation of the hash function on some
fields of a record. The output of the hash function defines the position of the block
where the records will be stored. Then various operations are displayed to the end user in
the form of the application, such as Add, Search, Delete, Update and View. The
inserted record will be initially packed and then will be put in the record file.
The File Structure method used here is Hashing File Organisation, where the data
record can be searched without using the index structure.




# Implementation

### About the techniques
The implementation of the entire process has been briefly described in
the following stages below.
Building a PhoneBook App requires us to create a CSV file as we are using
Python programming language.

### Building Block File
Block File (data.csv)
The Block file comprises of the primary key and it’s respective position in the
file. Here, the third column in the record file will be unique and it will be
considered as primary key column. Among the records, data-set used in
this project “Telephone” is the column which is unique. So it is being used as
primary key for the purpose of running various operations based on this
primary key like searching the record based on primary key, deleting the record
based on primary key and also modifying the records based on this primary
key.

![PrimaryFile](https://github.com/user-attachments/assets/8d2e5eea-0cb3-4d24-8b48-2c458426bc7f)

### ADDING THE RECORDS

The user is given with an option to insert the records into the Block file. Upon
execution of the insertion operation, hash function is used to generate a new
address of the Block in the Block file. This record will then be inserted into the
file directly. After insertion, the Block file is rebuilt once again. This insertion
operation is carried out by insert() method which reads all the required
fields,and then add() method packs all these data and then writes it to
corresponding files.

### SEARCHING THE RECORDS
The user can search a record from the Block file using the Hash key
columns. When a record is requested using the Hash key columns, an address is
generated from which, the required record can be obtained.
This search operation is carried out by to_search() method which searches all
the required fields and the search() method unpacks and displays the required
data to the user.

### DELETING AND UPDATING THE RECORDS

Just like Add and Search, Delete and Modify works in the same way, where, if the user
requests to delete a record, then an address is generated, from which the required record
can be deleted. Similarly, if the user wishes to update a record, an address is generated
from which the user can access and update the record by changing any of the fields of
the record.
Here, the to_update() and to_remove() methods will be utilized and the respective
remove() and update() methods carry out the required operation necessary to satisfy the
user.

### UNPACKING THE RECORDS
Unpacking is another operation which is used to display all the records present
in the Block file. This operation is carried out by show() method which ignores
the separator/delimiter (in this case “,”) and considers only the fields present in
the Block file to display. While displaying the records, if a record starts with an
asterisk(*) then that record will not be unpacked or displayed.

# Results and Snapshots

### App Screen :
![AppScreen](https://github.com/user-attachments/assets/356e51a8-bf39-43d1-9b91-3fd551f703c3)

### Inserting the record :
![Inserting_record](https://github.com/user-attachments/assets/f6a1f5aa-0c6b-4f13-87e7-c867fe125f21)

### Deleting the record : 
![Deleting_record](https://github.com/user-attachments/assets/31ae8ba6-fe7f-496c-86ad-b592b449cad6)

### Updating the record :
![Updating_record](https://github.com/user-attachments/assets/d29f4237-02e9-4a6f-ac69-ecfd4b4c8b6f)

### Searching a record :
![Searching](https://github.com/user-attachments/assets/82d2a73e-1d15-421f-a4ec-312cff369d56)



