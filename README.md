# BACKEND SKILLS ASSESSMENT PROJECT

For this task you will be creating a **Java application** that will expose an **Web API**. This application will take various input parameters and store data about transactions.

**It must be production quality according to your understanding of it: testing, readme.MD etc. We run on Unix environment, if there's no instruction how to run the code or/and it doesn't compile, it will NOT QUALIFY**

The application have to store data on the file system under the folder where the application is. So there is no need to use a database but if you feel that using a database can help your exercise, feel free to do so. We only ask you to not delegate any logic to the database like sum and others. We want to know your code.

The API should have the following features:

## ADD TRANSACTION
Receives <user_id> add <transaction_data> params.

This feature should add a transaction to the user specified in <user_id> using the information specified in <transaction_data>.  The transaction data should have the following data:


amount -> 1.23

description -> Joes Tacos

date -> 2018-12-30

user id -> 345


This command should return a version of the transaction added with a unique id for the transaction like this:


transaction_id -> 2299ce24-9eaf-417f-82d6-e57f93777dc4

amount -> 1.23

descrption -> Joes Tacos

date -> 2018-12-30

user_id -> 345


## SHOW TRANSACTION
Receives <user_id> <transaction_id> params.

This feature should return the transaction specified in the transaction_id. 

If the user_id is not the user_id that corresponds with the user_id for the specified transaction,  you should return _Transaction not found_. 

If the transaction does exists, you should print out the information for the transaction like this:


transaction_id -> 2299ce24-9eaf-417f-82d6-e57f93777dc4

amount -> 1.23

descrption -> Joes Tacos

date -> 2018-12-30

user_id -> 345


## LIST TRANSACTIONS
Receives <user_id> param.

This feature should print all the transactions associated with the user specified by user_id. The transactions should be in chronological order.

If the user_id does not exist, then the response should return an empty list. You should print the items with the following data:


List of ->

  transaction_id -> 2299ce24-9eaf-417f-82d6-e57f93777dc4
  
  amount -> 1.23
  
  descrption -> Joes Tacos
  
  date -> 2018-12-30
  
  user_id -> 345
  

## SUM TRANSACTIONS
Receives <user_id> param.

This command should sum all the transactions associated with the user specified by user_id. 

It should printout the sum with the following data:


user_id -> 123

sum -> 234.76

## TRANSACTIONS REPORT SERVICE
Receives <user_id> param.

This command should return all transactions accumulated by week, where the week starts on Friday and finishes on Thursday.
Also, if it is the first day of the month, it should start the next week (As the example below). The service should return only the *data*, it is not necessary to build the UI/PDF/HTML report.

The service should return an array if these datas:

user_id -> 123

week start date -> 2019-11-22 on Friday

week finish date -> 2019-11-28 on Thursday

quantity -> quantity of transactions inside the week

amount -> sum amout of the period/week

total_amount -> total amount before the week start date (all previous transactions before 2019-11-22, the current week is not included, as showed in the example below)


Whole example (including changing the month)

| Id | Week start | Week finish | Quantity | Amount | Total Amount |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 123 | 2019-11-08 Friday | 2019-11-14 Thursday | 2 | 10.00 | 00.00 |
| 123 | 2019-11-25 Friday | 2019-11-21 Thursday | 1 | 20.00 | 10.00 |
| 123 | 2019-11-22 Friday | 2019-11-28 Thursday | 4 | 100.00 | 30.00 |
| 123 | 2019-11-29 Friday | 2019-11-30 **Saturday** | 3 | 50.00 | 130.00 |
| 123 | 2019-12-01 **Sunday** | 2019-12-05 Thursday | 6 | 120.00 | 180.00 |
| 123 | 2019-12-06 Friday | 2019-12-12 Thursday | 3 | 100.00 | 300.00 |

It always start on Friday and finishes on Thursday, except on the start/end of the Month. In the example the total sum of transactions is 400.00.

If there's no one single day of transaction for the week, the report should hide the week.

The user can have no transaction in one day of the week, we still need to show the week.

Let some prepared data on the project so we can check everything is running fine.


## BONUS - RANDMON SINGLE TRANSACTION
This is not required, it is just a bonus, if you have time go ahead :)

Doesn't receive params.

This command should return one transaction in a randmon way. Don't use Math.random().


transaction_id -> 2299ce24-9eaf-417f-82d6-e57f93777dc4

amount -> 1.23

descrption -> Joes Tacos

date -> 2018-12-30

user_id -> 345


## FINAL CONSIDERATIONS
Please write this application in Java. You are free to implement this however you’d like with whatever resources or 3rd party code you’d want.

**Deadline**: We expect you to get back to us with the solution in 7 days. It won't be better if you delivery before, so if you finish early, improve your code. Finally, don't rush, if you need more time please ask us whenever you need.

Create a private project in GitHub and share with us your code.

The repo should have your name, for example **"_cesar-alcancio-sample-java-test_"**, it will help us to identify your test.

Feel free to ask questions at any time (cesar.alcancio@payclip.com).
