# Experiment-8
### AIM
To create a matrix by taking inputs from user and doing operations on it.

### Software Used-
VS Code

### Problem Statement
1.) To make a matrix by taking number of rows and column from user.

2.) To make a matrix by taking number of rows and column from user and do their addition and multiplication.

3.) To add the diagonal elements of the matrix.

4.) To make the transpose of a matrix.

## Theory
What is an Array?<br>
An array is like a row of boxes, where each box can hold a value. All the boxes are lined up in a row, and each box has a position number, called an index, which tells you where it is.

What is a Matrix?<br>
A matrix is like a grid or table where numbers are arranged in rows and columns. Think of it like a game board where each cell holds a number.

Matrix Addition:-<br>
To add two matrices, they must be the same size (same number of rows and columns). You simply add the number in each cell of the first matrix to the number in the same cell of the second matrix. For example, if one matrix has the number 1 in a cell and the other has 2 in the same cell, the result will be 3.

Matrix Multiplication:-<br>
Multiplying matrices is a bit more complicated. You need to make sure that the number of columns in the first matrix is the same as the number of rows in the second matrix. The result is a new matrix where each number is calculated by combining numbers from rows in the first matrix with columns in the second matrix in a special way.

Diagonal Elements:-<br>
In a square matrix (where the number of rows and columns is the same), there are two main diagonals:
Main Diagonal: Runs from the top-left corner to the bottom-right corner.
Secondary Diagonal: Runs from the top-right corner to the bottom-left corner. Diagonal elements are just the numbers found along these lines.

Transpose of a Matrix:-<br>
To transpose a matrix, you flip it over its diagonal. This means turning the rows into columns and columns into rows. So if the original matrix has numbers arranged in a certain way, the transposed matrix will have those numbers rearranged so that the first row becomes the first column, the second row becomes the second column, and so on.

## Program Codes:-

1. USER DEFINED ARRAY
``` javascript
//Sharvari Murade
//23070123088
#include<iostream>
using namespace std;
int main()
{
    int r,c , i , j;
    cout<< " Enter number of rows: ";
    cin>> r ;
    cout<<" Enter number of columns: ";
    cin>> c;
    int arr[r][c];
    for (i=0 ; i < r ; i++)
    {
        for(j = 0 ; j < c ; j++)
        {
            cout<< "Enter elements ("<<i<< "," <<j<<"): "  ;
            cin>>arr[i][j];
        }
    }
for (i=0 ; i<r ; i++)
{
    for(j = 0; j< c ; j++ )
    { 
        cout<< " "<< arr[i][j];
    }
    cout<<endl;
}

}
```

2.ARRAY OPERATIONS
``` javascript
//Sharvari Murade
//23070123088
#include<iostream>
using namespace std;
int main()
{
    int a,b,c,d , i , j ,k , e, f;
    cout<< " Enter matrix-1 rows: ";
    cin>> a ;
    cout<<" Enter matrix-1 columns: ";
    cin>> b;
    cout<< " Enter matrix-2 rows: ";
    cin>> c ;
    cout<<" Enter matrix-2 columns: ";
    cin>> d;

    int mat1[a][b];
    int mat2[c][d];
    int add [a][b];
    int mul [a][d];
    
 if ( a !=c || b!=d)
    {
        cout<< "Matrix cannot be added as dimension do not match."<<endl;
    }
    else
{for (i=0 ; i < a ; i++)
    {
        for(j = 0 ; j < b ; j++)
        {
            cout<< "Enter elements ("<<i<< "," <<j<<"): "  ;
            cin>>mat1[i][j];
        }
    }


    for (i=0 ; i < c ; i++)
    {
        for(j = 0 ; j < d ; j++)
        {
            cout<< "Enter elements ("<<i<< "," <<j<<"): "  ;
            cin>>mat2[i][j];
        }
    }

for (i=0 ; i < a ; i++)
    {
        for(j = 0 ; j < b ; j++)
        {
            add[i][j] = mat1[i][j] + mat2 [i][j];

        }
    }
cout<<"SUM OF MATRIX: "<<endl;
for (i=0 ; i< a ; i++)
{
    for(j = 0; j< b ; j++ )
    { 
        cout<< " " <<add[i][j];
    }
    cout<<endl;
}}

    if( b != c)
{
    cout<< "Matrices cannot be multiplied as dimensions do not match." <<endl;
    return 1;
}
for(i = 0; i<a ; i++)
{
    for( j = 0; j<d ; j++)
    {
        mul[i][j] = 0;
        for( k=0; k<b ; k++)
        {
            mul[i][j] += mat1[i][k] * mat2[k][j];
        }
    }
}
cout << "PRODUCT OF MATRIX: "<<endl;
for (i=0 ; i< a ; i++)
{
    for(j = 0; j< b ; j++ )
    { 
        cout<< " " <<mul[i][j];
    }
    cout<<endl;
}
}
```

