Deploy scoring model
====================

This package illustrates how to deploy a model for remote scoring/prediction. 


    # Install in R
    library(devtools)
    install_github("opencpu/beard")

    # Score in R
    library(beard)
    mydata <- data.frame(year=c(1915))
    beard(input = mydata)

    # Score remotely
    curl https://public.opencpu.org/ocpu/github/opencpu/beard/R/beard/json \
      -H "Content-Type: application/json" \
      -d '{"input" : [ {"year":1913} ]}'
      
The model is included in the `data` directory of the package, and was created
using the [createmodel.R](https://github.com/opencpu/beard/blob/master/inst/beard/createmodel.R) script. It predicts in the early 20th century the prevelance of beards among men.