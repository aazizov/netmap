# About the NPT project

## The NPT tool

The Network Planning Tool for Scotland (NPT) is a planning support system, research project, and web application to support strategic planning for active travel. The 2023 version is focused on cycle network planning and builds on the Department for Transport funded [Propensity to Cycle Tool](https://www.pct.bike/) for England and Wales.

The NPT uses data from the census and other reliable sources to estimate cycling uptake across Scotland. It delivers on the [vision](https://www.transport.gov.scot/media/33802/active_travel.pdf) for active travel to be the most popular choice for shorter everyday journeys.
It estimates what journeys would be taken by bike based on where people live, work, shop and socialise and the distances and hills between them.
Routing algorithms optimised for cycling assigns journeys to the existing road and path network, resulting cycling network flows for planning fast (direct), quiet (low traffic) and balanced (intermediate traffic) routes.
This evidence on estimated baseline and future potential cycling levels is provided at the network level, down to individual streets and cycleways nationwide across Scotland, allowing it to be used for planning and prioritising investment in joined up and cost-effective cycle networks.

It is designed to be used by local authorities, community groups and other organisations to help them plan for cycling but is open access and can be used by anyone to support more evidence-based and data-driven discussions about and decisions on cycling infrastructure and investment.

See the [manual](/manual) for more information on how to use the tool.

## The Network Planning Workspace (NPW)

The NPT is complemented by the related [Network Planning Workspace (NPW)](https://npw.scot) web application for sketching, evaluating and sharing cycle networks, which was developed as part of the same project. The NPW is a tool that builds on and makes use of the NPT data for more advanced users and people who want to design cycle networks in a web app with rapid feedback. It allows users to sketch a proposed cycle network on the map and assess the quality of the network plan. It can be accessed using the 'Local Authorities' tab or directly via [npw.scot](https://npw.scot).

The coherent network layer in the NPT can be used as a 'starter for 10' in the Network Planning Workspace to quickly plan a strategic cycle network in urban areas, prioritising investment by highlighting routes that maximize coverage and connectivity while aligning with demand.

## What's new?

<!-- See package.json: -->
### v2.1.0 (June 2025)

* Added A/B Street logo to welcome modal and updated logo ordering (see issue [#477](https://github.com/nptscot/nptscot.github.io/issues/477) and pull request [#484](https://github.com/nptscot/nptscot.github.io/pull/484))
* Updated initial map view to show all of Scotland by default (see issue [#475](https://github.com/nptscot/nptscot.github.io/issues/475) and pull request [#483](https://github.com/nptscot/nptscot.github.io/pull/483))
* Fixed issues with help page popups and improved manual navigation (see issue [#479](https://github.com/nptscot/nptscot.github.io/issues/479) and pull request [#480](https://github.com/nptscot/nptscot.github.io/pull/480))
* Fixed incorrect information in street space layer manual section - clarified that edge-to-edge widths include only carriageway and footways, not verges (see issue [#498](https://github.com/nptscot/nptscot.github.io/issues/498))
* Fixed typos and improved documentation (see pull request [#478](https://github.com/nptscot/nptscot.github.io/pull/478))
* Added missing dates to landing page popup (see issue [#471](https://github.com/nptscot/nptscot.github.io/issues/471) and pull request [#472](https://github.com/nptscot/nptscot.github.io/pull/472))
* Improved table of contents functionality in manual
* Enhanced user interface and styling improvements

### v2.0.0 (January 2025)

* Updates to the route network data, now using the all-purpose O/D data
* Addition of Coherent Network
* Addition of four new infrastructure and traffic layers
* Refinement of motor traffic volumes layer, including fixing anomalies in loop streets
* Updates to the manual
* Refinements to the user interface
* Permalinks for enabled layers

## The development team

The NPT Scotland project is a collaboration between Transport Scotland, Sustrans, the University of Leeds, CycleStreets and A/B Street.

<p id="logos">
	<a href="https://www.transport.gov.scot/" target="_blank"><img src="/images/logos/transportscotland.svg" alt="Transport Scotland" /></a>
	<a href="https://www.sustrans.org.uk/about-us/our-work-in-scotland" target="_blank"><img src="/images/logos/sustrans.png" alt="Sustrans" /></a>
	<a href="https://environment.leeds.ac.uk/transport" target="_blank"><img src="/images/logos/leeds.png" alt="University of Leeds" /></a>
	<a href="https://www.cyclestreets.org/" target="_blank"><img src="/images/logos/cyclestreets.svg" alt="CycleStreets" /></a>
	<a href="https://abstreet.org/" target="_blank"><img src="/images/abstreet-logo.svg" alt="A/B Street" /></a>
</p>

Contributors to the [codebase](https://github.com/nptscot) include:

- Robin Lovelace (University of Leeds)
- Malcolm Morgan (University of Leeds)
- Zhao Wang (University of Leeds)
- Hussein Mahfouz (University of Leeds)
- Juan Pablo Fonseca Zamora (University of Leeds)
- Martin Lucas-Smith (CycleStreets Ltd)
- Dustin Carlino (A/B Street Ltd)
- Angus Calder (Sustrans Scotland)

## Intellectual Property

The research and software underpinning the NPT tool is described in the following papers:

* The [Propensity to Cycle Tool (PCT)](https://www.pct.bike) for England and Wales (Lovelace [2016](https://eprints.whiterose.ac.uk/100080/); Lovelace et al. [2017](https://doi.org/10.5198/jtlu.2016.862); Goodman et al. [2019](https://doi.org/10.5198/jtlu.2016.862))
* The 'overline' method for generating and visualising route networks (Morgan and Lovelace [2020](https://doi.org/10.1177/2399808320942779))
* The 'jittering' method for disaggregating and adding geographic detail to origin-destination data (Lovelace et al. [2022](https://doi.org/10.1177/2399808320942779))

The NPT builds on the Propensity to Cycle Tool (PCT) for England and Wales which was funded by the Department for Transport, the development of which was led by Dr Robin Lovelace at the University of Leeds.

Non-transferable and non-exclusive rights to use background intellectual property are granted for the project's sole purpose. The arising intellectual property will be owned by the University of Leeds, Sustrans, or jointly, depending on who generated or developed it. The University of Leeds developed the code underlying the NPT tool as open source software licensed under the terms of the AGPLv3, as outlined below, to ensure public benefit arising from public investment in the tool and improvements to the underlying methods and software. The terms of any license agreement will be negotiated in good faith and will be fair and reasonable, taking into account the scientific and financial contributions of the University of Leeds and other parties.

## Open Source Policy

Like the PCT, the NPT tool is open source and licensed under the terms of the AGPLv3 to encourage community contributions and ensure public benefit arising from public investment in the tool, as outlined below.

The NPT Scotland project is open source, and the code is available on [GitHub](https://www.github.com/nptscot). The code is licensed under the Affero General Public License (AGPL) version 3.0 which enables anyone to use, modify and share the code for any purpose, subject to the conditions in the license, including the requirement that any modified versions of the code must be made available under the same license. See the full license in the project's open source repositories on GitHub in the bullet points below:

* Data processing and modelling code [license](https://github.com/nptscot/npt/blob/main/LICENSE)
* Web app code [license](https://github.com/nptscot/nptscot.github.io/blob/dev/LICENSE)

This means that you are free to copy and re-use the code but that if you use a version of the code, you must make the source code publicly available.

## Feedback and contributions

We encourage feedback and contributions to the project:

* For general feedback please fill in our 5 minute [feedback survey](https://forms.office.com/Pages/ResponsePage.aspx?id=qO3qvR3IzkWGPlIypTW3ywVZfmO0bwdAhK0UztpneQtUM1pCRlJQQjY1V0M3MUhBV0g0VTJRS1ZQVi4u)
* Feature requests and bug reports can be made via the [issue tracker](https://github.com/nptscot/npt/issues).
* Code contributions can be made via Pull Requests to the [GitHub repository containing the web app](https://github.com/nptscot/nptscot.github.io/pulls).
* Questions and discussions are welcome in the [Discussions](https://github.com/nptscot/npt/discussions) section of the project's GitHub repo
* For general enquiries you can contact us on: [nptscotland@gmail.com](mailto:nptscotland@gmail.com)

## Privacy

Our [privacy policy](/privacy/) is available.

## References

* Lovelace, Robin. ‘Mapping out the Future of Cycling’. _Get Britain Cycling_, [2016](http://eprints.whiterose.ac.uk/100080/).
* Goodman, Anna, Ilan Fridman Rojas, James Woodcock, Rachel Aldred, Nikolai Berkoff, Malcolm Morgan, Ali Abbas, and Robin Lovelace. ‘Scenarios of Cycling to School in England, and Associated Health and Carbon Impacts: Application of the “Propensity to Cycle Tool”’. _Journal of Transport & Health_ 12 (1 March 2019): 263–78. [https://doi.org/10.1016/j.jth.2019.01.008](https://doi.org/10.1016/j.jth.2019.01.008).
* Lovelace, Robin, Anna Goodman, Rachel Aldred, Nikolai Berkoff, Ali Abbas, and James Woodcock. ‘The Propensity to Cycle Tool: An Open Source Online System for Sustainable Transport Planning’. _Journal of Transport and Land Use_ 10, no. 1 (1 January 2017). [https://doi.org/10.5198/jtlu.2016.862](https://doi.org/10.5198/jtlu.2016.862).
* Lovelace, Robin, Rosa Félix, and Dustin Carlino.. ‘Jittering: A Computationally Efficient Method for Generating Realistic Route Networks from Origin-Destination Data’. _Findings_, 8 April 2022, 33873. [https://doi.org/10.32866/001c.33873](https://doi.org/10.32866/001c.33873).
* Morgan, Malcolm, and Robin Lovelace. ‘Travel Flow Aggregation: Nationally Scalable Methods for Interactive and Online Visualisation of Transport Behaviour at the Road Network Level’. _Environment & Planning B: Planning & Design_, July 2020. [https://doi.org/10.1177/2399808320942779](https://doi.org/10.1177/2399808320942779).
