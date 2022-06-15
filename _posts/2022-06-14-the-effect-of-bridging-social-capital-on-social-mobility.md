---
layout: post
title: "The Effect of Bridging Social Capital on Social Mobility"
description: This is the paper I wrote as the final project for Data Science and Society, a class offered by the Duke University Sociology Department. It also incorporates work I did for Methods of Social Research, another sociology class. It demonstrates my ability to conduct exploratory data analysis and uses ordinary least squares and logistic regression. In the paper, I found evidence that relationships with high-status individuals are associated with upward mobility.
---

# The Effect of Bridging Social Capital on Social Mobility

## Introduction

According to Chetty et al. (2014), there are areas of the country, such
as Charlotte, North Carolina, where intergenerational upward mobility is
particularly scarce as compared to the rest of the country. One factor
that Chetty et al. (2014) identified as having a positive effect on
social mobility is social capital, specifically “the strength of social
networks and engagement in community organizations in local areas”
(p. 1558).

One form of social capital that may be particularly influential for
social mobility is bridging social capital or network ties between
unlike people, such as people from different social class backgrounds.
Of course, inter-class relationships are but one manifestation of
bridging social capital. Relationships between immigrants and natives
would be another example (Kanas et al., 2011; Lancee, 2010; Lancee,
2012). Such ties are regarded as potential dampeners on inequality by
DiMaggio and Garip (2012). According to them, these relationships
facilitate the dispersion of resources from elite social circles that
would otherwise monopolize such advantages in the absence of any link to
the less fortunate (DiMaggio & Garip, 2012). Thus, my hypothesis is that
bridging social capital has a positive effect on intergenerational
mobility.

In this paper, I investigate the question, What is the effect of
relationships with high status people on social mobility? Specifically,
I examine whether knowing a bachelor’s degree holder has a positive
relationship with intergenerational occupational mobility. I also
determine whether the size of this aforementioned effect is related to
how long the respondent has known the bachelor’s degree holder. This is
important because the effect of relationship length is indicative of the
direction of the association between ties to high status people
(bachelor’s degree holders in this case) and upward mobility. A positive
relationship indicates that knowing bachelor’s degree holders longer
amplifies upward mobility, suggesting that perhaps knowing a bachelor’s
degree holder leads to upward mobility as opposed to the case where the
upwardly mobile comes into contact with bachelor’s degree holders after
mobility.

## Data

The data for this analysis comes from the General Social Survey (GSS).
The GSS is a record of American social trends dating back to the 1970s
(“The General Social Survey,” n.d.) and is administered by NORC at the
University of Chicago (“About Our Name,” n.d.). According to the
National Science Foundation (2007), the GSS provides data on “a
nationally representative sample of non-institutionalized adults who
speak either English or Spanish” (p. 11). Thus, the GSS is not
representative of the entire U.S. population. GSS respondents have to be
18 or older; they have to be “non-institutionalized;” and they have to
be able to speak either English or Spanish (National Science Foundation,
2007, p. 11). Moreover, prior to 2006, even Spanish speakers were absent
from the target population of the GSS (National Science Foundation,
2007, p. 12-13).

Using GSS data, I will conduct an analysis involving a sample size of
1534 people, the total number of respondents in 1985. I am only able to
analyze 1985 data because that is the year when the variables most
relevant to my research question are available, `educ1` through `educ5`
as well as `known1` through `known5`. These variables come from the
social network module of the GSS, which provides information about “the
people with whom \[the respondent\] discussed important matters” within
the past 6 months (Smith et al., 2018). Information is available for
five of the people the respondent lists, hence the numbering scheme of
`educ1` through `educ5` and `known1` and `known5`. `educ1` through
`educ5` describes the education level of each person within the
respondent’s 5-person network. Likewise, `known1` through `known5`
describes how long the respondent has known each person in their
network. I will use `educ1` through `educ5` as markers of the
socioeconomic status of the people in the respondent’s network.

