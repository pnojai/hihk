---
title: Going with Minimo
author: Jai
date: '2019-04-12'
slug: going-with-minimo
categories:
  - Web
tags:
  - Blogdown
authors: []
---

# A beginning is a delicate time

I initialized a static website in RStudio using Blogdown and the theme, Minimo. I'm not sure
Minimo is compatible. The function blogdown:::new_post_addin() returns the following
errors.

Error in attr(x, "yml_type") <- "seq" : 
  attempt to set an attribute on NULL
Warning in yaml::yaml.load(x, handlers = list(seq = function(x) { :
  an error occurred when handling type 'seq'; using default handler
Error in attr(x, "yml_type") <- "seq" : 
  attempt to set an attribute on NULL
Warning in yaml::yaml.load(x, handlers = list(seq = function(x) { :
  an error occurred when handling type 'seq'; using default handler