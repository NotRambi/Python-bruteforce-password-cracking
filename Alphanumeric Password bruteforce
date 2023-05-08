Try = ['']
First = []
J = []
#password
char ="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789<>\\|!\"£$%&/()=\'?ì^èé+*òçà°ù§,;.:-_[]@#]{}"

def ListToString(lista):
    l = lista.copy()
    l.reverse()
    s = ''
    for i in l:
        s += i
    return s
    
def F1(first,flag):
    while flag:
        if first:
            for i in range(len(char)):
                Try[0] = char[i]
                s = ListToString(Try)
                #print(s)
                if s == Pass:
                    flag = False
                    break
            if flag == False:
                break
            Try.append('A')
            First.append(True)
            J.append(0)
            first = False
        else:
            for i in range(len(char)):
                Try[0] = char[i]
                s = ListToString(Try)
                #print(s)
                if s == Pass:
                    flag = False
                    break
            if flag == False:
                break
            J[0],First[0] = F2(First[0],1,J[0])        
        
def F2(first,cont,i):
    if first:
        if i < len(char)-1:
            i += 1
            Try[cont] = char[i]
            return i,first
        else:
            i = 0
            Try[cont] = char[i]
            Try.append('A')
            First.append(True)
            J.append(0)
            return i,False
    else:
        if i < len(char)-1:
            i += 1
            Try[cont] = char[i]
            return i,first
        else:
            i = 0
            Try[cont] = char[i]
            J[cont],First[cont] = F2(First[cont],cont+1,J[cont])
            return i,first
                
Pass = input("write a password: ")
F1(True,True)
password = ListToString(Try)
print("password is: ",password)
