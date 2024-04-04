---
title: "starsTileServer visualizes large spatial data sets"
description: Making large spatial data sets accessible for dynamic visualization is challenging, starsTileServer facilitates this.
background: /assets/backgrounds/2022-01-21-starsTileServer.png
author: Bart Kranstauber
tags: [software]
published: false
---

New technologies were needed to address the challenge of visualizing large archives of weather radar data and bird specific products interactively. The goal of the R package [starsTileServer](https://cran.r-project.org/web/packages/starsTileServer/index.html) is to provide a simple way to add large data sets to a leaflet or shiny application.

![img](/assets/images/2022-01-21-starsTileServer.png){:.d-inline .w-50}![img](/assets/images/2022-01-21-starsTileServer_2.png){:.d-inline .w-50}
_Example visualizing birds and velocities from meteorological radar data_

Although the need arose from visualizing radar data the application is more general. Because it is possible to provide custom functions pretty much any data that can be projected, can be visualized, including composites or non square grids.

More examples are available on the [website](https://bartk.gitlab.io/starsTileServer/). The website also shows how applications can be made scalable. Using this it is possible to generate the images needed for longer animations like this one:

<blockquote class="twitter-tweet" data-conversation="none" data-dnt="true"><p lang="en" dir="ltr">Now also with video <a href="https://t.co/CwzEHtAS5F">pic.twitter.com/CwzEHtAS5F</a></p>&mdash; Bart Kranstauber (@bart_kra) <a href="https://twitter.com/bart_kra/status/1463560977144856582?ref_src=twsrc%5Etfw">November 24, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
