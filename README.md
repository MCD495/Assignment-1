Hello Octocat
-------------

I love Octocat. Sheâs the coolest cat in town.

![](https://dl.dropboxusercontent.com/u/11805474/painblogr/biostats/assignments/octocat.png)

Assignment 2
============

    data("anscombe")
    dim(anscombe)

    ## [1] 11  8

    colnames(anscombe)

    ## [1] "x1" "x2" "x3" "x4" "y1" "y2" "y3" "y4"

    head(anscombe)

    ##   x1 x2 x3 x4   y1   y2    y3   y4
    ## 1 10 10 10  8 8.04 9.14  7.46 6.58
    ## 2  8  8  8  8 6.95 8.14  6.77 5.76
    ## 3 13 13 13  8 7.58 8.74 12.74 7.71
    ## 4  9  9  9  8 8.81 8.77  7.11 8.84
    ## 5 11 11 11  8 8.33 9.26  7.81 8.47
    ## 6 14 14 14  8 9.96 8.10  8.84 7.04

    tail(anscombe)

    ##    x1 x2 x3 x4    y1   y2   y3    y4
    ## 6  14 14 14  8  9.96 8.10 8.84  7.04
    ## 7   6  6  6  8  7.24 6.13 6.08  5.25
    ## 8   4  4  4 19  4.26 3.10 5.39 12.50
    ## 9  12 12 12  8 10.84 9.13 8.15  5.56
    ## 10  7  7  7  8  4.82 7.26 6.42  7.91
    ## 11  5  5  5  8  5.68 4.74 5.73  6.89

    summary(anscombe)

    ##        x1             x2             x3             x4    
    ##  Min.   : 4.0   Min.   : 4.0   Min.   : 4.0   Min.   : 8  
    ##  1st Qu.: 6.5   1st Qu.: 6.5   1st Qu.: 6.5   1st Qu.: 8  
    ##  Median : 9.0   Median : 9.0   Median : 9.0   Median : 8  
    ##  Mean   : 9.0   Mean   : 9.0   Mean   : 9.0   Mean   : 9  
    ##  3rd Qu.:11.5   3rd Qu.:11.5   3rd Qu.:11.5   3rd Qu.: 8  
    ##  Max.   :14.0   Max.   :14.0   Max.   :14.0   Max.   :19  
    ##        y1               y2              y3              y4        
    ##  Min.   : 4.260   Min.   :3.100   Min.   : 5.39   Min.   : 5.250  
    ##  1st Qu.: 6.315   1st Qu.:6.695   1st Qu.: 6.25   1st Qu.: 6.170  
    ##  Median : 7.580   Median :8.140   Median : 7.11   Median : 7.040  
    ##  Mean   : 7.501   Mean   :7.501   Mean   : 7.50   Mean   : 7.501  
    ##  3rd Qu.: 8.570   3rd Qu.:8.950   3rd Qu.: 7.98   3rd Qu.: 8.190  
    ##  Max.   :10.840   Max.   :9.260   Max.   :12.74   Max.   :12.500

Assignment 3
============

    ##    x1 x2 x3 x4    y1   y2    y3    y4
    ## 1  10 10 10  8  8.04 9.14  7.46  6.58
    ## 2   8  8  8  8  6.95 8.14  6.77  5.76
    ## 3  13 13 13  8  7.58 8.74 12.74  7.71
    ## 4   9  9  9  8  8.81 8.77  7.11  8.84
    ## 5  11 11 11  8  8.33 9.26  7.81  8.47
    ## 6  14 14 14  8  9.96 8.10  8.84  7.04
    ## 7   6  6  6  8  7.24 6.13  6.08  5.25
    ## 8   4  4  4 19  4.26 3.10  5.39 12.50
    ## 9  12 12 12  8 10.84 9.13  8.15  5.56
    ## 10  7  7  7  8  4.82 7.26  6.42  7.91
    ## 11  5  5  5  8  5.68 4.74  5.73  6.89

<img src="./figures/xy_plot-1.svg" style="display: block; margin: auto;" />
Figure 1: represents a scatter plot of x1 vs y1 from the anscombe data,
fitted with y1 vs x1 regression line

Assignment 4
============

    library(readr)
    # Read from dropbox using url, and import into using read_csv to convert into a dataframe
    df <- read.csv("https://dl.dropboxusercontent.com/u/11805474/painblogr/biostats/assignments/analgesic.csv")

    # Explore the contents of df
    dim(df)

    ## [1] 40  5

    colnames(df)

    ## [1] "ID"            "Group"         "Measurement_1" "Measurement_2"
    ## [5] "Measurement_3"

    head(df)

    ##   ID     Group Measurement_1 Measurement_2 Measurement_3
    ## 1  1 Analgesic            26            26            21
    ## 2  2 Analgesic            29            26            23
    ## 3  3 Analgesic            24            28            22
    ## 4  4 Analgesic            25            22            24
    ## 5  5 Analgesic            24            28            23
    ## 6  6 Analgesic            22            23            26

    tail(df)

    ##    ID   Group Measurement_1 Measurement_2 Measurement_3
    ## 35 35 Placebo            17            21            15
    ## 36 36 Placebo            19            17            15
    ## 37 37 Placebo            14            19            13
    ## 38 38 Placebo            17            19            13
    ## 39 39 Placebo            11            20            18
    ## 40 40 Placebo            15            18            12

    summary(df)

    ##        ID              Group    Measurement_1   Measurement_2 
    ##  Min.   : 1.00   Analgesic:20   Min.   :10.00   Min.   : 8.0  
    ##  1st Qu.:10.75   Placebo  :20   1st Qu.:17.00   1st Qu.:17.0  
    ##  Median :20.50                  Median :20.00   Median :20.0  
    ##  Mean   :20.50                  Mean   :20.12   Mean   :20.7  
    ##  3rd Qu.:30.25                  3rd Qu.:24.00   3rd Qu.:25.0  
    ##  Max.   :40.00                  Max.   :30.00   Max.   :32.0  
    ##  Measurement_3  
    ##  Min.   :12.00  
    ##  1st Qu.:16.00  
    ##  Median :20.50  
    ##  Mean   :20.52  
    ##  3rd Qu.:24.25  
    ##  Max.   :30.00

    library(tidyr)
    library(dplyr)

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

      #Tidy up df data from wide long format
      df.tidying <- gather(df,data, Measurement, Measurement_1:Measurement_3)
     
      #Now group data by the ID column
      
      groupMD <- group_by(df.tidying, ID)
      

    #NOW Summarize  mean value each individual's measurements
      print <- summarise (groupMD, mean(Measurement))
      
    #Print out final data frame
    print

    ## # A tibble: 40 × 2
    ##       ID `mean(Measurement)`
    ##    <int>               <dbl>
    ## 1      1            24.33333
    ## 2      2            26.00000
    ## 3      3            24.66667
    ## 4      4            23.66667
    ## 5      5            25.00000
    ## 6      6            23.66667
    ## 7      7            26.66667
    ## 8      8            23.33333
    ## 9      9            22.66667
    ## 10    10            24.00000
    ## # ... with 30 more rows

Assignment 5
============

#### Chicken weights

**Null hypothesis:**There is no relationship between feed type
supplement and chiken weight.

**Alternative hypothesis:**There is a relationship between feed type
supplement and chiken weight.

exploring the data set provided
-------------------------------

    library(dplyr)
    library(knitr)
    library(ggplot2)
    library(tidyr)

    #import data

    df_chkn <- read.csv("Chick-Weights.csv")          

    #1summarise data

    summ <-  group_by(df_chkn, feed) %>% 
    summarise(sample_size= n(), mean=mean(weight), sd= sd(weight), minimum= min(weight), lower_quatile = quantile(weight, 0.25), median= median(weight), upper_quartile= quantile(weight, 0.75), maximum = max(weight))

    summ

    ## # A tibble: 6 × 9
    ##        feed sample_size     mean       sd minimum lower_quatile median
    ##      <fctr>       <int>    <dbl>    <dbl>   <int>         <dbl>  <dbl>
    ## 1    casein          12 323.5833 64.43384     216        277.25  342.0
    ## 2 horsebean          10 160.2000 38.62584     108        137.00  151.5
    ## 3   linseed          12 218.7500 52.23570     141        178.00  221.0
    ## 4  meatmeal          11 276.9091 64.90062     153        249.50  263.0
    ## 5   soybean          14 246.4286 54.12907     158        206.75  248.0
    ## 6 sunflower          12 328.9167 48.83638     226        312.75  328.0
    ## # ... with 2 more variables: upper_quartile <dbl>, maximum <int>

    #2constructing a boxplot
    qplot(x= feed, y= weight, data =df_chkn, geom= "boxplot") + stat_summary(fun.y = "mean", geom= "point", color= "blue")

![](README_files/figure-markdown_strict/chicken%20(chunk%201)-1.png)

    #3Statistical test (ANOVA)
    foo<- aov(weight~feed, data= df_chkn)
    summary(foo)

    ##             Df Sum Sq Mean Sq F value   Pr(>F)    
    ## feed         5 231129   46226   15.37 5.94e-10 ***
    ## Residuals   65 195556    3009                     
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    #Pairwise Post-hoc test.
    pairwise.t.test(df_chkn$weight,df_chkn$feed, p.adjust.method = 'holm', paired= FALSE)

    ## 
    ##  Pairwise comparisons using t tests with pooled SD 
    ## 
    ## data:  df_chkn$weight and df_chkn$feed 
    ## 
    ##           casein  horsebean linseed meatmeal soybean
    ## horsebean 2.9e-08 -         -       -        -      
    ## linseed   0.00016 0.09435   -       -        -      
    ## meatmeal  0.18227 9.0e-05   0.09435 -        -      
    ## soybean   0.00532 0.00298   0.51766 0.51766  -      
    ## sunflower 0.81249 1.2e-08   8.1e-05 0.13218  0.00298
    ## 
    ## P value adjustment method: holm

1.Table showing the summarised information of chick-weights data

The data is unpaired, parametric \[-1 &lt;mean-median&lt; 1\] with more
than two sample groups, hence, one- way ANOVA can be used to test the
hypothesis

2.By looking at the boxplot we have reason to believe that a difference
between feed type and weight, however, the overlapping of the boxplots
provides an incoclusive decision.

3.Test statistics

Before continuing with statistical test it is crucial to note that
significance level is set at 5%

It can be seen that F-value is 15.37, degrees of freedom is 5 and p-
value= 5.94e-10 Therefore, we have sufficient information to reject the
null hypothesis, hence, we conclude that there is a relationship between
feed type supplement and chiken weight.
