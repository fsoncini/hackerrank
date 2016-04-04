# hackerrank
AGP 1


Given that my background is not in computer science I have worked hard on solidifying my fundamentals in C++.
I’ve tackled most of the challenges in the introduction section, ranging from simple conditional statements to pointers and overloaded functions.
Of particular interest was the Classes section, where I went through exercise that related to constructors, virtual functions, and virtual constructors.
I have also familiarized with notions of inheritance, multi level inheritance and accessing inherited functions.

The algorithms sections was a bit more challenging.

The goal was to achieve 400 points and I reached that in the C++ section, and added 120 on the algorithms section.





##C++ CHALLENGES 

###Introduction

####Hello, World !

```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    printf("Hello, World!");
    return 0;
}
```


###Input and Output
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int n1 = 0;
    int n2 = 0;
    int n3 = 0;
    cin >> n1 >> n2 >> n3;
    
    cout << n1+n2+n3 << endl;
    
    return 0;
}
```

Basic Data Types
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    // Complete the code.
    int i = 0;
    long l = 0;
    long long ll = 0;
    char a = ' ';
    float f = 0.0f;
    double d = 0.0;
    
    scanf("%d %ld %lld %c %f %lf", &i, &l, &ll, &a, &f, &d);
    printf("%d \n%ld \n%lld \n%c \n%f \n%lf", i, l, ll, a, f, d);
    
    
    return 0;
}
```

Conditional Statements

```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */  
    int n = 0;
    cin >> n;
    if (n == 0) {
        cout << "zero";
    }
    else if (n == 1) {
        cout << "one";
    }
    else if (n ==2) {
        cout << "two";
    }
    else if (n==3) {
        cout << "three";
    }
    else if (n==4) {
        cout << "four";
    }
    else if (n==5) {
        cout << "five";
    }
    else if (n==6) {
        cout << "six";
    }
    else if (n==7) {
        cout << "seven";
    }
    else if (n==8) {
        cout << "eight";
    }
    else if (n==9){
        cout << "nine";
    }
    else {
        cout << "Greater than 9";
    }
   return 0;
}
```

For Loop

```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    // Complete the code.
    
    int a = 0;
    int b = 0;
    
    cin >> a >> b;
    
    for (int i = a; i <= b; i ++) {
        if (i > 9) {
            if (i%2 == 0) {
                cout << "even" << endl;
            }
            else if (i%2 != 0){
                cout << "odd" << endl;
            }
        }
        
        if (i == 1) {
        cout << "one" << endl;
        } 
        else if (i ==2) {
            cout << "two" << endl;
        }
        else if (i==3) {
            cout << "three" << endl;
        }
        else if (i==4) {
            cout << "four" << endl;
        }
        else if (i==5) {
            cout << "five" << endl;
        }
        else if (i==6) {
            cout << "six" << endl;
        }
        else if (i==7) {
            cout << "seven" << endl;
        }
        else if (i==8) {
            cout << "eight" << endl;
        }
        else if (i==9){
            cout << "nine" << endl;
        }
        
    }
        
    
        return 0;
}
```

Functions

```cpp
#include <iostream>
#include <cstdio>
using namespace std;

/*
Add `int max_of_four(int a, int b, int c, int d)` here.
*/
int max_of_four(int a, int b, int c, int d) {
 
    int max = 0;
    
    if (a > b && a > c && a > d) {
        max = a;
    }
    else if (b > a && b > c && b > d) {
        max = b;
    }
    else if (c > a && c > b && c > d) {
        max = c;
    }
    else if (d > a && d > b && d > c) {
        max = d;
    }

    return max;
}

int main() {
    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    int ans = max_of_four(a, b, c, d);
    printf("%d", ans);
    
    return 0;
}
```

Pointer

```cpp
#include <stdio.h>
#include <math.h>

void update(int *a,int *b) {
    // Complete this function    
    int sum = 0;
    int diff = 0;
    int d = 0;
    int d1 = 0;
    d = *a;
    d1 = *b;
    sum = d + d1;
    diff = fabs(d-d1);
    *a = sum;
    *b = diff;
       
}

int main() {
    int a, b;
    int *pa = &a, *pb = &b;
    
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}
```


Arrays Introduction

