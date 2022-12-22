Quick Start
===========

**INTRO**
---------

INTRO: GENERAL INFORMATION ON THE OPENBIS

OpenBIS is an open Information System, designed to facilitate robust
data management for a wide variety of experiment types and research
subjects. It allows tracking, annotating, archiving and sharing of data
throughout distributed research projects in various scientific
disciplines.

The openBIS platform has three primary functionalities:

1. **Inventory management** of laboratory samples, materials, protocols,
   equipment.

2. **Laboratory notebook**, to document lab experiments.

3. **Data management**, to store all data related to lab experiments
   (raw, processed, analysed data, scripts, Jupyter notebooks, etc.).

To represent a study, a project or case, openBIS applies its meta data
model entities such as:

-  **Space** is a folder (user/group/department/institution based) where
   a user/s can represent their projects, studies and corresponding
   experiments/collections, sample/objects and data sets

-  **Project** is a folder where user/s can represent their
   experiments/collections, samples/objects and data sets

-  **Experiment/Collection** is a folder to store the information on an
   experimental or theoretical investigation. The simplest experiment
   would involve just one sample, but, in general, most would include
   many. A typical example of an experiment would be a High Content
   Screening campaign, where the samples are the plates being screened.
   Different types of experiments may make use of data queries that are
   unique to their fields. In order to accommodate these differences,
   openBIS provides a variety of experiment types, such as HCS_CAMPAIGN
   for the example above.

-  | **Sample/Object/Experimental Step** **-** refers to any object that
     has been observed, measured, or compared. It must be uniquely
     identifiable, which means that any two samples must be
     distinguishable from one another. Please note that different use
     cases may use the term "sample" with slightly different meanings,
     dependent upon the context and utility.
   | For example, in one experiment a sample may refer to a biological
     specimen taken from an organism, while in another it could refer to
     a protein extract analyzed in a mass spectrometer. In a third
     experiment, the term "sample" could refer to an individual well in
     a multi-titer plate containing cells of different phenotypes.  Each
     of these cases refers to a different **sample type** in openBIS.

-  **Data Set** – is the result/s of the measurement/analysis/modeling.
   Data sets might have a **file type**, which represents the format
   used to store the data.

.. image:: /images/openbis-data-structure.png


**USE CASES - STORIES**
-----------------------

Current examples of the openBIS usage and its basic functionality have
been represented via 2 hypothetical stories. The stories cover 2
scientific domains: biological, biomedical/clinical and material.


BIOMED / CLINICAL STORY

Case explanation

A sick patient visits a doctor at the clinic. After collecting certain
information on the patient (age, date of birth, secondary diseases and
allergies) and the symptoms, the doctor does the general physical
checkup, decides on a diagnose, and prescribes the treatment. To exclude
potential complications, the doctor takes a blood sample (under a
certain protocol) for the clinical blood test analysis. The laboratory
performs the analysis and submits the results of the clinical test.
Additionally, the doctor finds this case interesting and suitable for
his medical research project related to the sequencing of the micro RNAs
in the blood. Thus, the medical practitioner submits the blood sample to
his research lab where it undergoes NGS sequenced. The output files
(FASTQ) of the sequencing are sent to the research lab for further
analysis.

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image2.png

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image3.png

Story representation via openBIS meta data entities PICTURE TO BE ADDED!!!

**SPACES**

================= =====================================================================================================
Space             Description
================= =====================================================================================================
Clinical info     represents information on patients and their medical visits
Research Project  represents information on clinical research projects run by a medical practitioner
Materials         represents information on biological samples extracted from the patients and clinical tests performed
Methods           represents information on laboratory protocols
Publications      represents information on publications related to the clinical projects
================= =====================================================================================================

**PROJECTS**

======================== ==================================================================================================
Project                  Description
======================== ==================================================================================================
Patient Info             stores general information on all patients
Patient Visit            stores general information on all patients' visit
Genomics NGS based       stores information on all patients' samples undergoing NGS sequencing.
Patient Laboratory Tests stores information on all patients' samples submitted for laboratory analysis (general blood test)
Patient Sample           stores information on all bio samples (blood) extracted from the patients
Protocols                store information on all protocols used to extract patients' samples
======================== ==================================================================================================

**COLLECTIONS**

