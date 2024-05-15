# NamasteKart
This is part of Ankit Bansal's course Namaste Python (Zero to Hero). Below is the problem statement

Imagine there is a online mart called namasteMart operating in Bangalore and Mumbai. Everday all the transactions/orders files are generated and sent to you for validation.
you need to verify all the files and notify business in case of any issues.

create this folder structure
NamasteKart
NamasteKart->incoming_files
NamasteKart->success_files
NamasteKart->rejected_files

Read all the files from current date folder NamasteKart->incoming_files->YYYYMMDD

do the following validations for each order

1- product id should be present in product master table

2- total sales amount should be (product price from product master table * quantity)

3- the order date should not be in future

4- any field should not be empty

5- The orders should be from Mumbai or Bangalore only.



files with no issues should go to NamasteKart->success_files->YYYYMMDD folder

if any single orders validation fail then full file should be rejected and that files should go to NamasteKart->rejected_files->YYYYMMDD folder

for each rejected file there should be one more file created in the same folder NamasteKart->rejected_files->YYYYMMDD folder with name error_{rejected_file_name}.
In this file only order records should be there which failed the validation and there should be one more column for each record specifying the reason of rejection
if there are more than one reason of reject for a particular order then both should be there ; separated

after processing all the files there should be an email sent to business. In the email mention below details
total 10 incoming files , 8 successsful files and 2 rejected files for that day.
subject : validation email 2023-06-09

note if there are no incoming files for the day, the email should still go.
