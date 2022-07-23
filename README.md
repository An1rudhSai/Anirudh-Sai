#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Wed Jul 20 12:29:44 2022

@author: anirudhsai
"""

import matplotlib.pyplot as ani

def compareSEE():
    
    sems=[]
    names=[]
    
    for i in range(sem):
        print("Enter the name of semester ",i+1)
        sems.append(input())
    for i in range(peeps):
        print("Enter the name of candidate ",i+1)
        names.append(input())
        
    color=['r','k','b','y','m']
    marks1=[]
    marks2=[]
    marks3=[]
    marks4=[]
    marks5=[]

    marks=[marks1,marks2,marks3,marks4,marks5]
    
    for i in range(peeps):
        for j in range(sem):
            while True:
                try:
                    print("Enter the SGPA of ",names[i]," in ",sems[j]," :")
                    marks[i].append(float(input()))
                    break
                except ValueError:
                    print("Not a valid integer! Please try again ...")
            
    #Plot
    ani.xlabel('SEMESTERS')
    ani.ylabel('POINTS')
    ani.title("CUMULATIVE GRADE POINT AVERAGE")
    if(sem==1):
        for i in range(peeps):
            ani.scatter( sems,marks[i],linestyle='-', label=names[i], color=color[i])
    else:
        for i in range(peeps):
            ani.plot( sems,marks[i],linestyle='-', label=names[i], color=color[i])
        
   
    ani.legend()
    ani.show()
    
def reqAttendance():
    flag=0
    while True:
        try:
            current=int(input(("Enter the number of classes you've attended :")))
            tot=int(input("Enter the total classes taken :"))
            req=int(input(("Enter the required attendance at your college(percentage):")))
            clas=int(input(("Enter an estimate of how many clases are left :")))
            club=int(input("Enter 1 if you're in any club and 0 if you're not :"))
            break
        except ValueError:
            print("Not a valid integer! Please try again ...")
            
    if(club==1):
        print("Lmao😂, you fkn clown!, Focus on cgpa not clubs...")
    elif(club==0):
        print("Lmao😂, you fkn loner!, what are you doing in college not in a club??")
        

    for i in range(0,clas+1):
        if(((current+i)/(tot+clas))*100>=req):
            print("You have to attend ",i," more classes!!!")
            flag=1
            break
    if(flag==0):
        print("It's too late😈,NSAR😂!!!!")
    

while True:
    choice=int(input(("0 : Exit the app \n1 : Graphically insult upto four loser friends who couldn't perform in their semesters!!!\n2 : Is the only thing score lesser than your cgpa your attendance???. Find out how many classes you need to attend in order to make the cut!!! "))) 
    if(choice==0):
        print("THANK YOU FOR USING THE APP🙏!!!")
        break
    elif(choice==1):
        while True:
            try:
                sem=int(input(("Enter the number of semesters :")))
                peeps=int(input(("Enter the number of students(Upto 5) :")))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        compareSEE()
    
    elif(choice==2):
        reqAttendance()
    else:
        print("0 or 1")
    