=========================== =====================================================================================================
Collections                 Description
=========================== =====================================================================================================
Patients Information        stores general information on the patients
Visits Information          stores information in the patients' visits to the doctor
Patient Samples             stores information on the bio samples extracted from the patients
Patient Laboratory Test     stores information on the patients' laboratory tests run on patients' bio samples taken by the doctor
Plasma small RNA sequencing stores information on the patients' bio samples submitted for sequencing
Publications Collection     stores information on the publications related to the research projects run by the doctor
General Protocols           stores information on the laboratory protocols used to extract patients bio samples
Patients Information        stores general information on the patients
Visits Information          stores information in the patients' visits to the doctor
Patient Samples             stores information on the bio samples extracted from the patients
Patient Laboratory Test     stores information on the patients' laboratory tests run on patients' bio samples taken by the doctor
Plasma small RNA sequencing stores information on the patients' bio samples submitted for sequencing
Publications Collection     stores information on the publications related to the research projects run by the doctor
General Protocols           stores information on the laboratory protocols used to extract patients' bio samples
=========================== =====================================================================================================

**OBJECTS / SAMPLES**

================= ================================================================================================================
Objects/Samples   Description
================= ================================================================================================================
Patient           stores information on a particular patient
Patient Visit     stores information on a particular visit of the particular patient
Biosample         stores information on a particular bio sample extracted from the particular patient during a particular visit
Clinical Test     stores information on a particular, clinical test performed on a particular bio sample of the particular patient
General Protocol  stores information on a particular protocol used to prepare a particular bio sample of the particular patient
Publication       stores information on a particular paper used in the research projects run by the doctor
Blood Plasma      stores information on a particular NGS sample prepared from the particular bio sample
================= ================================================================================================================


**DATA SET**

======== =========================================================================================
Data Set Description
======== =========================================================================================
Dataset  stores the FASTQ files of the sequenced particular bio samples of the particular patients
======== =========================================================================================


**HOW THE STORY WAS BUILT**
---------------------------

Steps:

1. Register object types (Level- Instance Admin)

2. Register Spaces (Level – Instance Admin)

