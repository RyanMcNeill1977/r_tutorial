# Analyzing data in R

So now the fun begins. The first thing we want to do is start nosing around our data. When I start with a new set of data, the first thing I like to do is run some frequencies on different columns to see what's in the data. To do that, let's import a new package. 

```R
install.packages("plyr")
```

Beneath the area labeled Global Environment, you'll see an area with tabs for files, plots, packages, help and viewer. Click on the Packages tab. 

Look in the User Library portion and see is plyr is installed. No? You might have to hit update (right beneath the packages tab). 

Now let's make it available. 

```R
library("plyr")
```

(P.S. --- you can also just check the box next to the package you want to use). 

## Lists, matrices and other data types 

Right now, our data is stored in the object original_data. But what is original_data?

In R, you can use [istype(x)](https://stat.ethz.ch/R-manual/R-devel/library/base/html/typeof.html) to determine the type of an object. 

```R
istype("original_data")
```

blah blah blah 


