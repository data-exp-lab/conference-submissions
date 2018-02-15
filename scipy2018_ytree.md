# ytree

## Title

### ytree: ingestion and analysis of merger-tree data from the plethora

## Keywords:
astronomy
astrophysics
galaxies
simulation
data
analysis
merger-trees

## Abstract

The merger-tree is a frequently used concept in the study of galaxy formation. It describes the process by which structures assemble hierarchically through the mergers of successively larger objects. A merger-tree is also a complex data product of a cosmological galaxy formation simulation. As with astrophysical simulations, there exists a variety of tools for constructing merger-trees, each with a unique output format. 

We present ytree, a tool for ingesting multi-format merger-tree data and potentially other tree-like data. ytree builds tree structures and loads field data strictly on demand, returns NumPy arrays with symbolic units, and writes an optimized file format.

## Extended Abstract

Large-scale cosmological structures (i.e, galaxies, clusters of galaxies, etc.) form through the mergers of initially small objects into successively larger ones. This process, called hierarchical structure formation, can be visualized as a tree, where the trunk represents a single object at a given time and the branches of decreasing size represent its ancestors. In astrophysical simulations, this tree concept is used to quantify the growth of individual simulated galaxies. "Merger-trees" can be constructed from simulations by analyzing the positions and contents of gravitationally bound objects over time. Like the simulations themselves, merger-tree calculations are computationally expensive. Also like simulations, there exist a multitude of methods and codes, all writing to file formats that differ in both design and implementation. The obvious outcome is that comparison of scientific results is difficult and a wheel is frequently re-invented. 

In this talk, We will present the ytree code, an extension of the yt analysis toolkit designed for ingesting merger-tree data from multiple sources and presenting it in structures familiar to most Python users, and especially users of yt. ytree has been designed to have both a similar user interface and source code structure as yt so as to ease entry for new users and developers coming from yt. 

ytree builds tree structures and loads field data in stages and strictly on demand, allowing users to efficiently extract small amounts of information from large data sets. Like yt, ytree contains a mapping of format-specific field names and units to universal field names, making it easier to reuse analysis scripts on different data. Field data are stored in YTArrays, NumPy arrays that support symbolic units. Individual trees or entire data sets can be re-written to an optimized file format built on HDF5. 

The ytree code also has a subpackage, treefarm, for constructing merger-trees. The treefarm package allows users to easily customize each aspect of merger-tree generation (e.g., selection of candidate objects for descendent/ancestor matching, determining matches, and strategies for parallelism.) This allows the code to be used as-is or as a platform for developing and testing merger-tree related algorithms. 

The ytree source code is available at: https://github.com/brittonsmith/ytree 
Documentation is available at: http://ytree.readthedocs.io 

This talk will provide an overview of ytree's features (both data ingestion and generation through treefarm) and key implementation aspects. The talk is intended for astronomers working with merger-trees or cosmological simulations and potentially people from other domains working with tree-like data. 

Britton Smith is the original author and designer of ytree. Meagan Lang implemented support for the LHaloTree format (a popular format for very large simulations) and inspired a number of critical design decisions. 

This will be the first talk I have given on ytree, but slides from a couple previous talks on the yt code/project can be found at the links below: 
https://figshare.com/articles/yt_Massively_Parallel_Astrophysical_Simulation_Analysis_Made_Easy/643390 
https://figshare.com/articles/The_yt_Project/1391957
