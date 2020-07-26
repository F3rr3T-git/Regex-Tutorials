
# C++ STL (Standard Template Library) Containers
\

\

## VECTOR  ( The array on steroids )

  
Ever wished you could shrink the array so that you could save all the extra space or if you could grow its size so that you could add those few extra elements, well here is vector at your rescue. Vector is a perfect hybrid of an array and a linked list.

## Decleration:

    vector< Data_Type > Vector_Name; // Example : vector<int> v;

As you can see above it’s not compulsory to specify the size of the vector although we can do so.

  



 ### Initialization:

  

There are follwing methods to initialize vectors:

(i) Method 1:  

    v = {1, 2, 5, 99, 21, 43, 31};

  

Above method is similar to what we use in arrays and is used when we have limited numver of elements to be initialized,

(ii) Method 2:

  
    v.push_back(1) ;
    v.push_back(2) ;

The push_back() is one of the funciton of vectore container . It push the element at the end of the vector.

  
(iiI) Method 3:

    vector< int > v( size_of_vector, value ) ; // Example vector<int> v(7, -1) ;

This method is generally used when we have to initialize all indecies of a vector with “given size” whith same value. (NOTE: This method can be used only while declaring the vector , contraty to above 2 methods.)

  

(iv) Method 4:
Using pre-existing array, string or vector. Similar to 3rd method this too can only be used while declaration.

    vecotr<int> v(ar, ar + size_of_array) ; // Here ar is the name of the array
    vector<char> v(s.begin(), s.end()) ; // Here s is the name of the string
    vector<char> v(v2.begin(), v2.end()) ; // Here ar is the name of the another vector
  

### Traversing : 
The traversal of vectors can achieved through following 2 methods :

  

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


 ### Some functions affiliated with stack


|  |  |
|--|--|
| v.begin( ) |  |
| v.end( ) |
| v.rbegin( ) |  |
| v.rend() |  |
| v.insert() / v.emplace() |  |
| v.push_back() / v.emplace_back() |  |
| v.pop_back() |  |
| v.empty() |  |
| v.size() |  |
| v.erase() |  |
| v.clear() |  |
| v.swap() |  |
| v.find() |  |
| v.at() / v[] |  |
| v.sort() |  |


## SET ( #NoDuplicates )

  

Similar to sets in mathematics this container also doesn’t allow duplicates . Another useful feature of this container is that it keeps its elements in sorted fashion even if we insert elements in random manner.

  

### Decleration:

    set< Data_Type > Set_Name ; // Example : set<int> st ;



  

### Initialization:

  

There are follwing methods to initialize vectors:

  
(i) Method 1:

    st = {1, 2, 5, 99, 21, 43, 31};

Similar to in arrays & vectors, this method is opted when we have limited number of elements to be initialized,

  
(ii) Method 2:
 

    st.insert(1) ;
    st.insert(2) ;

insert() is funciton provided in set container . It adds element into the set if its not present in the set already.

  
(iii) Method 3:
 Using pre-existing array, string, set, map, vector etc Similar to 3rd method this too can only be used while declaration.

    set<int> st(ar, ar + size_of_array) ; // Here ar is the name of the array
    set<char> st(s.begin(), s.end()) ; // Here s is the name of the string
    set<float> st(v.begin(), v.end()) ; // Here v is the name of the vector
    set<char> st(st2.begin(), st2.end()) ; // Here ar is the name of the another set




### Traversing : 
Traversal in sets can achieved using only 1 method :

  

(i) Using iterators.

    #include<bits/stdc++.h>
    using namespace std;
    
    int main()
    {
	    set<int> st = {1, 2, 5, 99, 21, 43, 31};
    
	    for(auto it = st.begin() ; it != st.end() ; it++)
	    cout << *it << “ “;
    }
    
    
 ### Some functions affiliated with stack

  
| Functions | Purpose |
|--|--|
| st.begin() |  |
| st.end() |
| st.rbegin() |  |
| st.rend() |  |
| st.insert() / st.emplace() |  |
| st.size() |  |
| st.empty() |  |
| st.erase()|  |
| st.clear()|  |
| st.swap() |  |
| st.find() |  |
| st.count() |  |
| st.lower_bound(); |  |
| st.upper_bound(); |  |


  
## MAP The magic array

  

You might be thinking what is co cryptic about maps. Well maps allow index of the element in the map to be of different datatype. That is you can have and index of type string, char, float, double etc.Well that may sound weird but its actually not. Data in maps is stored in “key-value” pairs and these “keys” have traits similar to index. Lets take an example to understand it better

  

ar[2] = 14;

  

