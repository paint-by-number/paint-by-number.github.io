---
layout: post
title: "Visualize multiple dimensions of development"
categories: blog
author: anh_le
excerpt: "Another way to visualize multi-dimensional comparison, using radar chart. Interactive version."
comments: true
share: true
tags: [vietnam, africa, radar chart, shiny]
image:
  feature:
---

Here is another way to visualize multi-dimensional comparison, using radar chart. Soccer fans are surely familiar with this type of plot, which is frequently used to compare an athelete based on various aspects of his stat:

<figure>
	<div style="text-align: center">
		<a href="http://statsbomb.com/wp-content/uploads/2014/01/Ronaldo_1213_NPG.jpg"><img src="http://statsbomb.com/wp-content/uploads/2014/01/Ronaldo_1213_NPG.jpg" alt="Messi Statistics" height="300" width="300"></a>
	</div>
	<figcaption>Credit: statsbomb.com</figcaption>
</figure>

Below is a interactive and multi-dimensional comparison of Vietnam & Africa. If the graph is slow to load, please [view it directly here](https://ladilettante.shinyapps.io/radar_shiny/).

<iframe src="https://ladilettante.shinyapps.io/radar_shiny/" width="900px" height="750px"></iframe>

---
How we plot the graphs:
<script src="http://gist-it.appspot.com/github.com/paint-by-number/visualization-code/blob/master/radar_shiny/server.R"></script>
<script src="http://gist-it.appspot.com/github.com/paint-by-number/visualization-code/blob/master/radar_shiny/ui.R"></script>
<script src="http://gist-it.appspot.com/github.com/paint-by-number/visualization-code/blob/master/radar_shiny/helper.R"></script>