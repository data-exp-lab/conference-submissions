The Long Description:

This talk covers a tool developed for fast, interactive, browser-based
visualization of datasets with yt, a python package used to analyze and
visualize volumetric data in a number of scientific domains. 
This tool uses Jupyter widgets to do interactive data exploration and
visualization in the browser. Jupyter widgets provide users with a 
balance between ease-of-use and access to API functionality, 
but have a lower barrier to entry for data
exploration than direct API manipulation alone. We anticipated latency 
issues with some datasets resulting from data transmission between yt and the
browser. As the data canvas is updated, a new image is created and this
computation is generally done outside of the browser environment, requiring
data transfer for canvas updates. We minimize this latency by
compiling our visualization routines to WebAssembly, pushing data to the
browser, and doing subsequent computations in the browser. This tool will 
provide a pathway for fast, interactive data visualization and exploration  
for a diverse user base. 

Our presentation will have the following structure:
* The development of the tool
  * Using Rust compiled to WebAssembly for image pixelization and rendering
  * The development of a modular widget structure to interact with both yt and
    webassembly to interactively explore and visualize data. 
* Comparing data exploration with this tool versus direct data exploration with
  the yt API or immersive visualization methods.  
* A live demonstration using a representative dataset 
  of the features available for data visualization with our widget.
* Discussion covering the challenges and lessons learned 
  from developing the tool, with commentary on how this functionality might be
  applied in other scenarios.
* A brief commentary on next steps and other features we'd like to implement. 

The authors of this toolkit are Nathanael Claussen and Madicken Munk. Both
authors intend to present their respective contributions to the project. 
Madicken developed the backend pixelization routines that port
data arrays from yt using rust to WebAssembly. 
Nathanael developed the Jupyter widget that readily interfaces with
yt and WebAssembly to interactively visualize data using widgets in 
Jupyter notebooks. 

We have developed this tool
as members of the data exploration lab (DXL), an interdisciplinary research 
group focused on data exploration and visualization at the
University of Illinois at Urbana Champaign. 
Madicken is a postdoctoral research scholar in the DXL and 
has presented at topical conferences and
departmental colloquia in her
scientific domain, listed (with slides when appropriate) here:
http://munkm.github.io/posts/2017/09/28/publications.html . Nathanael was an
undergraduate summer intern for the DXL. 
Nathanael has transitioned from a summer internship with the DXL to
joining it as an undergraduate researcher. He has given a number of 
classroom presentations. 

This talk will be of interest to any attendees interested in data visualization
and visual exploration of data. It will also be of interest to attendees that
have three-dimensional datasets that may be visualized using yt. 
Our tool potentially can be extended to other
three-dimensional data visualization tools, so developers interested in adding
this functionality to their packages may also find this talk of interest. Last,
individuals interested in developing advanced Jupyter widgets to do
browser-based computation or communicating nontrivially-sized datasets from
Python to the browser may find this talk of interest. 

The yt project
is a community-developed NUMFocus project that depends on core scipy
libraries--including matplotlib, numpy, and sympy--and has been
applied in several scientific domains, including astronomy, seismology, nuclear
engineering, and oceanography. Many contributors to yt
are also members of the Data Exploration Lab. 

Relevant links:
* The DXL group webpage: https://dxl.ncsa.illinois.edu/
* The yt project page: http://yt-project.org/
* yt repository: https://github.com/yt-project/yt 
* yt-tools widget repository: https://github.com/data-exp-lab/yt_widgets
* rust pixelizer to webassembly repository: https://github.com/data-exp-lab/rust-yt-tools