## Methods

In order to use the GSS to address my research question, I revised my
question to fit within the constraints of the variables available on the
survey. My research question is an attempt to understand one direction
of the relationship between high status ties and upward mobility, that
is the impact of high-status ties on upward mobility as opposed to
impact of upward mobility on high status ties. The directionality of
this relationship cannot be ascertained by simply identifying the
association between ties to high status people and upward mobility.
Thus, data on the length of the relationship between the respondent and
the high-status person, which is available on the GSS, is crucial. If
the effect of having a high-status contact gets larger the longer you
have this contact, we would have evidence (by no means definitive
though) that the high status contact itself is behind the effect. In
light of this, I rephrase my question to the following:

<br/>
<center>

>What effect does the length of a relationship with a high-status person
have on social mobility?

</center>

<br/>

To investigate this question, I first conducted exploratory data
analysis to obtain observational evidence of the relationship between
ties to high status people and upward mobility. For more robust results,
I also created an ordinary least squares regression model and a logistic
regression model so that a variety of control variables can be applied.

Before modeling can take place, I created two network variables: `educ`
and `known`. These variables are named for the prefixes of the GSS
variables from which they were derived. `educ` is the highest education
level present in the respondent’s network. The longest length of time
the respondent has known any person within their network with the
aforementioned education level is captured by `known`. Thus, `known`
describes how long the respondent has had contact with the most educated
person in their network. I also created a variable to quantify
socioeconomic mobility. The GSS scores the prestige of the respondent’s
occupation as well as the respondent’s father’s occupation. I took the
difference between the respondent’s score and their father’s score as a
measure of the extent of socioeconomic mobility experienced by the
respondent. This variable is the primary response variable of my models
and is akin to the way in which Nikolaev and Burns (2014)
operationalized occupational mobility.

The control variables that are included in my model can be divided into
five categories: parental socioeconomic status, demographic
characteristics, educational attainment, geography, and family
structure. Parental socioeconomic status is included because those who
come from families with higher socioeconomic statuses have, by
definition, less room with which to advance. Thus, variables such as the
father’s occupational prestige score, dummy variables to represent
whether or not the father or the mother has a bachelor’s degree, and
dummy variables for whether or not the respondent considered their
family income at age 16 as having been above or below the average for
American families are all included in the models. Demographic
characteristics such as age, sex, and race are also included. (In their
analysis of college majors and occupational status, Roksa and Levey
(2010) also controlled for age, sex, and race.) Moreover, there is a
dummy variable for whether or not the respondent has attained a
bachelor’s degree due to the financial benefits of doing so (Oreopoulos
& Petronijevic, 2013). Geography is considered because the work of
Chetty et al. (2014) demonstrates that there is significant regional
variation in rates of intergenerational upward mobility in the United
States and because “geographic mobility is related to income and
occupational status” (Markham, 1983). Finally, single parenthood was
found to negatively correlate with upward mobility by Chetty et
al. (2014).

## Results

<br/>

<img src="/images/2022-06-14/bar-plot-1-1.png" style="display: block; margin: auto;" />

<br/>

Exploratory data analysis supports my hypothesis that knowing a
high-status person has a positive effect on upward mobility. As can be
seen in Figure 1 above, a greater proportion of respondents who had a
high-status tie (knew a bachelor’s degree holder) experienced upward
mobility than respondents who did not have a high-status tie.
Specifically, the difference is 0.136, and it is significant at the 0.05
level. However, this finding says nothing about the direction of the
relationship between having high status ties and social mobility.

<br/>

<img src="/images/2022-06-14/bar-plot-2-1.png" style="display: block; margin: auto;" />

<br/>

