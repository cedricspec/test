
# coding: utf-8
# In[1]:


print 'test du premier code'


# In[38]:

def match_ends(words):
    ret=0
    for n in words:    
        if(len(n)>1):
            if(n[0]==n[-1]):
                ret+=1
    return ret


# In[47]:

mylist=["testt","testt"]
match_ends(mylist)


# In[44]:

def front_x(words):
    xlist=[]
    otherslist=[]
    for n in words:
        if(n[0]=="x"):
            xlist.append(n)
        else:
            otherslist.append(n)
    xlist=sorted(xlist, key=str.lower)
    otherslist=sorted(otherslist, key=str.lower)
    return xlist+otherslist


# In[48]:

mylis2=['mix', 'xyz', 'apple', 'xanadu', 'aardvark'] 
front_x(mylis2)


# In[30]:

def sort_last(tuples):
    latest=[]
    for t in tuples:
        latest.append(t[-1])
    indexes=sorted(range(len(latest)), key=lambda k: latest[k])  
    return [ tuples[i] for i in indexes ]



# In[49]:

liste3= [(1, 7), (1, 3), (3, 4, 5), (2, 2)] 
sort_last(liste3)


# In[31]:

def remove_adjacent(nums):
    to_remove=[]
    for i in list(range(0,len(nums)-1)):
        if(nums[i]==nums[i+1]):
            to_remove.append(i)
    for i in sorted(to_remove, reverse=True):
        del nums[i]
    return nums


# In[32]:

def linear_merge(list1,list2):
    output=[] 
    while min(len(list1),len(list2))>0:
        if list1[0]>list2[0]:
            output.append(list2[0])
            del list2[0]
                
        else:
            output.append(list1[0])
            del list1[0]
    return output+list1+list2


# In[33]:

def donuts(count):
    Prefix="Number of donuts: "
    if count>=10:
        return Prefix + "many"
    else:
        return Prefix + str(count)


# In[34]:

def both_ends(s):
    output=""
    if(len(s)>2):
        output=s[:2]+s[-2:]
    return output


# In[35]:

def fix_start(s):  
    return s[0]+s[1:].replace(s[0], "*")
    
    


# In[36]:

def mix_up(a, b):
    return b[:2]+a[2:] + " " + a[:2]+b[2:]

def verbing(s):
    if(len(s)>2):
        if(s[-3:]=="ing"):
          return s+"ly"
        else:
          return s+"ing"
    else:
        return s

def not_bad(s):
    output=s
    if(0<s.find("not")<s.find("bad")):
        output=s.replace(s[s.find("not"):s.find("bad")+3],"good")      
    return output


def front_back(a, b):
    return a[:int(len(a)/2)+len(a)%2]+b[:int(len(b)/2)+len(b)%2]+a[int(len(a)/2)+len(a)%2:]+b[int(len(b)/2)+len(b)%2:]

    


# In[ ]:




