# NPT manual

## Overview

Welcome to the Network Planning Tool ([NPT](https://www.npt.scot)), a web application for strategic cycle network planning in Scotland.
The NPT is designed to help local authorities, transport planners, and other stakeholders identify the best locations for cycling infrastructure and routes based on cycling potential and demand.

The NPT is funded by Transport Scotland and developed by the University of Leeds, [CycleStreets](https://www.cyclestreets.net/) and [A/B Street](https://a-b-street.github.io/docs/) in collaboration with and directed by [Sustrans Scotland](https://www.sustrans.org.uk/about-us/our-work-in-scotland/).
The NPT is complemented by the related Network Planning Workspace ([NPW](https://npw.scot)) web application for sketching, evaluating and sharing cycle networks, which was developed as part of the same project.

These tools build on the methods underlying the [Propensity to Cycle Tool](https://www.jtlu.org/index.php/jtlu/article/view/862) (available at [pct.bike](https://www.pct.bike/)) but go beyond them in several ways.
Compared with the PCT, the NPT has an improved map interface, includes additional trip purposes in the estimates of cycling potential, uses higher-resolution data resulting in denser networks, and includes new layers.
Each of these elements is described in this manual, which is divided into the following sections (see the figure below for an overview of the NPT):

1. [Map interface and controls](#interface) describes how to use the map interface and controls to view and interact with the different layers of information

2. [Layers that can be displayed on the map](#layers) provide information on cycling potential, existing cycle infrastructure, and other contextual information

  2.1. [The route network layer](#routenetwork) shows the estimated number of cycle trips on the transport network under different scenarios

  2.2. [The coherent network layer](#coherentnetwork) shows a strategic cycle network based on the route network

  2.3. [The existing cycle network layer](#clos) shows the quality of the existing cycle network using Cycling Level of Service (LoS), existing cycle infrastructure, traffic volumes and speed limits

  2.4. [The street space layer](#streetspace) shows the deliverability of segregated cycle infrastructure

  2.5. [Data zones](#data_zones) provide contextual area-based information based on small geographic zones created for summarising Census datasets
  
  2.6. [Other layers](#otherlayers) provide official boundaries, plus school locations and bus routes

3. [Accessing the NPT](#access) provides information on how to pin the app to your device's home screen
4. [Data downloads](#data) provides information on how to download data from the NPT
5. [The Network Planning Workspace](#npw) provides information on this separate web application for planning & assessing the quality of cycle networks.

![NPT Overview](/images/npt-interface-overview.png)

<!-- Caption: -->
*NPT Overview: The web application when you first open the [www.npt.scot](https://www.npt.scot) website. 
 The boxes shown and associated numbers in red correspond to the sections of this manual.*

The NPT is an open-source and open access project, meaning the source code and results are transparent and in the public domain for all stakeholders to benefit from and build on.
See the [open-source codebase at github.com/nptscot](https://github.com/nptscot/).
If you see an opportunity to improve the tool or its outputs, we encourage you to let us know by [raising an issue](https://github.com/nptscot/npt/issues) (requires a GitHub account).

## 1. Map interface and controls {#interface}

The user interface consists of the map interface and controls on the left side of the screen, as shown below. The map interface shown in the largest box in the figure above is the main part of the NPT.
You can pan, zoom and click on elements shown in this main map view.
The map controls on the left side of the screen allow you to search for locations, find your current location, change the basemap, and make other adjustments to the map view, as shown below.

![Map controls](/images/map_controls.png)

The layer controls are available in a panel on the right side of the screen, which can be minimised.

![Layer Controls](/images/layer_controls.png)

These layer controls determine the information shown on the map as described in the sections below. 

The NPT provides different basemaps. The example below shows the basemap selection options with the satellite basemap with 3D terrain enabled. You can hide the basemap selection option by clicking the change basemap button again.

![Basemap controls](/images/basemaps.png)

The Anti-alias option enables advanced rendering options that make the map look smoother and clearer. However, performance on low-end devices may be impaired when using anti-aliasing.

## 2. Layers {#layers}

This section describes layers that provide information on cycling potential, existing cycle infrastructure, and other contextual information.

### 2.1. The route network layer {#routenetwork}

The Route network layer displays estimates of cycling demand (i.e. number of cycle trips) on the road and path network, down to the level of individual segments. It is the first and for many use cases the most important layer in the NPT. The layer is useful for identifying where cycling infrastructure and new routes should ideally be located in order to meet latent demand, maximise usage and ultimately maximise modal shift to cycling. This data is used to inform the creation of the primary cycle network in the Network Planning Workspace.

The route network provides a range of options and filters to allow you to view cycling potential for different journey purposes and under different scenarios of cycling uptake. For example, if you are planning safe cycling routes to school, the primary and secondary school networks are particularly useful. The trip purpose and scenario options are described in detail below.

<!-- #purpose -->

#### Trip purposes

People have many reasons to travel, and their reasons often change their choice of destinations and routes. Therefore, a cycling network designed to serve commuters may look very different to a network designed for children to travel to school. The trip purpose drop-down allows you to view different networks based on different trip purposes.

##### All

This is the default view that displays all journey purposes that are part of the NPT (travel to work, travel to school and other everyday journeys) combined. It offers an overview of total cycling potential and as such, it is useful as a starting point for planning local authority and regional cycle networks. 

##### Commute

The commute network, as the second option in the travel purpose dropdown list, shows journeys to work and is based on aggregated journey to work origin-destination data from the 2011 Census at the Data Zone level (source: National Records of Scotland). Commuters tend to favour radial routes from suburban residential areas into town and city centres where most jobs are concentrated. This layer can help identify the core arterial cycle network.

##### Primary school

The primary school network, as the third option in the travel purpose dropdown list, shows cycling potential for children cycling to primary schools, whether by e-cargo, accompanied by adults, or including as part of 'cycle buses' or travelling independently. It is based on the Scottish Government's Pupil Census 2021 origin/destination data adjusted using school mode share data from the Hands Up Scotland Survey. It provides insights into the routes that could be taken by children and carers. Recognising these patterns is important for urban planners, enabling them to emphasize and develop infrastructure that prioritises the safety of young people. Schools tend to be located in residential areas, so the resulting primary and secondary school networks tend to favour denser orbital routes that could be supported by modal filters and traffic management.

##### Secondary school

The secondary school network is the fourth option in the travel purpose dropdown menu. It is based on the same data sources as the primary school network and offers insights into the networks that could provide young people with safe cycling options to get to and from secondary school.

##### Other Everyday

Other Everyday trips include trips for three purposes:

1. Shopping: travel to shops, supermarkets, and other retail destinations
2. Access leisure facilities: such as leisure centres, parks, cinemas, pubs and other 'points of interest' related to leisure activities from the Ordnance Survey
3. Social trips: visiting friends and family, meaning residential destinations

The total number of trips for each purpose between Data Zones was estimated using a spatial interaction model (SIM), described in an academic paper (Lovelace et al., [2024](https://doi.org/10.1186/s12544-024-00668-8)).
The SIM estimates the total number of trips as a function of the following inputs: the population of each zone (from the 2021 Census), location and size of trip attractors (from Ordnance Survey Points of Interest and other sources), and national data on the total number of trips for each purpose (based on Scottish Household Survey).
The number of trips *cycled* for each purpose was estimated using the same uptake function as used to estimate cycling potential for commuting trips, with the exception of shopping trips, in which cycling potential was reduced by half to account for the fact that people are less likely to use active modes when carrying shopping (Iacono et al., [2010](https://doi.org/10.1016/j.jtrangeo.2009.02.002)).

##### Trip purposes not considered

The NPT does not currently include estimates of cycling for recreational purposes or as part of a mixed-mode journey.

Recreational cycling is important in many places, but has high seasonal variability and is complex to model as people cycling often lack a clear destination. The NPT focuses on everyday cycling, which is more predictable and has a clearer destination.

The NPT currently only considers direct journeys where the whole trip is by bicycle. It does not consider mixed-mode journeys such as cycling to the station and then taking a train to your final destination. This means that the NPT slightly underestimates cycling potential overall and may significantly underestimate cycling potential in specific places (such as around train stations).

<!-- /#purpose -->

<!-- #scenario -->

#### Scenarios

This drop-down allows you to explore anticipated levels of cycling under several 'Scenarios' of change.

##### Baseline 

The baseline scenario represents the current level of cycling. As such, it is intended to show where there is an existing demand for cycling infrastructure.

##### Go Dutch

The Go Dutch scenario imagines a future with a high level of cycling, where people in Scotland are as likely to travel by cycle as people in the Netherlands, while still accounting for differences in trip distance and hilliness between locations. People in the Netherlands make 28% of trips by bicycle, greater than fifteen times higher than the figure of 1.7% in Scotland in 2022. The Go Dutch scenario scales up the baseline scenario to a Dutch modal share for cycling in Scotland. This is not produced by scaling up baseline trips by a uniform factor, rather it takes account of trip distance and hilliness. So for example, in flatter areas the Go Dutch scenario will show a greater increase over baseline than equivalent more hilly areas. As such, this network shows how a Dutch modal share for cycling could be distributed across Scotland. Planners should seek to design cycle networks that meet the needs of those currently cycling and those who may in future.

##### Ebikes

The Ebike scenario models the additional increase in cycling that would be achieved on top of the Go Dutch scenario, through the widespread uptake of electric cycles. The scenario alters both the assumptions around cycling uptake and the routes choices made by people cycling, for example a reduced penalty for going up hills. People using a pedal cycle incur a significant time and effort penalty from going uphill. Hence, a longer but flatter route is often faster. A good ebike can enable people to ride uphill at 15 mph without breaking a sweat. Thus ebike riders may choose shorter but hillier routes than those using a pedal cycle.

As ebikes increase the range a typical person can cycle, as well as carrying capacity, while reducing effort and journey times, a world with many ebikes would expect higher levels of cycling than one with only pedal cycles.

<!-- /#scenario -->

<!-- #type -->

#### Network type

The 'network type' reflects route choices people make when cycling. There is strong evidence that people prefer the most direct route, and it reduces journey times and the physical effort of cycling.

The need to prioritise creation of a network of safe & direct cycle routes is central to Transport Scotland's Cycling Framework for Active Travel and Active Travel Strategy Guidance. [Cycling By Design](https://www.transport.gov.scot/publication/cycling-by-design/) defines how to achieve a high level of service for cycling, either through providing cycling facilities physically separated from traffic or on carriageway where traffic speed and volume is sufficiently low.

However, until such a safe & direct network is created, people currently cycling often make detours away from roads that are (or are perceived to be) dangerous. There is strong evidence that safety concerns are the main barrier to more people cycling.

CycleStreets calculate the routes likely to be taken by people cycling, and each network type is based on one of their routeing [algorithms](https://www.cyclestreets.net/help/journey/howitworks/). The route choices are based on the current road infrastructure and don't account for planned improvements or missing links.

![Route network types](/images/rnet_types.png)

*Examples of the two network types in Edinburgh show how different assumptions about the routes people cycle affect where the busiest parts (pink) of the network are predicted to be.*

Note that the choice of network type does not just change the routes people take but also the number of cycle trips predicted under each scenario. This is because quieter routes are typically longer and hillier than the direct route which discourages cycling.

##### Fast/direct (preferred)

This network type should be treated as the default in the network planning process in line with Transport Scotland policy.

The fastest network is based on people taking the most direct routes on which it is legal to cycle. While people prefer direct routes, this will often bring them onto busy and dangerous major roads, which are a barrier to cycling without the provision of cycle infrastructure separated from traffic. Planners seeking to maximise cycling will build high-quality cycle infrastructure along main roads, which form part of the fast/direct cycle route network.

High quality cycle network plans, particularly in urban areas, will be based on joining up the fast/direct routes with the highest predicted numbers of cycle trips to create a dense & coherent network. Our associated Network Planning Workspace guides users step-by-step through a best practice process for creating a high-quality cycle network plan, based on the principles set out in Cycling by Design. 

##### Quiet/indirect

The quiet network models cyclist behaviour that avoids busy roads and takes significant detours. While directing people away from busy roads and onto quieter back streets may seem like a good idea, it can have significant downsides. Quiet routes are generally longer and more challenging to navigate as they weave around the back streets, discouraging cycling uptake. The NPT captures this effect, and the total number of cycle trips on the quiet route network is less than on the fast route network.

The intended uses of the 'Quiet/Indirect' network type are:

* Identification of potential low cost 'quick wins' where minor but meaningful additions to the cycle network can be made in the very short term e.g. by filtering residential streets parallel to main roads.

* Supporting the design of Low Traffic Neighbourhoods.

Quiet networks work best when the directness penalty is small. For example, a city with a grid layout could alternate between roads designed for cars and streets designed for active travel.

![Amsterdam car and cycle networks](/images/amsterdam_networks.JPG)

The image above ([source](https://maps.amsterdam.nl/plushoofdnetten/)) shows how Amsterdam uses its grid layout to have parallel but separate networks for cars (red, orange, black) and bicycles (green). Notice how the cycling network is much denser than the car network, ensuring that people who cycle almost always benefit from a more direct route.

<!-- /#type -->

<!-- #colour -->

#### Line colour

The line colour option allows you to visualise different characteristics of the route network. Below the line colour option is a contextual legend which shows the meaning of the colours on the map.

##### Number of cycle trips

![Number of cycle trips](/images/number_of_cyclists.png)

This is an estimate of the average annual daily traffic (AADT), meaning the number of daily cycle trips in both directions (so a return trip on the same route counts as 2), on each segment, for the selected purpose, network type, and scenario.

The thickness of the lines in the route network is also defined by the number of cycle trips, with thicker lines representing more people cycling.

##### Cycle friendliness

![Cycle friendliness](/images/cycle_friendliness.png)

Cycle friendliness is a subjective measure representing the quality of a route segment (a section of road or path) for cycling, with a score between 0 (very low quality) and 100 (very high quality). It considers a [range of factors](https://www.cyclestreets.net/api/v1/journey/), using data derived from OpenStreetMap.

Factors that contribute to a higher score of cycle friendliness include (as appropriate):

* Whether the cycleway is shared with motor vehicles or pedestrians,
* The type of road
* Presence of cycle infrastructure
* Speed limit
* Surface quality
* Cycle signage, 
* Any barriers or obstructions
* Path width
* Route legibility

See [CycleStreets](https://www.cyclestreets.net/help/journey/howitworks/#quietness) for further information; the term 'quietness' is used for the same measure that we call 'cycle friendliness'.

##### Gradient

![Gradient](/images/gradient.png)

The average gradient of the road is shown as a percentage. Steeper roads are a barrier to cycling and affect route choice and the uptake of cycling in the scenarios. Please note that in some locations where the network does not follow the land contours, such as elevated structures like North Bridge in Edinburgh, the gradient will incorrectly show flat sections of network as steep. This issue does not affect all bridges; for example, bridges over the River Clyde in Glasgow show correct gradients. We are aware of this inconsistency and are working to address it.

<!-- /#colour -->

<!-- #simplified_rnet -->

#### Simplified route network

The NPT includes a 'Simplified' toggle that simplifies the route network display. Major road corridors can be complex with multiple adjacent carriageways, cycle paths and footways, which are often shown as individual line features on OSM. This makes it hard to assess overall demand across corridors that contain multiple parallel segments. The simplified network attempts to address this problem by combining parallel routes into a single 'centerline' for each corridor.

**Disclaimer:** The simplified network uses OS Open Roads, which aggregates values from the OSM layer. This joining stage may yield some errors. Please report any noticed errors.

Application of the Simplified network can lead to a loss of detail. For a comprehensive analysis, it's advisable to consider both the simplified and the full route networks in tandem when evaluating cycling demand. This dual approach helps balance the big-picture overview with the nuanced details of specific routes. 

![Simplified Network](/images/simplified.png)

<!-- /#simplified_rnet -->

#### Popup

Clicking on any segment within the route network on the map will display a pop-up window.

![Popup](/images/rnet_popup.png)

The popup provides a summary table for all the information available about the route network. The table displays the number of cycle trips for each scenario - such as baseline, Go Dutch, and e-bikes - and distinguishes between the Fast/Direct and Quiet/Indirect network types. Above the table, the average gradient of the road and its cycle friendliness score are shown, which assesses the suitability of the road for cycling. Additionally, there's an option to directly access the Google Street View of the road, if available, for a more grounded perspective.

<!-- #filters -->

#### Route network filters

![Route network filters](/images/rnet_filters.png)

The sliders allow you to show/hide parts of the route network. You can filter on three variables:

#### Numbers of cycle trips

Tailor the map to display routes with a particular range of predicted cycling traffic, reflecting the selected scenario and route type.

#### Gradient

Set the maximum and minimum gradient of roads that are visible. Gradient measures the average gradient of the road segment as a percentage. E.g. 0% = flat, 100% = vertical cliff.

#### Cycle friendliness

Set the maximum and minimum quietness of roads that are visible. Quietness measures how cycle friendly the existing road is, from hostile (least friendly) to quiet (most friendly).

<!-- /#filters -->

### 2.2. The coherent network layer {#coherentnetwork}

<!-- #coherentnetwork -->

The coherent network is a strategic cycling network composed of high-potential, direct routes within urban areas. Created through automated analysis, this network emphasises coherence in network planning to ensure cycling infrastructure is functional, accessible and efficient.

The coherent network can be used as a 'starter for 10' in the Network Planning Workspace to quickly plan a strategic cycle network in urban areas, prioritising investment by highlighting routes that maximize coverage and connectivity, while aligning with demand. The methodology used focuses on several key aspects.
See [github.com/nptscot/corenet](https://github.com/nptscot/corenet) for details, links to the code and data, and a more detailed description of the methodology.

<!-- /#coherentnetwork -->

### 2.3. The existing cycle network layer {#clos}

<!-- #clos -->

The "existing cycle network" is defined as all roads and paths on which it is legal to cycle. The default view for this layer shows an assessment of the quality of the existing cycle network, using a high-level assessment of the Cycling Level of Service (LoS). In network planning, a high LoS network should be designed so that it is suitable for most users, including new and less confident users. In general the LoS will be high where either the traffic speeds and volumes are sufficiently low or where safe cycle infrastructure is provided to sufficiently physically separate people cycling from traffic. As a result, this layer is useful to help define where new infrastructure is needed as part of the network planning process. It provides a graphical representation of the distribution of high LoS roads across Scotland that are suitable for most users. 

This section also provides data on existing cycle infrastructure, speed limits and estimated traffic volumes. 

#### Level of service

The LoS layer provides an overview of the existing cycle network quality in Scotland, by providing a high-level assessment of LoS based on the [Cycling by Design guidance](https://www.transport.gov.scot/media/50323/cycling-by-design-update-2019-final-document-15-september-2021-1.pdf) (Table 3.2).
It is produced taking account of existing cycle infrastructure, speed limits and traffic volumes on each link.

![Table 3.2: When to separate cycle users from motor traffic](/images/clos_facilities.png)

Note: Table 3.2 displays Motor Traffic Speed in KPH ranges. For applying this guidance in the UK, these KPH ranges are mapped to the corresponding UK statutory MPH speed limits as follows:
*   20 mph statutory speed limit corresponds to the 0 kph to 30 kph range.
*   30 mph statutory speed limit corresponds to the 30 kph to 50 kph range.
*   40 mph statutory speed limit corresponds to the 50 kph to 65 kph range.
*   50 mph statutory speed limit corresponds to the 65 kph to 80 kph range.
*   60 mph statutory speed limit corresponds to the 80 kph to 95 kph range.
*   60+ mph statutory speed limit corresponds to the 95 kph to 110 kph range.

<!-- /#clos -->

<!-- #infrastructuretypes -->

#### Estimated traffic volume

The traffic volume layer visualises modelled traffic levels for roads on which cycling is permitted. The primary source of input data for major roads is the Department for Transport (DfT) road traffic statistics, which primarily cover major roads and are publicly available at [roadtraffic.dft.gov.uk](https://roadtraffic.dft.gov.uk).

To estimate motor traffic on roads for which data is lacking, we developed a model that uses [centrality](https://en.wikipedia.org/wiki/Centrality) (a measure of how central segments are to the road network), population density, and employment density to estimate average annual daily traffic (AADT). For specific low-speed environments, such as service roads and car parks, a 10 mph speed assumption is applied in the model.

The model was trained and validated using real-world traffic count data from a selection of 20 mph residential roads in Edinburgh to ensure its accuracy. The outputs are categorised into bands that correspond to the guidance in the [Cycling by Design document](https://www.transport.gov.scot/media/50323/cycling-by-design-update-2019-final-document-15-september-2021-1.pdf#page=68), with the following ranges: 0-999, 1,000-1,999, 2,000-3,999, and 4,000+ AADT.

Due to limitations in the size of the training dataset and the quality of the input datasets representing the road network, the model may not accurately predict traffic volumes for all roads and should be interpreted accordingly.
Traffic volumes vary over yearly, monthly, weekly, and daily timescales based on a range of factors, so users should defer to recent traffic counts or local knowledge where available.
Where traffic levels are a key determinant in decision-making, we recommend that users conduct their own traffic counts to validate the model outputs.

#### Cycle infrastructure

Cycle infrastructure is classified as follows:

<table>
    <tr>
        <th>Infrastructure type/name</th>
        <th>Description</th>
        <th>Example</th>
        <th>Colour on map</th>
    </tr>
    <tr>
        <td>Segregated Track (wide)</td>
        <td>Roadside infrastructure that is designated for cycling and provides physical protection from motor traffic and separation from pedestrians. Segregated Tracks include the following categories from Cycling by Design guidance: cycle tracks at carriageway level, light segregation, stepped cycle tracks, and footway level cycle tracks separated from pedestrians. Network segments classified with the Segregated Track (wide) category are the <a href="https://www.transport.gov.scot/media/50323/cycling-by-design-update-2019-final-document-15-september-2021-1.pdf#page=85" target="_blank">desirable minimum width</a> (2 m) or more according to OpenStreetMap <a href="https://wiki.openstreetmap.org/wiki/Key:width" target="_blank">width</a> or <a href="https://wiki.openstreetmap.org/wiki/Key:est_width" target="_blank">est_width</a> tags. Likely compliant with Cycling by Design guidance.</td>
        <td><a href="https://www.cyclestreets.net/location/81274/" target="_blank"><img src="/manual/segregated.jpg" alt="Segregated track" /></a></td>
        <td><span style="background-color: #054d05; color: white;">Dark green</span></td>
    </tr>
    <tr>
        <td>Off Road Path</td>
        <td>These are paths which are not adjacent to a road (defined as more than a 10 m threshold distance to a road on which cycling is permitted). They are often shared use, without separation between cycling and walking. In Cycling by Design they are called 'detached or remote cycle tracks'.</td>
        <td><a href="https://www.openstreetmap.org/way/41386401#map=18/56.368094/-2.891781" target="_blank"><img src="/manual/offroad.png" alt="Off Road Path" /></a></td>
        <td><span style="background-color: #3a9120; color: white;">Mid green</span></td>
    </tr>
        <tr>
        <td>Segregated Track (narrow)</td>
        <td>Segregated roadside cycle track, as described above, but which is less than the <a href="https://www.transport.gov.scot/media/50323/cycling-by-design-update-2019-final-document-15-september-2021-1.pdf#page=85" target="_blank">desirable minimum width</a> (2 m) or has no width information based on OpenStreetMap <a href="https://wiki.openstreetmap.org/wiki/Key:width" target="_blank">width</a> or <a href="https://wiki.openstreetmap.org/wiki/Key:est_width" target="_blank">est_width</a> tags. May or may not be Cycling by Design compliant.</td>
        <td><a href="https://www.cyclestreets.net/location/196620/" target="_blank"><img src="/manual/segregated-narrow.jpg" alt="Segregated track (narrow)" /></a></td>
        <td><span style="background-color: #87d668; color: white;">Light green</span></td>
    </tr>
    <tr>
    <tr>
        <td>Shared Footway</td>
        <td>In Cycling by Design this is a "cycle track at footway level (adjacent to carriageway)" that does not provide separation from pedestrians, i.e. a pavement that has been designated for use by both pedestrians and people cycling.</td>
        <td><a href="https://www.cyclestreets.net/location/92805/" target="_blank"><img src="/manual/shareduse.jpg" alt="Shared footway" /></a></td>
        <td><span style="background-color: #ffbf00; color: white;">Orange</span></td>
    </tr>
    <tr>
        <td>Painted Cycle Lane</td>
        <td>On-carriageway cycle lane that does not provide physical protection from motor traffic. It includes both advisory and mandatory cycle lanes.</td>
        <td><a href="https://www.cyclestreets.net/location/81341/" target="_blank"><img src="/manual/lane.jpg" alt="Painted cycle lane" /></a></td>
        <td><span style="background-color: #ff0000; color: white;">Red</span></td>
    </tr>
</table>

#### Speed limit

The speed limit data displayed in the NPT is primarily sourced from OpenStreetMap (OSM). In instances where speed limit information is not explicitly available in the OSM data, the following assumptions are applied to infer the speed limit based on the `highway` tag:

*   **10 mph**: Assumed for `highway` types classified as "service".
*   **30 mph**: Assumed for `highway` types classified as "residential".
*   **40 mph**: Assumed for `highway` types classified as "primary", "secondary", or "tertiary". This is a general assumption, as actual speed limits can vary between urban (often 30 or 40 mph) and rural (often 60 mph) contexts for these road types.
*   **60 mph**: Assumed for `highway` types classified as "trunk".
*   **70 mph**: Assumed for `highway` types classified as "motorway".
*   **No speed limit assigned (`NA`)**: For `highway` types such as "footway", "cycleway", "path", "pedestrian", or "razed", no speed limit is assigned.
*   If a `highway` type does not fall into any of the above categories and lacks an explicit speed tag, its speed limit also remains `NA`.

<!-- /#infrastructuretypes -->

### 2.4. Street space evaluation {#streetspace}

<!-- #streetspace -->

<!-- From index.html, see the table beginning:
        <div class="layertools layertools-streetspace">
-->

The Street Space layer shows whether segregated cycle infrastructure can be delivered on each road segment.

It calculates if there is enough space for new infrastructure by considering the required width for cycle tracks separated from motor traffic by light segregation measures or other physical barriers, such as kerbs or planters.
The layer also considers the space available on the road, including carriageway and pavement widths, cycle track widths, and buffer widths between the cycle track and motor traffic as specified in [Table 3.2 of Cycling by Design](https://www.transport.gov.scot/media/50323/cycling-by-design-update-2019-final-document-15-september-2021-1.pdf#page=68), based on the road's speed limit.

You can use checkboxes to switch between two width measurements:

- **Kerb-to-kerb (carriageway width):** Only the space between the kerbs, excluding pavements.
- **Full corridor width:** The total width from building-to-building or edge-to-edge, including pavements and other man-made surfaces, but excluding grass verges, trees, and other natural features. (Naturally, use of land either side of the carriageway may be subject to land acquisition and other issues.)

These options are available for two types of cycle infrastructure:

- **Two unidirectional cycle tracks** (one on each side of the street, suitable in most cases).
- **A single bidirectional cycle track** (on one side of the street, requires less space but is less suitable where there are many side roads or driveways).

Road segments are categorised based on whether they have enough space to accommodate desirable minimum cycle infrastructure widths, absolute minimum cycle infrastructure widths, or not enough space for even the absolute minimum width, assuming no changes to lanes for motor traffic or dedicated bus lanes.

#### Road width measurements

Two key measurements are taken to assess whether existing roads can accommodate cycle infrastructure: carriage width and corridor width. 
Data on carriageway widths were derived from Ordnance Survey Mastermap Highways data, using the "averageWidth" attribute from the RoadLink layer (see [docs.os.uk](https://docs.os.uk/os-downloads/networks/os-mastermap-highways-network-roads/os-mastermap-highways-network-roads-technical-specification/structured-data-types/roadwidthtype) for details).
Data on pavement widths were derived from Ordnance Survey Mastermap Topographic data (see terms and conditions below). These width attributes were truncated to 1 metre precision and aggregated to OS OpenRoads geometries to simplify the data for visualisation in the web app. In cases where a single OpenRoads centreline represents two or more carriageways or pavements, the width attributes were added.

#### Within road width (Carriageway width) 
   
- **Definition:** The width available within the carriageway only.
- **Excludes:** Man-made roadside area such as footways.
- **Usage:** Determines if cycle infrastructure can fit solely within the carriageway.

#### Using edge-to-edge (Corridor width)

- **Definition:** The total width of the road corridor, encompassing both the carriageway and footways. 
- **Usage:** Where local policy allows, part of the footway may be reallocated for cycle infrastructure, provided that minimum safe footway widths are maintained (2x 2 m footway width).

#### Cycle infrastructure width requirements

Two main types of cycle infrastructure are considered, depending on the street configuration:

Two Unidirectional Protected Cycle Tracks, one on each side of the street  (shown as '2 x 1-way tracks' in the tool):
  - *Absolute Minimum Width:* 1.5 m  
  - *Desirable Minimum Width:* 2.0 m  

A single Bidirectional Cycle Track on one side of the street  (shown as 2-way track):
  - *Absolute Minimum Width:* 2.0 m
  - *Desirable Minimum Width:* 3.0 m

#### Buffers for cycle infrastructure

Buffers are applied based on road speed and traffic conditions, as specified in Table 3.8 of the Cycling by Design document [Cycling by Design document](https://www.transport.gov.scot/media/50323/cycling-by-design-update-2019-final-document-15-september-2021-1.pdf#page=64). These buffers must be accounted for when calculating the effective available width for cycle infrastructure.

| Road type / Speed limit | Buffer width |
|-------------------------|--------------|
| 30 mph                  | 0.5 m        |
| 40 mph                  | 1.0 m        |
| 50 mph                  | 2.0 m        |
| 60 mph                  | 2.5 m        |
| 70 mph                  | 3.5 m        |

#### Bus routes and road traffic assumptions

##### Bus routes and dedicated bus lanes

Bus routes and dedicated bus lanes are key factors in determining the available space for cycle infrastructure:

- **Non-bus routes:**  
  The necessary carriageway lane width is considered to be **2 × 2.75 m**.

- **Bus routes without dedicated bus lanes:**  
  The necessary carriageway lane width to accommodate buses is considered to be **2 × 3.2 m**.

- **Bus routes with dedicated bus lanes:**  
  The necessary carriageway lane width to accommodate dedicated bus lanes is considered to be **2 × 3.2 m** plus an additional space of **`n_bus_lanes` × 3.2 m** for the dedicated bus lanes.

##### Road types

Roads are categorised based on their traffic configuration and bus route status:
- Two‐way for motor traffic (non–bus route)
- Two‐way for motor traffic (bus route without dedicated bus lanes)
- Two‐way for motor traffic (bus route with dedicated bus lanes)

#### Categorisation based on available width

The Street Space layer divides roads into three groups, depending on whether the available width (carriageway width or corridor width) can accommodate the cycle infrastructure:

- **Not enough space:**
  The available space is insufficient to fit even the absolute minimum width of cycle infrastructure.

- **Absolute minimum:**
  The available space is enough to accommodate the absolute minimum width of cycle infrastructure, but it does not meet the desirable minimum.

- **Desirable minimum:**
  The available space is sufficient to accommodate the desirable minimum width of cycle infrastructure, providing a more comfortable design for all users.

#### Limitations

Space used for parking and loading is currently excluded from the analysis.
This means that road segments that are wide enough to accommodate cycle infrastructure if parking were removed or relocated are shown as having enough space (green), even if they currently have on-street parking.
Interventions on segments with space available for cycle infrastructure according to the layer may therefore require parking to be removed or relocated, or may need to be made one-way, before cycle infrastructure can be installed.
This limitation is due to the lack of a national parking & loading dataset.

The layer also ignores the possibility of making roads one-way, which would allow for more space to be made available for cycle infrastructure.
We would like to address this in future work.

<!-- /#streetspace -->

### 2.5. Data zones {#data_zones}

<!-- #data_zones -->

Data Zones are small geographic zones created for summarising Census datasets.
In the NPT, they are used to provide contextual area-based information.

![Data zones](/images/data_zones.png)

Data zones can be visualised based on the following attributes:

* % commuter cycling (Baseline)
* % commuter cycling (Go Dutch)
* Population density (per hectare) (from 2021 Census)
* Index of Multiple Deprivation (2020) (from the Scottish Indices of Multiple Deprivation)
<!-- TODO: update these when we find out -->
* Drive time to a petrol station (from the Scottish Indices of Multiple Deprivation)
* Drive time to GP (from the Scottish Indices of Multiple Deprivation)

<!-- /#data_zones -->

### 2.6. Other layers {#otherlayers}

The NPT provides several supplementary map layers that enhance the contextual understanding of the cycling network.

<!-- TODO: add year to data sources -->

* Schools (click on a school to see current and potential future mode split data): Revealing the locations of primary, secondary, and other educational institutions, this layer allows users to click on individual schools to review the present and potential future distribution of travel modes among students.
* Wards: This layer overlays the boundaries of local electoral wards onto the map.
* Scottish Parliamentary Constituencies: Users can display the geographic divisions for Scottish parliamentary representation.
* Local Authority: Highlight the administrative areas within Scotland, aiding in planning and analysis at a local government level.

## 3. Accessing the NPT {#access}

#### Progressive Web App

The NPT is a Progressive Web App (PWA), which can be installed on many devices, including your smartphone. The App provides the same features as the website, but includes additional benefits such as pinning the App to your device's home screen and full-screen support.

How to install the NPT as an app

#### Android

1.  Visit [www.npt.scot](http://www.npt.scot) using Google Chrome
2.  Click the "Add NPT to Home screen" and follow the instructions

If the "Add NPT to Home screen" option does not appear, you can also select the "Install app" option from the main Chrome menu (…)

#### Windows 10 & 11 and Linux

1.  Visit [www.npt.scot](http://www.npt.scot) using Microsoft Edge or Chrome
2.  In the address bar, click the App install button
3.  Click install

#### iOS

1.  Visit [www.npt.scot](http://www.npt.scot) using Safari
2.  In the bottom menu bar, click the share button (middle button)
3.  Click "Add to Home Screen"
4.  Click "Add"

#### macOS

1.  Visit [www.npt.scot](http://www.npt.scot) using Safari
2.  In the address bar, click the App install button
3.  Click install

## 4. Data downloads {#data}

A series of open access [data downloads](https://github.com/nptscot/npt/releases/tag/v2025-05-01) can be analysed in-house with GIS such as QGIS or data science tools such as R and Python.
Click on the "Data" tab in the top menu to access the data downloads.

## 5. The Network Planning Workspace (NPW) {#npw}

The Network Planning Workspace (NPW) is a tool that builds on and makes use of the NPT data for more advanced users and people who want to plan cycle networks. It allows users to sketch a proposed cycle network on the map and assess the quality of the network plan. It can be accessed using the ‘Local Authorities’ tab or directly via npw.scot. See the NPW web application at [npw.scot](https://nptscot.github.io/npw/) for more information.

