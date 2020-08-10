---
title: A missing value by any other name
author: Jai
date: '2020-08-10'
slug: a-missing-value-by-any-other-name
categories:
  - Programming
tags:
  - R
description: ''
thumbnail: ''
---

Welp, I finally learned why people code missing values with absurd numbers. I feel like I should have untuited it from my personal experience.

If you collect data about body weight, for example, and you're missing a value for an observation, instead of leaving it null you might enter the value `-99`. You coded the missing value with an absurd number on purpose.

I always wondered why I saw that in some datasets.

The first reason you do that is so software imports of that data don't mess up the datatype of the variable, which is a possibility if you mix integer data with a string like `"MISSING"`.

It's safest if the software knows to return an error message like that. Error messages are good. They tell you something is inconsistent and you better figure out what.

Not all software does know to do that. I always loathed the old JET engine Microsoft SQL Server used to import Excel spreadsheets (which I also loathed for data interchange). If there was a value with an inconsistent datatype, the import would still succeed but the data driver would simply leave out the inconsistent values. I wouldn't know right away if the nulls I got in the load were due to missing values or data entry errors.

If you recode missing values with an absurd value, the user always knows what is going on. An absurd outlier is intended to tip them off that they forgot to handle the coded missing value on import. They'll see it when they look at the data.

When you import data, you do look at it, right?

Summarization of a data import is an essential task. If you make a habit of summarizing imported data and you forget to handle coded missing values, you'll see the absurd outlier and know what happened.

This is the safest ecosytem for a data user. Absurd outliers alert the user about missing values. Import errors alert the user about inconsistent datatypes that are likely to be data entry defects.

**The 101**

1. If you provide data, code missing values with an absurd value and document that in your codebook for all to see.
1. If you consume data, read the codebook and handle the missing values on import. Then summarize the data you loaded to detect outliers in the event you forgot to handle the missing values.

I learned these basic lessons during my daily reading of Andrew Gelman's treasure trove of a blog. His article and its accompanying commentary demonstrate the point. [Know your data, recode missing data codes](https://statmodeling.stat.columbia.edu/2020/08/10/know-your-data-recode-missing-data-codes/)