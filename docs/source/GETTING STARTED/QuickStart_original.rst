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

**IMAGE #1**
Picture > general schema & openBIS entities schema

**IMAGE #2**
Picture of the ELN menu that shows the Spaces/Projects/Collections 


Story representation via openBIS meta data model entities.

SPACES  

**Clinical Info** to collect information on patients and visits.

**Research Project** to collect information on clinical research projects run by a medical practitioner.

**Materials** to collect information on biological samples extracted from the patients and clinical tests performed. This is present by default in all openBIS instances.

**Methods** to collect information on laboratory protocols used during sample extraction and preparation. This is present by default in all openBIS instances.

**Publications** to collect information on publications related to the clinical projects run by a medical practitioner. This is present by default in all openBIS instances.


PROJECTS

**Patient Info** (under space Clinical Info) > to collect general information on all patients visiting a medical practitioner.

**Patient Visits** (under space Clinical Info) > to collect general information on all visits.

**Genomics NGS based** (under space Research Project) > to collect information on all samples undergoing NGS sequencing as a part of the research project run by a medical practitioner.

**Patient Laboratory Tests** (under space Materials) > to collect information on all samples submitted for laboratory analysis (general blood test).

**Patient Samples** (under space Materials) > to collect information on all bio samples (blood) extracted from the patients.

**Protocols** (under space Methods) > to collect information on all protocols used to extract patients’ samples. This is present by default in all openBIS instances.


COLLECTIONS

**Patients Information** (under project Patient Info) > to collect general information on the patients. 

**Visits Information** (under project Patient Info) > to collect information on the patients’ visits.

**Patient Samples** (under project Patient Sample) > to collect information on the bio samples extracted from the patients.

**Patient Laboratory Tests** (under project Patient Laboratory Tests) > to collect information on the patients’ laboratory tests.

**Plasma small RNA sequencing** (under project Genomics NGS based) > to collect information on the patients’ bio samples submitted for the NGS sequencing.

**Publications Collection** (under project Public Repositories) > stores information on the publications related to the research projects run by a medical practitioner published in Zenodo or the ETH Research Collection via openBIS. This is present by default in all openBIS instances.

**General Protocols** (under project Protocols) > to collect information on the laboratory protocols used to extract patients’ samples. This is present by default in all openBIS instances.

OBJECTS/SAMPLES

**Patient** (under collection Patients Information) > form to store information on a particular patient

**Patient Visit** (under collection Visits Information) > form to store information on a particular visit of the particular patient.  

**Biosample** (under collection Patient Samples) > form to store information on a particular bio sample extracted from the particular patient during a particular visit

**Clinical Test** (under collection Patient Laboratory Tests) > form to store information on a particular, clinical test performed on a particular bio sample of the particular patient 

**General Protocol** (under collection General Protocols) > form to store information on a particular protocol used to prepare a particular bio sample of the particular patient. This is present by default in all openBIS instances.

**Publication** (under collection Publication Collection) > form to store information on papers/datasets published via openBIS to Zenodo or the Research Collection. This is present by default in all openBIS instances.

**Blood Plasma** (under collection Plasma small RNA sequencing) > form to store information on a particular NGS sample prepared from the particular bio sample of the particular patient and submitted for NGS sequencing 

DATA SET

**Raw data** (under object Blood Plasma) > to store the FASTQ files of the sequenced bio samples of the particular patient.


**How the Story was built**
--------------------------

Steps:

1.	Register all Object Types (Level- Instance Admin)
2.	Register all Spaces (Level – Instance Admin)
3.	Register all Projects (Level – Space Admin/Group Admin and up)
4.	Register all Collections (Level – Space User and up)
5.	Register all Samples/Objects (Level – Space User and up)
6.	Upload data set via Web UI (Level – Space User and up)


Each step can be a clickable link with detailed descriptions.

** Register all Object Types** (Level- Instance Admin)

Prior to the registration of the samples/objects, it is necessary to create corresponding object types and properties.
For more details, see also https://openbis.ch/index.php/docs/admin-documentation/new-entity-type-registration/

Let’s register the object type **PATIENT** with its properties.

•	Patient Unique Identifier > unique patient ID
•	Unique center ID > medical center ID
•	Date of birth > dd.mm.yy
•	Gender > male, female
•	Main disease > patient’s primary sickness
•	Secondary disease > patient’s secondary sickness (primary sickness complications)
•	Allergy 

Steps:

Log in to the openBIS admin UI
https://openbis-biomed-demo.ethz.ch/openbis/webapp/openbis-ng-ui/

**IMAGE #3**
openBIS login page

Click on the Object Type (to add an arrow)

**IMAGE #4**
object type view