3. Register Projects (Level – Space Admin/Group Admin in openBIS HUB

4. Register Collections (Level – Space User and UP)

5. Register Samples/Object of the Objects (Level – Space User and UP)

6. Upload data sets via Web UI (Level – Space User and UP)

Each step can be a clickable link with detailed descriptions.

**Register object types (Level- Instance Admin)**

Prior to the registration of the samples/objects, it is necessary to
create corresponding object types and properties.

Let’s register an object type **PATIENT** with its properties.

-  Patient Unique Identifier > unique patient ID

-  Unique center ID > medical center ID

-  Date of birth > dd.mm.yy

-  Gender > male, female

-  Main disease > patient’s primary sickness

-  Secondary disease > patient’s secondary sickness (primary sickness
   complications)

-  Allergy

Steps:

Log in to the openBIS admin UI

https://openbis-biomed-demo.ethz.ch/openbis/webapp/openbis-ng-ui/

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image4.png


Click on the Object Type (to add an arrow)

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image5.png

Click on a blue ADD button (to add an arrow)

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image6.png

In the new windows, in the section New Object Type provide the following
information (see the picture below).

CODE: PATIENT

Description: Patient’s general information

Generated code prefix: PAT

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image7.png


Click on the **ADD SECTION** Button to create a section for the
properties.

Name the section **General Information**.

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image8.png


Click on the blue triangle then on the **ADD PROPERTY** button.

In the section Property add the following info for the property: Unique
patient ID (see the picture below)

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image9.png

Code: PATIENT_ID

Data Type: VARCHAR

Label: Unique patient ID

Description: unique ID of the patient

TO ADD ANOTHER PROPERTY, CLICK on **ADD PROPERTY** button.

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image10.png


In the section Property add the following info for the property: Unique
center ID (see the picture below)

Code: UNIQUE_CENTER_ID

Data Type: VARCHAR

Label: Unique center ID

Description: Unique Center ID

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image11.png

Click on the SAVE button to save the edits.

Repeat the same procees to register the remaining properties.

**Property: Date of birth**

Code: BIRTH_DATE

Data Type: Date

Label: Date of birth

Description: Date of birth

**Property: Gender**

Code: ADMINISTRATIVE_GENDER

Data Type: CONTROLLED_VOCABULARY

Vocabulary Type: ADMINISTRATIVE_GENDER

Label: Gender

Description: Gender

**SECTION ON HOW TO CREATE A VOCABULARY TO BE ADDED!!!**

**Property: Main disease**

Code: MAIN_DISEASE

Data Type: MULTIPLE_VARCHAR

Label: Main Disease

Description: Main disease diagnosis description.

**Property: Secondary disease**

Code: SECONDARY_DISEASE

Data Type: MULTIPLE_VARCHAR

Label: Secondary Disease

Description: Patient’s secondary sickness (primary sickness
complications)

**Property: Allergy**

Code: ALLERGY

Data Type: MULTIPLE_VARCHAR

Label: Allergy

Description: Patient’s know allergies

**THE SAME PROCESS IS REPEATED to register other object types and
corresponding properties.**

Object Type: PATIENT_VISIT

Properties: to be added

Object Type: BIOSAMPLE

Properties: to be added

Object Type: CLINICAL_TEST

Properties: to be added

Object Type: GENERAL_PROTOCOL

Properties: to de added

Object Type: PUBLICATION

Properties: to be added

Object Type: BLOOD_PLASMA

Properties: to be added

**Register Spaces (Level – Instance Admin)**

Let’s register a space **Clinical Info** in the section Inventory to
represent information on patients and patients’ visits.

Click on Inventory

Click on **+ New Inventory Space** button

In the window: Create Inventory Space type for

Code: CLINICAL_INFO

Description: Information on patients and patients’ visits.

Click on Save button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image12.png

Repeat the same process to register a space **Research Projects** in the
section Lab Notebook/Others to represent information on clinical
research projects run by a medical practitioner.

Use the following information.

Code: RESEARCH_PROJECTS

Descriptions: Information on clinical research projects run by a medical
practitioner.

**The rest of the spaces (Materials, Methods, Publications) should have
been already registered. To be checked.**

**Register Projects (Level – Space Admin/Group Admin in openBIS HUB)**

Let’s register a project **Patient Info** under the space **Clinical
Info** in the section Inventory to represent information on patients.

Click on the space Clinical Info

Click on + New Project button

In the window: Create Project type

Code: PATIENT_INFO

Description: Project to represent information on patients.

Click on Save button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image13.png


**Repeat the same process to register the following projects:**

Project: **Patient Visit**

Location: space **Clinical Info**

Code: PATIENT_VISIT

Description: Project to store general information on all patient’s
visit.

Project: **Patient Sample**

Location: space **Materials**

Code: PATIENT_SAMPLES

Description: Project to store information on all blood samples (blood)
extracted from the patients

Project: **Patient Laboratory Tests**

Location: space **Materials**

Code: PATIENT_LABORATORY_TESTS

Description: Project to store information on all patients’ samples
submitted for laboratory analysis (general blood test).

Project: **Protocols**

Location: space **Methods**

Code: PROTOCOLS

Description: Project to store information on all protocols used to
extract patients’ samples.

Project: **Genomics NGS based**

Location: space **Research Projects**

Code: GENOMICS_NGS_BASED

Description: Project to store information on all patients’ samples
undergoing NGS sequencing procedure as a part of the research project
conducted by the medical practitioner.

**Register Collections (Level – Space User and UP)**

Let’s register a collection **Patient Information** under the project
**Patient Info**, space **Clinical Info** in the section Inventory to
store information on the patients.

Click on the project **Patient Info**

Click on **+ New** button

Choose **Collection**

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image14.png


In the window: Create Collection type the following

Code: PATIENT_INFORMATION

Name: Patient information

Default object type: Patient

Default collection view: Form view

Click on Save button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image15.png


**Repeat the same process to register the following collections:**

Collection: **Visits information**

Location: space **Clinical Info**

Code: VISITS_INFORMATION

Name: Visits information

Default object type: Patient Visit

Default collection view: Form view

Collection: **Patient sample**

Location: space **Materials**

Code: PATIENT_SAMPLE

Name: Patient sample

Default object type: Biosample

Default collection view: Form view

Collection: **Patient laboratory test**

Location: space **Materials**

Code: PATIENT_LABORATORY_TEST

Name: Patient laboratory test

Default object type: Clinical Test

Default collection view: Form view

Collection: **General Protocols**

Location: space **Methods**

Code: GENERAL_PROTOCOLS

Name: General protocols

Default object type: General Protocol

Default collection view: Form view

Collection: **Publications Collection**

Location: space **Publication**

Code: PUBLICATIONS_COLLECTION

Name: Publications collection

Default object type: Publication

Default collection view: Form view

Collection: **Plasma small RNA Sequencing**

Location: space **Research Project**

Code: PLASMA_SMALL_RNA_SEQUENCING

Name: Plasma small RNA sequencing

Default object type: Blood Plasma

Default collection view: Form view

**Register Samples/Object of the Objects (Level – Space User and UP)**

Let’s register an object **PATIENT** in the collection **Patients
information**, project **Patient Info**, space **Clinical Info**.

Click on the Patients information collection

Click on **+ New Patient** button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image16.png


In the window: New Patient type the following

Code: nothing to type in. Will be automatically generated.

Patient Unique Identifier: 001

Unique center ID: 12345

Date of birth: 01.01.1970

Gender: male

Main disease: diabetes type 1 

Secondary disease: chronic kidney disease

Allergy: pollen, animal dander

Click on Save button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image17.png


Let’s register another object PATIENT VISIT in the collection **Visits
information**, project **Patient Visit**, space **Clinical Info**.

Click on the **Visits information** collection

Click on **+ New Patient Visit** button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image18.png


In the window: New Patient Visit type the following

Code: nothing to type in. Will be automatically generated.

Date of visit: 10.05.2022

Practitioner visiting the participant: Mark Shulz

Body weight (kg.): 80

Blood pressure: 140.80

Body temperature (Cel.): 36.9

Heart rate (per min): 95

Respiratory rate (per min.): 20

Oxigen saturation (%): 98

Problem condition: tiredness, Irritation, often night urination

Diagnosis (if applicable): urinary tract infection (UTI)

Treatment: Nitrofurantoin 1 t/day 7 days

Click on Save button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image19.png

**Repeat the same process to register the following objects:**

Object: **BIOLSAMPLE**

Location: collection **Patient sample,** project **Patient Samples**,
space **Materials**.

Patient Unique Identifier: 0001

Sampling institution: USZ

Date of sampling: 2022-09-12

Unique Identifier of the specimen (primary sample): 0001_1205_001

Volume of the specimen (primary sample) in ml:10

Type of the sample: Liquid

Object: **Clinical Test**

Location: collection **Patient laboratory test,** project **Patient
Laboratory Tests**, space **Materials**.

In the text field, you can paste the following information:

**Blood Test Results. 21.09.2022**

| Patient ID: 987654321 Status: Routine
| Ordering Dr: Smith, Peter MD Physician Copy for: Smith, Jane MD
| SPEC #: 223456 Collection Date/Time: 02/10/14 14:30
| Received Date/Time: 02/10/14 15:00
| SPECIMEN: Whole blood
| ORDERED: Complete Blood Count and White Blood Cell Differential
| QUERIES: [Comments and testing instructions]
| Test Normal Abnormal Flag Units Reference Range
| COMPLETE BLOOD COUNT
| White Blood Cell (WBC) 6.9 K/mcL 4.8-10.8
| Red Blood Cell (RBC) 1.8 L M/mcL 4.7-6.1
| Hemoglobin (HB/Hgb)) 6.5 L*\* g/dL 14.0-18.0
| Hematocrit (HCT) 19.5 L*\* % 42-52
| Mean Cell Volume (MCV) 109.6 H fL 80-100
| Mean Cell Hemoglobin (MCH) 36.5 H pg 27.0-32.0
| Mean Cell Hb Conc (MCHC) 33.3 g/dL 32.0-36.0
| Red Cell Dist Width (RDW) 16.0 H % 11.5-14.5
| Platelet count 180 K/mcL 150-450
| Mean Platelet Volume 7.9 fL 7.5-11.0
| WBC Differential
| Neutrophil (Neut) 50 % 33-73
| Lymphocyte (Lymph) 36 % 13-52
| Monocyte (Mono) 8 % 0-10
| Eosinophil (Eos) 5 % 0-5
| Basophil (Baso) 1 % 0-2
| Neutrophil, Absolute 3.5 K/mcL 1.8-7.8
| Lymphocyte, Absolute 2.5 K/mcL 1.0-4.8
| Monocyte, Absolute 0.6 K/mcL 0-0.8
| Eosinophil, Absolute 0.4 K/mcL 0-0.45
| Basophil, Absolute 0.1 K/mcL 0-0.2
| Flag Key: L= Abnormal Low, H= Abnormal High, \**= critical value
| Comment: \**Hgb of 6.5 and Hct of 19.5 reported to Dr. J Smith at
  15:20 on 2/10/14 by M. Peters

