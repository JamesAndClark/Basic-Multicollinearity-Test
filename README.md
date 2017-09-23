# Basic-Multicollinearity-Test
Testing for Multicollinearity in multiple regressions.  
I am using a dataset of high-grossing films and their respective user ratings on websites like IMDB and metacritic, to test if there
is any correlation between rating and gross.
I am expecting there to be multicollinearity between these variables, as if one user average is high, it is likely the other will be.  

Film <- read.csv("movies.csv")  
install.packages("asbio")  // The necessary package required to produce the pair plots is "asbio"  
library(asbio)  
pairs(~Box+Rate+User+Meta, data=Film, lower.panel = panel.lm, upper.panel = panel.cor.res)
