# R
## Syntax
### variable
`variable` must be an `identifier`.

An `identifier` in R must satisfy these requirements. Like that in other programming language.

+ It only consists of one or many uppercase letter (i.e. `A` to `Z`), lowercase letter (i.e. `a` to `z`), digit (i.e. `0` to `9`), and underscore (i.e. `_`).
+ The first character must be an uppercase letter or lowercase letter.

> [!IMPORTANT]
> `identifier` in R is case-sensitive.

#### Definition of variable 
It is first defined if and only if it is assigned at first time.

#### Assigment of variable
Use the symbol `<-` (recommend) or `=`.

assignment in R.

| symbol | is forbidden? | recommended | description |
| ------- | ------------ | ----------- | ---------   |
| `<-` | NO, it can be used in all contexts. | Yes | |
| `=` | Sometimes, it is forbidden in some contexts. | No | |
|  `<<-` | | No | alias symbol of `<-` | 
|  `->` | | No | alias symbol of `<-` | 
|  `->>` | | No | alias symbol of `<-` | 

> [!TIP]
> Like other programming language, many variables can be assigned with same value in one line. See below example (Example 2).

> [!NOTE]
> These are equivalent
> ```
> myVar1 <- 3
> ```
>
>
> ```
> 3 -> myVar1
> ```


+ Example 1:
  
```
myVar1 <- '123'
```

will define a variable named `myVar1` and assign value `'123'` to the variable.

+ Example 2:

```
myVar1 <- 3
myVar1 
myVar1 <<- 3
myVar1 
3 -> myVar1
myVar1 
3 ->> myVar1
myVar1
```

will output

```
3
3
3
3
```

+ Example 3:
  
```
myVar1 <- myVar2 <- myVar3 <- '123'
```

will define a variable named `myVar1` and assign value `'123'` to the variable. And so for `myVar2` and `myVar3`.

#### Print the value of variable 
Either 
- simply type the name of `variable` only if it is NOT in loop.
- use the formal approach. Use `print()` function.

+ Example 1:

```
myVar1 <- '123'
myVar1
```

will output 

```
'123'
```

+ Example 2:

```
myVar1 <- '123'
print(myVar1)
```

will also output 

```
'123'
```

+ Example 3:

```
for (x in 1:10) {
  print(x)
}
```

will output 

```
1
2
3
4
5
6
7
8
9
10
```

### Data type

Simple data type of variable in R.

| Data type |
| --------- |
| numeric |
| integer |
| complex |
| string |
| boolean |

Complex data structure of variable in R.

| Data structure |
| --------- |
| Vector |
| List |
| Array |
| Martix |
| DataFrame |
| Factor |

### Operation
#### Addition (i.e. `+`)
Use `+` symbol to add two numbers.

+ Example 1:

```
9 + 5
```

will output

```
14
```

#### Subtraction (i.e. `-`)
Use `-` symbol to subtract one number to another number.

+ Example 1:

```
9 - 5
```

will output

```
4
```

#### Multiplication (i.e. `*`)
Use `*` symbol to multiply two numbers.

+ Example 1:

```
9 * 5
```

will output

```
45
```

#### Division (i.e. `/`)
Use `/` symbol to divide one number into another number.

+ Example 1:

```
9 / 5
```

will output

```
1.8
```

+ Example 2:

```
9L / 5
```

will output

```
1.8
```

+ Example 3:

```
9L / 5L
```

will output

```
1.8
```

#### Exponent

+ Example 1:

```
3 ^ 4
```

will output

```
81
```

#### Modulus (Remainder from division)

+ Example 1:

```
7 %% 4
```

will output

```
3
```

+ Example 2:

```
5 %% 4
```

will output

```
1
```

+ Example 3:

```
8 %% 4
```

will output

```
0
```

+ Example 4:

```
-7 %% 4
```

will output

```
1
```

+ Example 5:

```
-5 %% 4
```

will output

```

```

+ Example 6:

```
5 %% -4
```

will output

```
-3
```

+ Example 7:

```
8 %% -4
```

will output

```
0
```

+ Example 8:

```
-5 %% -4
```

will output

```
-1
```

+ Example 9:

```
5 %% 0
```

will output

```
NaN
```

#### Integer Division
Integer divison (%/%) rounds the result down to the nearest whole number where the result is division of a number and another number.

+ Example 1:

```
15 %/% 2
```

will output

```
7
```

+ Example 2:

```
15 %/% 4
```

will output

```
3
```

+ Example 3:

