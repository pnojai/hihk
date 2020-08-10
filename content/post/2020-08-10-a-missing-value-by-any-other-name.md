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

If you collect data about body weight, for example, and you're missing a value for an observation, instead of leaving it null you might enter the value -99. You coded the missing value with an absurd number on purpose.

I always wondered why I saw that in some datasets.

The first reason you do that is so software imports of that data don't mess up. If you used a string like "MISSING", you'll frequently get an error when you try to import the data.

Now, error messages are good. They tell you something is inconsistent and you better figure out what. However, in a data import workflow there is another way to alert the user about missing values, by substituting (coding) an absurd value. If you forget to handle it, the outlier is intended to tip you off when you look at your data.

You did look at your data, right?

Summarization of your data import is an essential task. If you make a habit of that and you forget to handle missing values that have been coded, then the absurd outlier will tip you off.

I learned this basic lesson during my daily reading of Andrew Gelman's treasure-trove of a blog. The article and its commentary demonstrate the point. [Know your data, recode missing data codes](https://statmodeling.stat.columbia.edu/2020/08/10/know-your-data-recode-missing-data-codes/)