

# C++ STL (Standard Template Library) Containers
<br/>
<br/>
<br/>

## VECTOR  ( The array on steroids )

  
Ever wished you could shrink the array so that you could save all the extra space or if you could grow its size so that you could add those few extra elements, well here is vector at your rescue. Vector is a perfect hybrid of an array and a linked list.
<br/>
### Declaration:

    vector< Data_Type > Vector_Name; // Example : vector<int> v;



As you can see above it’s not compulsory to specify the size of the vector although we can do so.

  
<br/>


 ### Initialization:
There are follwing methods to initialize vectors:

(i) Method 1:  

    Gereral Format: 
    vector_Name = {d1, d2, d3, ... , dn}; where di (i= 1 to n ) is data of same data-type.
    
    Example:
    v = {1, 2, 5, 99, 21, 43, 31};
    
    
    

  

Above method is similar to what we use in arrays and is used when we have a limited number of elements to be initialized,

(ii) Method 2:

  
    General Format: 
    Vector_Name.push_back(data);
    
    Example:
    v.push_back(2) ;

The push_back() is one of the functions of vector container. It pushes the element at the end of the vector.

  
(iiI) Method 3:

    General Format:
    vector<Data_Type> Vector_Name( size_of_vector, value ) ; 
    
    Example :
    vector<int> v(7, -1) ;

This method is generally used when we have to initialize all indices of a vector of a “given size” with the same value. (NOTE: This method can be used only while declaring the vector, contrary to the above 2 methods.)

  

(iv) Method 4:
Using a pre-existing array, string, or vector. Similar to the 3rd method this too can only be used while declaration.

    General Format:
    vector<Data_Type> Vector_name(Array_Name , Array_Name + Array_Size)
    Or
    vector<Data_Type> Vector_name(Container_Name.begin() , Container_Name.end())
    
    Example:
    vecotr<int> v(ar, ar + size_of_array) ; // Here ar is the name of the array
    vector<char> v(s.begin(), s.end()) ; // Here s is the name of the string
    vector<char> v(v2.begin(), v2.end()) ; // Here v2 is the name of the another vector
    vector<int> v(st.begin(), st.end()) ; // Here st is the name of the set.
  
<br/>

### Traversing : 
The traversal of vectors can be achieved through the following 2 methods :

  

(i) Using the old school method of traversing an array.

  

    #include<bits/stdc++.h>
    using namespace std;
    
    int main()
    {
	    int i;
	    vector<int> v = {1, 2, 5, 99, 21, 43, 31};
	    
	    for(i=0 ; i<7 ; i++)
	    cout << v[i] << “ ”;
	}

  

(ii) Using iterators.

  

    #include<bits/stdc++.h>
    using namespace std;
    
    int main()
    {
	    vector<int> v = {1, 2, 5, 99, 21, 43, 31};
	    
	    for(auto it=v.begin() ; it!=v.end() ; it++)
	    cout << *it << “ “;
    }

<br/>

 ### Some functions affiliated with vector : 


