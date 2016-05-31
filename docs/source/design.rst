==============
 Design notes
==============

concept
=======

* Generating graph using NetworkX.
* This library generates networkx configuration data.
* This library take human readable configuration data.
* Input data permits automatic generated data or manual generated data.
* Generating graph draws as follows;

  * L3 layer network graph.
  * L2 wired/unwired network graph,
  
    * includes L2 switch ports wired conectivity.

* Enable to embed web application.

Input data
==========

L2 network
----------


L3 network
----------

as like Linkdraw
~~~~~~~~~~~~~~~~

configuration file

.. code-block:: JavaScript

   {
     "time": "2016-05-31 17:27:31",
     "descr": "some description.",
     "nodeColors": [
       {"id": "id_string", "descr": "some description", "color": "#ffffff"},
       ...
     ],
     "lineColors": [
       {"id": "id_string", "descr": "some description", "color": "#ffffff"},
       ...
     ],
     "nodes": [
       {"name": "name_string", "r": "10", "color": "node_color_id", "link": "http://example.org" },
       ...
     ],
     "lines": [
       {"source": "some_node_name", "target": "another_node_name", "color": "line_color_id", "width": "1", "descr": "some description", "link": "http://example.net"},
       ...
     ]
   }

position file

.. code-block:: JavaScript

   {
     "position": {
       "some_node_name": {"x": 100, "y": 100},
       "another_node_name": {"x": 10, "y": 10},
       ...
     },
     "scale": 1,
     "translate": [0, 0]
   }
