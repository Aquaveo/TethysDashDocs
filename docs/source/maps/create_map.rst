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

This option allows selecting either **"Use the Previewed Map Extent"** or **"Use a Custom Extent."**

When **Use the Previewed Map Extent** is selected, the map automatically zooms to the extent currently displayed.

When **Use a Custom Extent** is selected, fields appear for entering the minimum and maximum latitude and longitude values that define the extent. An extent variable name can also be added.


----------------
Map Drawing
----------------

Map drawing allows adding features directly to the map:

- **Drawn Feature Limit**: Set a maximum number of items that can be drawn.
- **Allowed Types**: Choose which shapes can be drawn: **Point**, **LineString**, **Polygon**, **Rectangle**.
- **Variable Name**: Save the drawings under a variable name so they can be used in other visualizations.





   .. image:: ../../images/create_map_completed.png
      :align: center

|


