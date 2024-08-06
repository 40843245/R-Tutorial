# R
## Intro
See [get started of R official website](#R-official-website)
## Installation
1. Visit [get started of R official website](#R-official-website)
2. Click [download to R](#CRAN-mirrors) link, it will redirect to [CRAN mirrors page](#CRAN-mirrors)
3. According to language you want to download, choose the corresponding mirror and click its link. It will redirect to download page.

> [!TIP]
> If, either you couldn't find the language you want, or you don't come up with any idea about language you want,
> I highly recommend you to download the [worldwide mirror](https://mirrors.cicku.me/cran/)

4. After choose the mirror, according to OS, download the corresponding platform of R by clicking the corresponding link.

![image](https://github.com/user-attachments/assets/e6eae8f7-b3e7-4b37-af05-96a28c7c5ffd)

> [!CAUTION]
> R is part of many Linux distributions, you should check with your Linux package management system in addition to the link above.

5. Wait for installation app. The name of installation should look like this `R-4.4.1-win.exe`.
6. Click the installation app to download.
7. Configure up the setting for downloading and click `Next` button.
8. Wait until download is completed.

## Get help
### Get help of a command
There are many ways to get help of a command.

#### Way 1: Get help of a command through help() function

+ Example 1: Get help text of command `lm`

Type these R code then execute it.

```
help(lm)
```

Or these code.

```
help("lm")
```

##### Ref
See [Help yourself in R](#Help-yourself-in-R)
 
#### Way 2: Get help of a command through ? directive

Let's continue the previous example.

+ Example 1: Get help text of command `lm`

Type these R code then execute it.

```
?lm
```

Or these code.

```
?"lm"
```

##### Ref
See [Help yourself in R](#Help-yourself-in-R)

### Get help online
#### Get help online through ??

Example 1:

Type these R code then execute it.
```
??install
```

will first display the message on the R console.

```
starting httpd help server ... done
```

then open and redirect to [the online help](http://127.0.0.1:27727/doc/html/Search?objects=1&port=27727)

## Packages
### Install packages in R
There are a few ways to install package in R.

#### Way 1: [Install packages in R through R code](https://stackoverflow.com/questions/14806705/manually-downloading-and-installing-packages-in-r)

Type these R code then execute it.

```
packagename <- 'caret' # name of package that you want to download.
foldername <- 'C:/PublicData/RawRPackages' # The name of destination folder that will be downloaded to.
install.packages(paste(foldername, packagename , sep = '/'),repos = NULL, type = "source") # command to download package.
library(packagenameWithoutQuotes, lib.loc = foldername) # add it into libarary.
```

Here, the variable `packagename` is `name of package that you want to download.`,

`foldername` is `The name of destination folder that will be downloaded to.`, and

`packagenameWithoutQuotes` is `name of package that you want to download But without quotes.`,

You may want to change the value of variable `packagename`,`foldername`, and `packagenameWithoutQuotes` as you want.

+ Example 1:

```
packagename <- 'caret' # name of package that you want to download.
foldername <- 'C:/PublicData/RawRPackages' # The name of destination folder that will be downloaded to.
install.packages(paste(foldername, packagename , sep = '/'),repos = NULL, type = "source") # command to download package.
library(caret, lib.loc = foldername) # add it into libarary.
```
##### Ref
From [the Thunder's answer on stackoverflow](https://stackoverflow.com/questions/14806705/manually-downloading-and-installing-packages-in-r),

![image](https://github.com/user-attachments/assets/f485888e-aa75-4d7d-a0f7-32644ff0ed16)

#### Way 2: Install packages in R through RStudio


### Look at path that packages will be installed
There are many ways to look at path that packages will be installed.

#### Way 1:Look at path that packages will be installed through R code

Type these R code then execute it.

```
.libPaths()
```

The output of these R code will look like this:

![image](https://github.com/user-attachments/assets/b5f689c5-3f4e-435e-9e53-1d82fd78db30)

##### Ref
From [the James Thompson's answer on stackoverflow](https://stackoverflow.com/questions/2615128/where-does-r-store-packages),

![image](https://github.com/user-attachments/assets/56b2a8cd-e7ef-4dc6-9e5f-c704e05af4c4)

## Console
### Clear the screen on the console
There are many ways to clear the screen on the console.

#### Way 1:Clear the screen on the console through keyboard shortcuts

If you are using the default R console, press <kbd>CTRL</kbd> + <kbd>L</kbd>

If you are using RStudio, press <kbd>CTRL</kbd> + <kbd>L</kbd>

##### Ref
From [the Rakesh's answer on stackoverflow](https://stackoverflow.com/questions/14260340/function-to-clear-the-console-in-r-and-rstudio),

![image](https://github.com/user-attachments/assets/d9e97298-7181-4ae5-a6e1-2e78b4fd7510)


# [R official website](https://www.r-project.org/)
# [CRAN mirrors](https://cran.r-project.org/mirrors.html)
# [Help yourself in R](https://www.r-project.org/help.html)

