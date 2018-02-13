The Short Description:

This talk covers a tool developed for fast, interactive, browser-based
visualization of datasets using Jupyter widgets developed for use with yt. 
Jupyter widgets offer a unique opportunity to access the functionality in yt 
using a graphical interface, 
allowing for simultaneous control over the data and an 
ease-of-use not immediately accessible through the API
alone. Further, browser latency may be an issue with direct
visualization of volumetric data with a widget. 
We minimize latency that results from data transmission between yt and the
browser by compiling to WebAssembly and pushing data to the browser. Operations
on the data are subsequently done in the browser.

