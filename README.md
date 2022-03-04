# ROS UK Project Map

This maps shows available community routes for Railway Operation Simulator within the United Kingdom. This project is open for contributions, but please read the below section carefully to ensure that you follow the same formatting ect.

## Guide to Contributing

In the project there are two main files:

- `map/ROSProjects.svg`
- `data/project-data.csv`

### Map Features

Should contain all National Rail routes which have a consistent service. By consistant service, I mean any route that has a predictable scheduled passenger service. This excludes routes that are used by freight services, or alternative routes used by a few passenger services in the day. However, routes which have a limited service, but has stations on it, such as the Brigg Line in Lincolnshire, should be mapped. If in doubt, let me know.

Not all stations need to be included in the map, however, preference should be put towards major stations. Other stations to be included should be:

- Stations near railway junctions, despite their relative quietness. (See Clarbeston Road, Craven Arms, Romsey)
- Stations that are well known. (See Pilning)

**Terminus stations should always be included.**

### Mapping

The map data is contained within `ROSProjects.svg`. It was created in [Inkscape](https://inkscape.org/) and this tool may be the best to continue with mapping

The map is built on to a `1mm` by `1mm` grid, with the origin being `x = 0` and `y = 0`. Some exceptions apply to this with diagonal `90` degree turns and double point stations.

Lines are created using the Bezier path tool.

There are two different varients of lines:

**No Project Line**

<img src="img/no-project-line.png" width="200"/>

- Width: `0.250mm`
- Colour: `b2b2b2ff`

**Project Line**

<img src="img/project-line.png" width="200"/>

- Width: `0.500mm`
- Colour: Different per project, chosen almost at random, though should avoid nearby colours.

**Curves**

The map is based on `45` and `90` degree turns as below:

<img src="img/90-turn.png" width="200"/>
<img src="img/45-turn.png" width="200"/>

An alternative `n by n` `90` degree turn can be used if required, though `2x2` is recommended.

If you are doing a `90` degree turn at a diagonal, two curves can be done:

<img src="img/90-diagonal-1.png" width="200"/>
<img src="img/90-diagonal-2.png" width="200"/>

Notice that the second of these curves has the centre at the intersection of the two diagonal lines as opposed to on the grid.

**Stations**

The easiest way to add a station is to copy a station *blob* from elsewhere in the correct orientation and paste it in and update the text.

Some stations have lines intersecting at several angles, in which case I've chosen a orientation that is between the intersection angles. (See Stratford, Watford Junction)

When lines intersect at a station on both intersecting lines (See Worcestershire Parkway, Willesdon Junction), then a *blob* is put on both lines, and the *blobs* and the station name can be moved off the grid to make everything look straight.

Station names should not be over a line, but can be over the water if there is no over alternative. (See Weston-super-Mare)

**Route Names and Authors**

The route name and author text should be placed somewhere in the centre of the route, but not covering any lines or station texts. It should be the last thing to be added.

The route name and author should be identical to the spreadsheet.

### Project Data

The project data is in the `data/project-data.csv` file in a csv format. However, this format can be opened in Excel if preferred.

**Guide to Columns**

- Name

This is the name of the route, should be identical to the website.

- Tags

These are the tags for the project as extracted from the website, these tags should contain the name of the author. If the project was added after the extraction, only the author will be in that column as it was added manually.

- Added to map?

The values for this column can be:

TRUE: The route is added to the map, and the route name and author text has been added.

WIP: The route is in the process of being added to the map.

FALSE: The route has not been added.

- Link

This is a link **directly to the image** on the website. Having these direct links speeds up the need to search for the route and find the image on the website. This can be updated by getting the URL of the image directly.

- Notes

Notes can be inserted here about the routes. The `-` note does not mean anything and is simply there to cut off the previous line. London Underground routes are shown as `LUL` as they may be mapped seperatly at a later time, but not on this map.