```
13 %/% 4
```

will output

```
3
```


#### Concatenation
Use `paste()` function to concatenate two strings.

> [!CAUTION]
> **DON'T** use `+` symbol to concatenate two strings. Use `paste()` function.

+ Example 1:

```
text1 <- "R is"
text2 <- "awesome"

text3 <- paste(text1, text2)
text3 
```

will output

```
"R is awesome"
```

#### Math function
Here list a few math function to perform operations about numbers.

##### min
Get the minimum among these numbers.

+ Example 1:

```
min(1,5,9)
```

will output

```
1
```

> [!CAUTION]
> In math, it is NOT allow to compare two complex number which the imaginary part of two complex numbers are NOT same. Such as `1+2i v.s. 3+4i`.
> It is NOT allowed to compare two numbers even if their imaginary part are same. Such as `1+1i v.s. 3+1i`.
> And thus, they are NOT allowed to get minimum among complex numnbers and get maximum among complex numnbers.
> Same principle is applied to R.
> Here is Wrong Example.
> + Wrong Example 1:
> ```
> min(1+2i,5+6i,9+10i)
> ```
>
> will throw error.
>
> ```
> Error in min(1 + (0+2i), 5 + (0+6i), 9 + (0+10i)) :
> invalid 'type' (complex) of argument
> Execution halted
> ```
> + Wrong Example 2:
> ```
> min(1+1i,5+1i,9+1i)
> ```
>
> will throw error.
>
> ```
> Error in min(1 + (0+1i), 5 + (0+1i), 9 + (0+1i)) :
> invalid 'type' (complex) of argument
> Execution halted
> ```

##### max
Get the maximum among these numbers.

+ Example 1:

```
max(1,5,9)
```

will output

```
9
```

> [!CAUTION]
> See above !CAUTION.

##### abs
Get the absolute of a number.

+ Example 1:

```
abs(1)
```

will output

```
1
```

+ Example 2:

```
abs(-1)
```

will output

```
1
```

+ Example 3:

```
abs(0)
```

will output

```
0
```

+ Example 4:

```
abs(-0)
```

will output

```
0
```

+ Example 5:

```
abs(3+4i)
```

will output

```
5
```

+ Example 6:

```
abs(3-4i)
```

will output

```
5
```

##### sqrt
Get square root of a number.

+ Example 1:

```
sqrt(4)
```

will output

```
2
```

+ Example 2:

```
sqrt(0)
```

will output

```
0
```

> [!CAUTION]
> It is allowed to get square root of a complex number which its imaginary part is positive.

+ Example 3:

```
sqrt(4i)
```

will output

```
1.414214+1.414214i
```

+ Example 4:

```
sqrt(4+4i)
```

will output

```
2.197368+0.91018i
```

+ Example 5:

```
sqrt(-4+4i)
```

will output

```
0.91018+2.197368i
```

+ Example 6:

```
sqrt(-4i)
```

will output

```
1.414214-1.414214i
```

+ Example 7:

```
sqrt(4-4i)
```

will output

```
2.197368-0.91018i
```

+ Example 8:

```
sqrt(-4-4i)
```

will output

```
0.91018-2.197368i
```

> [!CAUTION]
> In R, it is NOT recommend to square root a negative number. It will return `NAN`.
> However, it is okay to get square root of a complex numnber, even if the real part and imaginary part BOTH negative. See above example. 

Wrong Example :
+ Wrong Example 1:

```
sqrt(-4)
```

will output

```
Warning message:
In sqrt(-4) : NaNs produced
```

### Comparison

+ Example 1:
  
```
10 > 9
10 == 9
10 < 9
```

will output

```
TRUE
FALSE
FALSE
```

+ Example 2:
  
```
10i == 9i
```

will output

```
FALSE
```

+ Example 3:
  
```
10i != 9i
```

will output

```
TRUE
```

+ Example 4:
  
```
9i == 9i
```

will output

```
TRUE
```

+ Example 5:
  
```
9i != 9i
```

will output

```
FALSE
```

> [!CAUTION]
> In R, it is NOT allow to compare two complex number which the imaginary part of two complex numbers are NOT same. Such as `1+2i v.s. 3+4i`.
> For more details, see above `R` -> `syntax` -> `Operation` -> `math function` -> `min` section.

Wrong Example:

+ Wrong Example 1:

```
10i > 9i
```

will output

```
Error in 0+10i > 0+9i : invalid comparison with complex values
Execution halted
```

### Conditional statement
#### if-else statement

