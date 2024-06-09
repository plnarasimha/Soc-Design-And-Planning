# Soc-Design-And-Planning
# Table of the contents
* Day-1 Inception of Open-Source EDA, OpenLane and Sky130 PDK 
* Day-2 Good Floorplan Vs Bad Floorplan and Introduction to Library Cells
* Day-3 Design Library Cell using magic layout and ngspice charcterization
* Day-4 Timing Analysis and Clock Tree Synthesis (CTS)
* Day-5  Final steps in RTL2GDS
# Introduction to OpenLANE
OpenLane is an automated RTL to GDSII flow based on several components including OpenROAD, Yosys, Magic, Netgen, CVC, SPEF-Extractor, KLayout and a number of custom scripts for design exploration and optimization. It also provides a number of custom scripts for design exploration and optimization. The flow performs all ASIC implementation steps from RTL all the way down to GDSII. Currently, it supports both A and B variants of the sky130 PDK, the C variant of the gf180mcu PDK, and instructions to add support for other (including proprietary) PDKs are documented. The whole documentation can be found here [https://github.com/The-OpenROAD-Project/OpenLane]. OpenLane abstracts the underlying open source utilities, and allows users to configure all their behavior with just a single configuration file.
# OpenLane Architecture
![Screenshot 2024-06-09 165704](https://github.com/plnarasimha/Soc-Design-And-Planning/assets/75074032/fcaa7384-6bf2-45f2-b9b2-47f2d3f968ba)

# OpenLane Design Stages
OpenLane flow consists of several stages. By default all flow steps are run in sequence. Each stage may consist of multiple sub-stages. OpenLane can also be run interactively as shown here.
 
 1.**Synthesis**
 
 i. yosys/abc - Perform RTL synthesis and technology mapping.
 
 ii .OpenSTA - Performs static timing analysis on the resulting netlist to generate timing reports
 
 2.**Floorplaning**
 
 i. init_fp - Defines the core area for the macro as well as the rows (used for placement) and the tracks (used for routing).
 
 ii. ioplacer - Places the macro input and output ports
 
 iii. pdngen - Generates the power distribution network
 
 iv. tapcell - Inserts welltap and decap cells in the floorplan

 3.**Placement**
 
 i. RePLace - Performs global placement
 
 ii. Resizer - Performs optional optimizations on the design
 
 iii. OpenDP - Performs detailed placement to legalize the globally placed components
 
 4.**CTS**
 
 i. TritonCTS - Synthesizes the clock distribution network (the clock tree)

 5.**Routing**
 
 i. FastRoute - Performs global routing to generate a guide file for the detailed router
 
 ii.TritonRoute - Performs detailed routing
