# Restaurant-tips-analysis
![](https://chingsingh.com/wp-content/uploads/2024/02/1706607374966.webp)

Source: chingsingh

This project aims to use the restaurant tips dataset to practice creating composition plots and visualizations. We will examine the relationship between different variables and the tips given.

The dataset consists of information from 244 restaurant bills, collected in the US in 1987.

It includes details about the tips given to restaurant staff, such as the total bill, tip amount, gender of the person paying, smoking status, day of the week, time of day, and party size.

## Data exploration
### Overview dataset

|    |   id |   total_bill |   tip | sex    | smoker   | day   | time   |   size |
|---:|-----:|-------------:|------:|:-------|:---------|:------|:-------|-------:|
|  0 |    0 |        16.99 |  1.01 | Female | No       | Sun   | Dinner |      2 |
|  1 |    1 |        10.34 |  1.66 | Male   | No       | Sun   | Dinner |      3 |
|  2 |    2 |        21.01 |  3.5  | Male   | No       | Sun   | Dinner |      3 |
|  3 |    3 |        23.68 |  3.31 | Male   | No       | Sun   | Dinner |      2 |
|  4 |    4 |        24.59 |  3.61 | Female | No       | Sun   | Dinner |      4 |

The columns of the dataframe and their types are not right types. We fix their types and change them from object to string

### Descriptive statistics

|       |       id |   total_bill |       tip |      size |
|:------|---------:|-------------:|----------:|----------:|
| count | 244      |    244       | 244       | 244       |
| mean  | 121.5    |     19.7859  |   2.99828 |   2.56967 |
| std   |  70.5809 |      8.90241 |   1.38364 |   0.9511  |
| min   |   0      |      3.07    |   1       |   1       |
| 25%   |  60.75   |     13.3475  |   2       |   2       |
| 50%   | 121.5    |     17.795   |   2.9     |   2       |
| 75%   | 182.25   |     24.1275  |   3.5625  |   3       |
| max   | 243      |     50.81    |  10       |   6       |

## Data Description
### I.🚬 Do people who smoke or non-smoke give more tips?
#### 1. Separate smokers and non-smokers

**Smoker**
|     |   id |   total_bill |   tip | sex    | smoker   | day   | time   |   size |  
|----:|-----:|-------------:|------:|:-------|:---------|:------|:-------|-------:|
| 216 |  216 |        28.15 |  3    | Male   | Yes      | Sat   | Dinner |      5 |
|  97 |   97 |        12.03 |  1.5  | Male   | Yes      | Fri   | Dinner |      2 |
| 214 |  214 |        28.17 |  6.5  | Female | Yes      | Sat   | Dinner |      3 |
| 218 |  218 |         7.74 |  1.44 | Male   | Yes      | Sat   | Dinner |      2 |
| 210 |  210 |        30.06 |  2    | Male   | Yes      | Sat   | Dinner |      3 |


**Non-smoker**
|     |   id |   total_bill |   tip | sex   | smoker   | day   | time   |   size |
|----:|-----:|-------------:|------:|:------|:---------|:------|:-------|-------:|
| 185 |  185 |        20.69 |  5    | Male  | No       | Sun   | Dinner |      5 |
| 212 |  212 |        48.33 |  9    | Male  | No       | Sat   | Dinner |      4 |
|  88 |   88 |        24.71 |  5.85 | Male  | No       | Thur  | Lunch  |      2 |
|  84 |   84 |        15.98 |  2.03 | Male  | No       | Thur  | Lunch  |      2 |
| 167 |  167 |        31.71 |  4.5  | Male  | No       | Sun   | Dinner |      4 |


#### 2. Compare their measures of central tendency

At this step, we calculate measures of central tendency for the whole dataset, smoker and non-smoker dataset.

|        |   Common |   Smokers |   Non-smokers |
|:-------|---------:|----------:|--------------:|
| min    |  1       |   1       |       1       |
| max    | 10       |  10       |       9       |
| mean   |  2.99828 |   3.00871 |       2.99185 |
| median |  2.9     |   3       |       2.74    |

