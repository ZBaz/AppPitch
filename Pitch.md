Predicting the Vehicle Horse Power of Motor Trend 1974 cars
========================================================
author: 
date: 



Purpose of Shiny App
========================================================

A Shiny App was created to look at how you could use various attributes of a vehicle to see what Horse Power the vehicle will likely have. The attributes that will be used are: The number of cylinders a car has, the miles per gallon it gets and weight of the car in half tons.

The Shiny App can be found at: https://zbaz.shinyapps.io/ShinyApp/ 

Backend Calculated Model
========================================================
This is the model that will produce the predicted Horse Power given the inputs.


```r
mtModel <- lm( hp ~ mpg + wt + cyl, data = mtcars)
OutPt = coefficients(lm( hp ~ mpg + wt + cyl, data = mtcars))
CalcOutPt <- as.numeric(OutPt[1] +OutPt[2]+OutPt[3]+OutPt[4])
CalcOutPt
```

```
[1] 124.333
```

Results Interpretation
========================================================

Given the input variables, the algorithm gives predicted amount of Horse Power a car will have. The more weight, and the worse miles per gallon a car has, offset the gain in the amount of cylinders bring to Horse Power.

Conclusion
========================================================

This Shiny App gives a powerful example of how to use a multivariate linear regression to predict the outcome of variable of interest. The app can be easily expanded to fit almost any data set and find the variable of interest!
