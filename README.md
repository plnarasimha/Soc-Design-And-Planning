# Soc-Design-And-Planning
# Table of the contents
* Day-1
  [ Inception of Open-Source EDA, OpenLane and Sky130 PDK ]
* Day-2 Good Floorplan Vs Bad Floorplan and Introduction to Library Cells
* Day-3 Design Library Cell using magic layout and ngspice charcterization
* Day-4 Timing Analysis and Clock Tree Synthesis (CTS)
* Day-5  Final steps in RTL2GDS
# Introduction to OpenLANE
OpenLane is an automated RTL to GDSII flow based on several components including OpenROAD, Yosys, Magic, Netgen, CVC, SPEF-Extractor, KLayout and a number of custom scripts for design exploration and optimization. It also provides a number of custom scripts for design exploration and optimization. The flow performs all ASIC implementation steps from RTL all the way down to GDSII. Currently, it supports both A and B variants of the sky130 PDK, the C variant of the gf180mcu PDK, and instructions to add support for other (including proprietary) PDKs are documented. The whole documentation can be found here [https://github.com/The-OpenROAD-Project/OpenLane]. OpenLane abstracts the underlying open source utilities, and allows users to configure all their behavior with just a single configuration file.
# OpenLane Architecture
![Screenshot 2024-06-09 165704](https://github.com/plnarasimha/Soc-Design-And-Planning/assets/75074032/fcaa7384-6bf2-45f2-b9b2-47f2d3f968ba)
