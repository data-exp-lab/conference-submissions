The Long Description:

This talk covers a tool developed for fast, interactive, browser-based
visualization of datasets using Jupyter widgets developed for use with yt. 
Jupyter widgets offer a unique opportunity to access the functionality in yt 
using a graphical interface, 
allowing for simultaneous control over the data and an 
ease-of-use not immediately accessible through the API
alone. Further, browser latency may be an issue with direct
visualization of volumetric data with a widget. By compiling our
pixelizer directly to WebAssembly we can minimize latency that
results from transmission between yt and the browser. 

, datasets can be interactively visualized
without latency occurring from transmission between yt and the browser.

Our presentation will have the following general structure:
* The development of the tool
  * Using Rust compiled to WebAssembly for image pixelization and rendering
  * The development of a modular widget structure to interact with both yt and
    webassembly to interactively explore data. 
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
Jupyter notebooks. Madicken is a postdoctoral research scholar and 
has presented at topical conferences and
departmental colloquia in her
scientific domain, listed (with slides when appropriate) here:
http://munkm.github.io/posts/2017/09/28/publications.html . Nathanael was an
undergraduate summer intern for the data exploration lab, which includes
several core contributors to yt. 
Nathanael has transitioned from his internship to joining the data
exploration lab as an undergraduate researcher and has given a number of 
classroom presentations. 

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
* rust pixelizer to webassembly repository: https://github.com/data-exp-lab/rust-yt-tools

