---
layout: post
title:  "Dataset Analysis [Part 1]: Cost of Living / Introduction"
categories: data-science
---

# Introduction
This work aims to analyze a set of data that has the price of products in several cities in countries around the world, obtaining a model for grouping these cities according to the price of the products.

# Related Works

The Worldwide Cost of Living is a twice-yearly survey by the Economist Intelligence Unit that compares more than 400 individual prices across 160 products and services. This includes food, drinks, clothing, household items and personal care items, renting houses, transportation, utility bills, private schools, domestic help and recreation costs [Economist 2015].

The survey helps human and financial resource managers calculate cost of living allowances and create compensation packages for expatriates and business travelers. The survey incorporates comparative cost of living indices that are easy to understand across cities. The survey allows city-to-city comparisons, but for the purposes of this report, all cities are compared to a New York base city, with an index set at 100. The survey has been conducted for more than 30 years [Economist 2015].

# Motivation

The motivation of the present work is: to group cities according to the cost of living, characterizing each group. To solve the problem, we opted for the use of **K-Means**, which is an unsupervised learning algorithm.

# Dataset

The dataset was selected from the <a href="https://www.kaggle.com">Kaggle</a> website, and is called <a href="https://www.kaggle.com/stephenofarrell/cost-of-living">Cost of Living</a>, in which the columns represent the cities and lines the products with the cost in each city. This dataset was built with data from the <a href="https://www.numbeo.com/">Numbeo</a> website, which provides a global database of prices, crime rates, quality of health care, among other statistics.

In this original data set, the columns represent the cities and the lines represent the value of each item in the city, but for practical purposes we will invert the data, such that the lines will represent the cities and the columns the value of each item in this city, in addition an additional column will be used to store which cluster the city belongs to.

This dataset contains 160 cities in several countries and 55 items with price in each citie.

# References

Economist, T. (2015). Worldwide cost of living report 2015, <a href="https://www.eiu.com/public/topical_report.aspx?campaignid=wcol2015">https://www.eiu.com/public/topical_report.aspx?campaignid=wcol2015</a>, last acess on 28 February of 2020.