To obtain any sense of directionality, one must incorporate time into
the analysis. After all, it is not hard to imagine a poor person who
lacked high-status contacts in the past attaining high-status friends
after achieving upward mobility. The rightmost plot in Figure 2 allows
us to see whether there is evidence for the reverse, that high-status
friends precedes upward mobility. Here, I only consider respondents who
have a relationship with a high-status person (a bachelor’s degree
holder). From the plot, it is apparent that a greater proportion of
those who knew a high-status person for more than six years (who
presumably are more likely to have known the high-status person prior to
upward mobility than those who knew the high-status person for a shorter
period of time) achieved upward mobility than those who only knew such a
person for up to six years, a difference of 0.129. However, the
difference in proportions is not statistically significant at the 0.05
level, just barely missing the mark. The difference is significant at
the 0.1 level though. There thus appears to be a positive relationship
between knowing a bachelor’s degree holder for a longer period of time
and upward mobility.

Perhaps simply knowing the most educated person in your network for more
than six years, regardless of whether they have a bachelor’s degree or
not, is positively associated with upward mobility. We examine this
possibility with the leftmost plot above where we take a look at only
those respondents who had no bachelor’s degree holders in their network.
If it is the length of the relationship that matters, then we would
expect a greater proportion of those who knew the most educated person
in their network for more than six years to have experienced upward
mobility even if they do not hold a bachelor’s degree. This is not the
case. Indeed, the reverse is true, a smaller proportion of those who
knew the most educated person for more than six years experienced upward
mobility compared with those who knew the non-graduate for up to six
years. However, the difference is not statistically significant. Thus,
if they do not have a bachelor’s degree, there appears to be no
association between knowing the most educated person in your network for
more than six years and upward mobility.

Of course, no variables were controlled for in any of the plots thus far
described. Thus, these visualizations do not account for the possibility
that confounding variables may actually lie at the heart of these
findings. To account for such variables, modeling can be used. I created
two different models, an ordinary least squares (OLS) regression model
as well as a logistic regression model. These two models differ on the
basis of their response variable. While the OLS model is intended to
predict the difference between the respondent’s occupational prestige
score and their father’s occupational prestige score, the logit model
can be used to predict the probability that the respondent would have an
occupational prestige score that is greater than their father’s. As a
result of this difference in variable type, discrepancies between the
two models can be expected.

| Term                                               | Estimate | Std. error | Statistic | p-value   |
|:--------------------------------------|-------:|---------:|--------:|:------|
| Intercept                                          |   25.780 |      3.704 |     6.960 | 0\*\*\*   |
| Has high status tie                                |    3.673 |      1.727 |     2.127 | 0.034\*   |
| Had tie for over 6 years                           |   -1.240 |      1.258 |    -0.985 | 0.325     |
| Father’s occupational prestige score               |   -0.920 |      0.036 |   -25.685 | 0\*\*\*   |
| Below average income at 16                         |   -1.123 |      1.257 |    -0.894 | 0.372     |
| Above average income at 16                         |    4.831 |      1.517 |     3.184 | 0.001\*\* |
| Father has bachelor’s                              |   -1.277 |      1.530 |    -0.834 | 0.404     |
| Mother has bachelor’s                              |   -0.364 |      1.609 |    -0.226 | 0.821     |
| Age                                                |    0.342 |      0.149 |     2.288 | 0.022\*   |
| Age squared                                        |   -0.003 |      0.002 |    -1.997 | 0.046\*   |
| Is female                                          |    0.137 |      0.778 |     0.176 | 0.86      |
| Is non-white                                       |   -2.982 |      1.432 |    -2.082 | 0.038\*   |
| Has bachelor’s                                     |   14.416 |      1.536 |     9.384 | 0\*\*\*   |
| Lived in the south at 16                           |   -0.604 |      0.960 |    -0.629 | 0.53      |
| Lived in rural area at 16                          |   -1.625 |      0.919 |    -1.767 | 0.077     |
| Lived in city at 16                                |    2.252 |      1.301 |     1.731 | 0.084     |
| Moved to different city in same state since 16     |    1.234 |      0.964 |     1.281 | 0.201     |
| Moved to different state since 16                  |    2.181 |      0.953 |     2.289 | 0.022\*   |
| Single-parent household                            |   -0.856 |      5.359 |    -0.160 | 0.873     |
| Below average income at 16 and has bachelor’s      |    1.447 |      2.704 |     0.535 | 0.593     |
| Above average income at 16 and has bachelor’s      |   -6.088 |      2.479 |    -2.455 | 0.014\*   |
| Below average income at 16 and has high status tie |   -0.343 |      2.172 |    -0.158 | 0.875     |
| Above average income at 16 and has high status tie |   -4.130 |      2.250 |    -1.836 | 0.067     |
| Had high status tie for over 6 years               |    4.474 |      1.747 |     2.560 | 0.011\*   |

