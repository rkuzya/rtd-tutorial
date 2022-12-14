Quick Start
===========

**Intro**
---------

openBIS is an open Information System designed to facilitate robust data management for a wide variety of experiment types and research subjects.
It allows tracking, annotating, archiving, and sharing of data in various scientific disciplines.  

The openBIS platform has three primary functionalities:
    1.	**Inventory management** to register samples/extractions/simulations, materials, protocols, equipment.
    2.	**Laboratory notebook** to document scientific projects and experiments.
    3.	**Data management** to store all data related to the scientific projects and experiments (raw, processed, analyzed data, scripts, Jupyter notebooks, etc.).

To represent a scientific study or project, openBIS uses the following meta data model entities:

•	**Space**: a folder (user/group/department/institution based) where  users can organize their projects, studies and corresponding experiments/collections, sample/objects and data sets;
    link How to register space
•	**Project**: a folder where users can organize their experiments/collections, samples/objects and data sets;   
    link How to register Project
•	**Experiment/Collection**: a folder to store the information on experimental or theoretical investigations along with samples/objects and data sets.
    link How to register Experiment/Collection
•	**Object/Sample**: this is the basic entity. An object can be an Experimental Step, and Entry, a Protocol, any type of sample (e.g. bacterium, chemical, wood, plant, battery, etc) or any equipment.
    link How to register Object
•	**Data Set** is a folder where the result/s of the measurement/analysis/modeling of the experimental measurements or analysis are stored. Data sets can be attached to Experiments/Collections or Samples/Objects.
    link How to register Data Set

.. image:: /images/openbis-data-structure.png


**Use Cases - Stories**
----------------------
BIOMED / CLINICAL STORY

Case explanation

A sick patient visits a doctor at the clinic. After collecting certain information on the patient (age, date of birth, secondary diseases and allergies) and the symptoms, the doctor does the general physical checkup, decides on a diagnose, and prescribes the treatment.
To exclude potential complications, the doctor takes a blood sample (following a certain protocol) for the clinical blood test analysis.
The laboratory performs the analysis and submits the results back to the clinic. Additionally, the doctor finds this case interesting and suitable for his medical research project related to the sequencing of the micro RNAs in the blood.
Thus, the medical practitioner submits the blood sample to his research lab where it undergoes NGS sequencing.
The output files (FASTQ) are sent to the research lab for further analysis. 





**How the Story was built**
--------------------------