+ Example 1:
  
```
a <- 200
b <- 33

if (b > a) {
  print("b is greater than a")
} else if (a == b) {
  print("a and b are equal")
} else {
  print("a is greater than b")
}
```

will output

```
a is greater than b.
```

+ Example 2:

```
x <- 41

if (x > 10) {
  print("Above ten")
  if (x > 20) {
    print("and also above 20!")
  } else {
    print("but not above 20.")
  }
} else {
  print("below 10.")
}
```

will output

```
"Above ten"
"and also above 20!"
```

### Repetive loop
#### for loop 

+ Example 1:
  
```
for (x in 1:6) {
  print(x)
}
```

will output

```
1
2
3
4
5
6
```

+ Example 2:

```
fruits <- list("apple", "banana", "cherry")
for (x in fruits) {
  print(x)
}
```

will output

```
"apple"
"banana"
"cherry"
```

+ Example 3:

```
dice <- c(1, 2, 3, 4, 5, 6)
for (x in dice) {
  print(x)
}
```

will output

```
1
2
3
4
5
6
```

#### while loop

+ Example 1:

```
i <- 1
while (i <= 6) {
  print(i)
  i <- i + 1
}
```

will output

```
1
2
3
4
5
6
```

> [!CAUTION]
> In above example, please assign to the variable `i`. If not assign, the value of variable `i` will NEVER change and thus, eithr it will get stuck in th
> infinite loop, or the loop is NOT executed.

#### break keyword

```
fruits <- list("apple", "banana", "cherry")
for (x in fruits) {
  if (x == "banana") {
    break
  }
  print(x)
}
```

will output

```
"apple"
```

#### next keyword

+ Example 1:

```
fruits <- list("apple", "banana", "cherry")
for (x in fruits) {
  if (x == "banana") {
    next
  }
  print(x)
}
```

will output

```
"apple"
"cherry"
```

### Function
#### Definition of function
To define a function, use `function` keyword with 0 or many `parameters`, then assign it to a function name

#### Invocation of function
To invoke a function, simply type the function name and pass `0` or many arguments.

+ Example 1:

```
myFunction <- function() {
  print("Hello World!")
}

myFunction()
```

will output 

```
"Hello World!"
```

+ Example 3: function that have parameter with default value.
  
```
myFunction <- function(country = "Norway") {
  print(paste("I am from", country))
}

myFunction("Sweden")
myFunction("India")
myFunction() # will use the default value, which is Norway
myFunction("USA")
```

will output

```
"I am from Sweden"
"I am from India"
"I am from Norway"
"I am from USA"
```

+ Example 4:

```
myFunction <- function(x) {
  return (5 * x)
}

print(myFunction(3))
print(myFunction(5))
print(myFunction(9))
```

will output

```
15
25
45
```

> [!CAUTION]
> The numner of `parameter` in function must match the numner of `argument` in function call.
> Otherwise, it will throw error at compile time. See below example.

Wrong example:

+ Wrong Example 1:

```
my_function <- function(fname, lname) {
  paste(fname, lname)
}
my_function("Peter")
```

will throw an error at complie time.

### Global variables

+ Example 1:
  
```
txt <- "global variable"
myFunction <- function() {
  txt = "fantastic"
  paste("R is", txt)
}
myFunction()
txt
```

will output

```
"global variable"


```

+ Example 2:

```
myFunction <- function() {
txt <<- "fantastic"
  paste("R is", txt)
}

myFunction()
print(txt)
```

will output

```
"fantastic"
```

+ Example 3:

```
txt <- "awesome"
myFunction <- function() {
txt <<- "fantastic"
  paste("R is", txt)
}

myFunction()
print(txt)
```

will output

```
"fantastic"
```

### Complex data structure
#### Vector
##### Constructor
+ Example 1:
  
```
fruits <- c("banana", "apple", "orange")
fruits
```

will output

```
"banana" "apple" "orange"
```

+ Example 2:
  
```
numbers <- c(1, 2, 3)
numbers
```

will output

```
1 2 3
```

+ Example 3:
  
```
numbers <- 1:10
numbers

```

will output

```
1 2 3 4 5 6 7 8 9 10
```

#### list
##### Constructor

> [!IMPORTANT]
> The index starts at 1.

+ Example 1:
  
```
thislist <- list("apple", "banana", "cherry")
thislist
```

will output 

```
apple", "banana", "cherry"
```

##### Access the index

+ Example 1:
  
```
thislist <- list("apple", "banana", "cherry")
thislist[1]
```

