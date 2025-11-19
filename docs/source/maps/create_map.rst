.. _create_map:

Create a Map
============

To create a map in the dashboard, A new dashboard item will need to be added (:ref:`add_dashboard_items`) or an 
existing item needs to be edited (:ref:`edit_dashboard_items`).

Once in the visualizaion editor, open the **Visualization Type** dropdown and select the **Map** option.

   .. image:: ../../images/create_map.png
      :align: center

|

The following arguments will be shown to configure the map.

--------
Base Map
--------

A list of available basemaps to use with the map. 

-------------------
Layer Controls
-------------------

This setting determines if a layer control panel will be shown in the map. This panel allows users to toggle layer visibility in the map.

-----------------
Layers
-----------------

A table summarizing the configured layers for the map. To add a new layer, click on the "Add Layer" button and add 
the necessary configurations. Once configured and saved, the layers will be shown in the table, where they can also be 
deleted or editted. See the :ref:`layer_configuration` section for more information on how to configure layers

Layers in this table can also be moved to switch order of rendering.

----------------
Map Extent
----------------

This allows you to choose either "Use the Previewed Map Extent" or "Use a Custom Extent". If you choose to use the previewed map extent, your map will automatically zoom to the extent that you currently have displayed in the map. If you choose to use a custom extent, you will be given the option to enter the minimum and maximum latitude and longitude values for the map extent. Then you can aslo add an extent variable name.

----------------
Map Drawing
----------------

Map drawing allows used to draw on the map. You can choose to place a limit on the number items users can draw under "Drawn Feature Limit". You can select what types of shapes users are able to draw on the map by chooseing the checkbox for allowed types. The options are Point, LineString, Polygon and Rectangle. The map drawings can be saved as a variable name which allows the drawings to be used in other visualizations.





   .. image:: ../../images/create_map_completed.png
      :align: center

|


