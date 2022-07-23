#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Wed Jul 20 12:29:44 2022

@author: anirudhsai
"""

import matplotlib.pyplot as ani

def compareCIE():
    
    subs=[]
    names=[]
    #Names of subjects and candidates
    for i in range(sub):
        print("Enter the name of subject ",i+1)
        subs.append(input())
    for i in range(peeps):
        print("Enter the name of candidate ",i+1)
        names.append(input())
        
    color=['r','k','b','y','g']
    marks1=[]
    marks2=[]
    marks3=[]
    marks4=[]
    marks5=[]
    marks=[marks1,marks2,marks3,marks4,marks5]
    
    #Marks of each candidate in each subject
    
    for i in range(peeps):
        for j in range(sub):
            while True:
                try:
                    print("Enter the marks of ",names[i]," in ",subs[j]," :")
                    marks[i].append(int(input()))
                    break
                except ValueError:
                    print("Not a valid integer! Please try again ...")
            
    #Plotting of data
    
    ani.xlabel('SUBJECTS')
    ani.ylabel('MARKS')
    ani.title("CONTIONOUS INTERNAL EVALUATION")
    if(sub==1):
        for i in range(peeps):
            ani.scatter( subs,marks[i],linestyle='-', label=names[i], color=color[i])
    else:
        for i in range(peeps):
            ani.plot( subs,marks[i],linestyle='-', label=names[i], color=color[i])
        
    ani.legend()
    ani.show()
    
#Interaction with the user

while True:
    choice=int(input(("0 : Exit the app \n1: Graphically insult upto four loser friends who couldn't perform in the internals???  "))) 
    if(choice==0):
        print("THANK YOU FOR USING THE APP🙏!!!")
        break
    elif(choice==1):
        while True:
            try:
                sub=int(input(("Enter the number of subjects :")))
                peeps=int(input(("Enter the number of students(Upto 5) :")))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")

        compareCIE();
    else:
        print("0 or 1")
    




