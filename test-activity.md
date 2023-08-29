Test activity
================
ECON 122

## First steps

If you followed the directions in the README file, you should be viewing
this file in RStudio. As discussed in class, `.Rmd` files allow you to
combine the **analysis** *AND* **writeup** of a project all in one
document. If you use a different dataset, the code should dynamically
update all the variables in the file.

## To Do: Complete before Wednesday’s class

Go through and answer the questions below.

Note: The grey portions of code between ```` ```{r} ```` and
```` ``` ```` are called R chunks. They allow you to run code in real
time by clicking on the green arrow.

## Data description:

For today’s assignment, I include code to import a data set related to
bank loans. Later on in the course, we will cover importing data more
thoroughly.

Click on the green arrow for the R chunk below. It may look like nothing
happened but now you should have a new item `loans` appear in the
environment tab to your right. If you click on the variable, it will
show you the different variables that are included in the `loans`
dataset.

``` r
> loans <- read.csv("https://raw.githubusercontent.com/mgelman/data/master/day1CreditData.csv")
```

## Data basics

When we load a data set, we typically want to know basic characteristics
such as how many variables and observations there are. In R, the number
of observations will be the `rows` and the number of variables will be
the `columns`. The code chunk below shows how to return these values.

``` r
> nrow(loans)
[1] 700
> ncol(loans)
[1] 21
```

## Hard coding data

From the code above, how many observations and variables are there in
this dataset? Fill in your answer below by replacing XXXXX with the
actual numbers. The “\*\*” formats the output to be bold.

*answer:* There are **700** cases and **21** variables in the dataset.

## Embedding R variables into your Rmd code

Hard coding your data is appealing if your data set doesn’t change.
Sometimes, it’s nice to see the output without having to `Knit` your
code. However, if the data set changes, you have to go in and manually
update the numbers.

`Rmd` files have the ability to embed one R code command into your text
by wrapping it in “`r" followed by "`”

For example, the square root of 10 is 3.1622777. When you `Knit` your
`Rmd` file, you will see that now sqrt(10) is replaced by the actual
value. Try it now by clicking on the `Knit` button above.

Using what you know about embedding R commands, write a dynamic version
of your answer above by using the R command for computing the number of
rows and number of columns instead of the actual numbers

*answer:* There are **700** cases and **21** variables in the dataset.

## Wrapping up

That’s it for the `Rmd` portion of the assignment! Be sure to complete
the assignment by following the steps below

1.  `Knit` your file so that your `.Rmd` file produces an `.md` file
    that is readable from GitHub
2.  Go to the Git tab on the upper right panel of Rstudio and `commit`
    the changes you made. The two important changes are
    1.  A new file `test-activity.md` created from knitting your `.Rmd`
        file
    2.  Your `test-activity.Rmd` file should have changes made to it
        from filling in your answers
3.  `push` your changes to your `test-activity` GitHub repository
4.  Lastly, go back to GitHub to check that your changes were properly
    `pushed`. Once, I see that your new files have been pushed, you will
    receive credit for the assignment.
