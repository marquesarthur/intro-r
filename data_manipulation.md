---
layout: default
title: Data Manipulation
nav_order: 3
description:
---
<style>
table {
  padding: 0; }
  table tr {
    border-top: 1px solid #cccccc;
    background-color: white;
    margin: 0;
    padding: 0; }
    table tr:nth-child(odd) {
      background-color: #f8f8f8; }
      table tr th {
      font-weight: bold;
      border: 1px solid #cccccc;
      text-align: left;
      margin: 0;
      padding: 6px 13px; }
    table tr td {
      border: 1px solid #cccccc;
      text-align: left;
      margin: 0;
      padding: 6px 13px; }
    table tr th :first-child, table tr td :first-child {
      margin-top: 0; }
    table tr th :last-child, table tr td :last-child {
margin-bottom: 0; }
</style>

# Data Manipulation

<img src="{{site.baseurl}}/jupyter/figures/learning_objectives.png">

#### Our data

<img src="{{site.baseurl}}/jupyter/figures/global_warming.jpeg">

***

### Import data from excel



<img src="{{site.baseurl}}/jupyter/figures/data_import_from_excel.png">

***

### Preview data and give it a nice name


<img src="{{site.baseurl}}/jupyter/figures/data_import_preview.png">


***

### You can also load your data with the read_csv command


```R
mydata <- read.csv("GlobalLandTemperaturesByCountry.csv")
```


```R
head(mydata, 15)
```


<table>
<caption>A data.frame: 15 × 4</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1743-11-01</td><td> 4.384</td><td>2.294</td><td>Ã…land</td></tr>
	<tr><th scope="row">2</th><td>1743-12-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">3</th><td>1744-01-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">4</th><td>1744-02-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">5</th><td>1744-03-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">6</th><td>1744-04-01</td><td> 1.530</td><td>4.680</td><td>Ã…land</td></tr>
	<tr><th scope="row">7</th><td>1744-05-01</td><td> 6.702</td><td>1.789</td><td>Ã…land</td></tr>
	<tr><th scope="row">8</th><td>1744-06-01</td><td>11.609</td><td>1.577</td><td>Ã…land</td></tr>
	<tr><th scope="row">9</th><td>1744-07-01</td><td>15.342</td><td>1.410</td><td>Ã…land</td></tr>
	<tr><th scope="row">10</th><td>1744-08-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">11</th><td>1744-09-01</td><td>11.702</td><td>1.517</td><td>Ã…land</td></tr>
	<tr><th scope="row">12</th><td>1744-10-01</td><td> 5.477</td><td>1.862</td><td>Ã…land</td></tr>
	<tr><th scope="row">13</th><td>1744-11-01</td><td> 3.407</td><td>1.425</td><td>Ã…land</td></tr>
	<tr><th scope="row">14</th><td>1744-12-01</td><td>-2.181</td><td>1.641</td><td>Ã…land</td></tr>
	<tr><th scope="row">15</th><td>1745-01-01</td><td>-3.850</td><td>1.841</td><td>Ã…land</td></tr>
</tbody>
</table>



***

## Basic data commands 

### names( ): check variable names


```R
names(mydata)
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class="list-inline">
<li>'dt'</li>
<li>'AverageTemperature'</li>
<li>'AverageTemperatureUncertainty'</li>
<li>'Country'</li>
</ol>



***

### View first n lines of the table


```R
head(mydata, n = 10)
```


<table>
<caption>A data.frame: 10 × 4</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1743-11-01</td><td> 4.384</td><td>2.294</td><td>Ã…land</td></tr>
	<tr><th scope="row">2</th><td>1743-12-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">3</th><td>1744-01-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">4</th><td>1744-02-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">5</th><td>1744-03-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">6</th><td>1744-04-01</td><td> 1.530</td><td>4.680</td><td>Ã…land</td></tr>
	<tr><th scope="row">7</th><td>1744-05-01</td><td> 6.702</td><td>1.789</td><td>Ã…land</td></tr>
	<tr><th scope="row">8</th><td>1744-06-01</td><td>11.609</td><td>1.577</td><td>Ã…land</td></tr>
	<tr><th scope="row">9</th><td>1744-07-01</td><td>15.342</td><td>1.410</td><td>Ã…land</td></tr>
	<tr><th scope="row">10</th><td>1744-08-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
</tbody>
</table>



***

### table( ): check variable values and frequency

```
table(mydata$Country)
```


```R
head(table(mydata$Country), n=10)
```


    
            Ã…land    Afghanistan         Africa        Albania        Algeria 
              3239           2106           1965           3239           2721 
    American Samoa        Andorra         Angola       Anguilla     Antarctica 
              1761           3239           1878           2277            764 


***

## Basic data management commands

### is.factor( ): check if the variable is defined as categorical


```R
is.factor(mydata$Country)
```


TRUE


### as.factor( ): changes variable to categorical format


```R
mydata$Country <- as.factor(mydata$Country)
```


```R
is.factor(mydata$Country)
```


TRUE


### numeric( ): check if the variable is defined as numerical


```R
is.numeric(mydata$AverageTemperature)
```


TRUE


***

## Data management with "dplyr" package

### Removing empty cells/rows


```R
head(mydata, n = 10)
```


<table>
<caption>A data.frame: 10 × 4</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1743-11-01</td><td> 4.384</td><td>2.294</td><td>Ã…land</td></tr>
	<tr><th scope="row">2</th><td>1743-12-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">3</th><td>1744-01-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">4</th><td>1744-02-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">5</th><td>1744-03-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
	<tr><th scope="row">6</th><td>1744-04-01</td><td> 1.530</td><td>4.680</td><td>Ã…land</td></tr>
	<tr><th scope="row">7</th><td>1744-05-01</td><td> 6.702</td><td>1.789</td><td>Ã…land</td></tr>
	<tr><th scope="row">8</th><td>1744-06-01</td><td>11.609</td><td>1.577</td><td>Ã…land</td></tr>
	<tr><th scope="row">9</th><td>1744-07-01</td><td>15.342</td><td>1.410</td><td>Ã…land</td></tr>
	<tr><th scope="row">10</th><td>1744-08-01</td><td>    NA</td><td>   NA</td><td>Ã…land</td></tr>
</tbody>
</table>




```R
mydata <- na.omit(mydata)
```


```R
head(mydata, n = 10)
```


<table>
<caption>A data.frame: 10 × 4</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1743-11-01</td><td> 4.384</td><td>2.294</td><td>Ã…land</td></tr>
	<tr><th scope="row">6</th><td>1744-04-01</td><td> 1.530</td><td>4.680</td><td>Ã…land</td></tr>
	<tr><th scope="row">7</th><td>1744-05-01</td><td> 6.702</td><td>1.789</td><td>Ã…land</td></tr>
	<tr><th scope="row">8</th><td>1744-06-01</td><td>11.609</td><td>1.577</td><td>Ã…land</td></tr>
	<tr><th scope="row">9</th><td>1744-07-01</td><td>15.342</td><td>1.410</td><td>Ã…land</td></tr>
	<tr><th scope="row">11</th><td>1744-09-01</td><td>11.702</td><td>1.517</td><td>Ã…land</td></tr>
	<tr><th scope="row">12</th><td>1744-10-01</td><td> 5.477</td><td>1.862</td><td>Ã…land</td></tr>
	<tr><th scope="row">13</th><td>1744-11-01</td><td> 3.407</td><td>1.425</td><td>Ã…land</td></tr>
	<tr><th scope="row">14</th><td>1744-12-01</td><td>-2.181</td><td>1.641</td><td>Ã…land</td></tr>
	<tr><th scope="row">15</th><td>1745-01-01</td><td>-3.850</td><td>1.841</td><td>Ã…land</td></tr>
</tbody>
</table>




***

### select ( ): selects columns based on columns names


```R
head(select(mydata, dt, Country), n=5)
```


<table>
<caption>A data.frame: 5 × 2</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1743-11-01</td><td>Ã…land</td></tr>
	<tr><th scope="row">6</th><td>1744-04-01</td><td>Ã…land</td></tr>
	<tr><th scope="row">7</th><td>1744-05-01</td><td>Ã…land</td></tr>
	<tr><th scope="row">8</th><td>1744-06-01</td><td>Ã…land</td></tr>
	<tr><th scope="row">9</th><td>1744-07-01</td><td>Ã…land</td></tr>
</tbody>
</table>



***

### filter ( ): selects cases based on conditions


```R
head(filter(mydata, Country=="Canada"))
```


<table>
<caption>A data.frame: 6 × 4</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1768-09-01</td><td>  5.257</td><td>3.107</td><td>Canada</td></tr>
	<tr><th scope="row">2</th><td>1768-10-01</td><td> -3.393</td><td>2.981</td><td>Canada</td></tr>
	<tr><th scope="row">3</th><td>1768-11-01</td><td>-12.829</td><td>3.967</td><td>Canada</td></tr>
	<tr><th scope="row">4</th><td>1768-12-01</td><td>-20.582</td><td>4.622</td><td>Canada</td></tr>
	<tr><th scope="row">5</th><td>1769-01-01</td><td>-24.756</td><td>4.722</td><td>Canada</td></tr>
	<tr><th scope="row">6</th><td>1769-02-01</td><td>-22.915</td><td>2.871</td><td>Canada</td></tr>
</tbody>
</table>



### filter may accept more than one condition


```R
head(filter(mydata, Country=="Canada" | Country == "China"))
```


<table>
<caption>A data.frame: 6 × 4</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1768-09-01</td><td>  5.257</td><td>3.107</td><td>Canada</td></tr>
	<tr><th scope="row">2</th><td>1768-10-01</td><td> -3.393</td><td>2.981</td><td>Canada</td></tr>
	<tr><th scope="row">3</th><td>1768-11-01</td><td>-12.829</td><td>3.967</td><td>Canada</td></tr>
	<tr><th scope="row">4</th><td>1768-12-01</td><td>-20.582</td><td>4.622</td><td>Canada</td></tr>
	<tr><th scope="row">5</th><td>1769-01-01</td><td>-24.756</td><td>4.722</td><td>Canada</td></tr>
	<tr><th scope="row">6</th><td>1769-02-01</td><td>-22.915</td><td>2.871</td><td>Canada</td></tr>
</tbody>
</table>




```R
head(filter(mydata, Country=="Canada" & AverageTemperature > 12))
```


<table>
<caption>A data.frame: 6 × 4</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1769-07-01</td><td>13.953</td><td>2.945</td><td>Canada</td></tr>
	<tr><th scope="row">2</th><td>1775-07-01</td><td>12.797</td><td>2.343</td><td>Canada</td></tr>
	<tr><th scope="row">3</th><td>1776-08-01</td><td>12.487</td><td>3.137</td><td>Canada</td></tr>
	<tr><th scope="row">4</th><td>1780-07-01</td><td>14.635</td><td>2.816</td><td>Canada</td></tr>
	<tr><th scope="row">5</th><td>1782-07-01</td><td>12.307</td><td>4.053</td><td>Canada</td></tr>
	<tr><th scope="row">6</th><td>1796-07-01</td><td>12.637</td><td>3.010</td><td>Canada</td></tr>
</tbody>
</table>



***

### mutate( ): adds new variables

#### Adding column representing the year


```R
mydata <- mutate(mydata, year = as.numeric(format(as.Date(dt), "%Y")))
```


```R
head(mydata)
```


<table>
<caption>A data.frame: 6 × 5</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th><th scope="col">year</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1743-11-01</td><td> 4.384</td><td>2.294</td><td>Ã…land</td><td>1743</td></tr>
	<tr><th scope="row">2</th><td>1744-04-01</td><td> 1.530</td><td>4.680</td><td>Ã…land</td><td>1744</td></tr>
	<tr><th scope="row">3</th><td>1744-05-01</td><td> 6.702</td><td>1.789</td><td>Ã…land</td><td>1744</td></tr>
	<tr><th scope="row">4</th><td>1744-06-01</td><td>11.609</td><td>1.577</td><td>Ã…land</td><td>1744</td></tr>
	<tr><th scope="row">5</th><td>1744-07-01</td><td>15.342</td><td>1.410</td><td>Ã…land</td><td>1744</td></tr>
	<tr><th scope="row">6</th><td>1744-09-01</td><td>11.702</td><td>1.517</td><td>Ã…land</td><td>1744</td></tr>
</tbody>
</table>




```R
is.numeric(mydata$year)
```


TRUE


**Whait? What?**

Command breakdown:

The commands below should be run on RStudio:

```
format(as.Date(mydata$dt), "%Y")
as.numeric(format(as.Date(mydata$dt), "%Y"))
mutate(mydata, year = as.numeric(format(as.Date(dt), "%Y")))
mydata <- mutate(mydata, year = as.numeric(format(as.Date(dt), "%Y")))
```

***

#### Adding column representing the industrial era


```R
mydata <- mutate(mydata, era=if_else(
    year <= 1969, "gas & oil", "electronic",
))

head(mydata, n=5)
```


<table>
<caption>A data.frame: 5 × 6</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th><th scope="col">year</th><th scope="col">era</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">1</th><td>1743-11-01</td><td> 4.384</td><td>2.294</td><td>Ã…land</td><td>1743</td><td>gas &amp; oil</td></tr>
	<tr><th scope="row">2</th><td>1744-04-01</td><td> 1.530</td><td>4.680</td><td>Ã…land</td><td>1744</td><td>gas &amp; oil</td></tr>
	<tr><th scope="row">3</th><td>1744-05-01</td><td> 6.702</td><td>1.789</td><td>Ã…land</td><td>1744</td><td>gas &amp; oil</td></tr>
	<tr><th scope="row">4</th><td>1744-06-01</td><td>11.609</td><td>1.577</td><td>Ã…land</td><td>1744</td><td>gas &amp; oil</td></tr>
	<tr><th scope="row">5</th><td>1744-07-01</td><td>15.342</td><td>1.410</td><td>Ã…land</td><td>1744</td><td>gas &amp; oil</td></tr>
</tbody>
</table>




```R
tail(mydata, n=5)
```


<table>
<caption>A data.frame: 5 × 6</caption>
<thead>
	<tr><th></th><th scope="col">dt</th><th scope="col">AverageTemperature</th><th scope="col">AverageTemperatureUncertainty</th><th scope="col">Country</th><th scope="col">year</th><th scope="col">era</th></tr>
	<tr><th></th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">544807</th><td>2013-04-01</td><td>21.142</td><td>0.495</td><td>Zimbabwe</td><td>2013</td><td>electronic</td></tr>
	<tr><th scope="row">544808</th><td>2013-05-01</td><td>19.059</td><td>1.022</td><td>Zimbabwe</td><td>2013</td><td>electronic</td></tr>
	<tr><th scope="row">544809</th><td>2013-06-01</td><td>17.613</td><td>0.473</td><td>Zimbabwe</td><td>2013</td><td>electronic</td></tr>
	<tr><th scope="row">544810</th><td>2013-07-01</td><td>17.000</td><td>0.453</td><td>Zimbabwe</td><td>2013</td><td>electronic</td></tr>
	<tr><th scope="row">544811</th><td>2013-08-01</td><td>19.759</td><td>0.717</td><td>Zimbabwe</td><td>2013</td><td>electronic</td></tr>
</tbody>
</table>



***