Figure 3: Ordinary least squares regression model output

\*p \< 0.05 \*\*p \< 0.01 \*\*\*p \< 0.001

<br/>

The output of the OLS model is shown in Figure 3. All five categories of
control variables, parental socioeconomic status, demographic
characteristics, educational attainment, geography, and family structure
are included. A term representing the square of the `age` variable has
been added to account for the nonlinear relationship between `age` and
mobility. In total there are 23 variables in the model. However, the
variables most relevant to my research question are whether or not the
respondent has a high-status tie (The most educated person in their
5-person network is a bachelor’s degree holder.), whether or not the
respondent has known the most educated person in their 5-person network
for over six years, and the interaction between these two variables (the
effect of knowing a bachelor’s degree holder for more than six years).
The coefficients for these three variables are around 3.673, -1.24, and
4.474 respectively. Only knowing a bachelor’s degree holder and knowing
a bachelor’s degree holder for over six years are statistically
significant at the 0.05 level. The result that, if the respondent knows
no bachelor’s degree holders, knowing the most educated person in a
5-person network for over six years does not have a significant impact
on upward mobility is consistent with the exploratory data analysis. The
regression output also expands on the EDA by showing that knowing a
high-status tie for up to six years yields a positive effect on
occupational mobility. Likewise, the variable most important for
answering my research question, the interaction term that represents
knowing a high-status tie for over six years, is positive and
significant at the 0.05 level, indicating that knowing the high-status
tie for a longer period of time (over six years vs. up to six years)
further increases the extent of upward occupational mobility.

<br/>

| Term                                               | Estimate | Std. error | Statistic | p-value     |
|:--------------------------------------|-------:|---------:|--------:|:-------|
| Intercept                                          |    3.340 |      0.818 |     4.083 | 0\*\*\*     |
| Has high status tie                                |    0.091 |      0.367 |     0.247 | 0.805       |
| Had tie for over 6 years                           |   -0.659 |      0.266 |    -2.474 | 0.013\*     |
| Father’s occupational prestige score               |   -0.139 |      0.011 |   -12.520 | 0\*\*\*     |
| Below average income at 16                         |    0.015 |      0.265 |     0.057 | 0.954       |
| Above average income at 16                         |    0.615 |      0.315 |     1.950 | 0.051       |
| Father has bachelor’s                              |   -0.895 |      0.382 |    -2.344 | 0.019\*     |
| Mother has bachelor’s                              |    0.391 |      0.366 |     1.068 | 0.286       |
| Age                                                |    0.080 |      0.032 |     2.464 | 0.014\*     |
| Age squared                                        |   -0.001 |      0.000 |    -2.240 | 0.025\*     |
| Is female                                          |    0.396 |      0.171 |     2.320 | 0.02\*      |
| Is non-white                                       |   -0.789 |      0.317 |    -2.486 | 0.013\*     |
| Has bachelor’s                                     |    2.544 |      0.390 |     6.515 | 0\*\*\*     |
| Lived in the south at 16                           |   -0.397 |      0.207 |    -1.922 | 0.055       |
| Lived in rural area at 16                          |   -0.419 |      0.195 |    -2.155 | 0.031\*     |
| Lived in city at 16                                |    0.552 |      0.294 |     1.879 | 0.06        |
| Moved to different city in same state since 16     |    0.300 |      0.211 |     1.427 | 0.154       |
| Moved to different state since 16                  |    0.378 |      0.206 |     1.833 | 0.067       |
| Single-parent household                            |    0.427 |      1.722 |     0.248 | 0.804       |
| Below average income at 16 and has bachelor’s      |   -0.601 |      0.716 |    -0.840 | 0.401       |
| Above average income at 16 and has bachelor’s      |   -1.024 |      0.569 |    -1.801 | 0.072       |
| Below average income at 16 and has high status tie |    0.017 |      0.481 |     0.035 | 0.972       |
| Above average income at 16 and has high status tie |   -0.785 |      0.483 |    -1.628 | 0.104       |
| Had high status tie for over 6 years               |    1.266 |      0.381 |     3.324 | 0.001\*\*\* |

