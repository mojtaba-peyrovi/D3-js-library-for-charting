# D3 Tutorial: [D3 website](https://d3js.org/)


### Resource: [d3Videos](https://www.youtube.com/playlist?list=PL6il2r9i3BqH9PmbOf5wA5E1wOG3FT22p)


#### tutorial 5 (1-4 skipped)-Scaling:

There is a useful function in d3 called scale. We can use it anytime we want to have the graph to be responsive to show any data scales.
we use it this way for linear scaling :
```
d3.scale.linear()
.domain([0,60])
.range([0,500]);   
									where 60 is the highest value in the data, and 500 is the canvas width.
```

We can also use scaling for colors. It means instead of having .range([0,500]) we can say:
```
scale(["red","blue'])
```
It will paint the data bars using different shades of blue and red.

#### tutorial 6-Groups & Axis:

In order to group elements in a canvas we can simply append a "g" tag to the canvas like this:
```
.append("g");
```
Then we need to define the axis, we can do it this way:
```
var axis = d3.svg.axis()
                    .ticks(5)
                    .scale(widthScale);
```
and then we have to call axis in canvas:
```
.call(axis);
```