3.ARRAY DIAGONAL SUM
``` javascript
// Sharvari Murade
// 23070123088
#include<iostream>
using namespace std;
int main()

{ int i,j, r1, c1, sum=0, sum2=0;
 cout<<"Enter number of rows and cloumns of first matrix: ";
cin>>r1>>c1;
int mat1[r1][c1];

if(r1!=c1)
{
    cout<<"ONLY SQUARE MATRICES ARE TO BE ENTERED!"<<endl;
}
else
{
for(i=0; i<r1; i++)
{
    for (j=0 ; j<c1 ; j++)
    {
        cout<<"Enter elements ("<<i<< "," <<j<<"): ";
        cin>>mat1[i][j];
    }
}


for(i=0; i<r1; i++)
{
    for (j=0 ; j<c1 ; j++)
    { if(i==j)
    {
        sum +=mat1[i][j];
    }
    if (i+j == r1-1)
    sum2 += mat1[i][j];
    }
    }
    cout<< "Sum of diagoal elements is: "<<sum<<endl;
    cout<<"Sum of diagonal elements is: "<<sum2<<endl;
}

}
```

4. ARRAY TRANSPOSE
``` javascipt
//Sharvari Murade
//23070123088
#include<iostream>
using namespace std;
int main()
{
    int r,c , i , j;
    cout<< " Enter number of rows: ";
    cin>> r;
    cout<<" Enter number of columns: ";
    cin>> c;
    int arr[r][c], arr2[c][r];
    for (i=0 ; i < r ; i++)
    {
        for(j = 0 ; j < c ; j++)
        {
            cout<< "Enter elements ("<<i<< "," <<j<<"): "  ;
            cin>>arr[i][j];
        }
    }
for (i=0 ; i<r ; i++)
{
    for(j = 0; j< c ; j++ )
    { 
        cout<< "  "<< arr[i][j];
    }
    cout<<endl;
}
for (i=0 ; i<c ; i++)
{
    for(j = 0; j< r ; j++ )
    { 
        arr2[i][j]= arr[j][i];
    }

    
}
cout<<endl;
for (i=0 ; i<c ; i++)
{
    for(j = 0; j< r ; j++ )
    { 
        cout<< " "<< arr2[i][j];
    }
    cout<<endl;
}

}
```
## Outputs
1. USER DEFINED ARRAY<br>
   <img width="311" alt="Screenshot 2024-08-29 at 3 49 24 PM" src="https://github.com/user-attachments/assets/3227b17b-8d02-43a1-acd0-f529be97cf8c">


   
2. ARRAY OPERATIONS<br>
   <img width="296" alt="Screenshot 2024-08-29 at 3 53 50 PM" src="https://github.com/user-attachments/assets/0b4e4547-d4a8-442a-8ab3-cf432c94170a">


   
3. ARRAY DIAGONAL SUM<br>
   <img width="448" alt="Screenshot 2024-08-29 at 3 56 40 PM" src="https://github.com/user-attachments/assets/eac067f1-2202-4b30-b14a-ef1f8f89e6a8">



4. ARRAY TRANSPOSE<br>
   <img width="315" alt="Screenshot 2024-08-29 at 3 58 31 PM" src="https://github.com/user-attachments/assets/d31bb7b0-bb95-46c2-8596-83a45d4ce2f1">

## Conclusion
Here's a simple summary of what you’ve learned:

Create a Matrix: Gather numbers from the user to form a grid of rows and columns.

Add Matrices: Combine two grids by adding the numbers in the same positions from each grid.

Multiply Matrices: Calculate a new grid by mixing rows from one grid with columns from another grid, but only if the grids have compatible sizes.

Diagonal Sum: Find the total of the numbers along the main diagonal (from top-left to bottom-right) and the secondary diagonal (from top-right to bottom-left) of a square grid.

Transpose Matrix: Flip the grid by swapping rows with columns.

This covers the basics of working with matrices, including creating, combining, and transforming them.