will output 

```
"apple"
```

##### Check elem contain 

+ Example 1:
  
```
thislist <- list("apple", "banana", "cherry")
"apple" %in% thislist
```

will output 

```
True
```

##### Insert the elem

+ Example 2:
  
```
thislist <- list("apple", "banana", "cherry")
append(thislist, "orange")
thislist
```

will output 

```
"apple" "banana" "cherry" "orange"
```

+ Example 2:
  
```
thislist <- list("apple", "banana", "cherry")
append(thislist, "orange" , after = 2)
thislist
```

will output 

```
"apple" "banana" "orange" "cherry" 
```

##### Remove the elem 

+ Example 1:
  
```
thislist <- list("apple", "banana", "cherry")
newlist <- thislist[-1]
thislist
```

will output 

```
"banana" "cherry" 
```

##### Range of Indexes

+ Example 1: 
  
```
thislist <- list("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
(thislist)[2:5]
```

will output 

```
"banana", "cherry", "orange", "kiwi"
```

##### Loop through a list

+ Example 1: 
  
```
thislist <- list("apple", "banana", "cherry")
for (x in thislist) {
  print(x)
}
```

will output 

```
"apple"
"banana"
"cherry"
```

##### Join two list

+ Example 1: 
  
```
list1 <- list("a", "b", "c")
list2 <- list(1,2,3)
list3 <- c(list1,list2)
list3
```

will output 

```
"a" "b" "c" 1 2 3
```

#### Matrix
##### Constructor

+ Example 1: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
thismatrix
```

will output 

```
    [,1] [,2]
[1,] 1 4
[2,] 2 5
[3,] 3 6
```

##### Access single row or single column by index

+ Example 1: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
# Access 1th row and 2th col.
thismatrix[1,2]
```

will output 

```
    [,1]
[1,] 4
```

+ Example 2: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
# Access 1th row.
thismatrix[1,]
```

will output 

```
    [,1] [,2] 
[1,] 1 4
```

+ Example 3: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
# Access 2th col.
thismatrix[,2]
```

will output 

```
    [,1]
[1,] 4
[2,] 5
[3,] 6
```

##### Access more than one row or column by index

+ Example 1: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
thismatrix[c(1,2),c(1,2)]
```

will output 

```
    [,1] [,2]
[1,] 1 4
[2,] 2 5
```

+ Example 2: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
thismatrix[,c(1,2)]
```

will output 

```
     [,1] [,2]
[1,] 1 4
[2,] 2 5
[3,] 3 6
```

+ Example 3: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
thismatrix[c(1,2),]
```

will output 

```
    [,1] [,2]
[1,] 1 4
[2,] 2 5
```

##### Add new columns at end
Use the `cbind()` function to add additional columns in a Matrix.

> [!IMPORTANT]
> The cells in the new column must be of the same length as the existing matrix.

+ Example 1: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
newmatrix <- cbind(thismatrix,c(7,8,9))
newmatrix
```

will output 

```
    [,1] [,2] [,3]
[1,] 1 4 7
[2,] 2 5 8
[3,] 3 6 9
```

##### Add new rows at end
Use the `rbind()` function to add additional rows in a Matrix.

> [!IMPORTANT]
> The cells in the new row must be of the same length as the existing matrix.

+ Example 1: 
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
newmatrix <- rbind(thismatrix,c(7,8))
newmatrix
```

will output 

```
    [,1] [,2]
[1,] 1 4 
[2,] 2 5 
[3,] 3 6
[4,] 7 8
```

##### Remove rows and columns by index

+ Example 1: Remove first row
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
newmatrix <- thismatrix[ -c(1),]
newmatrix
```

will output 

```
    [,1] [,2]
[1,] 2 5 
[2,] 3 6
```

+ Example 2: Remove first column
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
newmatrix <- thismatrix[ ,-c(1)]
newmatrix
```

will output 

``` 
4
5
6
```

+ Example 3: Remove first row and first column
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
newmatrix <- thismatrix[ -c(1),-c(1)]
newmatrix
```

will output 

``` 
5
6
```

##### Check if an item exists

+ Example 1:
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
1 %in% thismatrix
```

will output 

``` 
TRUE
```

##### Get number of rows and columns

+ Example 1:
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
dim(thismatrix)
```

will output 

``` 
3 2
```

##### Get Matrix length (i.e. number of elems)
Use the `length()` function to find the number of elems of a Matrix.

