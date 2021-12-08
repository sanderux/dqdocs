# Planning survey missions

A survey allows you to create a grid flight pattern over a polygonal area. You can specify the polygon as well as the specifications for the grid and camera settings appropriate for creating geotagged images. To setup your camera for mapping please see [this instruction video](https://drive.google.com/open?id=133Ffh29p\_Tf\_3\_R\_IrRG17kVnYU9UUjs)

To draw the polygon for your survey, click the "Draw" button and click in the map to set polygon vertices.

![](https://github.com/sanderux/qgc-user-guide/raw/Abridged/assets/Survey.jpg)

There are multiple options for a survey grid. You can select the main option from the dropdown at the top of the editor.

## Manual Grid

[![](https://github.com/sanderux/qgc-user-guide/raw/Abridged/images/plan/SurveyManual.jpg)](https://github.com/sanderux/qgc-user-guide/blob/Abridged/images/plan/SurveyManual.jpg)

The Manual Grid option allows you to specify all the values for generating the grid pattern over the polygon by hand.

* Grid angle - The angle for the parallel flight tracks of the grid. For example 0 degrees will generate parallel lines which travel north/south.
* Grid spacing - The distance between each parallel flight track.
* Altitude - The altitude to fly the entire grid pattern.
* Turnaround distance - The mount of additional distance to fly past the edge of the polygon before performing the turnaround for the next flight track.
* Trigger Distance - Used to trigger an image taken by the camera based on distance flown.

##

### Geotagging <a href="#geotagging" id="geotagging"></a>

Please refer to the [Geo-referencing](geo-referencing.md) section.
