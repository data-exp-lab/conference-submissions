Title:

The Demeshening: the next generation of particle support in yt

Abstract:

(Around 100 words; this will be used a the summary of your talk in the online program.)

Large N-body particle datasets present a unique challenge for analysis and visualization. With multi-terabyte datasets becoming increasingly common, the goal of performing large-scale analysis and visualization of such large quantities of data becomes increasingly challenging.

In this talk we describe a new particle indexing scheme we have designed for yt, a python toolkit for the analysis and visualization of 3D simulation data. By making use of compressed Morton bitmaps to index the locations of particles, we substantially decrease the overhead to perform spatial chunking. By rethinking the high-level yt API for N-body data to be more particle-centric, we are able to scale analysis and visualization to datasets containing very large numbers of particles while reaping performance improvements and decreased memory overhead when working with smaller datasets.

Extended Abstract:

(Should be no more than 2 pages, and address the following: Do you intend to present a demo? Does the work make any new contributions to open-source software? Which existing open-source tools does it use? What science fields are impacted by the work? How does it work fit into the Scientific Python community?)

This talk can be readily split into two main sections corresponding to the primary code contributions of the two authors. The authors intend to both speak during the talk about their own contributions.

Meagan Lang is the primary author of the new Morton bitmap index scheme. She will describe the design and low-level implementation, focusing on the parts of the work that will be most interesting to a wide audience of interested scientific python programmers, including wrapping the EWAHBoolArray C++ library in Cython.

Nathan Goldbaum is primarily responsible for changes to the high-level yt API that were needed after removing the global octree. He will describe the process of proposing and implementing a backward incompatible change to a large codebase, discussing testing strategies and the design of migration paths for existing users as well and present benchmarks for common analysis tasks.

Time permitting, the authors will present a live demo, visualizing and analyzing a large particle dataset stored on the presenter’s laptop. This will show how it is possible to visualize and analyze a reasonably sized subset of the simulation in real-time, as well as a large fraction of the simulation volume in an IO-bound fashion.

This talk primarily focuses on improvements to yt, a free and open source toolkit for analyzing and visualizing simulation data, used for day-to-day work by a diverse community of researchers around the world at all stages in their careers. The yt method paper, which we suggest people to cite if they use yt in their published work, currently has approximately 300 citations. Currently yt is most commonly used in computational astrophysics but also has official support for simulations of nuclear reactors as well as particle-in-cell plasma physics simulations. It has also been used by geophysicists to visualize earthquake propagation, doctors working with medical imaging data, and meteorologists to analyze computational models of thunderstorms and tornados. The work described in this talk will allow researchers who work with extremely large particle datasets to make use of yt and will improve performance and memory overhead for current users of yt with smaller particle datasets. This includes computational astrophysicists working with N-body data or smoothed particle hydrodynamics (SPH) simulations as well as plasma physicists working with data from particle-in-cell simulations. We are also interested in experimenting with point cloud data generated for medical imaging as well as geo-referenced digital elevation models.

The yt project is a NumFocus fiscally sponsored project with a well-defined set of codified community norms, a steering committee, and a diverse contributor base of more than 100 individuals over the history of the codebase. Almost all yt contributors are scientists who use yt in their research. The yt python codebase directly depends on a number of core SciPy projects, including NumPy, matplotlib, Cython, Sympy. It also optionally supports integration with SciPy, IPython and the Jupyter notebook. It has been used by a number of researchers as a key component of their scientific python stack, in cooperation with other tools with similar or complementary capabilities like Mayavi and astropy.
