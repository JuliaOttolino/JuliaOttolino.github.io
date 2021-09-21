---
layout: post
title: The Shocking Comparison 
subtitle: The Absence of Disposable Income
#cover-img: /SLACK PHOTO.jpg
#thumbnail-img: "/assets/img/SLACK PHOTO.jpg"
#share-img: /SLACK PHOTO.jpg
---

First thing first, I went onto BLSbetaLabs.gov and I found the data I needed for _Average Annual Income_ and _Average Annual Expenditures_ for all wage quintiles. I sourced this data back to the earliest year it supplied (1984), and retrieved the most recent year I could (2020). 
With this raw CSV data and some simple arithmetic, I carried on to create two new comparative categories, __Average Disposable Income__ …

Example:

_avg_inc_vs_exp['Top20_DI'] = pd.DataFrame(avg_inc_vs_exp['Top20_income'] - avg_inc_vs_exp['Top20_expenditures'])_

…and __Disposable Income Percentages__.

Example:

_GDP['TopQ_DI_pct'] = pd.DataFrame(avg_inc_vs_exp['Top20_DI'] / avg_inc_vs_exp['Top20_income']*100)_

(Who says math isn’t useful anymore!?)

To complete my data sets, I went onto TheWorldBank.org’s Data Bank and retrieved GDP growth percentages from the very same years (1984-2020). 

37 years’ worth of GDP and income data will surely allow us to see if any relationships exist between Average GDP growth and Average Disposable Income Percentages per quintile.

**Note: There was a ton of very tedious column organizing, but I won’t bore you with those details. Enjoy the ride.
**Also Note: You can find my Data sources in the drop-down menu. 


After organizing all of the data into usable data-frames, it was time to finally see all of the quintile’s Average Disposable Income Percentages (DI%) in comparison to one another. I chose to implement this with stacked boxplots. 

img: ->!"/assets/img/DI box plot.png"<-

The image above gives us loads of information.

It is quite obvious that the Lowest Quintile has the widest range of DI% over the 37-year period. We can infer that the income stability is very volatile. We can also see that the Lowest Quintile had it’s highest DI% sitting at approximately -350%, which is shockingly considered to be its highest outlier year; sadly all other data points from the 37-year period sit exceedingly lower than that, with the mean percentage sitting just below -600%. That is not a feasible way to live.

The 2nd Quintile has a much smaller range when in comparison to the lowest quintile, but a much larger range when compared to the 3 higher ones. Income seems to be much less volatile. However, according to all of the DI%’s sitting roughly between the -75% and -200%, we can surely conclude that it is exceedingly difficult to stay monetarily afloat. 

Now let’s look at our middle class, the third quintile. The range is much more condensed, yet we see the middle class still sitting in the negatives for all years 1984-2020. The bulk of the data points for the third quintile sit between -25% and -50%. This pretty explains why the middle-class households are still living paycheck to paycheck with two incomes under one roof. 

When we get to the fourth quintile, we finally see an income class that has the mean of its data points sitting at the breakeven-point (0). Still, about half of the dataset’s years has the fourth quintile income bracket seeing negative average disposable income percentages.
It isn’t until we get all the up to the top quintile, do we see all over the data points for the 37-year period sitting in the positives. It is such a jump, too. The lucky echelon of our society sees their lowest outlier year at the breakeven-point, and the majority of their years they are seeing DI% at about 25%.
(Keep in mind, the top quintile’s 25% of annual disposable income looks __a lot__ different than the lower quintile’s 25% of DI.)
