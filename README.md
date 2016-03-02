# plotly examples


When trying to download a plot as png in browser (chrome), plot is not downloaded.
It stalls with message "Taking snapshot - this may take a few seconds" and then "Snapshotting is still in progress - please hold".
RStudio crashes if I try to do the same.

Here's my code and session info.

```R
library(plotly)
## Loading required package: ggplot2
## 
## Attaching package: 'plotly'
## The following object is masked from 'package:ggplot2':
## 
##     last_plot
## The following object is masked from 'package:graphics':
## 
##     layout
p <- ggplot(data = diamonds, aes(x = cut, fill = clarity)) +
            geom_bar(position = "dodge")
ggplotly(p)
## Warning: Using size for a discrete variable is not advised.

devtools::session_info()
## Session info --------------------------------------------------------------
##  setting  value                       
##  version  R version 3.2.2 (2015-08-14)
##  system   x86_64, linux-gnu           
##  ui       X11                         
##  language en_US                       
##  collate  en_US.UTF-8                 
##  tz       <NA>                        
##  date     2016-03-01
## Packages ------------------------------------------------------------------
##  package     * version date       source        
##  base64enc     0.1-3   2015-07-28 CRAN (R 3.2.2)
##  colorspace    1.2-6   2015-03-11 CRAN (R 3.2.0)
##  devtools      1.10.0  2016-01-23 CRAN (R 3.2.2)
##  digest        0.6.9   2016-01-08 CRAN (R 3.2.2)
##  evaluate      0.8     2015-09-18 CRAN (R 3.2.2)
##  ggplot2     * 2.1.0   2016-03-01 CRAN (R 3.2.2)
##  gridExtra     2.2.1   2016-02-29 CRAN (R 3.2.2)
##  gtable        0.2.0   2016-02-26 CRAN (R 3.2.2)
##  htmltools     0.3     2015-12-29 CRAN (R 3.2.2)
##  htmlwidgets   0.6     2016-02-25 CRAN (R 3.2.2)
##  httr          1.1.0   2016-01-28 CRAN (R 3.2.2)
##  jsonlite      0.9.19  2015-11-28 CRAN (R 3.2.2)
##  knitr         1.12.3  2016-01-22 CRAN (R 3.2.2)
##  labeling      0.3     2014-08-23 CRAN (R 3.2.0)
##  magrittr      1.5     2014-11-22 CRAN (R 3.2.0)
##  memoise       1.0.0   2016-01-29 CRAN (R 3.2.2)
##  munsell       0.4.3   2016-02-13 CRAN (R 3.2.2)
##  plotly      * 2.0.16  2015-12-20 CRAN (R 3.2.2)
##  plyr          1.8.3   2015-06-12 CRAN (R 3.2.0)
##  R6            2.1.2   2016-01-26 CRAN (R 3.2.2)
##  Rcpp          0.12.3  2016-01-10 CRAN (R 3.2.2)
##  rmarkdown     0.9.2   2016-01-01 CRAN (R 3.2.2)
##  scales        0.4.0   2016-02-26 CRAN (R 3.2.2)
##  stringi       1.0-1   2015-10-22 CRAN (R 3.2.2)
##  stringr       1.0.0   2015-04-30 CRAN (R 3.2.2)
##  viridis       0.3.2   2015-12-31 CRAN (R 3.2.2)
##  yaml          2.1.13  2014-06-12 CRAN (R 3.2.0)
devtools::install_github("ropensci/plotly")
## Downloading GitHub repo ropensci/plotly@master
## from URL https://api.github.com/repos/ropensci/plotly/zipball/master
## Installing plotly
## '/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore  \
##   CMD INSTALL  \
##   '/tmp/Rtmp79kii9/devtools2d173afde9bc/ropensci-plotly-63608e5'  \
##   --library='/home/joseah/R/x86_64-pc-linux-gnu-library/3.2'  \
##   --install-tests
## 
## Reloading installed plotly
## 
## Attaching package: 'plotly'
## The following object is masked from 'package:ggplot2':
## 
##     last_plot
## The following object is masked from 'package:graphics':
## 
##     layout
library(plotly)
p <- ggplot(data = diamonds, aes(x = cut, fill = clarity)) +
            geom_bar(position = "dodge")
ggplotly(p)
## Warning: Using size for a discrete variable is not advised.

devtools::session_info()
## Session info --------------------------------------------------------------
##  setting  value                       
##  version  R version 3.2.2 (2015-08-14)
##  system   x86_64, linux-gnu           
##  ui       X11                         
##  language en_US                       
##  collate  en_US.UTF-8                 
##  tz       <NA>                        
##  date     2016-03-01
## Packages ------------------------------------------------------------------
##  package     * version date       source                          
##  base64enc     0.1-3   2015-07-28 CRAN (R 3.2.2)                  
##  colorspace    1.2-6   2015-03-11 CRAN (R 3.2.0)                  
##  curl          0.9.6   2016-02-17 CRAN (R 3.2.2)                  
##  devtools      1.10.0  2016-01-23 CRAN (R 3.2.2)                  
##  digest        0.6.9   2016-01-08 CRAN (R 3.2.2)                  
##  evaluate      0.8     2015-09-18 CRAN (R 3.2.2)                  
##  ggplot2     * 2.1.0   2016-03-01 CRAN (R 3.2.2)                  
##  git2r         0.13.1  2015-12-10 CRAN (R 3.2.2)                  
##  gridExtra     2.2.1   2016-02-29 CRAN (R 3.2.2)                  
##  gtable        0.2.0   2016-02-26 CRAN (R 3.2.2)                  
##  htmltools     0.3     2015-12-29 CRAN (R 3.2.2)                  
##  htmlwidgets   0.6     2016-02-25 CRAN (R 3.2.2)                  
##  httr          1.1.0   2016-01-28 CRAN (R 3.2.2)                  
##  jsonlite      0.9.19  2015-11-28 CRAN (R 3.2.2)                  
##  knitr         1.12.3  2016-01-22 CRAN (R 3.2.2)                  
##  labeling      0.3     2014-08-23 CRAN (R 3.2.0)                  
##  magrittr      1.5     2014-11-22 CRAN (R 3.2.0)                  
##  memoise       1.0.0   2016-01-29 CRAN (R 3.2.2)                  
##  munsell       0.4.3   2016-02-13 CRAN (R 3.2.2)                  
##  plotly      * 2.5.0   2016-03-02 Github (ropensci/plotly@63608e5)
##  plyr          1.8.3   2015-06-12 CRAN (R 3.2.0)                  
##  R6            2.1.2   2016-01-26 CRAN (R 3.2.2)                  
##  Rcpp          0.12.3  2016-01-10 CRAN (R 3.2.2)                  
##  rmarkdown     0.9.2   2016-01-01 CRAN (R 3.2.2)                  
##  rstudioapi    0.5     2016-01-24 CRAN (R 3.2.2)                  
##  scales        0.4.0   2016-02-26 CRAN (R 3.2.2)                  
##  stringi       1.0-1   2015-10-22 CRAN (R 3.2.2)                  
##  stringr       1.0.0   2015-04-30 CRAN (R 3.2.2)                  
##  viridis       0.3.2   2015-12-31 CRAN (R 3.2.2)                  
##  withr         1.0.0   2015-09-23 CRAN (R 3.2.2)                  
##  yaml          2.1.13  2014-06-12 CRAN (R 3.2.0)
```
