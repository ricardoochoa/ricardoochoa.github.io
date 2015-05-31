---
layout: post
title:  "Two factor ANOVA in R"
date:   2015-05-30 19:52:48
categories: Statistics R
---

Follow this code for a two-way ANOVA. In this example we will test region *v.s.* treatment

{% highlight splus %}
# libraries
library(ggplot2)

# anova
anova(lm(time ~ region * treatment, my.table))

# box and whiskers plot
qplot(region, time, data=my.table, notch=TRUE, geom="boxplot")
qplot(treatment, time, data=my.table, notch=TRUE, geom="boxplot")

{% endhighlight %}


