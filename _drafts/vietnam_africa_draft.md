---
layout: post
title: "Vietnam and Africa comparison"
modified:
categories: blog
excerpt:
comments: true
share: true
tags: [vietnam, africa]
image:
  feature:
---

Despite knowing that there is a huge variation among African countries, I was still pleasantly shocked to find out the other day that [Africa is larger than the US, Mexico, China, India, and Europe *combined*](http://www.economist.com/blogs/dailychart/2010/11/cartography). Given Africa's geographic size, I'm curious to see a graph of its economic landscape. We compare GDP per capita of African countries with that of Vietnam (which we know well.) Vietnam is the bold red line in the graph.

<figure>
	<img src="/images/vietnam_africa_full.png" alt="vietnam_africa_full">
</figure>

The graph shows a few shocking cases:

- *Why are Seychelles so wealthy?* Small island, lots of tourists.
- *What's up with Equatorial Guinea's rise?* Small island, huge recent discovery of oil. It is unfortunately a classic case of [resource curse](http://www.bbc.com/news/world-africa-13317174), with ordinary people suffering from poverty despite the misleadingly high GDP per capita.

Given these outliers, the graph also poses an interesting visualization challenge. If we want to compare Vietnam with Africa, how should we construct a valid comparison group?

**The first solution** is to ignore the outliers and zoom in the region of interest. We also plot the median line in blue and the surrounding 50% confidence interval. It turns out that there has been only limited growth in Africa, whereas Vietnam has grown steadily since 1985, [the start of its economic reform](http://www.vietnam-logistics.com/2012/05/vietnam-s-logistics-industry.html). 

<figure>
	<img src="/images/vietnam_africa_comparison.png" alt="vietnam_africa_comparison">
	<figcaption><a href="/images/vietnam_africa_comparison.png" title="Comparing GDP per cap between Vietnam - Africa">Comparing GDP per cap between Vietnam - Africa</a>.</figcaption>
</figure>

**The second solution** is to construct a similarity index, then use it to select a subset of African countries that are similar to Vietnam. This index must be able to distill the similarity along multiple dimensions (say, population, amount of export, etc.) into a single number.

We use [Gower's similarity coefficient](http://venus.unive.it/romanaz/modstat_ba/gowdis.pdf) to construct an index along four dimensions: population, export (% of GDP), resource revenue (% of GDP), and agriculture output (% of GDP). We then select half of the African countries that are most similar to Vietnam. Gower's coefficient is a popular choice because:

- It works with missing data
- It works with regardless of the data type of the dimensions (either binary, categorical, or continuous)
- The distance matrix it creates is easily interpretable on the Euclidean space

<figure>
	<img src="/images/vietnam_africa_similarity.png" alt="vietnam_africa_comparison">
</figure>