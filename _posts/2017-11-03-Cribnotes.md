---
title: "Cribnotes for Principles of Health Informatics"
excerpt: "Principles of Health Informatics UCL CHMEGH23"
header:
  teaser: "http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"
tags:
  - UCL
  - Health Informatics
  - Notes
---
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Webinar!](#webinar)
	- [Controlled clinical terminologies](#controlled-clinical-terminologies)
		- [ICD-10](#icd-10)
		- [SNOMED CT](#snomed-ct)
		- [National Approaches to IT implementation](#national-approaches-to-it-implementation)
			- [National Programme for IT](#national-programme-for-it)
			- [HITECH](#hitech)
				- [Meaningful use](#meaningful-use)
				- [Result](#result)
				- [HITECH Requirements](#hitech-requirements)
					- [Core Requirements:](#core-requirements)
					- [Menu Requirements:](#menu-requirements)
	- [Ontologies](#ontologies)
					- [Entity Relationship Models](#entity-relationship-models)
					- [Decision analysis](#decision-analysis)
				- [Diagnostic tests](#diagnostic-tests)
	- [Procurement processes](#procurement-processes)
		- [Personal health records & EHR](#personal-health-records-ehr)
			- [HealthSpace](#healthspace)
			- [Key theme 1- Health records](#key-theme-1-health-records)
	- [Telehealth](#telehealth)
		- [Whole System Demonstrator](#whole-system-demonstrator)
		- [Florence or “flo”](#florence-or-flo)
	- [Cost effectiveness](#cost-effectiveness)
		- [Choose & Book/eRS](#choose-bookers)
- [Dataflow Diagrams](#dataflow-diagrams)
- [Record Linkages](#record-linkages)

<!-- /TOC -->

# Webinar!
Description logic in snomed? Not sure if this makes any sense but it’s all I can find

SNOMED CT consists of four primary core components:
Concept Codes – numerical codes that identify clinical terms, primitive or defined, organized in hierarchies
Descriptions – textual descriptions of Concept Codes
Relationships – relationships between Concept Codes that have a related meaning
Reference Sets – used to group Concepts or Descriptions into sets, including reference sets and cross-maps to other classifications and standards.
SNOMED CT's relational statements are basically triplets of the form Concept1 – Relationx – Concept2, with Relationx being from a small number of relation types (called linkage concepts), e.g. finding site, due to, etc. The interpretation of these triplets is (implicitly) based on the semantics of a simple Description logic (DL). E.g., the triplet Common Cold – causative agent – Virus, corresponds to the first-order expression

Record keeping standards
solve the problems of ambiguity and redundancy in medical records.
standardised

1. The patient’s complete medical record should be available at all times during their stay in hospital.
2. Every page in the medical record should include the patient’s name, identification number (NHS number) and location in the hospital.
3. The contents of the medical record should have a standardised structure and layout.
4. Documentation within the medical record should reflect the continuum of patient care and should be viewable in chronological order.
5. Data recorded or communicated on admission, handover and discharge should be recorded using a standardised proforma.
6. Every entry in the medical record should be dated, timed (24 hour clock), legible and signed by the person making the entry. The name and designation of the person making the entry should be legibly printed against their signature. Deletions and alterations should be countersigned, dated and timed.
7. Entries to the medical record should be made as soon as possible after the event to be documented (e.g. change in clinical state, ward round, investigation) and before the relevant staff member goes off duty. If there is a delay, the time of the event and the delay should be recorded.
8. Every entry in the medical record should identify the most senior healthcare professional present (who is responsible for decision making) at the time the entry is made.
9. On each occasion the consultant responsible for the patient’s care changes, the name of the new responsible consultant and the date and time of the agreed transfer of care, should be recorded.
10. An entry should be made in the medical record whenever a patient is seen by a doctor. When there is no entry in the hospital record for more than four (4) days for acute medical care or seven (7) days for long-stay continuing care, the next entry should explain why.
11. The discharge record/discharge summary should be commenced at the time a patient is admitted to hospital.
12. Advance Decisions to Refuse Treatment, Consent, Cardio-Pulmonary Resuscitation decisions must be clearly recorded in the medical record. In circumstances where the patient is not the decision maker, that person should be identified e.g. Lasting Power of Attorney.



## Controlled clinical terminologies

A controlled clinical terminology is a system which allows the regulated and constrained expression of clinical concepts eg SNOMED CT, ICD-10

Varies in 3 ways

* single v multiple hierarchies
* fixed v variable depth
* compositional v enumerative


* Enumerative – a list of everything you might want to represent, with a separate symbol identified for each item eg ICD-10
* Compositional – symbols corresponding to core concepts are combined with modifiers and qualifiers eg combine acute bacterial with septicaemia to represent acute bacterial septicaemia SNOMED CT
* Interoperability – have a common standard and understanding of terms

### ICD-10
Originally designed to code cause of death

enumerative, single hierarchy, fixed depth

22 chapters

for each code there is a definition, diagnostic guidelines, inclusion criteria and exclusion criteria

issues – limited scope ‘classification of diseases’, constrained structure makes it hard to update, use of not specified/not elsewhere classified, one disease not in two categories breast cancer is a cancer not a disease of the breast (arbitrary choices of category)

### SNOMED CT

Systematised nomenclature of medicine

Unique id, description, definition, compositional logic, combinatorial

The basic unit of SNOMED CT is the concept

Each concept is given a unique identifier and a set of descriptions. A unique numerical code assigned to each concept.

Issues – pre and post coordinated concepts, situations with explicit context, representing parts and wholes, size long lists of concepts, natural language processing

Post coordination – allows users to specify new meaning by referencing existing SNOMED CT concepts – building on existing concepts

Situations with explicit context – the definition of the concept has a context that modifies the original concept eg diabetes mellitus a situation with no explicit context. Family history of diabetes mellitus = situation with explicit context.

Structure, entire, part triples. SNOMED CT represents anatomical structures as parts of the structure (P) (eg parts of the heart – the aorta, the pulmonary artery, the myocardium), the entire structure (E) (the heart) and one that subsumes both (S) (parts of the heart plus the entire structure). Distinguishes between injury to specific part of an anatomical structure (hole in the aorta) and the whole structure (cardiac arrest). Advantage – specific. Disadvantage – can be miscoded.



### National Approaches to IT implementation
#### National Programme for IT

Established in 2002.

1 April 2005, NHS Connecting for Health formed to deliver the programme
Contracts for the Spine and five clusters awarded in December 2003 and Jan 2004
Patients access records through “HealthSpace”
Huge cost, withdrawal and sacking of two of the four IT providers
Expected to cost £2.3 Bn over three years
By June 2006, National Audit Office estimated cost to be £12.4bn over 10 years
Other predictions - cost overrun from 440% to 770%
Programme could not  demonstrate that the financial benefits would exceed cost of programme
- Five clusters
- Southern
- London
- East and East Midlands
- North West and West Midlands
- North East

 - Different Local Service Provider contracted for each cluster
 - July 2007, accenture withdrew from their 2 clusters.
- May 2008, fujitsu contract terminated
- BT Health London (formerly BT Capital Care Alliance) – London cluster
- Computer Sciences Corporation (CSC) – North, Midlands & Eastern (NME) cluster
- Accenture had full responsibility for the North East and East/East Midlands clusters until January 2007, when it handed over the bulk of its responsibilities to the CSC, retaining responsibility for Picture archiving and communication system (PACS) rollout only.
- Fujitsu – had responsibility for the Southern cluster until May 2008 when their contract was terminated.Most of their responsibilities were subsequently transferred to BT Health except for PACS which was transferred to the CSC Alliance.

- Some deliverables
  - NHS Care Records Service (NCRS) or Lorenzo
  - Store patient health care records on computers that will link together. Need a credit card sized plastic card with an electronic chip, name of user and unique user identity number.
    - Is this now the Summary Care Record?? I think they are separate things.
  - NHS electronic prescription service
  - Choose and Book
  - New National Network N3
  - Secure broadband network
   - Terminated march 2017
   - Replaced by Health and Social Care Network
  - Picture Archiving and communication system
  - Quality Management and Analysis System
    - Ended 2012, replaced with Calculating Quality Reporting Services and Quality and Outcomes Frameworks performance management and payment of GPs
  - NHS mail
  - The Spine - used by NHS Care Record Service
   - Personal Demographics Service - stores demographic infor about patients
   - Cannot opt out
  - Summary Care Record - summary of clinical information, allergies and adverse reactions to medicine
  - Secondary Uses Service- data from patient records for business reports and statistics for research, planning and public health delivery.
- Reasons for failure
 - Little functionality
 - Inadequate security and patient privacy
 - Reservations of staff
 - Programme failed to engage clinicians
 - For many staff, benefits are theoretical
 - IT providers
  - Vast amount of risk associated with project to service providers
  - When accenture withdrew, Granger (NPfIT head) did not use clauses in contracts, Accenture did not have to pay £930m for contract breach
  - ISOFT
   - Irregular accounting
   - Acquired by CSC
  - Staff not trained
  - Could not access vital data on patients
  - Enfield PCT : system did not flag up possible child abuse victims
   - Massive amount of manual amending records
  - Poor clinical buy-in
  - Top down
  - Large central contracts
  - Systems were imposed
  - Political interference
#### HITECH
Health Information Technology for Economic and Clinical Health Act

- USA spending $25.9 billion to promote and expand health information technology - economic stimulus project - high update
- Meaningful use of interoperable EHR adoption
- $63,750 to those who adopt and use “certified EHRs” over 6 years from 2011
- Those who do not by 2015 will be penalized 1% of medicare payments, increasing to 3% over 3 years
##### Meaningful use
- The use of a certified EHR in a meaningful manner, such as e-prescribing.
- The use of certified EHR technology for electronic exchange of health information to improve quality of health care.
- The use of certified EHR technology to submit clinical quality and other measures.
- Stage 1 finalised in July 2010
- 25 objectives and measures for eligible providers
- 24  objectives and measures for eligible hospitals
- Divided into core (have to meet all) and menu (have to meet 5 of 10)
- Pretty vague
- Stage 2 finalised in August 2012
- Encourage use of health IT for continuous quality improvement at point of care and exchange of information in structure format
##### Result
- Bulk of organisations bought EPR  - comprehensive integrated system that provide a wide range of EHR functionality
- Probably not actually good value for money
- Stifled innovation, certain players have benefitted and cemented their position. Unlikely to have new participants
- Barriers to EHR adoption and meaningful use
- Cost
- Lack of knowledge
- Workflow challenges
- Lack of interoperability
- Downstream effects unknown
- Is the meaningful use system actually effective?

##### HITECH Requirements
###### Core Requirements:
1. Use computerized order entry for medication orders.
2. Implement drug-drug, drug-allergy checks.
3. Generate and transmit permissible prescriptions electronically.
4. Record demographics.
5. Maintain an up-to-date problem list of current and active diagnoses.
6. Maintain active medication list.
7. Maintain active medication allergy list.
8. Record and chart changes in vital signs.
9. Record smoking status for patients 13 years old or older.
2. Implement one clinical decision support rule.
2. Report ambulatory quality measures to CMS or the States.
2. Provide patients with an electronic copy of their health information upon request.
2. Provide clinical summaries to patients for each office visit.
2. Capability to exchange key clinical information electronically among providers and patient authorized entities.
2. Protect electronic health information (privacy & security)


###### Menu Requirements:
2. Incorporate clinical lab-test results into certified EHR as structured data.
2. Implement drug-formulary checks.
2. Generate lists of patients by specific conditions to use for quality improvement, reduction of disparities, research, and outreach.
2. Send reminders to patients per patient preference for preventive/ follow-up care
2. Provide patients with timely electronic access to their health information (including lab results, problem list, medication lists, allergies)
2. Use certified EHR to identify patient-specific education resources and provide to patient if appropriate.
2. Perform medication reconciliation as relevant
2. Provide summary care record for transitions in care or referrals.
2. Capability to submit electronic data to immunization registries and actual submission.
2. Capability to provide electronic syndromic surveillance data to public health agencies and actual transmission.



## Ontologies

A data model that represents knowledge as a set of concepts (the things) within a domain (a particular subject) and the relationship between these concepts (things).

E.g. medicine ontology - concepts such as “heart attack” relationship between “Heart Attack” and synonyms, the organ “heart”, things that affect the “heart”.
E.g. Disease ontology - concepts e.g. Disease, disease classifications, symptoms, treatments.

From the greek onto (existence or being real) and logia (science or study). In philosophy ontology is the study of what exists. In non-philosophy it is the description of what exists specifically within a determined field.

An ontology is a representation of the concepts and relationships that need to be modelled in order to represent a particular domain. Eg 1. gene ontology which is a bioinformatics initiative to unify the representation of gene and gene products 2. Autism spectrum disorder phenotype (Thank you Merwaan) - an ontology that can be used 1) to provide improved access to the data collected by those who study ASD and other neurodevelopmental disorders, and 2) to assess and compare the characteristics of the instruments that are used in the assessment of ASD


Classes (are a type of thing, e.g. People. Classes and subclasses form a hierarchical taxonomy e.g. Fruit - Pome - Apple. The members of a subclass inherit the characteristics of their parent class so Apples “is a” type of Pome and “is a” type of fruit)

Properties - relate members of one class to another class. “(class)Child (property)hasFather (class)Father”


“Todd” is an instance of class “person” and “Company Inc” is an instance of class “organisation”


###### Entity Relationship Models
Entity is an object or concept about which you want to store information. Eg patient.
Actions or relationship shows how two entities share information.
Attributes are unique distinguishing characteristics of the entity. Eg patient - age.
###### Decision analysis

Decision trees: Associate each outcome with a value or utility (dotted square)
Calculate probability of each outcome (square underneath name)
<figure>
 <a href="/assets/images/decision1.jpg"><img src="/assets/images/decision1.jpg"></a>
</figure>


Then calculate the “expected utility” which is the utility of an outcome multiplied by its probability (circle)
<figure>
 <a href="/assets/images/decision1.jpg"><img src="/assets/images/decision2.jpg"></a>
</figure>
Add up all the circles to get the “expected utility for each decision option
<figure>
 <a href="/assets/images/decision1.jpg"><img src="/assets/images/decision3.jpg"></a>
</figure>
Combined
<figure>
 <a href="/assets/images/decision1.jpg"><img src="/assets/images/decision4.jpg"></a>
</figure>
<figure>
 <a href="/assets/images/decision1.jpg"><img src="/assets/images/decision5.jpg"></a>
</figure>
==>
<figure>
 <a href="/assets/images/decision1.jpg"><img src="/assets/images/decision6.jpg"></a>
</figure>

1. Uses:
  - Basically decisions of any kind
1. Problems:
  - Where you get the numbers from ( lack of data)
  - May not accurately model the process

##### Diagnostic tests

|With disease	|Without disease
---|---|---
Positive|	a|		b
Negative| 	c|	d

Sensitivity = a / (a + c)  number of positive tests with disease / number of people with disease

Specificity = d / (b + d) number of negative tests without disease / number of people without disease

Positive predictive value = a / (a + b) number of positives with disease/ number of positives

Negative predictive value = d / (c + d) number of negatives without disease / number of negatives


## Procurement processes
1. In the NHS:
  - Equal treatment - all vendors must have equal opportunity to compete for a contract
  - Transparent decision making
  - Non-discrimination
  - Open tender: - make an announcement and then “Request for Proposal”
  - Closed tender- make an announcement, then “Request for information” from potential candidates, selected candidates are allowed to “Request for Proposal”.


 - Selection team
  - Developing of an evaluation schema
  - Evaluating vendors
  - Selecting the system
  - Negotiating the contract
  - Establishing a relationship with vendor
- Criteria :
  - Monetary
  - Cost to change
  - Cost to create
  - Cost to end
  - Cost to open
  - Cost effectiveness
  - Qualitative
  - System fit for purpose
  - Extended economical analysis

### Personal health records & EHR

Personal health record is a collection of health data and information related to the care of a patient which is maintained and accessed by the patient.  Eg HealthVault and Patients Know Best

Electronic health record is a collection of patient and population health data stored in a digitised format accessed and maintained by clinicians. Eg
1. GP The Spine record
2. Estonia e-Health EHR.
Nationwide EHR system. 95% of health data is digitised. Also have e-Prescription. Organised through a individual health card.

**Advantages to PHR** - the NHS is hopeless at having an integrated medical record. Patient maintained might have more detail. People move country so PHR are more complete.

**Microsoft HealthVault web based PHR**. USA Oct 2007. UK 2010. Store and maintain health and fitness information. Parent can manage child’s account. Can be shared with anyone. Blood pressure. Monitors. Heart rate. Microsoft band. Direct competition with Apple’s HealthKit.

#### HealthSpace
The HealthSpace website was operated by the English National Health Service for patients to record blood pressure, blood sugar levels and other medical data. It was also the portal for the patient to view their Summary Care Record and for making hospital appointments. In December 2012 the service was shut down due to lack of interest. In April 2013 all HealthSpace Data was destroyed in order to comply with the Data Protection Act.

**Patients know best**. British social enterprise. Aim - put patients in control of their own medical records. Integrates into the nhs connecting for health network to provide patients with tools to work with clinicians. Direct engagement with clinicians.

#### Key theme 1- Health records
1. Personal Health Record (PHR): a collection of health data and information related to the care of a patient which is maintained and accessed by the patient.
1. Electronic Health Record (EHR): collection of patient and population health data stored in a digitized format accessed and maintained by clinicians.
1. Benefits of PHRs
 - Allows patients access to a wide range of info and knowledge
 - Ease of access- all info/data in one place for patient to see
 - Can help clinicians- submit data for clinicians to see, continuous updates
 - Identify early risk factors for disease
2. Downsides of PHRs
 - Digital divide (accessibility)- may exclude some patients who are not tech savvy
 - Security and privacy concerns i.e. accidental disclosure, inside/outside intrusion
 - Functionality concerns- data entry, validation, info display
3. Benefits of EHRs
 - Improves efficiency, quick access to data, data sharing
 - Financial incentives
 - Streamlined coding & standardised practice throughout entire healthcare system
 - Privacy and security enhancement
 - Reducing costs and labour through less paperwork
1. Downsides of EHRs
 - Training clinicians to use system can be time consuming; may interpret coding in different ways
 - Some privacy issues- protocol may not be adhered to, ransomware etc
 - Converting from paper to digital can be a lengthy process
 - Initial outlay for system and set up can be expensive



## Telehealth
Telehealth is the remote exchange of data between a patient and/or their clinician(s) to assist in diagnosis/monitoring/treatment. Typically used to support patients with long term conditions.

Eg **Whole System Demonstrator** and **Florence**
### Whole System Demonstrator
- “DoH cherry picked unanalysed data” (Greenhalgh 2012)
substantial mismatch between [Nuffield trust paper] findings and conclusions (which were measured and cautious) and those used by the Department of Health to inform policy (which were one sided and sensationalist),
largest randomised control trial of telehealth and telecare in the world
- 6191 patients, 238 GP practices across three sites, Newham, Kent and Cornwall.
- According to the Official report
  - If properly delivered, telehealth can substantially reduce mortality, need for admissions to hospitals, lower number of bed days spent in A&E and reduce the time spent in A&E
  - 3 million people with long term conditions and/or social care needs could benefit from telehealth/telecare
 - 45% reduction in mortality rates
 - 20% reduction in emergency admissions
 - 15% reduction in A&E visits
 - 14% reduction in elective admissions
 - 14% reduction in bed days
 - 8% reduction in tariff costs
- Telehealth-active participation of patients to measure vital signs
- Telecare - monitors without need for patient input
 - From WSD, came the three million people programme where telehealth/care would be extended from 2012 to 2017.
  - Abandoned in November 2013.
  - In September 2014, NHSE announced a new “technology enabled care services programme”


### Florence or “flo”
- Mobile phone text service ‘SMS’ to communicate with the patient directly
- Flo reminds patients to collect readings and text them back
- Flo can then record the readings and display them
- Flo can send alerts if patient’s readings look wrong or show worrying trends
- Allows patients to take readings at their convenience
- Personalised health tips and medication reminders based on readings
- Patient becomes more involved and take more responsibility for their own healthcare
- Uses
  - It can be used for any condition where the patient at home might benefit from motivation and prompting; questions or education; or reporting symptoms and home measurements
   - Heart Rate
   - Temperature
   - Weight
   - Medication
   - Blood pressures
   - Blood oxygen
   - Stress
   - Urine tests
   - Exercise reminders
   - Blood glucose
   - Smoking cessation
   - Results
   - Top "Digital" accolade at NHS Sustainability Awards 2017
   - improved satisfaction with patient / nurse care
   - compliance with medication and appointment reminders, reduction in DNA rates
   - improved physical health and mental well being
   - patient led focus
   - patients’ lives no longer revolve around provision of services

## Cost effectiveness
### Choose & Book/eRS
- Need list of all services available at a trust
- Definition different in different Trust’s Patient Administration Systems
- Definition of clinics defined in a variety of ways
- C&B creating a new system and a requirement for a level of interoperability between the new and old systems
- Choice and Capacity
- Booked admissions
- Proposed as way of dealing with limited capacity
- However:
 - Choice requires additional capacity
 - Conventional system, doesn’t book far ahead, so patient told in July that appointment is in July
 - New system, gp seeing patient in march has to have knowledge of when suitable appointment slots is, (e.g. july)
 - Hard to guarantee this with variable hospital lengths of stay, emergency admissions, cancellations etc.
 - Can only guarantee IF there is spare capacity
 - Supposed to reduce DNA rates. Evidence suggests this is not the case.
 - Choice due to political interference
 - Choice is considered good,
 - Allows patients to avoid poor providers who will have to adapt
 - However
 - Patients go to clinicians looking for care, to be offered a choice isn’t necessarily to be looked after
- From Choose and Book
 - Patients didn’t feel they had a choice
 - Those who didn’t use C&B felt that they had a choice
 - Could drive up standards
 - Would require patients to be able to make an informed choice and actually they can’t due to availability of accurate and useful information on the quality of hospitals
 - Information is too partial, collected at wrong level or over the wrong timescales to give patients a clear idea of what their experiences would be
 - Reasons for failure
 - Assumed patient is rational chooser, that giving a patient statistical information on “quality” of services will prompt the “right” choices and lead to the “best” services winning in a competitive market.
 - Top down process of change are unpopular. Resulting lack of take up seen by the “top” as due to resistance which is a barrier to overcome through incentives or coercion
 - C&B actually against healthcare staff’s legitimate ideas about how to deliver high quality clinical care
 - Four foci of intelligible resistance
 - Healthcare staff resisted policy of choice built into C&B.
 - Staff did not offer choice or presented as external requirement and presented as an absurd situation
 - Resisted practical consequences of system’s poor functionality
 - System cumbersome, unreliable, time consuming.
 - Took twice as long as manual
 - Doctor’s sense that the system prevented them from using more personal knowledge
 - Either accrued through their practice as professionals, deals with individual patients and locally available services, transport services, expertise and interests of consultants
 - GPs felt this knowledge super important. Not avaliable on C&B
 - System alter roles and relationship in consultation
 - Appointment booking by GPs seemed inappropriate and indicate loss of status.


# Dataflow Diagrams



# Record Linkages
- Definition: merging two or more datasets together


- **Probabilisti**
  - Match them on a range of criteria and assign weighting on different criteria and calculate a probability. Only link if it crosses a threshold
- Advantages
  - Link more diverse range of data sets
  - Deals with missing data better
  - More practical
- Disadvantages
  - Sketchy
  - Depends on threshold
  - Never be perfect


- **Deterministic** (Rule based)
 - Have a unique identifier and you can link patients directly and you know that it’s them
- Advantages
  - Easier
  - More certain
- Disadvantages
  - Typos
  - Limited data you can use
  - Has to have a unique identifier
  - Perhaps identifiable
  - Missing values/ partial agreements

- **Endeavour project in East London**
  - Basically a system to merge primary and secondary data
  - Collaboration between four boroughs
   - Newham
   - Tower hamlets
   - City and hackney
   - Waltham forest
  - Two Hospitals
   - Homerton University Foundation Trust
   - Barts Health Trust
 - Part of “systems infrastructure” served by East London Patient Record
 - Gets all Data into one place and links GP and hospital data in line with clinical research and planning principles
 - Share read only patient records
 - Clinicians are data controllers
 - Benefits
 - Engender citizen confidence - through integrated data resource that facilitates the development of patient access and patient facings apps
 - Reports on whole populations along full pathways of care
 - Enabling identification and measurement of outcomes of interventions across primary and secondary care
 - Access to real time clinical data (primary and secondary) collected at point of care




 - To facilitate extensive clinical audits and research
 - Both standard term and strict definition. Standard term for interoperability, strict definition for classification of the terms
 - It’s too complicated. To input codes, requires automation and an appropriate Electronic Health Record as well as sufficient training for staff to understand the intricacies of the system, the SEP, situation with explicit context etc.

- Controlled clinical terminology is a system which allows the use of regulated and constrained expression of clinical terms. They are used to code clinician terms for secondary uses such as payment, statistical reporting, decision-making, measurement of outcomes and performance. Also allows for interoperability between different EHRs
- Snomed vs ICD is compositional vs enumerative –
 - Compositional
  - Advantages
   - Granularity
   - Scope
   - Post coordination
  - Disadvantages
   - Combinatorial explosion
   - Complex








Record linkage – is the task of finding records in a dataset that refer to the same entity across different datasets. Record linkage is necessary when joining datasets based on entities that may or may not share a common identifier. Ie connecting patient level information to obtain a better understanding of health condition or treatment. Eg linking mental health and primary or secondary care records based on pseudonymised NHS numbers. This would need to take place in a DSCRO (Data Services for Commissioners Regional Office).

Rule-based or deterministic record linkage generates links based on the number of individual identifiers that match among the available datasets ie some or all identifiers are identical binary matches – eg pseudonymised NHS no. encounter id

Probabilistic record linkage or fuzzy matching linkage by taking into account a wider range of potential identifiers, computing weights for each identifier based on its estimated ability to correctly identify a match or non-match, and using these weights to calculate the probability that two given records refer to the same entity.

-       Missed matches vs false matches. Accuracy of fuzzy matching is questionable.
Issues patients may be identifiable (numbers below thresholds should be controlled)

Definitions we might want to just learn off

**A controlled clinical terminology is a system which allows the regulated and constrained expression of clinical concepts

An ontology is a representation of the concepts and relationships that need to be modelled in order to represent a particular domain.

Personal health record is a collection of health data and information related to the care of a patient which is maintained and accessed by the patient.

Electronic Health Record is a collection of patient and population health data stored in a digitised format accessed and maintained by clinicians

Telehealth is the remote exchange of data between a patient and/or their clinician(s) to assist in diagnosis/monitoring/treatment.

***Record linkage – is the task of finding records in a dataset that refer to the same entity across different datasets.

Rule-based or deterministic record linkage generates links based on the number of individual identifiers that match among the available datasets ie some or all identifiers are identical binary matches

Probabilistic record linkage or fuzzy matching linkage by taking into account a wider range of potential identifiers, computing weights for each identifier based on its estimated ability to correctly identify a match or non-match, and using these weights to calculate the probability that two given records refer to the same entity.

Electronic health record a collection of patient and population health data stored in a digitised format accessed and maintained

Post coordination – allows users to specify new meaning by referencing existing SNOMED CT concepts – building on existing concepts

Situations with explicit context – the definition of the concept has a context that modifies the original concept eg diabetes mellitus a situation with no explicit context. Family history of diabetes mellitus = situation with explicit context.

Random ones from old papers

logistic regression: A statistical method for analysing a dataset in which there are one or more independent variables that determine an outcome.

Systematic Review: A type of literature reviews that collect and critically analyze multiple research studies or papers, using methods that are selected before one or more research questions are formulated, and then finding and analyzing studies that relate to and answer those questions in a structured methodology.

Observational Study: An investigation that draws inferences from a sample to a population where the independent variable is not under the control of the researcher because of ethical concerns or logistical constraints.

Controlled Study: An investigation where one group of participants is exposed to a substance while those in the "control" group are not