Object: Blood Plasma

Location: collection Plasma small RNA Sequencing, project Genomics Ngs Based, space Research Projects, Lab Notebook

Patient Unique identifier: 0001

Name: 0001_1205_001

Supplier: BioMed Sample Laboratory


LINKING OBJECTS VIA PARENT-CHILD RELANTIONSHIPS

Let’s link the newly created objects via the parent-child relationships.

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image20.png


The object PAT1 (patient) in the collection Patients information will be
a parent of the object PAN_VISIT1 (patient’s visit) in the collection
Visits information.

Click on the collection Visits information

Click on the object PAN_VISIT1

Click on Edit Button in the PAN_VISIT1 view mode

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image21.png


Scroll down to the section **Parents** and click on **Search Any**
button

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image22.png


Choose the **Patient** object type in the scroll down menu

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image23.png


Type PAT1 in the text field underneath the Search Any button

Choose the PAT1 object in the dropdown menu.

.. image:: /vertopal_7815620a208e47a0995d07a240c3174d/media/image24.png


Click on +Add

Save

The objects PAN_VISIT1 (patient’s visit) in the collection Patients
information and the object GEN1 (general protocol) will be the parent of
the object SAM1 (biosample) in the collection Patient sample.

Click on the collection Patient sample

Click on the object SAM1 (biosample)

