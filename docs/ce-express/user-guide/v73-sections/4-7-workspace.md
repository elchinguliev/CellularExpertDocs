# 4.7 Workspace

| Parameter | Description |
|---|---|
| Workspace_name | Workspace identification. |
| Extent_xmin | Minimum workspace extent longitude |
| Extent_ymin | Minimum workspace extent latitude |
| Extent_xmax | Maximum workspace extent longitude |
| Extent_ymax | Maximum workspace extent latitude |
| Extra_layers | JSON array containing links to ArcGIS layer services. e.g.: [“url1”, “url2”] |
| Use_clutter_loss | Possible values: • t – clutter losses included in the prediction model. f – clutter losses not included in the prediction model. • |
| Calculate_eirp | True – EIRP is calculated with the formula power - misc_loss + antenna gain. False – power value is used as EIRP. |
| Geodata_set_id | Path to folder containing geodata rasters: elevation.tif, building_height.tif (optional), clutter_classes.tif (optional), clutter_height.tif (optional). |
