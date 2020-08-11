_An example blog for Gov 1347_

-------

Welcome to my election analysis blog! It will be updated **every Sunday.** Feel free to reach out to me ([sunyoungpark@g.harvard.edu](sunyoungpark@g.harvard.edu)) if you have any comments or questions.

# Past Presidential Election Results
## Aug 30, 2020

Predictions of the future are based on the patterns of the past. If X tended to predict Y well in the past, we would want to use that X in our model. So we start our journey by looking into past presidential election results -- first at the national level. 

One thing in particular stands out: in the last 60 or so years, the race for the presidency has been **remarkably competitive between the two major parties**. Since FDR, neither Republicans nor Democrats have maintained a monopoly over the White House:

![](past_results.png)

The first half of the twentieth century experienced greater swings and greater margins of victory, while point spreads in the last 20 years have been less than 10 points. We can zero in a few specific races and the prevailing narratives around the horse race:

* 1960
* 1968
* 1976
* 2000

We note another set of observations around **the winner's popular vote**. First, very famously in two races, the winner of the popular vote lost the election: Al Gore in 2000 and Hillary Clinton in 2016. This is a reflection of how *each* popular vote for a candidate is not equally valuable to their electoral victory because of the electoral college. The <u>state</u> where it is won matters. 

For example, winning 22 million votes in California (a state with 25 million voting-age citizens) is impressive but unnecessary to beat your opponent and win its 55 electoral votes (EV). Instead, it would be better if a candidate just won a slim majority of 12.5 million votes in California (55 EV), a slim majority of 5 million votes in Pennsylvannia (20 EV), and a slim majority of 4.5 million votes in North Carolina (15 EV). That's the same 22 million votes, but in one scenario a candidate wins 55 EV while in the other a candidate wins 90 EV. Whoa! This is an illustration of the distortions of a **winner-takes-all** electoral system where slim majorities in just a few moderately large states translate to huge gains in electoral college votes. Empirically, it ends up that electoral college vote margins [are more dramatic](https://www.pewresearch.org/fact-tank/2016/12/20/why-electoral-college-landslides-are-easier-to-win-than-popular-vote-ones/) than popular vote margins.

This is why presidential candidates tend to (mostly) focus their resources on swing states where they can win by a slim majority rather than firing up the base or purusing lost causes. We can also see which states vote blue/red and how consistently so.

![](past_results_state.png)

# How to predict election outcome?

I will try to predict 2020 election outcome using 7 variables: polling results, economic indexes, incumbency, campaign expenditure, mobilization stratetgies, exogenous shocks such as COVID19, and election administration. I use `R` and a simple ordinary least square model.

```r
lm(voteshare ~ polls + econ + incumbency + ads + 
               mobi + covidcases + admin, data)
```

## Polls

Can we trust polls? In 2016, many polls did not predict Trump's win. Below is the polling average across months leading up to 2016 election.

![](polls2016.png)

### Pollsters

+ Not all pollsters provide high quality data and interpretation. FiveThirtyEight provides *pollster ratings* based on the accuracy of their past prediction: [https://projects.fivethirtyeight.com/pollster-ratings/](https://projects.fivethirtyeight.com/pollster-ratings/)

+ But it is important to note that even good pollsters often disagree. [Same raw data can lead to different predictions by renowned pollsters.](https://www.nytimes.com/interactive/2016/09/20/upshot/the-error-the-polling-world-rarely-talks-about.html)

### Predictive Power

Polls do predict the outcome by and large.

![](polls_results.png)

## Economic Forces

1. GDP growth
2. Real Disposable Income
3. Unemployment

For the detailed analysis, please see this [separate page.](econ_analysis.md)

## Incumbency

## Advertising

## Mobilization

## Shocks

See [Healy and Malhotra 2013](healy_review.pdf) and [Ashworth et al. 2017](https://onlinelibrary.wiley.com/doi/abs/10.1111/ajps.12334) for the comprehensive review of the literature.

## Law and Adminisration

-----

### cf. Markdown basics

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