| Name  | Purpose |
|--|--|
| [v.begin( )](http://www.cplusplus.com/reference/vector/vector/begin/) | This funciton returns an iterator pointing at the first element/begining of the vector container |
| [v.end( )](http://www.cplusplus.com/reference/vector/vector/end/) | This funciton returns an iterator pointing at the last element/end of the vector container |
| [v.rbegin( )](http://www.cplusplus.com/reference/vector/vector/rbegin/) | This funciton returns "a reverse" iterator pointing at the last element/end of the vector container |
| [v.rend()](http://www.cplusplus.com/reference/vector/vector/rend/) | This funciton returns "a reverse" iterator pointing at the first element/begining of the vector container |
| [v.insert()](http://www.cplusplus.com/reference/vector/vector/insert/) / [v.emplace()](http://www.cplusplus.com/reference/vector/vector/emplace/) | Both the function inserts the element at the specified location and push the element already at the location forward.  |
| [v.push_back()](http://www.cplusplus.com/reference/vector/vector/push_back/) / [v.emplace_back()](http://www.cplusplus.com/reference/vector/vector/emplace_back/) | Both the functions are used to add an element at the end of the vector container |
| [v.pop_back()](http://www.cplusplus.com/reference/vector/vector/pop_back/) | This function is used to remove an element from the end of vector container |
| [v.empty()](http://www.cplusplus.com/reference/vector/vector/empty/) | This function returns true if container is empty else its return false |
| [v.size()](http://www.cplusplus.com/reference/vector/vector/size/) | This function return total number of elements in the container |
| [v.erase()](http://www.cplusplus.com/reference/vector/vector/erase/) | This function aids in removing the element from a specific location |
| [v.clear()](http://www.cplusplus.com/reference/vector/vector/clear/) | This funciton removes all the elements form the container |
| [v.find()](http://www.cplusplus.com/reference/algorithm/find/) | This function returns an iterator pointing a element to be found in the vector. If there are multiple occurences of the element it returns iterator pointing at the 1st occurence and if there is no such element it returns "npos"  |
|[ v.at(i)](http://www.cplusplus.com/reference/vector/vector/at/) / [v[i]](http://www.cplusplus.com/reference/vector/vector/operator%5B%5D/) | This function returns a value of the element located at position ‘i’ in the vector |
| [v.sort()](http://www.cplusplus.com/reference/algorithm/sort/) | This function sorts the vector container in ascending order |

<br/>
<br/>
<br/>

## SET ( #NoDuplicates )

  

Similar to sets in mathematics this container also doesn’t allow duplicates. Another useful feature of this container is that it keeps its elements in sorted fashion even if we insert elements randomly.

  

### Decleration:

    set<Data_Type> Set_Name ; // Example : set<int> st ;



  

### Initialization:

  

There are follwing methods to initialize vectors:

  
(i) Method 1:

    
    Gereral Format: 
    Set_Name = {d1, d2, d3, ... , dn}; where di (i= 1 to n ) is data of same data-type.
    
    Example:
    st = {1, 2, 5, 99, 21, 43, 31};

Similar to in arrays & vectors, this method is opted when we have limited number of elements to be initialized,

  
(ii) Method 2:
 

    General Format: 
    Set_Name.insert(data);
    
    Example:
    st.insert(1) ;
    

insert() is a function provided in the set container. It adds element into the set if it's not present in the set already.

  
(iii) Method 3:
 Using a pre-existing array, string, set, map, vector, etc Similar to 3rd method this too can only be used while declaration.

   
    General Format:
    set<Data_Type> Vector_name(Array_Name , Array_Name + Array_Size)
    Or
    set<Data_Type> Vector_name(Container_Name.begin() , Container_Name.end())
    
    Example:
    set<int> st(ar, ar + size_of_array) ; // Here ar is the name of the array
    set<char> st(s.begin(), s.end()) ; // Here s is the name of the string
    set<float> st(v.begin(), v.end()) ; // Here v is the name of the vector
    set<char> st(st2.begin(), st2.end()) ; // Here st2 is the name of the another set
    

<br/>


### Traversing : 
Traversal in sets can be achieved using only 1 method :

  

(i) Using iterators.

    #include<bits/stdc++.h>
    using namespace std;
    
    int main()
    {
	    set<int> st = {1, 2, 5, 99, 21, 43, 31};
    
	    for(auto it = st.begin() ; it != st.end() ; it++)
	    cout << *it << “ “;
    }
    
 <br/>
    
 ### Some functions affiliated with the stack

  
| Functions | Purpose |
|--|--|
| [st.begin()](http://www.cplusplus.com/reference/set/set/begin/) | This funciton returns an iterator pointing at the first element/begining of the set container |
| [st.end()](http://www.cplusplus.com/reference/set/set/end/) | This funciton returns an iterator pointing at the last element/end of the set container |
| [st.rbegin()](http://www.cplusplus.com/reference/set/set/rbegin/) |  This funciton returns "a reverse" iterator pointing at the last element/end of the set container |
| [st.rend()](http://www.cplusplus.com/reference/set/set/rend/) | This funciton returns "a reverse" iterator pointing at the first element/begining of the set container |
| [st.insert()](http://www.cplusplus.com/reference/set/set/insert/) / [st.emplace()](http://www.cplusplus.com/reference/set/set/emplace/) | This function inserts a new element into the container |
| [st.size()](http://www.cplusplus.com/reference/set/set/size/) | This function return total number of elements in the container |
| [st.empty()](http://www.cplusplus.com/reference/set/set/empty/) | This function returns true if container is empty else its return false  |
| [st.erase()](http://www.cplusplus.com/reference/set/set/erase/)|  This function aids in removing an element from a specific location |
| [st.clear()](http://www.cplusplus.com/reference/set/set/clear/)|  This funciton removes all the elements form the container |
| [st.find()](http://www.cplusplus.com/reference/set/set/find/) | This function returns an iterator pointing a element to be found in the set. If there are multiple occurences of the element it returns iterator pointing at the 1st occurence and if there is no such element it returns "npos"   |
| [st.count()](http://www.cplusplus.com/reference/set/set/count/) | This function returns 1 if elment is present in the container and if it isn't present it returns 0 |
| [st.lower_bound(d)](http://www.cplusplus.com/reference/set/set/lower_bound/) | This function returns an element which is equal to 'd' and in its absence it returns 1st element just greater than d  |
| [st.upper_bound(d)](http://www.cplusplus.com/reference/set/set/upper_bound/) | This function returns an element which is equal to 'd' and in its absence it returns 1st element just less than d |


<br/>
<br/>
<br/>
  
## MAP  ( The magic array )

  

You might be thinking what is co cryptic about maps. Well, maps allow the index of the element in the map to be of different data types. That is you can have an index of type string, char, float, double, etc. Well, that may sound weird but it's not. Data in maps is stored in “key-value” pairs and these “keys” have traits similar to the index. Let's take an example to understand it better

  

ar[2] = 14;

  

The above statement will give us the value stored at index “2” of array “ar”.

  

mp[“Apple”] = 4;

  

The above statement will give us the value stored with the key “Apple” of map “mp”.

  

  <br/>

### Decleration:

  

    General Format:
    map<Data_Type , Data_Type> Map_Name ;
    
    Example : 
    map<string,int> mp ;


<br/>
  
### Initialization:

  

There are follwing methods to initialize vectors:

(i) Method 1:

    Gereral Format: 
    Map_Name = { {k1,v1} , {k2, v2} , {k3,v3} ... , {kn,vn} } 
    where ki (i= 1 to n ) is key of same data-type and vi (i= 1 to n ) is value of same data-type 
    
    Example:
    st = { {“Red”,1} , {“Blue”, 2} , {“Green”,5} , {“Yellow”,99} , {“Orange”,21} , {“Black”43} } 



Or


    Gereral Format: 
    Map_Name = { make_pair(k1,v1) , make_pair(k2, v2) , make_pair(k3,v3) ... , make_pair(kn,vn) } 
    where ki (i= 1 to n ) is key of same data-type and vi (i= 1 to n ) is value of same data-type 
    
    Example:
    st = { make_pair(“Red”,1) , make_pair(“Blue”, 2) , make_pair(“Green”,5) , make_pair(“Yellow”,99) , make_pair(“Orange”,21) , make_pair(“Black”43) }



This is quite different to the way array is initialized as we have to write the data in pairs of key and value, this method too is adopted when we have limited number of elements to be initialized,

  
(ii) Method 2:

    General Format: 
    Map_Name.insert(make_pair(key, value));
    
    Example:
    st.insert(make_pair(“Kiwi”, 12));


insert() is a function provided in the set container. It adds key-value pairs into the map if it's not present already.

  

(iii) Using a pre-existing array, string, set, map, vector, etc Similar to 3rd method this too can only be used while declaration.

   
    General Format:
    map<Data_Type,Data_Type> Map_name(Array_Name , Array_Name + Array_Size)
    Or
    map<Data_Type,Data_Type> Map_name(Container_Name.begin() , Container_Name.end())
    
    Example:
    map< string, int > mp(ar, ar + 15) ; // Here ar is the name of the array
    map<string, float> mp(v.begin(), v.end()) ; // Here v is the name of the vector
    map< string, char> mp(mp2.begin(), mp2.end()) ; // Here mp2 is the name of the another


But the point to be noted here is the array,vector,set etc has to be in the form of pairs, as given below:

  

    pair<srting,int > ar[array_size];
    vector< pair < string, float> > v;

<br/>`

### Traversing : 

Similar to sets, traversal in maps can be achieved using only 1 method :

  

(i) Using iterators.

  

    #include<bits/stdc++.h>
    using namespace std;
    
    int main()
    {
	    map<int> mp = {1, 2, 5, 99, 21, 43, 31};
	    
	    for(auto it = mp.begin() ; it != mp.end() ; it++)
	    cout << it -> first << “ ” << it -> second << endl;
    }




Here “ it -> first “ prints the key and “ it -> second “ prints the value.

<br/>
  
 ### Some functions affiliated with map
 
  
| Name | Purpose |
|--|--|
| [mp.begin()](http://www.cplusplus.com/reference/map/map/begin/) | This function returns an iterator pointing at the first element/begining of the map container |
| [mp.end()](http://www.cplusplus.com/reference/map/map/end/) | This function returns an iterator pointing at the last element/end of the map container |
|[ mp.rbegin()](http://www.cplusplus.com/reference/map/map/rbegin/) | This function returns "a reverse" iterator pointing at the last element/end of the map container  |
| [mp.rend()](http://www.cplusplus.com/reference/map/map/rend/) | This function returns "a reverse" iterator pointing at the first element/begining of the map container  |
| [mp.insert()](http://www.cplusplus.com/reference/map/map/insert/) / [mp.emplace()](http://www.cplusplus.com/reference/map/map/emplace/) | Both functions aids in adding a specific key value pair |
| [mp.size()](http://www.cplusplus.com/reference/map/map/size/) | This function return total number of elements in the container  |
| [mp.empty()](http://www.cplusplus.com/reference/map/map/empty/) |  This function returns true if container is empty else its return false |
| [mp.erase()](http://www.cplusplus.com/reference/map/map/erase/)| This function aids in removing a specific key value pair |
| [mp.clear()](http://www.cplusplus.com/reference/map/map/clear/)| This funciton removes all the elements form the container  |
| [mp.find()](http://www.cplusplus.com/reference/map/map/find/) | This function returns an iterator pointing a key to be found in the map. If there are multiple occurences of the key it returns iterator pointing at the 1st occurence and if there is no such key it returns "npos"  |
| [mp.lower_bound()](http://www.cplusplus.com/reference/map/map/lower_bound/) | This function returns an value of the key which is equal to 'd' and in its absence it returns 1st value of the key just greater than d  |
| [mp.upper_bound(d)](http://www.cplusplus.com/reference/map/map/upper_bound/) | This function returns the value of the key equal to 'd' and in its absence it returns 1st value of the key just less than d  |
| [mp.at(d)](http://www.cplusplus.com/reference/map/map/at/) / [mp[d]](http://www.cplusplus.com/reference/map/map/operator%5B%5D/) | Both the functions return the value of the key "d" |

   
   <br/>
   <br/> 
   <br/>

## STACK (Ctrl + Z)

  

The characteristics of this container are similar to that of stacks in the real world like stacks of plates or chairs. Similar to stacks in physical world contents of stacks in c++ containers are stored and accessed uniquely. It follows the FILO (First In Last Out) method of storing and LIFO (Last In First Out) of accessing its content/data. The Ctrl + Z (undo) function in the word processors is implemented using a data structure similar to stack.

  

### Decleration:

  

    General Format:
    stack<Data_Type> Stack_Name ;
    
    Example : 
    stack<string> stk;



  

###  Initialization:

There are follwing methods to initialize vectors:

  

  
(i) Method 1:

    General Format: 
    Stack_Name.push(data);
    
    Example:
    stk.push(“Kiwi”) ;


push() is function provided in stack container. It adds an element to the top/end of the stack.

  
(ii) Method 2:
Using pre-existing vector, list & stack Similar to 3rd method this too can only be used while declaration.

    General Format:
    stack<Data_Type,Container<Data_Type>> Stack_name(Container_Name)
    Or
    stack<Data_Type> Stack_name(Container_Name)
    
    Example:
    stack<int,vector<int> > stk (v); // Here v is the name of the vector
    stack<int,list<int> > stk (l); // Here l is the name of the list.
    stack<int> stk (stk2); // Here stk2 is the name of the an already existing stack.

  


One thing to be careful about in the above method is that while initialization using list and vector is similar whereas that using stack it's different.

  

###  Traversing :

  

We cant traverse through a stack although we can use a method that gives us an illusion that we are traversing through the stack.

  

(i) Using top() & pop() method.

  

    #include<bits/stdc++.h>
    using namespace std;
    
    int main()
    {
	    stack<int> stk;
	    
	    stk.push(1); 
	    stk.push(2);
	    stk.push(5);
	    stk.push(99);
	    stk.push(21);
	    stk.push(43);
    
	    while (stk.size()>0)
	    {  
		    cout << stk.top() << " ";
		    stk.pop();
	    }
	    
	    return 0;
    }

   
The top() function gives the value of the element at the top/end of the stack while pop() removes the element at the top/end. Using these two function inside the loop gives us an illusion that we are traversing through the stack

  

The function works in the following manner:

+ top() functions prints the value at the top of the stack.
+ pop() function pops the element at the top of the stack hence reducing the size of the stack by one unit.
+ size() function checks if the size of the stack is greater than 0 as if it's 0 all the elements must have been already popped out.
+ The loop stops when the stack is empty i.e. size of the stack is 0.

  

This method can only be used once as after it the stack eventually becomes empty.

 ### Some functions affiliated with the stack
  
| Name | Purpose  |
|--|--|
| [stk.push()](http://www.cplusplus.com/reference/stack/stack/push/) / [stk.emplace()](http://www.cplusplus.com/reference/stack/stack/emplace/) | Both these function insert the element at top/end of the stack |
| [stk.pop()](http://www.cplusplus.com/reference/stack/stack/pop/) | This function removes the element from top/end of the stack |
| [stk.top()](http://www.cplusplus.com/reference/stack/stack/top/) | This function returns the value of the element at top/end of the stack |
| [stk.size()](http://www.cplusplus.com/reference/stack/stack/size/) | This function returns total number of elements present in the stack |
|[ stk.empty()](http://www.cplusplus.com/reference/stack/stack/empty/) | This function returns true if the stack is empty and false if it's not |