```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int num_ints = 0;
    int input = 0;
    cin >> num_ints;
    
    int array[num_ints];
   
    
    for (int i = 0; i < num_ints; i++ ){
        cin >> array[i];        
        }
    
    for (int i = num_ints - 1; i >=0; i--){
        cout << array[i] << " ";
    }
    
    return 0;
}

```
Operator Overloading

```cpp
class Matrix {
    public:
        vector<vector<int>> a;
   
          Matrix &operator + (const Matrix &rhs) {
              for (int i = 0; i < rhs.a.size(); i++) {
                  for (int j = 0; j < rhs.a[0].size(); j++) {
                      this -> a[i][j] = this -> a[i][j]+ rhs.a[i][j];                     
                  }
              }
              return *this;
          }
    
};
```

Variable Sized Arrays

```cpp
    //number of integer sequences
    int n = 0;
    //number of queries 
    int q = 0;

    cin >> n;
    cin >> q;
    int **nums = new int*[n]; 
    for (int i = 0; i < n; i++) {  
        int size = 0;
        cin >> size;
        int *seq = new int[size]; 
        for (int j = 0; j <size; j++){
            int s = 0;
            cin >> s;
            seq[j] = s;
        }
        *(nums +i) = seq;        
    }

    for (int i = 0; i < q; i++){
        int a = 0;
        int b = 0;
        cin >> a >> b;
        cout << nums[a][b] << endl;
   }
	return 0;

}    
```
Overload Operators

```cpp
//Overload operators + and << for the class complex
//+ should add two complex numbers as (a+ib) + (c+id) = (a+c) + i(b+d)
//<< should print a complex number in the format "a+ib"
Complex operator+(const Complex &a, const Complex &b){
	Complex c;
	c.a = a.a + b.a;
	c.b  =a.b + b.b;
	return c;
}

ostream& operator<<(ostream& out,const Complex &c) {
		return out << c.a << "+i" << c.b;
    }
```

Virtual Functions

```cpp
static int idProf = 0;
static int idStud = 0;

class Person {
    protected:
        string name;
        int age;
    public: 
        virtual void getdata() {
            cin >> name;
            cin >> age;
        } 
        virtual void putdata() {
            cout << name << " " << age << " ";
        } 
        
};

class Professor : public Person {
    private:
        int publications = 0;
        int id = 0;

    public: 
        Professor() {
            idProf ++;
        }
        
        void getdata() { 
            Person :: getdata();
            cin >> publications;
            id = idProf;
        }
        
        void putdata() {
            Person :: putdata(); 
            cout << publications << " " << id << endl;
        }
};

class Student : public Person {
    private:
        int marks[6];
        //cur id
        int id;
    public:
        Student() {
            idStud++;
        }      
        
        void getdata() {
            Person::getdata();
            for (int i = 0; i < 6; i++) {
                cin >> marks[i];
            }
            id = idStud;
        }
    
        void putdata() {
            Person::putdata();
            int sum = 0;
            for (int i = 0; i < 6; i++) {
                sum += marks[i];
            }
            cout << sum << " " << id << endl;        
        }         
};
```

Strings

Strings
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
   // Complete the program
    string a = " ";
    string b = " ";
    
    cin >> a >> b;
    int len_a = a.size();
    int len_b = b.size();
    
    cout << len_a << " " << len_b << endl;
    cout << a + b << endl;
    
    char first_a = a[0];
    char first_b = b[0];
    
    a[0] = first_b;
    b[0] = first_a;
    
    cout << a << " " << b << endl;
    
    return 0;
}
```

Stringstream
```cpp
#include <sstream>
#include <vector>
#include <iostream>
using namespace std;

vector<int> parseInts(string str) {
   // Complete this function
    stringstream ss(str);
    vector < int > v;
    int nums;
    char ch;
    while (ss >> nums) {
        v.push_back(nums);
        ss >> ch;
    }
    return v;
}

