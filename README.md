_An example blog for Gov 1347_

-------

Welcome to my election analysis blog! It will be updated *every Sunday.* Feel free to reach out to me ([sunyoungpark@g.harvard.edu](sunyoungpark@g.harvard.edu)) if you have any comments or questions.

A note for students on blogging / writing principles:

* Please either title your figures in `R` or label them in the `.md` files.
* Please date each entry.
* Each blog entry should be no more than 1000 words. 
* A good blog post will focus on 2-3 big points (observations or predictions or opinions or insights) and provide clear, interpretable, and convincing evidence -- that is, analysis, visualizations, and qualitative commentary -- supporting that.
* Tip: use **bold** and *italics* wisely -- **bold** is most effective for highlighting your big points as section headings or paragraph starters, while *italics* help draw attention to surprising statements, facts, or concepts. 

Here is an example blog post for reference. It's not perfect, nor finished, but has the key elements of a good election analysis blog.

# Past Presidential Election Results
## Aug 30, 2020

Predictions of the future are based on the patterns of the past. If X tended to predict Y well in the past, we would want to use that X in our model. So we start our journey by looking into past presidential election results -- first at the national level. 

**Elections are generally competitive between the two parties.** One thing in particular stands out: in the last 60 or so years, the race for the presidency has overall been *remarkably competitive between the two major parties*. Since FDR, neither Republicans nor Democrats have maintained a monopoly over the White House:

![](past_results.png)

The first half of the twentieth century experienced greater swings and greater margins of victory, while point spreads in the last 20 years have been less than 10 points. The 4 closest elections in the last 60 years and their "prevailing narratives" are:

* **2000, `0.5%` margin or 500k votes (Bush vs. Gore).** Gore managed to distance himself from Clinton's scandals (which put him neckand-neck with Bush); though, really, this was anyone's election.
* **1960, `0.7%` margin or 120k votes (JFK vs. Nixon).** The Republican party was hurt by the 1958 recession (we'll talk about this more when we read [The Message Matters](https://www.amazon.com/Message-Matters-Economy-Presidential-Campaigns/dp/0691139636)); JFK mobilized a new cohort of Catholic voters; JFK campaigned wisely in key swing states. 
* **1968, `0.7%` margin or 500k votes (Nixon vs. Humphrey).** As the South began to re-align, Nixon's [Southern Strategy](https://en.wikipedia.org/wiki/Southern_strategy) appealed to racist whites in the South; beginning of the "culture wars" which favored the Republicans in rural areas; protests against Humphrey for his unpopular pro-war position.
* **1976, `2.1%` margin or 1.7 million votes (Carter vs. Ford).** Incumbent Republicans saddled by a poor economy (again) and hurt by Watergate scandal; Carter campaigned effectively as an "outsider"; blunders by Ford on the campaign trail.

Similarly, the 4 biggest landslides in the last 60 years are:


We will explore this semester, what empirical evidence we really have for these "prevailing narratives" and whether they generalize beyond these races.

**A winner-take-all system with electors based on population distorts win margins.** We note another set of observations around *the winner's popular vote*. First, very famously in two races, the winner of the popular vote lost the election: Al Gore in 2000 and Hillary Clinton in 2016. This is a reflection of how *each* popular vote for a candidate is not equally valuable to their electoral victory because of the electoral college. The <u>state</u> where it is won matters. 

For example, winning 22 million votes in California (a state with 25 million voting-age citizens) is impressive but unnecessary to beat your opponent and win its 55 electoral votes (`EV`). Instead, it would be better if a candidate just won a slim majority of 12.5 million votes in California (`55 EV`), a slim majority of 5 million votes in Pennsylvannia (`20 EV`), and a slim majority of 4.5 million votes in North Carolina (`15 EV`). That's the same 22 million votes, but in one scenario a candidate wins `55 EV` while in the other a candidate wins `90 EV`. Whoa! 

This is an illustration of the distortions of a *winner-takes-all* electoral system where slim majorities in just a few moderately large states (which promise substantial EVs!) translate to huge electoral gains. Empirically, it ends up that electoral college vote margins [are more dramatic](https://www.pewresearch.org/fact-tank/2016/12/20/why-electoral-college-landslides-are-easier-to-win-than-popular-vote-ones/) than popular vote margins. This is why presidential candidates tend to (mostly) focus their resources on moderately large swing states where they can win by a slim majority rather than firing up the base or purusing lost causes. 

Below we can see which states vote blue/red and how consistently so. In section, we will produce more nuanced versions of these maps that highlight ''swinginess'' of various states.

![](past_results_state.png)

**Prediction: using past election returns.** Using the insights above, I will predict 2020 election state-by-state election outcomes, for each state `i` simply using the average of the past two election popular vote returns: 

```
voteshare2020_i = (voteshare2016_i + voteshare2012_i)/2
```

(Results in graphical form with commentary follows here)

<!--
## Polls

```r
lm(voteshare ~ polls + econ + incumbency + ads + 
               mobi + covidcases + admin, data)
```

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
-->

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
