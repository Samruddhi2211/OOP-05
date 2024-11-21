# OOP-05
Experiment 5: 
Write a function template selection Sort. Write a program that inputs,
sorts and outputs an integer array and a float array.

#include<iostream>
using namespace std;
#define Size 10
int n;
template<class T>
void selection(T A[Size])
{
           int i, j,Min;
            T temp;
            for (i = 0; i <= n - 2; i++)
            {
                       Min = i;
                       for (j = i + 1; j <=n - 1; j++)
                        {
                                    if(A[j]<A[Min])
                                                Min= j;
                        }
                        temp = A[i];
                        A[i] = A[Min];
                        A[Min] = temp;
            }
            cout << "\n The sorted List is ...\n";
            for (i = 0; i<n; i++)
                        cout<<"\t"<<A[i];
      int main()

{
            int i, A[Size];
            float B[Size];
           cout<<"\n\t\t Selection Sort\n ";
            cout << "\n\t Handling Integer elements ";
            cout<<"\n How many elements are there ? ";
           cin>>n;
            cout<<"\n Enter the integer elements\n ";
           for (i = 0; i<n; i++)
           cin>>A[i];
            selection(A);
            cout << "\n\t Handling Float elements ";
            cout << "\n How many elements are there ? ";
            cin >> n;
            cout << "\n Enter the float elements\n ";
           for (i = 0; i<n; i++)
            cin >> B[i];
            selection(B);
           cout << "\n";
            return 0;
}


Output
Selection Sort
Handling Integer elements
How many elements are there ? 5
Enter the integer elements
30
50
40
20
10
The sorted List is ...
10      20   30      40      50
----------------------------------------------------------------------------------

Handling Float elements
How many elements are there ? 5
Enter the float elements
44.44
22.22
11.11
55.55
33.33

The sorted List is ...
11.11   22.22  33.33   44.44   55.55
