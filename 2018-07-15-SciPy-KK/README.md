SciPy 2018 (KK, MT)
===================

Authors
-------
Kacper Kowalik (NCSA, UIUC)
Matthew Turk (NCSA/iSchool, UIUC)

Short description
-----------------
Accessing remote data with persistent, user-definable computational environments is a key challenge in digital scholarship.  The Whole Tale is a response to this, building and combining components to provide a virtual research "home" on the web.  In this talk, we'll describe how the Whole Tale project leverages existing Python projects (Jupyter, PyFilesystem, fusepy, WsgiDAV, Girder and many others) to bring remote analysis and data together, providing persistent workspaces and capturing provenance and data lineage to facilitate the scholarly process.

Long description
----------------

This talk introduces the Whole Tale project, which aims to enable researchers to examine, transform and then seamlessly republish research data that was used in a scientific articles. We strive to strengthen the three layers of scholarly publication: scholarly process, data access, and computational analysis.

A principle of The Whole Tale is running custom, containerized compute environments, along with external data exposed to the user as a unified FUSE filesystem, transparently mediating access to remote and diverse data sources. We believe that our approach to handling data this way can be easily generalized to other similar projects in the SciPy "ecosystem", such as JupyterHub/BinderHub. Furthermore, introducing an abstract layer between data and computations allows for a finegrained provenace tracking making it easy to provide an automatic credit attribution and boost the reproducibility of the scholarly process.

Our presentation will have the following structure:

* Introducing Whole Tale
    * Project goals
    * Major concepts
* Overview of the architecture
    * Comparison with exisiting solutions
    * Highlight software projects from Python ecosystem used in WT
* FUSE filesystem as way of getting data into remote environment
    * Problems we are trying to solve
    * Current implementation
* A brief outlook of upcoming features 

This talk should be of interest to anyone trying to solve the issues related to "injecting" data into containerized environments (Docker etc.), handling authentication issues related to running anonymous compute environments, and tracking provenance and reproducibility of scientific articles.

Matthew Turk is co-PI of The Whole Tale project. Kacper Kowalik serves as a software architect for WT.

Online references:
* https://github.com/whole-tale -- Project software repositories
* https://wholetale.org -- Main project page
* https://dashboard.wholetale.org -- Working prototype
* A. Brinckman, et al., Computing environments for reproducibility: Capturing the ‘‘Whole Tale’’, Future Generation Computer Systems (2018), https://doi.org/10.1016/j.future.2017.12.029
* B. Ludäscher, K. Chard, N. Gaffney, M.B. Jones, J. Nabrzyski, V. Stodden, M. Turk, Capturing the ‘‘whole tale’’ of computational research:Reproducibility in computing environments. http://arxiv.org/abs/1610.09958
