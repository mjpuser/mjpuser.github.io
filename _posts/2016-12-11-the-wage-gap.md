---
layout: post
---

I was surprised to hear about the pay gap.  It's messed up, and if it exists, I want to understand why.  This post is an attempt gain a better understanding why the wage gap exists.

<style>
.women { color: green; }
.men { color: blue; }
</style>


### The research

One day I got the nerve to do some research, and I found <a href="http://www.aauw.org/research/the-simple-truth-about-the-gender-pay-gap/" target="_blank" hack="_">The Simple Truth about the Gender Pay Gap (Fall 2016)</a>.  It's the first article to come up in Google's search results, and it shows some shocking stats on the difference in pay.  They showcase this table of salaries:

![The Truth: Gender Pay Gap](/images/posts/wage-gap/the-simple-truth-figure-2-v2.jpg)

The second article that comes up in Google, <a href="http://www.infoplease.com/ipa/A0763170.html" target="_blank" hack="_">Infoplease.com: The Wage Gap</a>, also shows that in 2013, women made 78 cents on the dollar.  Making sure I research this properly, I played devil's advocate, and searched for "gender wage gap myth", and I found <a href="http://www.forbes.com/sites/karinagness/2016/04/12/dont-buy-into-the-gender-pay-gap-myth/" target="_blank" hack="_">Don't Buy Into The Gender Pay Gap Myth</a>, which claims to be written by a woman, and breaks down the wage gap argument, taking into account factors such as hours worked or likelihood to be in a union.  They claim that this accounts for about 15% of the gap, and so women are within 5 cents on the dollar vs men.  It also claims that we could close the gap to 0 by taking into account even more factors that are at play.   This still sounds scandalous, even if it is at a lesser degree.  Although, if I am being honest with myself, we can't just say it's sexist.  We have rule out other possibilities like schooling, grades, career choice, and performance.

### Looking closer

One problem I had with both sources was that the data was hard to get to.  All I want is a link, and I couldn't easily find one.  I also took issue with the use of the median (which is the middle value), since there are a lot more characteristics of a distribution that should be considered.  Let's say the distributions that determine the expected pay rate look like the one below (they are made up graphs), where the x-axis is the dollars/hour, and the y-axis is how likely you are to get paid that amount.  In statistics, these are called <a href="https://en.wikipedia.org/wiki/Probability_density_function" target="_blank" hack="_">density functions</a>.

![Worst case Senario](/images/posts/wage-gap/normal-dist-median.png)


Let's say the green is the distribution of pay for women, and blue is the distribution for men.  The median for each of these groups is at the peak.  So the median in this case, would be an easy way to communicate that there is a wage gap, but this is not how every distribution is shaped.  


## Graphing Wage, Hours worked, and Hourly rate

DISCLAIMER: I am not a statistician, so my math might be crap.  Also, I didn't consider location as a factor.  If I did, it would have made my sample sizes a lot smaller.  With that said, let's look at some graphs...

### The data source

I ended up using <a href="https://www.census.gov/programs-surveys/acs/data/pums.html" target="_blank" hack="_">2015 ACS Public Use Microdata Sample files (PUMS)</a>.  It comes from the United States Census Bureau, which I believe is independent of the wage gap issue, so I think we're good.  

**For all the following graphs, <span class="men">blue = men</span>, <span class="women">green = women</span>**.

### Chief executives and legislators

**Summary** Executives and legislators are generally considered important people and are paid well.  They are also the first category in the census data.  The general trend here is that men are more likely to get paid more, and work more hours per week.  Overall, men are around 2 - 3 times as likely as women to have this career.

#### 20-year-olds

There were a total of 103 women in this sample, and 193 men.

| <img src="/images/posts/wage-gap/chief-execs/20-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/chief-execs/20-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/chief-execs/20-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage, Hours/Week, $/Hour:</span>** $40,000, 40h, $19/h

**<span class="men">Men's Median Wage, Hours, $/Hour:</span>** $50,000, 45h, $19/h