Figure 4: Logistic regression model output

\*p \< 0.05 \*\*p \< 0.01 \*\*\*p \< 0.001

<br/>

I also ran a logit model using the exact same variables as the OLS
model. In the logit model output shown in Figure 4, the p-value of the
interaction term is even smaller than the OLS model. Indeed, it is
significant at the 0.001 level. However, the positive effect of knowing
a bachelor’s degree holder is no longer significant at the 0.05 level,
and there is also a significant negative effect of knowing the most
educated person in the 5-person network for more than six years.
However, since the coefficient of the interaction term is greater than
the coefficient of knowing the most educated person for more than six
years, knowing a bachelor’s degree holder for more than six years still
yields a net positive effect on social mobility. This result does
suggest that, if the respondent does not know a high-status person
(bachelor’s degree holder), then knowing the highest status person in
their network for more than six years has a negative effect on social
mobility, contradicting both the OLS model as well as the exploratory
data analysis. Both of these previous analyses indicated that if the
respondent’s network lacks a bachelor’s degree holder, knowing the most
educated person in the network affords no effect on social mobility.

Despite the differences between the OLS and logit models, the two models
agree that the variable most important for my research question, the
effect of knowing a bachelor’s degree holder for more than six years, is
significant and positive. I also ran the OLS model with only the
occupational prestige score of the respondent as the response variable
as opposed to the difference between child and father. Results were
consistent between the two response variable specifications including
the significant positive relationship between knowing a bachelor’s
degree holder for more than six years and social mobility. Finally, both
the logit and OLS models agree that having above average family income
at 16 and having a high-status tie produces a significant negative
effect on social mobility, indicating that the benefit of having a
relationship with a high-status person is higher for those who report
average or below average family income at 16.

## Discussion

My analysis has produced evidence to affirm my hypothesis that having a
relationship with high-status people leads to greater social mobility.
This result is consistent with other articles on bridging social
capital/cross-class ties. Literature on this subject show that
relationships that unite people from distinct backgrounds improve the
outcomes of the less advantaged in terms of income/occupational status
(Kanas et al., 2011; Lancee 2010; Lancee, 2012; and Zhang et al., 2011)
as well as educational achievement (Lessard and Juvonen, 2019). However,
to the best of my knowledge, no analysis has been conducted to
investigate the role of bridging social capital on intergenerational
social mobility. Other papers have found improvements across briefer
time spans as opposed to intergenerational improvements.

Although my finding is consistent with a circumstance in which the
educational level of people’s networks increases upward mobility, it
ought not to be considered conclusive proof. Moreover, my analysis
cannot explain the precise mechanism by which increased exposure to high
status people leads to greater social mobility. Additionally, a
significant portion of the 1985 sample of the GSS were not included in
my models due to missing values. Indeed, my OLS and logit models use
only 61.93% of the sample. Finally, to ascertain occupational mobility,
I only had access to the occupational prestige score of the respondent’s
father. According to Beller (2009), ignoring characteristics of the
mother when analyzing mobility may produce inaccurate results.

