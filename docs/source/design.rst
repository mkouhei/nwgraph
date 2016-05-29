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

.. include:: _static/linkdraw_config.json

position file

.. include:: _static/linkdraw_position.json