#### 30-year-olds

There were a total of 414 women and 1,023 men in this sample.

| <img src="/images/posts/wage-gap/chief-execs/30-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/chief-execs/30-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/chief-execs/30-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage, Hours/Week, $/Hour:</span>** $75,000, 40h, $33/h

**<span class="men">Men's Median Wage, Hours/Week, $/Hour:</span>** $100,000, 50h, $38/h

#### 40-year-olds

There were a total of 826 women and 2,183 men in this sample.

| <img src="/images/posts/wage-gap/chief-execs/40-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/chief-execs/40-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/chief-execs/40-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage:</span>** $100,000, 45h, $43/h

**<span class="men">Men's Median Wage:</span>** $140,000, 50h, $54/h

### Physicians

**Summary** Men tend to make more, except for the 20-year-old bracket.  Men tend to work more except for the 20-year-old bracket.  Men and women are about equally likely to become physicians.

#### 20-year-olds

There were a total of 303 women in this sample, and 315 men.

| <img src="/images/posts/wage-gap/physicians/20-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/physicians/20-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/physicians/20-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage, Hours/Week, $/Hour:</span>** $50,000, 65h, $14/h

**<span class="men">Men's Median Wage, Hours, $/Hour:</span>** $50,000, 60h, $15/h

#### 30-year-olds

There were a total of 1,085 women and 1,217 men in this sample.

| <img src="/images/posts/wage-gap/physicians/30-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/physicians/30-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/physicians/30-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage, Hours/Week, $/Hour:</span>** $105,000, 50h, $48/h

**<span class="men">Men's Median Wage, Hours/Week, $/Hour:</span>** $150,000, 55h, $56/h

#### 40-year-olds

There were a total of 851 women and 1,283 men in this sample.

| <img src="/images/posts/wage-gap/physicians/40-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/physicians/40-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/physicians/40-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage:</span>** $177,000, 42h, $76/h

**<span class="men">Men's Median Wage:</span>** $333,000, 50h, $108/h


### Accountants

**Summary** Men are slightly more likely to work more hours, and men are slightly more likely to make more money.  Women are 1 - 2 times more likely to pursue a career as an accountant than men.

#### 20-year-olds

There were a total of 1,627 women in this sample, and 1,340 men.

| <img src="/images/posts/wage-gap/accountants/20-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/accountants/20-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/accountants/20-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage, Hours/Week, $/Hour:</span>** $40,000, 40h, $19/h

**<span class="men">Men's Median Wage, Hours, $/Hour:</span>** $45,000, 40h, $19/h

#### 30-year-olds

There were a total of 2,671 women and 1,499 men in this sample.

| <img src="/images/posts/wage-gap/accountants/30-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/accountants/30-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/accountants/30-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage, Hours/Week, $/Hour:</span>** $50,000, 40h, $23/h

**<span class="men">Men's Median Wage, Hours/Week, $/Hour:</span>** $70,000, 40h, $30/h

#### 40-year-olds

There were a total of 3,001 women and 1,366 men in this sample.

| <img src="/images/posts/wage-gap/accountants/40-wage.png" style="width:400px"/> | <img src="/images/posts/wage-gap/accountants/40-hours.png" style="width:400px"/> | <img src="/images/posts/wage-gap/accountants/40-hourly.png" style="width:400px"/> |

**<span class="women">Women's Median Wage:</span>** $52,000, 40h, $37/h

**<span class="men">Men's Median Wage:</span>** $85,000, 40h, $108/h

## Conclusion

The wage gap exists, but did this data answer why? And can we say with 100%, or at least 95% certainty that it's because of sexism?  I think to answer that question, the best thing I could do next is make a linear regression between hours worked and wage to see if there is a correlation.  I could also do a Chi-Squared test to see if women are within the same distribution as men.  I will add updates to this post as I do this work.

If I did anything here that doesn't make sense statistically, or if you want me to share the code I used to graph this data, then please <a href="/#contact">contact me</a>.  

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