With such limitations in mind, a potential policy response to my finding
could be the expansion of national service programs, as proposed by
former presidential candidate Pete Buttigieg, that seeks to bring
together young people from all walks of life (Ismay, 2019). If the
results of this paper were to hold, such a policy would increase upward
mobility in America.

## Acknowledgements

I would like to thank Dr. Christopher A. Bail and Devin J. Cornell for
their help on this project.

## Bibliography

“About Our Name.” NORC at the University of Chicago,
<https://www.norc.org/about/Pages/about-our-name.aspx>. Accessed 23
Oct. 2020.

Beller, E. (2009). Bringing intergenerational social mobility research
into the twenty-first century: Why mothers matter. *American
Sociological Review*. 74(4), 507-528.
<https://doi.org/10.1177/000312240907400401>

Chetty, R., Hendren, N., Kline, P., & Saez, E. (2014). Where is the land
of opportunity? The Geography of intergenerational mobility in the
United States. *Quarterly Journal of Economics*, 4(129), 1553-1623.
<https://doi.org/10.1093/qje/qju022>

DiMaggio, P., & Garip, F. (2012). Network effects and social inequality.
*Annual Review of Sociology*, 38, 93-118.
<https://doi.org/10.1146/annurev.soc.012809.102545>

The General Social Survey. NORC at the University of Chicago,
<https://gss.norc.org>. Accessed 23 Oct. 2020.

Kanas, A., van Tubergen, F., & Van der Lippe, T. (2011). The role of
social contacts in the employment status of immigrants: A panel study of
immigrants in Germany. *International Sociology*, 26(1), 95-122.
<https://doi.org/10.1177/0268580910380977>

Lancee, B. (2010). The economic returns of immigrants’ bonding and
bridging social capital: The case of the Netherlands. *International
Migration Review*, 44(1), 202-226.
<https://doi.org/10.1111/j.1747-7379.2009.00803.x>

Lancee, B. (2012). The economic returns of bonding and bridging social
capital for immigrant men in Germany. *Ethnic and Racial Studies*,
35(4), 664-683. <https://doi.org/10.1080/01419870.2011.591405>

Lessard, L. M., & Juvonen, J. (2019). Cross-class friendship and
academic achievement in middle school. *Developmental Psychology*,
55(8), 1666-1679. <http://dx.doi.org/10.1037/dev0000755>

Markham, W. T., Macken, P. O., Bonjean, C. M., & Corder, J. (1983). A
note on sex, geographic mobility, and career advancement. *Social
Forces*, 61(4), 1138-1146. <https://doi.org/10.2307/2578283>

National Science Foundation. (2007). *The General Social Survey (GSS):
The next decade and beyond*. National Science Foundation.
<https://www.nsf.gov/pubs/2007/nsf0748/nsf0748.pdf>

Nikolaev, B., & Burns, A. (2014). Intergenerational mobility and
subjective well-being—Evidence from the general social survey. *Journal
of Behavioral and Experimental Economics*, 53, 82-96.
<http://dx.doi.org/10.1016/j.socec.2014.08.005>

Oreopoulos, P., & Petronijevic, U. (2013). Making college worth it: A
review of research on the returns to higher education (NBER Working
Paper No. 19053). Cambridge, MA: National Bureau of Economic Research.
<http://www.nber.org/papers/w19053>

Palardy, G. J., (2013). High school socioeconomic segregation and
student attainment. *American Educational Research Journal*, 50(4),
714-754. <https://doi.org/10.3102/0002831213481240>

Roksa, J., & Levey, T. (2010). What can you do with that degree? College
major and occupational status of college graduates over time. *Social
Forces*, 89(2), 389-415. <https://doi.org/10.1353/sof.2010.0085>

Ismay, J. (2019, July 3). Pete Buttigieg proposes national service
programs for climate change and mental health. *The New York Times*.
Retrieved from <https://www.nytimes.com>
