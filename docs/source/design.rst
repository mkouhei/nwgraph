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

as like Linkdraw
~~~~~~~~~~~~~~~~

.. code-block:: Javascript

   {
     "nodes": [
       {"name": "some_node_name", "ports": [{"name": "1", "vlan": null}, {"name": "2", "vlan": 100}, ...]},
       {"name": "another_node_name", "ports": [{"name": "en0", "vlan": null}, {"name": "en1", "vlan": 100}, ...]},
       ...
     ],
     "lines": [
       {"source": {"node": "some_node_name", "port": 1}, "target": {"node": "another_node_name", "port": "en0"}},
       {"source": {"node": "some_node_name", "port": 2}, "target": {"node": "another_node_name", "port": "en1"}},
       ...
     ]
   }

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
