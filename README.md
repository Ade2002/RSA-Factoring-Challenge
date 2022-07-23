# factors.c-Factoring-Challenge
Alx factors.c-Factoring-Challenge


chmod u+x lists.h && git add --chmod=+x lists.h && git commit -m 'header file lists.h' && git push

chmod u+x factors && git add --chmod=+x factors && git commit -m 'Task 01 factors Laboratories states that: for each factors number n, there exist prime numbers p and q such that factors' && git push


chmod u+x 100-print_python_list_info.c  && git add --chmod=+x 100-print_python_list_info.c  && git commit -m 'Advanced Task 14 a C function that prints some basic info about Python lists. 100-print_python_list_info.c ' && git push

chmod u+x 4-print_hexa.py && git add --all && git commit -m 'task 04 4-print_hexa.py' && git push







#!/usr/bin/python3
import sys
import math


def reading(file):
    # total = 0
    with open(file) as data:
        new_data = data.readlines()
        # print(new_data)
    return new_data


for file_index in range(len(sys.argv)):
    if file_index != 0:
        data = reading(sys.argv[file_index])
        for item in data:
            number = int(item)
            # print(number)

            if number % 2 == 0:
                print("{}*2".format(number//2))
                continue
            for i in range(3, number, 2):
                if number % i == 0:
                    factor = number//i
                    for j in range(3, factor, 2):
                        if factor % j == 0 or i % j == 0:
                                break
                        print("{}*{}".format(factor, i))
                        break
