docrepo-viz
===========

2D visualisation tool - designed to be used with docrepo-backend but can be used independently

description
===========

A set of visualisations that represent a set of resources. This is being designed to be used with https://github.com/adieyal/docrepo-backend but can be used independently.

visualisation
=============

To be developed

Below are the specifications:

Please produce a tree map as shown below but using the d3 visualisation library.
- http://static.guim.co.uk/sys-images/Guardian/Pix/maps_and_graphs/2010/3/1/1267465128053/2-Information-is-Beautifu-001.jpg

This example code is available for re-use: http://mbostock.github.com/d3/ex/treemap.html

The code should take a context hash as a parameter e.g.

TreemapViz = function(ctx) {
}

where ctx should contain at least the following::
    ctx = {
        width: 600, // width in pixels
        height: 300, // height in pixels
        node: '#viz', // id of the element to put the treemap in
        series: ['size', 'count'], // the names of the data series that can be found in the values array in each data item. This can be a variable number of series. The series should appear on the top left of the visualisation (although if there is only one series then it shouldn't appear at all). Pressing on the series will transform the visualisation as it does in the d3 example link listed above). 
        data : [ 
            // tag1 will be used for the big boxes (1st dimension) and tag2 for the small boxes (2nd dimension. The tag name should appear in the top left of the each box. 
            {'tag1' : 'green', 'tag2' : 'five', 'url' : '/path/to/resource/', 'values' : [345, 67]},
            {'tag1' : 'blue', 'tag2' : 'one', 'url' : '/path/to/resource/', 'values' : [23, 133]},
            {'tag1' : 'green', 'tag2' : 'four', 'url' : '/path/to/resource/', 'values' : [86, 468]},
            {'tag1' : 'yellow', 'tag2' : 'one', 'url' : '/path/to/resource/', 'values' : [413, 124]},
            {'tag1' : 'green', 'tag2' : 'five', 'url' : '/path/to/resource/', 'values' : [32, 577]},
            {'tag1' : 'green', 'tag2' : 'one', 'url' : '/path/to/resource/', 'values' : [467, 23]}
        ]
    }

Additionally - each element should be given the appropriate css classes so that the treemap can be styled appropriately.