+ Example 1:
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
length(thismatrix)
```

will output 

``` 
6
```

##### Loop through a Matrix

+ Example 1:
  
```
# Create a matrix with 3 rows and 2 cols.
thismatrix <- matrix(c(1,2,3,4,5,6), nrow = 3, ncol = 2)
for (rows in 1:nrow(thismatrix)) {
  for (columns in 1:ncol(thismatrix)) {
    print(thismatrix[rows, columns])
  }
}
```

will output 

``` 
1
2
3
4
5
6
```

##### Combine two Matrices

+ Example 1:
  
```
# Example of combine matrices
Matrix1 <- matrix(c("apple", "banana", "cherry", "grape"), nrow = 2, ncol = 2)
Matrix2 <- matrix(c("orange", "mango", "pineapple", "watermelon"), nrow = 2, ncol = 2)

# Adding it as a rows
Matrix_Combined <- rbind(Matrix1, Matrix2)
Matrix_Combined

# Adding it as a columns
Matrix_Combined <- cbind(Matrix1, Matrix2)
Matrix_Combined
```

will output 

```
     [,1]      [,2]
[1,] "apple"  "cherry"    
[2,] "banana" "grape"     
[3,] "orange" "pineapple" 
[4,] "mango"  "watermelon"

     [,1]      [,2]    [,3]      [,4]
[1,] "apple"  "cherry" "orange" "pineapple" 
[2,] "banana" "grape"  "mango"  "watermelon"
```

#### Array
##### Constructor

> [!IMPORTANT]
> Arrays can only have one data type.

+ Example 1:
  
```
# An array with one dimension with values ranging from 1 to 24
thisarray <- c(1:24)
thisarray

# An array with more than one dimension
multiarray <- array(thisarray, dim = c(4, 3, 2))
multiarray
```

will output 

``` 
[1] 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24

, , 1

     [,1] [,2] [,3]
[1,]    1    5    9
[2,]    2    6   10
[3,]    3    7   11
[4,]    4    8   12

, , 2

     [,1] [,2] [,3]
[1,]   13   17   21
[2,]   14   18   22
[3,]   15   19   23
[4,]   16   20   24
```

in [w3school demo](https://www.w3schools.com/r/tryr.asp?filename=demo_array)

##### Access Array items by index

> [!NOTE]
> The syntax is as follow: `array[row position, column position, matrix level]`

> [!TIP]
> A comma (,) before c() means that we want to access the column.
>
> A comma (,) after c() means that we want to access the row.

You can also access the whole row or column from a matrix in an array, by using the c() function:

+ Example 1:
  
```
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))
multiarray[2, 3, 2]
```

will output 

```
[1] 22
```

+ Example 2:
  
```
thisarray <- c(1:24)

# Access all the items from the first row from matrix one
multiarray <- array(thisarray, dim = c(4, 3, 2))
multiarray[c(1),,1]

# Access all the items from the first column from matrix one
multiarray <- array(thisarray, dim = c(4, 3, 2))
multiarray[,c(1),1]
```

will output 

```
[1] 1 5 9
[1] 1 2 3 4
```

##### Check if an item exists

+ Example 1:
  
```
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))
2 %in% multiarray
```

will output 

```
TRUE
```

##### Get the dimension of an Array

+ Example 1:
  
```
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))
dim(multiarray)
```

will output 

```
4 3 2
```

##### Get length (i.e. number of elems) of an Array 

+ Example 1:
  
```
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))
length(multiarray)
```

will output 

```
24
```

##### Loop through an Array

+ Example 1:
  
```
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))
for(x in multiarray){
  print(x)
}
```

will output 

```
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
```

#### DataFrame
> [!NOTE]
> Data Frames are data displayed in a format as a table.

> [!NOTE]
> Data Frames can have different types of data inside it.
> While the first column can be character, the second and third can be numeric or logical.
> However, each column should have the same type of data.

##### Constructor
Use the `data.frame()` function to create a data frame.

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

# Print the data frame
Data_Frame
```

will output

```
  Training Pulse Duration
1 Strength   100       60
2  Stamina   150       30
3    Other   120       45
```

##### Summarize a DataFrame

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

Data_Frame

summary(Data_Frame)
```

will output

```
  Training Pulse Duration
1 Strength   100       60
2  Stamina   150       30
3    Other   120       45
     Training     Pulse          Duration   
 Other   :1   Min.   :100.0   Min.   :30.0  
 Stamina :1   1st Qu.:110.0   1st Qu.:37.5  
 Strength:1   Median :120.0   Median :45.0  
              Mean   :123.3   Mean   :45.0  
              3rd Qu.:135.0   3rd Qu.:52.5  
              Max.   :150.0   Max.   :60.0
