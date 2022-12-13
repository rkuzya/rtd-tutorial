Quick Start
===========

Intro
-----

openBIS is an open Information System designed to facilitate robust data management for a wide variety of experiment types and research subjects.
It allows tracking, annotating, archiving, and sharing of data in various scientific disciplines.  

The openBIS platform has three primary functionalities:
    1.	Inventory management, to register samples/extractions/simulations, materials, protocols, equipment.
    2.	Laboratory notebook, to document scientific projects and experiments.
    3.	Data management, to store all data related to the scientific projects and experiments (raw, processed, analyzed data, scripts, Jupyter notebooks, etc.).

To represent a scientific study or project, openBIS uses the following meta data model entities:

•	Space: a folder (user/group/department/institution based) where  users can organize their projects, studies and corresponding experiments/collections, sample/objects and data sets;

•	Project: a folder where users can organize their experiments/collections, samples/objects and data sets;   

•	Experiment/Collection: a folder to store the information on experimental or theoretical investigations along with samples/objects and data sets.

•	Object/Sample: this is the basic entity. An object can be an Experimental Step, and Entry, a Protocol, any type of sample (e.g. bacterium, chemical, wood, plant, battery, etc) or any equipment.

•	Data Set is a folder where the result/s of the measurement/analysis/modeling of the experimental measurements or analysis are stored. Data sets can be attached to Experiments/Collections or Samples/Objects.

.. image:: /images/openbis-data-structure.png

Use Cases - Stories
-------------------





How the Story was built
-----------------------