The above statement will give us the value stored at index “2” of array “ar”.

  

mp[“Apple”] = 4;

  

The above statement will give us the value stored with key “Apple” of map “mp”.

  

  

### Decleration:

  

    map< Data_Type , Data_Type> Map_Name ; // Example : map<string,int> mp ;



  
### Initialization:

  

There are follwing methods to initialize vectors:

(i) Method 1:

    st = { {“Red”,1} , {“Blue”, 2} , {“Green”,5} , {“Yellow”,99} , {“Orange”,21} , {“Black”43} }


Or

    st = { make_pair(“Red”,1) , make_pair(“Blue”, 2) , make_pair(“Green”,5) , make_pair(“Yellow”,99) , make_pair(“Orange”,21) , make_pair(“Black”43) }



This is quiet different to the way array is initialized as we have to write the data in pairs of key and value, this method too is adopted when we have limited number of elements to be initialized,

  
(ii) Method 2:

    st.insert(make_pair(“Apple”, 5));
    st.insert(make_pair(“Kiwi”, 12));


insert() is funciton provided in set container . It adds element into the set if its not present in the set already.

  

(iv) Using pre-existing array, string, set, map, vector etc Similar to 3rd method this too can only be used while declaration.

    map< string, int > mp(ar, ar + size_of_array) ; // Here ar is the name of the array
    map<string, float> mp(v.begin(), v.end()) ; // Here v is the name of the vector
    map< string, char> mp(mp2.begin(), mp2.end()) ; // Here mp2 is the name of the another


But the point to be noted here is the array,vector,set etc has to be in the form of pairs, as given below:

  

    pair<srting,int > ar[array_size];
    vector< pair < string, float> > v;

`

### Traversing : 

Similar to sets, traversal in maps can achieved using only 1 method :

  

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

  
 ### Some functions affiliated with map
 
  
| Name | Purpose |
|--|--|
| mp.begin() |  |
| mp.end() |
| mp.rbegin() |  |
| mp.rend() |  |
| mp.insert() / st.emplace() |  |
| mp.size() |  |
| mp.empty() |  |
| mp.erase()|  |
| mp.clear()|  |
| mp.swap() |  |
| mp.find() |  |
| mplower_bound() |  |
| mp.upper_bound() |  |
| mp.at() / mp[] |  |

    

## STACK (Ctrl + Z)

  

The characteristics of this container is similar to that of stacks in real world like stacks of plates or of chairs. Similar to stacks in physical world contents of a stacks in c++ container are stored and accessed in a unique manner. It follows the FILO (First In Last Out) method of storing and LIFO (Last In First Out) of accessing its content/data. The Crtl + Z (undo) function in computer is implemented using datastructure similar to stack.

  

### Decleration:

  

    stack< Data_Type > Stack_Name ; // Example : stack<string> stk;



  

###  Initialization:

There are follwing methods to initialize vectors:

  

  
(i) Method 1:

    stk.push(“Apple”) ;
    stk.push(“Kiwi”) ;


push() is funciton provided in stack container . It adds an element to top/end of stack.

  
Method 2:
Using pre-existing vector, list & stack Similar to 3rd method this too can only be used while declaration.

    stack<int,vector<int> > stk (v); // Here v is the name of the vector
    stack<int,list<int> > stk (l); // Here l is the name of the list.
    stack<int> stk (stk2); // Here stk2 is the name of the an already existing stack.

  


One thing to be careful about in the above method is that while initialization using list and vector is similar whereas that using stack its different.

  

###  Traversing :

  

Actually we cant traverse through a stack although we can use a method which gives us an illusion that we are traversing through the stack.

  

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
		    cout << stk.top() << endl;
		    stk.pop();
	    }
	    
	    return 0;
    }

   
The top() function gives the value of the element at top/end of the stack while pop() removes the element at the top/end. Using this two function inside the loop gives us an illusion that we are traversing through the stack

  

The function works in the following manner:

(A) top() functions prints the value at the top of the stack.
(B) pop() function pops the element at the top of the stack hence reducing the size of the stack by one unit.
(C ) size() function checks if size of the stack is greater that 0 as if its 0 all the elements must have been already poped out.
(D) The loop stops when the stack is empty i.e. size of the stack is 0.

  

This method can only be used once as after it stack eventually becomes empty.

 ### Some functions affiliated with stack
  
| Name | Purpose  |
|--|--|
| stk.push() |  |
| stk.pop() |  |
| stk.top() |  |
| stk.size() |  |
| stk.empty() | |
| stk.swap() |  |
| stk.emplace() |  |



  

  



  



  



  



  



  



  


> Written with [StackEdit](https://stackedit.io/).
