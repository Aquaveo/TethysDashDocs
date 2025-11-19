.. _layer_tab:

---------
Layer Tab
---------

The layer tab is used for configuring the overall layer, including a name and some properties. The properties in this 
tab are based on the `Openlayers Layer class <https://openlayers.org/en/latest/apidoc/module-ol_layer_Layer-Layer.html>`_.

**Name:** Determines the map layer name. This is what will be shown in the layer contol menu and in the summary table.

**Default Visibility:** This allows you to choose if the layer will be visible by default when the map is first loaded.

**Layer Properties:**
    - **Opacity:** Determines the transparency of the layer. Must be a number or float between 0 and 1.
    - **minResolution:** The minimum resolution (inclusive) at which this layer will be visible.
    - **maxResolution:** The maximum resolution (exclusive) below which this layer will be visible.
    - **minZoom:** The minimum view zoom level (exclusive) above which this layer will be visible.
    - **maxZoom:** The maximum view zoom level (inclusive) at which this layer will be visible.
    - **minZoomQuery** The minimum view zoom level (inclusive) at which this layer can be queried. If the mp is clicked beyond the zoom level, then the map will zoom into the minZoomQuery value.

    **Layer Template:** At the bottom of all the tabs is the option to choose a layer template. This will load in a layer that is preconfigured. There is a dropdown menu to choose between a couple layer options.
