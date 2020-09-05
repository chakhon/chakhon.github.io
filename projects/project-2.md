---
layout: project
type: project
image: images/ics212p2.jpg
title: ICS 212 Project 2
permalink: projects/project-2
# All dates must be YYYY-MM-DD format!
date: 2019-12-13
labels:
  - C++
  - Git
  - g++
  - Makefile
summary: A simple bank account manager IN C++.
---

This is a project I work on for ICS 212, the objective of the project is to convert the C code project 1 to C++. On top of the 5 original methods, we also have to implement a reverse method that reverse the list:

```
1.Add a record
2.Print a record onto the console
3.Print all record onto the console
4.Delete a record
5.Modify a record
6.Reverse the list
```

Everything was basically the same as project 1, but we had to change all the output and input to use istream instead or stdio. We also implemented a list class that look like this.

```c++
class llist
{
private:
    record *    start;
    char        filename[16];
    int         readfile();
    int         writefile();
    record *    reverse(record * );
    void        cleanup();

public:
    llist();
    llist(char[]);
    llist(const llist &);
    ~llist();
    llist &operator = (const llist &);
    int addRecord(int, char [ ],char [ ]);
    int printRecord(int);
    friend std::ostream &operator << (std::ostream &, const llist &);
    int modifyRecord(int, char [ ]);
    int deleteRecord(int);
    void reverse();
};
```
Every time the program starts, it would open a text document to read for the previous records, and each time we exit the program would also write to the file to save the records. Converting the C singly linked list to C+++ was way easier than I thought. The reverse function was the hardest part of the project, to solve it I used a recursive method.

```c++
/*****************************************************************
//
// Function name: reverse
//
// DESCRIPTION: reverse the record with the one next to it
//
// Parameters:  rec (record *) record to reverse
//
// Returns : rec (record *) the next record
//
******************************************************************/
record* llist::reverse(record * rec)
{
    if (rec == NULL)
    {
        return NULL;
    }
    if (rec->next == NULL)
    {
        start = rec;
        return rec;
    }
    record* temp = reverse(rec->next);
    temp->next = rec;
    rec->next = NULL;
    return rec;
}

/*****************************************************************
//
// Function name: reverse
//
// DESCRIPTION: Calles the reverse(llist) function
//
******************************************************************/
void llist::reverse()
{
    reverse(start);
}
```

While the project 2 was a lot easier then project 1, I learned a lot form it. Mainly the difficulty of converting code from one language to another. It showed me that different languages have different strengths, and even though C and C++ is very similar, C++ is way better at object orientated programming.



Source: <a href="https://github.com/chakhon/ICS212/tree/master/Project2"><i class="large github icon"></i></a>