int main() {
    string str;
    cin >> str;
    vector<int> integers = parseInts(str);
    for(int i = 0; i < integers.size(); i++) {
        cout << integers[i] << "\n";
    }
    
    return 0;
}
```

Classes

Structs

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


struct Student {
    int age;
    string first_name;
    string last_name; 
    int standard;
};



int main() {
    Student st;
    
    cin >> st.age >> st.first_name >> st.last_name >> st.standard;
    cout << st.age << " " << st.first_name << " " << st.last_name << " " << st.standard;
    
    return 0;
}


Class

#include <iostream>
#include <sstream>
using namespace std;

/*
Enter code for class Student here.
Read statement for specification.
*/

class Student {
    private:
        int age;
        string first_name;
        string last_name;
        int standard;
    public:
        void set_age(int a) {
            age = a;
            }
        int get_age(){
            return age;
        }
        void set_first_name(string fn) {
            first_name = fn;
        }
        string get_first_name(){
            return first_name;
        }
        void set_last_name(string ln) {
            last_name = ln;
        }
      
        string get_last_name() {
            return last_name;
        }
        void set_standard(int st) {
            standard = st;
        }
        int get_standard(){
            return standard;
        }
         
        string to_string(){
            stringstream ss;
            ss << age << ","<< first_name << "," << last_name <<","<< standard;
            string s = ss.str();
            return s;
        }
};
                 
                                    

int main() {
    int age, standard;
    string first_name, last_name;
    
    cin >> age >> first_name >> last_name >> standard;
    
    Student st;
    st.set_age(age);
    st.set_standard(standard);
    st.set_first_name(first_name);
    st.set_last_name(last_name);
    
    cout << st.get_age() << "\n";
    cout << st.get_last_name() << ", " << st.get_first_name() << "\n";
    cout << st.get_standard() << "\n";
    cout << "\n";
    cout << st.to_string();
    
    return 0;
}

Classes and Objects

// Write your Student class here
class Student {
    private:              
        int scores[5];
    public:
        void input(){
             cin >> scores[0] >> scores [1] >> scores[2] >> scores[3] >> scores[4];
        }
        int calculateTotalScore() {
            int total = 0;
            for (int i = 0; i < 5; i++) {
                total += scores[i];
            }
            return total;
    }
};


C++ Class Templates

template<class T>
class AddElements{
	T e;
public:
	AddElements(const T &_e):e(_e){}
	T add(const T &a){
        return e+a;
    }
	T concatenate(const T &a){
        return e+a;
    }
};

Box it!


//Implement the class Box  
//l,b,h are integers representing the dimensions of the box
class Box {
  public:
    int length = 0;
    int breadth = 0;
    int height = 0;;
    
    Box() {
        BoxesCreated++;
    }
    
    Box(int l, int b, int h) {
        length = l;
        breadth = b;
        height = h;
        BoxesCreated++;
    }
    
    Box(Box& b) {
        length = b.length;
        breadth = b.breadth;
        height = b.height;
        BoxesCreated++;
    }
    
    ~Box() {
        BoxesDestroyed++;
    }
    
    int getLength() {
        return this->length;
    }

    int getBreadth() {
        return this->breadth;
    }
    
    int getHeight() {
        return this->height;
    }
    
    long long CalculateVolume() {
        return (long long)length * breadth * height;
    }
    
    bool operator<(Box &b) {
        if(this->length != b.length) return this->length < b.length;
        if(this->breadth != b.breadth) return this->breadth < b.breadth;
        return this->height < b.height;
    }
    
};

ostream& operator<<(ostream& out, const Box b) {
    out << b.length << " " << b.breadth << " " << b.height;
    return out;
} 


// The class should have the following functions : 

// Constructors: 
// Box();
// Box(int,int,int);
// Box(Box);

// Destructor
// ~Box()
// {

// }

// int getLength(); // Return box's length
// int getBreadth (); // Return box's breadth
// int getHeight ();  //Return box's height
// long long CalculateVolume(); // Return the volume of the box

//Overload operator < as specified
//bool operator<(Box &b)

//Overload operator << as specified
//ostream& operator<<(ostream& out, Box B)



Vector-Sort

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */  
    int size = 0;
    vector <int> v;
    cin >> size;
    for (int i=0; i < size; i++) {
        int n = 0;
        cin >> n;
        v.push_back(n);
    }
    sort(v.begin(), v.end());
    for (int i = 0; i < v.size(); i++) {
        cout << v[i] << " ";
        
    }
   
    return 0;
}

Vector-Erase

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int n = 0;
    int pos = 0;
    int a = 0;
    int b = 0;
    vector <int> v;
    cin >> n;
    
    for (int i = 0; i < n; i++) {
        int s = 0;
        cin >> s;
        v.push_back(s);
    }
  
    cin >> pos;
    v.erase(v.begin()+(pos-1));
    
    cin >> a;
    cin >> b;

    v.erase(v.begin()+(a-1), v.begin()+(b-1));
    cout << v.size() << endl;
    
    for (int i = 0; i < v.size(); i ++) {
        cout << v[i] << " ";
    }
    
    return 0;
}

Inheritance

Inheritance Introduction

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


class Triangle{
    public:
       void triangle(){
           cout<<"I am a triangle\n";
       }
};
class Isosceles : public Triangle{
    public:
       void isosceles(){
          cout<<"I am an isosceles triangle\n";
       }
        //Write your code here.
        void description() {
            cout << "In an isosceles triangle two sides are equal\n";
        };
};
int main(){
    Isosceles isc;
    isc.isosceles();
    isc.description();
    isc.triangle();
    return 0;
}



Rectangle Area

class Rectangle {
    protected:
        int w = 0;
        int h = 0;
    public:
     void Display() {
         cout<< w <<" "<< h <<endl;
     }
};

class RectangleArea : public Rectangle {
    private:
        int a = 0;
    public:
        void Input(){
            cin >> w >> h;
        }
    void Display(){
        cout << w*h <<endl;
    }
};


Multi Level Inheritance


#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

class Triangle{
   public:
      void triangle(){
         cout<<"I am a triangle\n";
      }
};

class Isosceles : public Triangle{
     public:
        void isosceles(){
          cout<<"I am an isosceles triangle\n";
        }
};

class Equilateral : public Isosceles {
    
    public:
        void equilateral () {
            cout << "I am an equilateral triangle" << endl;
        }
};

   
//Write your code here.
int main(){
  
    Equilateral eqr;
    eqr.equilateral();
    eqr.isosceles();
    eqr.triangle();
    return 0;
}

Accessing Inherited Functions

class D : public A,B,C
{
	int val;
	public:
		//Initially val is 1
		D()
		{
			val=1;
		}

		//Implement this function
		void update_val(int new_val)
		{
			for(;new_val%2==0;new_val/=2)
                {A::func(val);}
			for(;new_val%3==0;new_val/=3)
                {B::func(val);}
			for(;new_val%5==0;new_val/=5)
                {C::func(val);}
		}
		//For Checking Purpose
		void check(int); //Do not delete this line.
};



ALGORITHMS CHALLENGES

Warmup

Solve Me First

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int solveMeFirst(int a, int b) {
 // Hint: Type return a+b; below
    return a + b;
  
}
int main() {
  int num1, num2;
  int sum;
  cin>>num1>>num2;
  sum = solveMeFirst(num1,num2);
  cout<<sum;
  return 0;
}

Simple Array Sum

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main(){
    int n;
    int sum = 0;
    cin >> n;
    vector<int> arr(n);
    for(int arr_i = 0;arr_i < n;arr_i++){
       cin >> arr[arr_i];
       sum += arr[arr_i]; 
    }
    cout << sum;
    return 0;
}

A Very Big Sum

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main(){
    int n;
    long int sum = 0;
    cin >> n;
    vector<int> arr(n);
    for(int arr_i = 0;arr_i < n;arr_i++){
       cin >> arr[arr_i];
       sum += arr[arr_i]; 
    }
    cout << sum;
    return 0;
}


Implementation

Angry Professor

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main(){
    //t = number of test cases
    int t;
    cin >> t;
    for(int a0 = 0; a0 < t; a0++){ //a = time of arrival
        int n; // n = students in the class
        int k; //cancellation threshold
        cin >> n >> k;
        vector<int> a(n); //a(n) times of arrival of students in the class (<n)
        for(int a_i = 0;a_i < n;a_i++){
           cin >> a[a_i];
        }
    vector<int> on_time;    
    for (int i = 0; i < n; i++) {
        if (a[i] <= 0) {on_time.push_back(a[i]);}
        }
   
        int j = 0;
        j = on_time.size();
    
        if (j >= k) {
            cout << "NO" << endl;
        }
        else cout << "YES" << endl;
    }
    
    return 0;
}

Sherlock and the Beast

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <string>
using namespace std;

int main(){
    int t;
    cin >> t;
    
    char five = '5';
    char three = '3';
    
    for(int a0 = 0; a0 < t; a0++){
        int n;
        cin >> n;
        int k = 0;
        k = n;
        
        while (k%3!=0) {
            k-=5;
        }
        if (k < 0) {
            cout << -1 << endl;
        }
        else {
            cout << string(k, five) + string(n-k, three) << endl; //fromt the STL to multiply chars in string.
        }
    }
    return 0;
}

