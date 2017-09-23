# Basic-Multicollinearity-Test
Testing for Multicollinearity in multiple regressions.  
I am using a dataset of high-grossing films and their respective user ratings on websites like IMDB and metacritic, to test if there
is any correlation between rating and gross.
I am expecting there to be multicollinearity between these variables, as if one user average is high, it is likely the other will be.  

Film <- read.csv("movies.csv")  
install.packages("asbio")  // The necessary package required to produce the pair plots is "asbio"  
library(asbio)  
pairs(~Box+Rate+User+Meta, data=Film, lower.panel = panel.lm, upper.panel = panel.cor.res)

// I am unsure how to attach the plot to github, so I have created an issue with the plot attached. This plot confirms there is 
collinearity between our variables as there is a high correlation coefficient that is very significant.
