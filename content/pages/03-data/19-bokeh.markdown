title: Bokeh
category: page
slug: bokeh
sortorder: 0319
toc: False
sidebartitle: Bokeh
meta: Bokeh is a data visualization library that builds visuals in Python and outputs them in JavaScript.


# Bokeh
[Bokeh](http://bokeh.pydata.org/en/latest/) is a data visualization
library that allows a developer to code in Python and output 
[JavaScript](/javascript.html) charts and visuals in web browsers.

<img src="/img/logos/bokeh.jpg" width="100%" alt="Bokeh logo on a dark background." class="technical-diagram" style="border-radius:5px" />


## Why is Bokeh a useful library?
Web browsers are ideal clients for consuming interactive visualizations.
However, libraries such as [d3.js](https://d3js.org/) can be
difficult to learn and time consuming to connect to your Python backend
web app. Bokeh instead generates the JavaScript for your application while
you write all your code in Python. The removal of context switching between
the two programming languages can make it easier and faster to create 
charts and visualizations. 


## What do Bokeh visualizations look like?
Bokeh can create any type of custom graph or visualization. For example,
here is a screenshot of a bar chart created with the 
[figure](http://bokeh.pydata.org/en/latest/docs/reference/plotting.html)
plot:

<img src="/img/170526-bar-charts-bokeh-flask/chart-example-64.png" width="100%" class="technical-diagram img-rounded" style="border:1px solid #ccc" alt="Responsive Bokeh bar chart with 64 bars.">

For more references, including interactive live demonstrations, check out
these sites:

* The 
  [official Bokeh gallery](http://bokeh.pydata.org/en/latest/docs/gallery.html)
  has many example Bokeh visual formats.

* [Bokeh Applications](https://demo.bokehplots.com/) hosts numerous
  data visualizations built with Bokeh.


### Bokeh resources
Bokeh is under heavy development ahead of the upcoming 1.0 release. Note that
while all of the following tutorials are useful, it is possible some of the
basic syntax will change as the library's API is not yet stable.

* [Responsive Bar Charts with Bokeh, Flask and Python 3](/blog/responsive-bar-charts-bokeh-flask-python-3.html) is my recommended
  tutorial for those new to Bokeh who want to try out the library and get
  an example project running quickly with [Flask](/flask.html).

* [Data is beautiful: Visualizing Roman imperial dynasties](http://machineloveus.com/data-is-beautiful-visualizing-roman-imperial-dynasties/)
  provides a walkthrough for creating a gorgeous visualization based on
  historical Roman data. The post is about more than just the visual, it also
  goes into the ideation, data wrangling and analysis phases that came
  before using Bokeh to show the results.

* [Creating Bar Chart Visuals with Bokeh, Bottle and Python 3](/blog/python-bottle-bokeh-bar-charts.html)
  is a tutorial that combines the [Bottle](/bottle.html) 
  [web framework](/web-frameworks.html)

* [Building Bullet Graphs and Waterfall Charts with Bokeh](http://pbpython.com/bokeh-bullet-waterfall.html)
  covers buildings two types of useful visualizations into your applications
  using Bokeh.

* [Interactive Visualization of Australian Wine Ratings](http://pbpython.com/wine_visualization.html)
  builds a non-trivial visualization with a nice sample set of data based
  on wine ratings.

* [Visualization with Bokeh](http://www.blog.pythonlibrary.org/2016/07/27/python-visualization-with-bokeh/)

* [Drawing a Brain with Bokeh](http://merqur.io/2015/10/02/drawing-a-brain-with-bokeh/)
  is a fun example of a chord diagram that represents neural connections in
  the brain.

* [Bryan Van de Ven on Bokeh](https://pythonpodcast.com/episode-22-bryan-van-de-ven-on-bokeh/)
  is a podcast episode by one of the main Bokeh maintainers.

* [The Python Visualization Landscape](https://www.youtube.com/watch?v=FytuB8nFHPQ)
  by Jake VanderPlas at PyCon 2017 covers many Python data visualization
  tools, including Bokeh.

* [Enjoying the bokeh.models API](https://bokeh.github.io/blog/2017/7/5/idiomatic_bokeh/)
  explains the `bokeh.models.plots.Plot` object and data ranges.

* This 
  [flask-bokeh-example](https://github.com/realpython/flask-bokeh-example/blob/master/tutorial.md)
  project has the code to create a simple chart with Bokeh and 
  [Flask](/flask.html).

* [Styling Bokeh Visualizations](https://bokeh.github.io/blog/2017/7/24/styling-bokeh/)
  shows how to use themes and style dictionaries to customize your Bokeh
  visuals.

* [Bokeh vs Dash?????????Which is the Best Dashboard Framework for Python?](https://blog.sicara.com/bokeh-dash-best-dashboard-framework-python-shiny-alternative-c5b576375f7f)
  contains a single project that was written in both Dash and Bokeh. The
  author gives his subjective view on the implementation difficulty 
  although the web application only contained a single type of data 
  visualization so it is hard to drawn any real conclusions from his
  opinion.
