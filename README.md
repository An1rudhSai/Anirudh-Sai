import matplotlib.pyplot as ani

def compareCIE():
    while True:
        try:
            sub=int(input(("Enter the number of subjects :")))
            break
        except ValueError:
            print("Not a valid integer! Please try again ...")
    while True:
        try:
            peeps=int(input(("Enter the number of students(Upto 5) :")))
            break
        except ValueError:
            print("Not a valid integer! Please try again ...")
    subs=[]
    i=0
    while(i<sub):
        subs.append(input("Enter the name of the subject :"))
        i+=1
    names=[]
    for i in range(peeps):
        print("Enter the name of candidate ",i+1)
        names.append(input())
        
    color=['r','g','b','y','c']
    marks1=[]
    marks2=[]
    marks3=[]
    marks4=[]
    marks5=[]
    marks=[marks1,marks2,marks3,marks4,marks5]
    
    for i in range(0,peeps):
        for j in range(0,sub):
            while True:
                try:
                    print("Enter the marks of ",names[i]," in ",subs[j]," :")
                    marks[i].append(int(input()))
                    break
                except ValueError:
                    print("Not a valid integer! Please try again ...")
            
    #Scatter plot
    ani.xlabel('NAMES')
    ani.ylabel('MARKS')
    ani.title("CONTIONOUS INTERNAL EVALUATION")
    for i in range(peeps):
        ani.plot( subs,marks[i],linestyle='-', label=names[i], color=color[i])
    
    ani.legend()
    ani.show()
        
    
choice=int(input(("Are you interested in graphically insulting upto four loser friends who couldn't perform in the internals??? , Choose 1!!! : ")))  
if(choice==1):
    compareCIE();
else:
    print("Loser !!!!")



