Sneaking Data into Containers with the Whole Tale
=================================================

See [video](https://www.youtube.com/watch?v=X0UX4bW_4w0).

Track
-----

SciPy 2018 Talks and Posters

Authors
-------

Kacper Kowalik (NCSA, UIUC)
Matthew Turk (NCSA/iSchool, UIUC)

Author keywords
---------------

* data
* reproducibility
* filesystems
* containers
* remote analysis
* workflows

Short description
-----------------

Accessing remote data with persistent, user-definable computational environments
is a key challenge in digital scholarship.  The Whole Tale is a response to this
requirement, building and combining components to provide a virtual research
"home" on the web.  In this talk, we'll describe how the Whole Tale project
leverages existing Python projects (Jupyter, PyFilesystem, fusepy, WsgiDAV,
Girder and many others) to bring remote analysis (including code and
environment) and data together, providing persistent workspaces while
automatically capturing provenance and data lineage to facilitate
reproducibility and verifiability -- cornerstones of the scholarly process.

Long description
----------------

This talk introduces the Whole Tale project, an effort to enrich computational
and data-driven research by enabling fully reproducible publication of the
research process. The Whole Tale provides an intuitive environment which enables
seamless data discovery and access, reproducible data manipulation, and
automated provenance capture. In effect, Whole Tale strengthens the three layers
of scholarly publication: sharing the scholarly methodology applied, the data
used, and the analysis process and computational environment via which results
were obtained.

To deliver on this vision, the Whole Tale relies on customized, containerized
compute environments to capture the entire research process. It augments these
containers with a managed data access interface built upon a unified FUSE
filesystem. The filesystem not only abstracts and mediates access to remote data
sources, it also captures the data lineage of all objects used in an analysis to
support subsequent reproducibility.  We believe that our approach to handling
data this way can be easily generalized to other similar projects in the SciPy
"ecosystem", such as JupyterHub/BinderHub. Furthermore, introducing an abstract
layer between data and computations allows for finegrained provenance tracking
making it easy to provide an automatic credit attribution and boost the
reproducibility of the scholarly process.

Our presentation will have the following structure:

* Introducing Whole Tale (WT)
    * Project goals
    * Major concepts
* Overview of the architecture
    * Comparison with existing solutions
    * Highlight software projects from Python ecosystem used in WT
* FUSE filesystem as way of getting data into remote environment
    * Problems we are trying to solve
    * Current implementation
* A brief outlook of upcoming features 

This talk will be of interest to those trying to solve the issues related to
"injecting" data into containerized environments (Docker etc.), handling
authentication issues related to running anonymous compute environments, and
tracking provenance. Scientists interested in reproducible research may find
Whole Tale a powerful addition to their computational toolbox.

Kacper Kowalik serves as a software architect for WT. Matthew Turk is co-PI of
The Whole Tale project.

Online references:
* https://github.com/whole-tale -- Project software repositories
* https://wholetale.org -- Main project page
* https://dashboard.wholetale.org -- Working prototype
* A. Brinckman, et al., Computing environments for reproducibility: Capturing the ‘‘Whole Tale’’, Future Generation Computer Systems (2018), https://doi.org/10.1016/j.future.2017.12.029
* B. Ludäscher, K. Chard, N. Gaffney, M.B. Jones, J. Nabrzyski, V. Stodden, M. Turk, Capturing the ‘‘whole tale’’ of computational research:Reproducibility in computing environments. http://arxiv.org/abs/1610.09958
