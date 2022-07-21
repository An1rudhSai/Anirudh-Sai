# Anirudh-Sai
-
import matplotlib.pyplot as ani

def compareCIE():
    while True:
        try:
            sub=int(input(("Enter the number of subjects :")))
            break
        except ValueError:
            print("Not a valid integer! Please try again ...")
    subs=[]
    i=0
    while(i<sub):
        subs.append(input("Enter the name of the subject :"))
        i+=1
    names=[]
    for i in range(1,6):
        print("Enter the name of candidate ",i)
        names.append(input())
        
    marks1=[]
    marks2=[]
    marks3=[]
    marks4=[]
    marks5=[]
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",names[0]," in ",subs[i]," :")
                marks1.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",names[1]," in ",subs[i]," :")
                marks2.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",names[2]," in ",subs[i]," :")
                marks3.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",names[3]," in ",subs[i]," :")
                marks4.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",names[4]," in ",subs[i]," :")
                marks5.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    #Scatter plot
    ani.xlabel('NAMES')
    ani.ylabel('MARKS')
    ani.title("CONTIONOUS INTERNAL EVALUATION")
    ani.scatter( subs,marks1, label=names[0], color='r')
    ani.scatter( subs,marks2, label=names[1], color='g')
    ani.scatter( subs,marks3, label=names[2], color='b')
    ani.scatter( subs,marks4, label=names[3], color='y')
    ani.scatter( subs,marks5, label=names[4], color='c')
    ani.legend()
    ani.show()
        
    
choice=int(input(("Are you interested in graphically insulting upto four loser friends who couldn't perform in the internals??? , Choose 1!!! : ")))  
if(choice==1):
    compareCIE();
else:
    print("Loser !!!!")

