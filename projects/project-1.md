---
layout: project
type: project
image: images/ics212p1.jpg
title: ICS 212 Project 1
permalink: projects/project-1
# All dates must be YYYY-MM-DD format!
date: 2019-9-14
labels:
  - C
  - Git
  - g++
summary: A simple bank account manager.
---

This is a project I work on for ICS 212, the objective of the project is to create a simple bank record manager with 5 functions:

```
1.Add a record
2.Print a record onto the console
3.Print all record onto the console
4.Delete a record
5.Modify a record
```

A record a is object that was provided by the professor, and we used a single linked list to manage the record. To add a record you will need to provide account number, name and address. One of the requirement for taking in an address is that it must also be able to take in a multi-line address. Every time a new record is added or deleted we must also sort the list of record by its account number. To print,delete or modify a specific record, you will need to provide a account number. The print all record function has to print out all the records in a sorted manner. When the program end, it will save all records to a text file, next time the program starts it will read the text file and add all record back on the list. We also create a testing plan to test for bugs for this program.

Here is a sample output from the console when the program is running:
```
uhx02:/home/c/chakhon/Project1% ./project1



Welcome to the record holding system.



To choose an option, enter a number corresponding to the fuction.

1: Add a new record in the database

2: Print information on a record

3: Print all records

4: Modify the address of a record

5: Delete an existing record

0: Exit

1



Add a new record in the database:

Enter the account number: 1234

Enter name of record holder: Chak Hon Lam

Enter address below:

5095 Likinki ST

APT A204
```