Click on Edit Button in the SAM1 view mode

Scroll down to the section **Parents** and click on **Search Any**
button

Choose the **Patient Visit** object type in the scroll down menu

Type PAN_VISIT in the text field underneath the Search Any button

Choose the PAN_VISIT1 object in the dropdown menu

Click on +Add

Save

**Upload data sets via Web UI (Level – Space User and UP)**

Info + screenshots

Use your openBIS credentials to log into the openBIS user UI.

Click on

**MATERIAL STUDY STORY**

Case explanation …

Picture > general schema & openBIS entities schema

openBIS meta data entities used the case

Spaces >

Projects >

Collections >

Samples >

Data Sets >

**CLICK > HOW THE STORY WAS BUILT <**

**2 - TECHNICAL EXPLANATIONS ON HOW THE STORY WAS DEVELOPED IN THE
OPENBIS (quick way)**

**BioLab Example**

1. Register all collection and object types for the case (permission
   Level - Instance Admin)

2. Register Spaces (one by one) (permission level – Space Admin / Group
   Admin in openBIS hub and UP)

3. Register Projects (one by one) (permission level – Space User and UP)

4. Register Collections (one by one) (permission level – Space User and
   UP)

5. Register Objects/Samples/Experimental Steps (permission level – Space
   User and UP)

6. Upload Data Sets via Web UI

**Biomedical/Clinical Example**

1. Register all collection and object types for the case (permission
   Level - Instance Admin)

2. Register Spaces (one by one) (permission level – Space Admin / Group
   Admin in openBIS hub and UP)

3. Register Projects (one by one) (permission level – Space User and UP)

4. Register Collections (one by one) (permission level – Space User and
   UP)

5. Register Objects/Samples/Experimental Steps (permission level – Space
   User and UP)

6. Upload Data Sets via Web UI

**Material Studies Example**

1. Register all collection and object types for the case (permission
   Level - Instance Admin)

2. Register Spaces (one by one) (permission level – Space Admin / Group
   Admin in openBIS hub and UP)

3. Register Projects (one by one) (permission level – Space User and UP)

4. Register Collections (one by one) (permission level – Space User and
   UP)

5. Register Objects/Samples/Experimental Steps (permission level – Space
   User and UP)

6. Upload Data Sets via Web UI

.. |Diagram Description automatically generated| image:: vertopal_7815620a208e47a0995d07a240c3174d/media/image2.png
   :width: 3.01852in
   :height: 1.69792in
.. |image1| image:: vertopal_7815620a208e47a0995d07a240c3174d/media/image3.png
   :width: 2.82292in
   :height: 1.58789in
