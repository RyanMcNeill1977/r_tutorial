# Importing data into R

The thing that makes R so powerful is its use of packages. These are programs that others have created that can help make your life a little easier. When you download R, it comes with a number of packages already installed. Others you have to download. Below we're going to use a package called [haven] (https://github.com/tidyverse/haven), which allows you to import data formatted for SPSS, Stata and SAS --- some of the most popular statistical packages. 

## Install haven 

Frequently packages have instructions on how to install them. haven is [no different](https://github.com/tidyverse/haven#installation). Take a look. Then enter the below code in R. 

```R
install.packages("haven")
```

Now R will do a bunch of stuff and install the package. It might take a bit. When it's finished, assuming you didn't get error messages, you're ready to use haven. 

### Importing data in a SAS format 

Now we're going to import a dataset you've downloaded from iPUMS in SAS format. 

To use a package, you first have to use the follow code: 

```R
library(haven)
```

But wait. A short interlude. Before we import the file, a quick tip. When we go to import the data, we could do this a couple of different ways. 

```R
read_sas("c:/path/to/YOURFILENAME.sas7bdat")
```

Well, that's one way to do it. But that's a lot of typing. I think it kind of sucks having to type what could be a lengthy path. Wouldn't it be better if we could just type this?

```R
read_sas("YOURFILENAME.sas7bdat")
```

Well, we can by setting the "working directory." Basically, this is telling R, "Hey, I'm going to do everything in this directory right now so here's the path in advance." It's real easy to remember, but if you don't want to type the code, you can use RStudio to do it by going to Session->Set Working Directory->Choose directory. 

```R
setwd("D:/RTutorial")
```

OK, after you do that, let's just enter the below code. 

```R
read_sas("YOURFILENAME.sas7bdat")
```

OK. So notice R just sort of spits the top part of the file onto the screen? That's not terribly helpful. For one thing, we can't work with it because it hasn't actually been assigned to an object. 

Let's try this. 

```R
original_data <- read_sas("YOURFILENAME.sas7bdat")
```

Ah, that's much better. Look up in your Global Environment window in R. 
