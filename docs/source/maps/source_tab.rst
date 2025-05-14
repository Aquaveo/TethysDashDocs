.. _source_tab:

----------
Source Tab
----------

The source tab defines the source of the data for the layer and any additional properties. Once a source type is selected, 
source properties will appear for further customizations and setup. Some properties are required for layers to render while 
others are optional. Source type options are predefined and currently consist of the following options with their available 
properties. 

------------------------------------------------------------------------------------------------------------------------

++++++++++++++++++++++++++
ESRI Image and Map Service
++++++++++++++++++++++++++

**Openlayers Class:** `ImageArcGISRest <https://openlayers.org/en/latest/apidoc/module-ol_source_ImageArcGISRest-ImageArcGISRest.html>`_

**Layer Properties:**
    - **url:** (required) ArcGIS Rest service URL for a Map Service or Image Service. The url should include /MapServer or /ImageServer.
    - **attributions:** (optional) Attributions.
    - **params - LAYERS:** (optional) Determines which layers appear on the exported map. Syntax is in the form of "[show | hide | include | exclude]:layerId1,layerId2". See `ESRI documentation <https://developers.arcgis.com/rest/services-reference/enterprise/export-map/>`_ for more information.
    - **params - TIME:** (optional) The time instant or time extent of the exported map image. Syntax is in the form of "<timeInstant>" or "<startTime>, <endTime>". See `ESRI documentation <https://developers.arcgis.com/rest/services-reference/enterprise/export-map/>`_ for more information.
    - **params - LAYERDEFS:** (optional) Allows you to filter the features of individual layers in the exported map by specifying definition expressions for those layers. Syntax is in the form of "{"<layerId1>": "<layerDef1>", "<layerId2>": "<layerDef2>"}". See `ESRI documentation <https://developers.arcgis.com/rest/services-reference/enterprise/export-map/>`_ for more information.
    - **params - mosaicRule:** (optional) Allows you to set a mosaic rule for image services.
    - **projection:** (optional) Projection of the source data. Default is the view projection (EPSG:3857).

------------------------------------------------------------------------------------------------------------------------

++++++++++++++++++++
ESRI Feature Service
++++++++++++++++++++

**Openlayers Class:** `EsriJSON <https://openlayers.org/en/latest/apidoc/module-ol_format_EsriJSON-EsriJSON.html>`_

**Layer Properties:**
    - **url:** (required) ArcGIS Rest service URL for the feature service
    - **layer:** (required) Layer index to use.
    - **attributions:** (optional) Attributions.
    - **params - TIME:** (optional) The time instant or time extent of the exported map image. Syntax is in the form of "<timeInstant>" or "<startTime>, <endTime>". See `ESRI documentation <https://developers.arcgis.com/rest/services-reference/enterprise/export-map/>`_ for more information.
    - **params - WHERE:** (optional) A query filter for the feature service. e.g. confidence='high'
    - **projection:** (optional) Projection of the source data. Default is the view projection (EPSG:3857).

------------------------------------------------------------------------------------------------------------------------

+++
WMS
+++

**Openlayers Class:** `ImageWMS <https://openlayers.org/en/latest/apidoc/module-ol_source_ImageWMS-ImageWMS.html>`_

**Layer Properties:**
    - **url:** (required) WMS service URL.
    - **params - LAYERS:** (required) A comma delimited list of layers within the WMS service. Syntax is in the form of "<workspace>:<layerName>,<workspace>:<layerName>".
    - **attributions:** (optional) Attributions.
    - **params - STYLES:** (optional) The name of a preloaded SLD (Styled Layer Descriptor). For additional custom styling, see the style tab.
    - **params - TIME:** (optional) Time value of layer desired.  Syntax is in the form of "yyyy-MM-ddThh:mm:ss.SSSZ".
    - **projection:** (optional) Projection. Default is the view projection (EPSG:3857)

------------------------------------------------------------------------------------------------------------------------

++++++++++
Image Tile
++++++++++

**Openlayers Class:** `ImageTileSource <https://openlayers.org/en/latest/apidoc/module-ol_source_ImageTile-ImageTileSource.html>`_

**Layer Properties:**
    - **url:** (required) Image Tile URL.
    - **attributions:** (optional) Attributions.
    - **projection:** (optional) Projection. Default is the view projection (EPSG:3857)

------------------------------------------------------------------------------------------------------------------------

++++++++
GeoJSON
++++++++

The GeoJSON source is slightly different from the other source options. This option will display a text area and a 
button to upload your GeoJSON that may be stored in a file. GeoJSONs must follow 
`the GeoJSON specification <https://datatracker.ietf.org/doc/html/rfc7946>`_ and also contain a "crs.properties.name" 
value for projection information. A example of a valid GeoJSON is::

    {
        "type": "FeatureCollection",
        "crs": {
            "properties": {
                "name": "EPSG:3857"
            }
        },
        "features": [{
            "type": "Feature",
            "geometry": {
                "type": "Point",
            "coordinates": [0, 0]
            }
        }]
    }

------------------------------------------------------------------------------------------------------------------------

+++++++++++
Vector Tile
+++++++++++

**Openlayers Class:** `VectorTile <https://openlayers.org/en/latest/apidoc/module-ol_source_VectorTile-VectorTile.html>`_

**Layer Properties:**
    - **urls:** (required) A comma delimited list of URL templates. Must include {x}, {y} or {-y}, and {z} placeholders. A {?-?} template pattern, for example subdomain{a-f}.domain.com, may be used instead of defining each one separately in the urls option.
    - **attributions:** (optional) Attributions.
    - **projection:** (optional) Projection. Default is the view projection (EPSG:3857)





