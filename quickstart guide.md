# R
## Qt
Qt [^1]
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

## Version
### Look at version 

![image](https://github.com/user-attachments/assets/c8a6b1fc-95a0-4c8e-865c-c7e1b14c6b67)

![image](https://github.com/user-attachments/assets/c0942b21-4e25-4777-bd96-646342c151a3)

## Update version 

[How to automatically update R to the latest version?](https://stackoverflow.com/questions/59389515/how-to-automatically-update-r-to-the-latest-version)


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

```
Here, the variable `packagename` is `name of package that you want to download.`,
`foldername` is `The name of destination folder that will be downloaded to.`, and
`packagenameWithoutQuotes` is `name of package that you want to download But without quotes.`,
You may want to change the value of variable `packagename`,`foldername`, and `packagenameWithoutQuotes` as you want.
```

or simply type these R code then execute it.

```
packagename <- 'caret'
install.packages(packagename)
```

```
Here, the variable `packagename` is `name of package that you want to download.
```

+ Example 1:

Type these R code then execute it.

```
install.packages('rmarkdown')
```

It will show the mirror of package for download. And if one select `Taiwan` mirror. Then the `Taiwan mirror` of `rmarkdown` will be downloaded. In addition, during downloading, the message will be displayed. Such as

```
--- Please select a CRAN mirror for use in this session ---
Warning: failed to download mirrors file (cannot open URL 'https://cran.r-project.org/CRAN_mirrors.csv'); using local file 'C:/PROGRA~1/R/R-44~1.1/doc/CRAN_mirrors.csv'
also installing the dependencies ‘cli’, ‘glue’, ‘fs’, ‘R6’, ‘rappdirs’, ‘base64enc’, ‘cachem’, ‘fastmap’, ‘lifecycle’, ‘memoise’, ‘mime’, ‘rlang’, ‘sass’, ‘digest’, ‘highr’, ‘bslib’, ‘evaluate’, ‘fontawesome’, ‘htmltools’, ‘jquerylib’, ‘jsonlite’, ‘knitr’, ‘tinytex’, ‘xfun’, ‘yaml’

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/cli_3.6.3.zip'
Content type 'application/zip' length 1361839 bytes (1.3 MB)
downloaded 1.3 MB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/glue_1.7.0.zip'
Content type 'application/zip' length 163516 bytes (159 KB)
downloaded 159 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/fs_1.6.4.zip'
Content type 'application/zip' length 412943 bytes (403 KB)
downloaded 403 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/R6_2.5.1.zip'
Content type 'application/zip' length 85007 bytes (83 KB)
downloaded 83 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/rappdirs_0.3.3.zip'
Content type 'application/zip' length 52566 bytes (51 KB)
downloaded 51 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/base64enc_0.1-3.zip'
Content type 'application/zip' length 33130 bytes (32 KB)
downloaded 32 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/cachem_1.1.0.zip'
Content type 'application/zip' length 73872 bytes (72 KB)
downloaded 72 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/fastmap_1.2.0.zip'
Content type 'application/zip' length 135365 bytes (132 KB)
downloaded 132 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/lifecycle_1.0.4.zip'
Content type 'application/zip' length 141047 bytes (137 KB)
downloaded 137 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/memoise_2.0.1.zip'
Content type 'application/zip' length 51156 bytes (49 KB)
downloaded 49 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/mime_0.12.zip'
Content type 'application/zip' length 40893 bytes (39 KB)
downloaded 39 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/rlang_1.1.4.zip'
Content type 'application/zip' length 1622822 bytes (1.5 MB)
downloaded 1.5 MB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/sass_0.4.9.zip'
Content type 'application/zip' length 2613570 bytes (2.5 MB)
downloaded 2.5 MB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/digest_0.6.36.zip'
Content type 'application/zip' length 221462 bytes (216 KB)
downloaded 216 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/highr_0.11.zip'
Content type 'application/zip' length 44214 bytes (43 KB)
downloaded 43 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/bslib_0.8.0.zip'
Content type 'application/zip' length 5594589 bytes (5.3 MB)
downloaded 5.3 MB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/evaluate_0.24.0.zip'
Content type 'application/zip' length 87036 bytes (84 KB)
downloaded 84 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/fontawesome_0.5.2.zip'
Content type 'application/zip' length 1351152 bytes (1.3 MB)
downloaded 1.3 MB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/htmltools_0.5.8.1.zip'
Content type 'application/zip' length 363175 bytes (354 KB)
downloaded 354 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/jquerylib_0.1.4.zip'
Content type 'application/zip' length 526071 bytes (513 KB)
downloaded 513 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/jsonlite_1.8.8.zip'
Content type 'application/zip' length 1107194 bytes (1.1 MB)
downloaded 1.1 MB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/knitr_1.48.zip'
Content type 'application/zip' length 1207784 bytes (1.2 MB)
downloaded 1.2 MB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/tinytex_0.52.zip'
Content type 'application/zip' length 143217 bytes (139 KB)
downloaded 139 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/xfun_0.46.zip'
Content type 'application/zip' length 538110 bytes (525 KB)
downloaded 525 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/yaml_2.3.10.zip'
Content type 'application/zip' length 119450 bytes (116 KB)
downloaded 116 KB

trying URL 'https://cran.csie.ntu.edu.tw/bin/windows/contrib/4.4/rmarkdown_2.27.zip'
Content type 'application/zip' length 2694395 bytes (2.6 MB)
downloaded 2.6 MB

package ‘cli’ successfully unpacked and MD5 sums checked
package ‘glue’ successfully unpacked and MD5 sums checked
package ‘fs’ successfully unpacked and MD5 sums checked
package ‘R6’ successfully unpacked and MD5 sums checked
package ‘rappdirs’ successfully unpacked and MD5 sums checked
package ‘base64enc’ successfully unpacked and MD5 sums checked
package ‘cachem’ successfully unpacked and MD5 sums checked
package ‘fastmap’ successfully unpacked and MD5 sums checked
package ‘lifecycle’ successfully unpacked and MD5 sums checked
package ‘memoise’ successfully unpacked and MD5 sums checked
package ‘mime’ successfully unpacked and MD5 sums checked
package ‘rlang’ successfully unpacked and MD5 sums checked
package ‘sass’ successfully unpacked and MD5 sums checked
package ‘digest’ successfully unpacked and MD5 sums checked
package ‘highr’ successfully unpacked and MD5 sums checked
package ‘bslib’ successfully unpacked and MD5 sums checked
package ‘evaluate’ successfully unpacked and MD5 sums checked
package ‘fontawesome’ successfully unpacked and MD5 sums checked
package ‘htmltools’ successfully unpacked and MD5 sums checked
package ‘jquerylib’ successfully unpacked and MD5 sums checked
package ‘jsonlite’ successfully unpacked and MD5 sums checked
package ‘knitr’ successfully unpacked and MD5 sums checked
package ‘tinytex’ successfully unpacked and MD5 sums checked
package ‘xfun’ successfully unpacked and MD5 sums checked
package ‘yaml’ successfully unpacked and MD5 sums checked
package ‘rmarkdown’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
        C:\Users\40843\AppData\Local\Temp\RtmpGs5Mad\downloaded_packages
Warning message:
In download.file(url, destfile = f, quiet = TRUE) :
  URL 'https://cran.r-project.org/CRAN_mirrors.csv': status was 'Couldn't connect to server'
```

##### Ref
From [the Thunder's answer on stackoverflow](https://stackoverflow.com/questions/14806705/manually-downloading-and-installing-packages-in-r),

![image](https://github.com/user-attachments/assets/f485888e-aa75-4d7d-a0f7-32644ff0ed16)

#### Way 2: Install packages in R through RStudio

1. In RStudio, select `Packages` -> `Install package(s)...`.
2. Then it will popup a windown. Select the package you want to download.

+ Example 1:

For demo of download `rmarkdown` package in RStudio, see [Download R package in RStudio - way 2](https://www.youtube.com/watch?v=Fv0HhrW1dVw)

> [!TIP]
> Since there are no search query to quickly find the package you want to download.
> Thus, I highly recommend that download the package by first way if you know the exactly name of package.
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

## Footnotes

[^1]: https://doc.qt.io/

# [R official website](https://www.r-project.org/)
# [CRAN mirrors](https://cran.r-project.org/mirrors.html)
# [Help yourself in R](https://www.r-project.org/help.html)