```

###### Accessing items of a DataFrame

syntax:
| syntax | where | description |
| -----  | ----- | ----------- |
| `Data_Frame[<index>]` | `<index>` indicates the index of the DataFrame. It should be an integer between `1` and `ncol(Data_Frame)`. | Select `<index>`th column of `Data_Frame`. |
| `Data_Frame[[<index_name>]]` | `<index_name>` indicates the index name of the DataFrame (and should be quoted if it is a string). It should exist in row of `Data_Frame`. | Select the row of `Data_Frame` where index name is `<index_name>`. |
| `Data_Frame$<index_name>` | `<index_name>` indicates the index name of the DataFrame (and should **NOT** be quoted if it is a string). It should exist in row of `Data_Frame`. | Select the row of `Data_Frame` where index name is `<index_name>`. |

For more fully understand, see the following example.

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

Data_Frame

'--------------------'

Data_Frame[1]

'--------------------'

Data_Frame[["Training"]]

'--------------------'

Data_Frame$Training
```

will output

```
  Training Pulse Duration
1 Strength   100       60
2  Stamina   150       30
3    Other   120       45
[1] "--------------------"
  Training
1 Strength
2  Stamina
3    Other
[1] "--------------------"
[1] Strength Stamina  Other   
Levels: Other Stamina Strength
[1] "--------------------"
[1] Strength Stamina  Other   
Levels: Other Stamina Strength
```

##### Add rows
Use the `rbind()` function to add new rows in a Data Frame.

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

# Add a new row
New_row_DF <- rbind(Data_Frame, c("Strength", 110, 110))

# Print the new row
New_row_DF
```

will output

```
  Training Pulse Duration
1 Strength   100       60
2  Stamina   150       30
3    Other   120       45
4 Strength   110      110
```

##### Add columns
Use the `cbind()` function to add new columns in a Data Frame.

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

# Add a new column
New_col_DF <- cbind(Data_Frame, Steps = c(1000, 6000, 2000))

# Print the new column
New_col_DF
```

will output

```
  Training Pulse Duration Steps
1 Strength   100       60  1000
2  Stamina   150       30  6000
3    Other   120       45  2000
```

##### Remove rows and columns
Use the `c()` function to remove rows and columns in a Data Frame.

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

# Remove the first row and column
Data_Frame_New <- Data_Frame[-c(1), -c(1)]

# Print the new data frame
Data_Frame_New
```

will output

```
  Pulse Duration
2   150       30
3   120       45
```

##### Get number of rows and columns

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

dim(Data_Frame)
```

will output

```
3 3
```

##### Get number of rows

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

nrow(Data_Frame)
```

will output

```
3
```

##### Get number of columns

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

ncol(Data_Frame)
```

will output

```
3
```

##### Get length (i.e. the number of elem ) of a DataFrame

+ Example 1:
  
```
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

length(Data_Frame)
```

will output

```
9
```

##### Combine DataFrames

> [!TIP]
> Use the `rbind()` function to combine two or more DataFrames `vertically` in R.
>
> Use the `cbind()` function to combine two or more DataFrames `horizontally` in R.

+ Example 1:

```
Data_Frame1 <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

Data_Frame2 <- data.frame (
  Training = c("Stamina", "Stamina", "Strength"),
  Pulse = c(140, 150, 160),
  Duration = c(30, 30, 20)
)

New_Data_Frame <- rbind(Data_Frame1, Data_Frame2)
New_Data_Frame
```

will output

```
  Training Pulse Duration
1 Strength   100       60
2  Stamina   150       30
3    Other   120       45
4  Stamina   140       30
5  Stamina   150       30
6 Strength   160       20
```

+ Example 2:

```
Data_Frame3 <- data.frame (
  Training = c("Strength", "Stamina", "Other"),
  Pulse = c(100, 150, 120),
  Duration = c(60, 30, 45)
)

Data_Frame4 <- data.frame (
  Steps = c(3000, 6000, 2000),
  Calories = c(300, 400, 300)
)

New_Data_Frame1 <- cbind(Data_Frame3, Data_Frame4)
New_Data_Frame1
```

will output

```
  Training Pulse Duration Steps Calories
1 Strength   100       60  3000      300
2  Stamina   150       30  6000      400
3    Other   120       45  2000      300
```

#### Factor
