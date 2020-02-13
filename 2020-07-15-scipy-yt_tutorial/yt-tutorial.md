# SciPy 2020 Tutorial Submissions: An Introduction to Exploring and Manipulating Volumetric Data with yt

Contributors:

- Matthew Turk
- Kacper Kowalik 
- Madicken Munk

Bio: 
Matthew Turk is an Assistant Professor in the School of Information Sciences at
the University of Illinois at Urbana-Champaign. Matthew is one of the original
authors of the yt package and can provide unique insight into the evolution of
the package from its genesis. Matthew regularly instructs courses in
computation and data visualization. A sample of his coursework can be viewed
here: https://uiuc-ischool-dataviz.github.io/fall2019/

Kacper Kowalik is a research scientist at the National Center for
Supercomputing Applications. He a core contributor of yt and helps to maintain the
infrastructure around the project, including the project's CI, the project
website, and the yt-hub. Kacper's knowledge of yt infrastructure will be
integral in diagnosing user issues throughout the workshop. 

Madicken Munk is a postdoc at the National Center for Supercomputing
Applications and serves on the steering committee for the yt project. She has
been a user of yt since 2016 and a contributor since 2017. Madicken is a
certified Software Carpentry instructor, is on the Curriculum Advisory
Committee for Software Carpentry, and also helps to maintain the Software
Carpentry lesson on git for novices. Madicken has guest-instructed a number of
courses, and also has served as lead instructor at numerous carpentry workshops.
Madicken has helped to add support in yt for nuclear engineering and
geospatially-located data. 

## Audience Expectations

We expect audience members to be familiar with numpy array operations and
some familiarity with matplotlib plotting operations. Much of the tutorial will
be done in Jupyter notebooks, so learners will find the tutorial easier to
follow if they have some experience with notebook cell execution and launching. 
No previous experience with yt is
expected, but attendees with yt experience are also welcome to attend and
learn. Ideally audience members should be working with data that is volumetric
in nature; the data can be at any scale but should be either mesh-based or
pointwise. 

## Short Description

Do you have mesh-based or particle-based data that's volumetric in nature? Have
you been hacking together a pipeline to get your data into a form that you can
plot it effectively? Do you need to slice through your data, select a region of
your data, and then perform custom analysis on them? Do you want to visualize
your data as a slice, projected through space, or as a volume? Then 
yt may be a tool for you!

yt (https://yt-project.org/) is a python package for the analysis, visualization, 
and manipulation of volumetric data. yt has support for variable and regular 
mesh-based data as well as discrete (particle-like) data. 
In this tutorial, we will show users both
new to the package and those already familiar with it about how yt loads, 
stores, and handles data so they can
effectively maximize their use of it on their own data. The project
has made an effort in recent years to be domain-agnostic, so our tutorial will
leverage real data from a number of scientific domains. Broadly, we will cover
loading various data with yt routines, how the data object is handled by yt,
how the data can be manipulated with volumetric and numerical selection
routines, how various data objects can be visualized with yt, and how those
visualizations can be modified and annotated to create high-quality
publication-level figures. 

## Long Description

We are developing a set of tutorial lessons to give seasoned users and new
users of yt deeper insight into the fundamentals of how yt data is structured, how it
can be manipulated, and how it can be visualized. This tutorial will be
available online in a GitHub repository and allow users to step through 
the exercises in real time
along with the instructors. We plan on having the notebooks supplemented with
text that roughly will match what the instructor will be saying so that the
tutorial is accessible to learners of all levels. At the end of each section we
will have a 5-10 minute session where learners will be able to solve a short
problem with the concepts that they have learned. This tutorial will use real
data from a number of scientific domains so learners can gain some intuition of
how they might use yt to analyze their own data. 

All of the instructors teaching this tutorial are yt developers and will be
able to provide learners with insight into the package as needed. 

A draft outline of the tutorial (can be altered for flexibility):

- Verifying installations, cloning tutorial notebooks. (10 min)
- Summary of yt CoC and location of various versions of the documentation. (10 min)
- Loading data with yt. (30 min)
    - Importing yt and yt convenience functions
    - Loading a dataset into yt
    - Properties and attributes of the dataset object
    - Exercise: Load IsolatedGalaxy and find the fields available, the units of
      the fields, and the span of the data in km
- Selection routines with yt (60 min)
    - Filtering data with min/max selectors
    - filtering data with region selectors, like spheres and cylinders
    - plotting selected/filtered data 
    - Non-local analysis and path traversal
    - Exercise: Using the loaded IsolatedGalaxy example from the first session,
      create a sphere object of width 5 Mpc and find the minimum and maximum
      data values on both the full dataset and the sphere object. 
- SlicePlots in yt (60 min)
    - Slices in axial directions
    - Off-axes slices
    - Plot annotations for the SlicePlot
    - Exercise: Create a plot of IsolatedGalaxy with two different field
      annotations of your choice. 
- -- break --
- ProjectionPlots (45m)
    - Description of the ProjectionPlot
    - projections on regions 
    - Projection methods
    - Exercise: create a ProjectionPlot of 'density' weighted with 'temperature'.
- PhasePlots (30m)
- Volume Rendering (30m)

- Total running time should be roughly 275 minutes, however we have built in
  some buffer time to each of these subsections to help keep things running on
  time. This tutorial can also be cut down for time if necessary. 

## Setup Instructions

yt has wheels available for current versions on pypi and conda-forge. 
We plan on providing a configuration file for learners to create their own
conda environment for reproducible analysis in yt to be distributed with the
lesson materials. This will be supplemented with step-by-step directions on 
how to recreate that environment on their local machine. 
We also plan to provide alternative instructions for learners
who wish to install yt from source, should they wish to do so. 

The yt project also has resources to provide remote environments available to
users with builds of the software and the data that will be used in the
tutorial. We would be willing to set this up if the learners will have access to a
strong internet connection. 

# Relevant links

https://www.scipy2019.scipy.org/tutorials
