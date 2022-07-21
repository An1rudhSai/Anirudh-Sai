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
    
    name1=input("Enter the name of the  first conetetsant :")
    name2=input("Enter the name of the second constestant: ")
    name3=input("Enter the name of the second constestant: ")
    
    marks1=[]
    marks2=[]
    marks3=[]
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",name1," in ",subs[i]," :")
                marks1.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",name2," in ",subs[i]," :")
                marks2.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    i=0
    while (i<sub):
        while True:
            try:
                print("Enter marks of ",name3," in ",subs[i]," :")
                marks3.append(int(input()))
                break
            except ValueError:
                print("Not a valid integer! Please try again ...")
        i+=1
    #Scatter plot
    ani.xlabel('NAMES')
    ani.ylabel('MARKS')
    ani.title("CONTIONOUS INTERNAL EVALUATION")
    ani.scatter( subs,marks1, label=name1, color='r')
    ani.scatter( subs,marks2, label=name2, color='g')
    ani.scatter( subs,marks3, label=name3, color='b')
    ani.legend()
    ani.show()
    
   
    
choice=int(input(("Are you interested in graphically insulting your two loser friends who couldn't perform in the internals??? , Choose 1!!!")))  
if(choice==1):
    compareCIE();
else:
    print("Loser !!!!")

