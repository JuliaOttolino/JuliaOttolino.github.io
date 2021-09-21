---
layout: post
title: Let's Get Started 
subtitle: Sourcing and Sorting Quality Data
cover-img: /SLACK PHOTO.jpg
thumbnail-img: /SLACK PHOTO.jpg
share-img: /SLACK PHOTO.jpg
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
