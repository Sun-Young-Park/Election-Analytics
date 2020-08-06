Welcome to my election prediction blog! It's updated every Sunday. Feel free to reach out to me (sunyoungpark@g.harvard.edu) if you have any comments and questions.

# Past Presidential Election Results

![](past_results.png)

We can also see which states vote blue/red and how consistently so.

![](past_results_state.png)

# How to predict election outcome?

I will try to predict 2020 election outcome using 7 variables: polling results, economic indexes, incumbency, campaign expenditure, mobilization stratetgies, exogenous shocks such as COVID19, and election administration. I use R and a simple ordinary least square model.

```r
lm(voteshare ~ polls + econ + incumbency + ads + mobi + covidcases + admin, data)
```

## Polls

Can we trust polls? In 2016, many polls did not expect Trump's win. Below is the polling average across months leading up to 2016 election.

![](polls_2016.png)

### Pollsters

https://projects.fivethirtyeight.com/pollster-ratings/

We have to note that even good pollsters could disagree. [same raw data, four different predictions](https://www.nytimes.com/interactive/2016/09/20/upshot/the-error-the-polling-world-rarely-talks-about.html)

![](polls_results.png)

## Economic Forces

## Incumbency

## Advertising

## Mobilization

## Shocks

## Law and Adminisration

### cf. Markdown basics

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

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
