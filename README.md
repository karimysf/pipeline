# FeverTokens Technical Assessment
Welcome! This repository contains my submission for the FeverTokens internship technical assessment.
---
## 🔍 Overview
This assessment includes three tasks:
- **Task 1**: CI/CD on a Docker Swarm Cluster.
- **Task 2**: Algorithmic.
- **Task 3**: Logic.
---
## 🛠 Setup & Run Instructions (Task 1)
keep this empty for now 


## 📊 Task 2: Algorithmic Challenge
### Problem Description
The task requires writing a program that prints numbers from 1 to 100 with the following rules:
- For multiples of 3, print "Hello" instead of the number
- For multiples of 5, print "World" instead of the number
- For multiples of 7, print "Yoo" instead of the number
- For numbers that are multiples of more than one of these values, print the corresponding outputs concatenated
- For all other numbers, print the number itself

### Solution in C
```c
#include <stdio.h>
int main() {
    for (int i = 1; i <= 100; i++) {
        int flag = 0;
        if (i % 3 == 0) {
            printf("Hello");
            flag = 1;
        }
        if (i % 5 == 0) {
            printf("World");
            flag = 1;
        }
        if (i % 7 == 0) {
            printf("Yoo");
            flag = 1;
        }
        if (!flag) {
            printf("%d", i);
        }
        printf("\n");
    }
}
```
### Solution in Python
```python
for i in range(1, 101):
    tmp = ""
    if i % 3 == 0:
        tmp += "Hello"
    if i % 5 == 0:
        tmp += "World"
    if i % 7 == 0:
        tmp += "Yoo"
    print(tmp or i)
```
## 🧩 Task 3: Logic Problem

### To find the red car in a finite amount of time:

1. Start at your current position (let's call it **position 0**).
2. Drive a certain amount of distance d let's take **d = 1 km** as an example in one direction, then turn back and return to position 0.
3. Now drive **2*d km** in the opposite direction , then return to position 0.
4. Next, drive **4*d km** forward , then return.
5. Then **8*d km** backward , then return.
6. Continue this process, **doubling the distance** each time and **alternating directions**.

---

### 🧠 Explanation

Thie approach implemented guarantees finding the red car in finite time:

- By **doubling the search distance** in each iteration, we cover increasingly larger areas.
- **Alternating directions** ensures we don't miss my friend's car regardless of which way he is from my starting point(position 0).


