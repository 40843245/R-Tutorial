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

| symbol | is forbidden? | recommended |
| ------- | ------------ | ----------- |
| `<-` | NO, it can be used in all contexts. | Yes |
| `=` | Sometimes, it is forbidden in some contexts. | No |

> [!TIP]
> Like other programming language, many variables can be assigned with same value in one line. See below example (Example 2).

+ Example 1:
  
```
myVar1 <- '123'
```

will define a variable named `myVar1` and assign value `'123'` to the variable.

+ Example 2:
  
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
3
```

+ Example 6:

```
5 %% -4
```

will output

```
```

+ Example 7:

```
8 %% -4
```

will output

```
```

+ Example 8:

```
-5 %% -4
```

will output

```
```

+ Example 9:

```
5 %% 0
```

will output

```
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

