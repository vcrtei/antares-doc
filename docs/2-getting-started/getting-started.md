# Getting started

## Software Presentation

[Antares-Simulator](https://antares-simulator.org ) is an Open Source (GNU GPL 3.0) standalone software. It is a sequential Monte-Carlo simulator designed for short to long term studies of large interconnected power grids. It simulates the economic behavior of the whole transmission-generation system, throughout the year and with a resolution of one hour.


**Antares-Simulator can be downloaded free of charge, installed on any local computer or server and use without any limitation.**


RTE (French Electricity Transmission system Operator) has initially developed the tool for its own purposes and keeps on improving and enhancing its capabilities. Antares-Simulator is currently one of key tool of [reference studies](https://antares-simulator.org/pages/etudes/4/) such as the French Generation Adequacy Report, published by RTE, or the ENTSO-E’s Ten Years Network Development Plan (TYNDP). More generally, the tool has been proving very useful for assessing the economic performances, ecological impact and security of supply levels of power systems, as well as the contribution of its assets (generation units, interconnectors, storages, etc.) to these three axes.


The executable file of Antares-Simulator is [provided free of charge](https://antares-simulator.org/pages/antares-simulator/6/). By subscribing to the User’s Club, one can also benefit from services such as software maintenance or trainings.

### Starting with _Antares-Simulator_

User can define an electrical network using _nodes_ that represent regions or countries. Each _node_ contains data on its electrical **production**, **consumption** and **reserves**. The nodes can also exchange flows using _links_ with defined parameters such as commercial capacities or impedance.


The consumption of a _node_ is defined by its _Load_. The _Load_ can be an user-input with _Time-series_ or it can be generated via probabilistic models. The different production means which can be set are: renewable energies such as _Wind_ and _Solar_ energy, _Hydro_ energy, and different kinds of _Thermal_ units. _Wind_ and _Solar_ production units are a fatal production means which cannot be optimized: they are either user input or randomly generated through probabilistic models. The _Thermal_ units can be defined as being _Gas_, _Hard Coal_, _Lignite_, _Mixed Fuel_, _Nuclear_, _Oil_ or _Other_. They are set using their _Operating Parameters_, _Operating Costs_ and _Reliability Model_. Finally, the _Hydro_ units are defined between a fatal _Run-of-the-river (ROR)_ production and _Hydro Storage_.

The use of the _Thermal_ units and of _Hydro Storage_ is optimized to reduce costs. It is also possible to simulate multiple _Monte Carlo_ years in Antares in order to compare different production scenarios.


### Post-processing with R-packages

Different R-packages have been developed by RTE around Antares. They can be used to study, read simulation outputs or visualize them. After running an Antares study, one can use the package [_antaresRead_](https://rte-antares-rpackage.github.io/antaresRead/index.html) to import the output to a R session. One can then use [_antaresProcessing_](https://github.com/rte-antares-rpackage/antaresProcessing) to manipualte the results or [ _antaresViz_](https://rte-antares-rpackage.github.io/antaresViz/index.html) to visualize them using interactive graphs.


### Pre-processing with R-packages

Different packages have been developed to launch Antares studies from a R session: the package [_antaresEditObject_](https://rte-antares-rpackage.github.io/antaresEditObject/index.html) to edit an Antares study before launching it, [_antaresXpansion_](https://github.com/rte-antares-rpackage/antaresXpansion) to optimizes the installed capacities of an Antares study, [_antaresFlowbased_](https://github.com/rte-antares-rpackage/antaresFlowbased) to  launch a flowBased study from an existed Antares study and [_antaresWaterValues_](https://rte-antares-rpackage.github.io/antaresWaterValues/index.html) to  generate water values for Antares and to run specific simulations.