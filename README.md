The gist can be viewed [here](http://bl.ocks.org/bibinmjose/465959c52fbc7f9b5ff58b60f4d19fa6)

Github Repository [link](https://github.com/bibinmjose/baseball_d3)

## Summary

Dataset contains median statistics of baseball players grouped by `handedness`. Each row contains `handedness`, `height`,`weight`,`avg`, `HR` and `Count`. Each graph explains the difference in performance as well as body metrics based on handedness of player.

### Graph #1 (Performance based on handedness):
* Better performance are noted for Left handed players with higher median `avg` and `HR`

### Graph #2 (Body Metrics based on handedness):
* Both handed players are found to have lower `weight` and `height`.

## Design

[Dimple.js](http://dimplejs.org/) library is used create the visualization based on example ["Vertical Bubble Lollipop"](http://dimplejs.org/examples_viewer.html?id=bubbles_vertical_lollipop).

Dual axis is used to plot two parameters into one chart with categorical variables on x-axis. Dual axis allows clubbing together performance on to one graph and body metrics on to another.

Tooltip animation allows explicitly read plotted data. Animation of the second graph is delayed as it has to be read after the first one.

A smoothes spline is added to each series of data as a guide to eye.

Summary of each graph is included on top of graph.



## Feedback

### Feedback 1 - [[index\_initial.html](http://bl.ocks.org/bibinmjose/raw/d9db996f2c13e6ec5af92aed8c60e24b/) --> [index\_1.html](http://bl.ocks.org/bibinmjose/57898f960e99190f902ea7c774df2439#file-index-html)]
* Doesn't convey any story. Cloud of point are obscuring the difference between them.  Might have to change what to plot. Good Animation
* Legend is not clear/undestandable.
#### Improvements made
Completely revamped the visualization to explain performance based on handedness. Legends are clearer. Grouped the data based on handedness for fewer but clearer data points (used median value in each group). Used a dual axis chart to convey both performance metric with one chart. Minimum and maximum for each axis is controlled to delineate both series.

### Feedback 2 - [[index\_1.html](http://bl.ocks.org/bibinmjose/57898f960e99190f902ea7c774df2439#file-index-html) --> [index\_2.html](http://bl.ocks.org/bibinmjose/eef59f1fb00a05fb05b01c4db29d93ca)]
* Overplotting obscures the story. Try to plot the bar graphs of `HR` and `avg` side bye side rather than on top of each other.
* Include the sample size used in each category of `handednes`.
#### Improvements made
Not able to plot bars side by side using Dimplejs, hence moved to bubble plot. Size of the bubble is maped to population used to find the median.

### Feedback 3 - [[index\_2.html](http://bl.ocks.org/bibinmjose/eef59f1fb00a05fb05b01c4db29d93ca) --> [index.html](http://bl.ocks.org/bibinmjose/465959c52fbc7f9b5ff58b60f4d19fa6)]
* May be add body statistics to show how height and weight vary
* Add a line to guide the eye for each series 
#### Explain improvement made
Two seperate graphs 1) for performance and 2) for body statistics.
A smoothed line is added for each series to guide the eye.
Animation is added for aesthetic loading of data.

## Resouces

* (http://dimplejs.org/examples_viewer.html?id=bubbles_vertical_lollipop)
* (http://bl.ocks.org/judemoon/c48b65e8570eacd9c6ed7d6a1c5aab93)