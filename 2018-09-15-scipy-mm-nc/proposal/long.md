The Long Description:

We will present a tool developed for fast, interactive, browser-based
interactivity of datasets using Jupyter widgets with yt. Jupyter widgets
offer a unique opportunity to access the functionality in yt 
using a graphical interface, 
allowing for a relatively high degree of control over the data and simultaneously 
providing the user with 
an accessibility and ease-of-use not traditionally accessible through the API
alone. Further, browser latency may be an issue with direct
exploration of data with a widget. By compiling our
pixelizer directly to webassebly, datasets can be interactively explored
without delays resulting from transmission from yt to the browser.

Our presentation will have the following general outline:
* The development of the tool
  * Using Rust compiled to WebAssembly for image pixelization and rendering
  * The development of a modular widget structure to interact with both yt and
    webassembly to interactively explore data. 
* Comparing data exploration with this tool versus direct data exploration with
  the yt API or immersive visualization methods.  
* A live demonstration using a representative dataset 
  of the features available for data visualization with our widget.
* Discuss the lessons learned from developing the tool and discuss how it might
  be applied to other three-dimensional volumetric visualization packages. 

The authors of this toolkit are Nathanael Clausen and Madicken Munk. Both
authors intend to present their respective contributions to the project. 
Madicken developed the backend pixelization routines that port
data arrays from yt using rust to webassembly. 
Nathanael developed the jupyter widget that readily interfaces with
yt and webassembly to interactively visualize data using widgets in 
Jupyter notebooks. Madicken has presented at topical conferences and
departmental colloquia in her
scientific domain, listed (with slides when appropriate) here:
http://munkm.github.io/posts/2017/09/28/publications.html . Nathanael has
[INSERT INFO HERE]. 

This talk will be of interest to any attendees interested in data visualization
and visual exploration of data. It will also be of interest to attendees that
have three-dimensional datasets that may be visualized using yt. yt has been
applied in several scientific domains, including astronomy, seismology, nuclear
engineering, and oceanography. This tool potentially can be extended to other
three-dimensional data visualization tools, so developers interested in adding
this functionality to their packages may also find this talk of interest. 

Relevant links:
* The yt project page: http://yt-project.org/
* yt repository: https://github.com/yt-project/yt 
* yt-tools widget repository: https://github.com/data-exp-lab/yt_widgets
* pixelizer to webassembly repository: https://github.com/data-exp-lab/rust-yt-tools

