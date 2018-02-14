The Short Description:

This talk covers a Jupyter widget built using Rust and WebAssembly for
interactive, browser-based visualization of datasets with yt, a
python package used to analyze and visualize volumetric data in
a number of scientific domains. Users can interact and explore datasets of
varying sizes with our Jupyter widget. We minimize latency that results from
data transmission between yt and the 
browser by compiling our pixelization routines to WebAssembly and 
pushing data to the browser. Operations
on the canvas are subsequently done in the browser. Our tool enables interactive
data exploration accessible to a broad user base. 

