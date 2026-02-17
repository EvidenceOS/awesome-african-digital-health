# Awesome African Digital Health [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of digital health standards, platforms, AI companies, and interoperability resources for building sovereign health systems across Africa -- with deep landscape analysis.

Maintained by [PAATHI](https://paathi.org) (Pan-African Alliance for Technology & Health Innovation) and [EvidenceOS](https://evidenceos.com).

**What makes this list different:** Beyond links, we provide structured intelligence on African health AI companies (AI type, clinical claims, regulatory status, evidence base) and a country-by-country regulatory landscape. This is a living resource for investors, policymakers, implementers, and researchers.

---

## Contents

- **Infrastructure & Standards**
  - [WHO Standards & Classifications](#who-standards--classifications)
  - [Data Exchange & Interoperability](#data-exchange--interoperability)
  - [Terminology & Vocabulary](#terminology--vocabulary)
  - [Clinical Data Models](#clinical-data-models)
  - [Digital Public Infrastructure (DPI)](#digital-public-infrastructure-dpi)
  - [African Health Information Platforms](#african-health-information-platforms)
  - [Developer Tools & SDKs](#developer-tools--sdks)
- **Landscape Intelligence**
  - [African Health AI & Tech Companies](#african-health-ai--tech-companies)
  - [AI Radiology & Imaging in Africa](#ai-radiology--imaging-in-africa)
  - [Supply Chain & Logistics AI](#supply-chain--logistics-ai)
  - [Genomics & Precision Medicine](#genomics--precision-medicine)
  - [Accelerators & Cohort Programs](#accelerators--cohort-programs)
- **Governance & Evidence**
  - [Continental & Regional Frameworks](#continental--regional-frameworks)
  - [Regulatory Landscape by Country](#regulatory-landscape-by-country)
  - [International Standards & Compliance](#international-standards--compliance)
  - [Research & Evidence Networks](#research--evidence-networks)
- **Ecosystem**
  - [Community & Learning](#community--learning)
  - [Key Research Papers](#key-research-papers)
- [Contributing](#contributing)
- [About](#about)
- [License](#license)

---

# Infrastructure & Standards

## WHO Standards & Classifications

- [ICD-11](https://icd.who.int) - International Classification of Diseases, 11th Revision. 80,000+ entities, 43 languages, postcoordination with 6.3M+ combinations. Docker self-hosting available for offline African deployment via `docker pull whoicd/icd-api`.
- [ICF](https://www.who.int/standards/classifications/international-classification-of-functioning-disability-and-health) - International Classification of Functioning, Disability and Health. Framework for disability and rehabilitation measurement.
- [ICHI](https://www.who.int/standards/classifications/international-classification-of-health-interventions) - International Classification of Health Interventions. Coding for medical, surgical, and primary care interventions.
- [WHO SMART Guidelines](https://www.who.int/teams/digital-health-and-innovation/smart-guidelines) - Machine-readable clinical guidelines using L1-L5 layers. FHIR-native, translating narrative guidelines into computable logic. [Reference Architecture on GitHub](https://github.com/WorldHealthOrganization/smart-ra).
- [WHO Digital Health Atlas](https://digitalhealthatlas.org) - Registry of digital health deployments across countries. Tracks implementations to reduce duplication.
- [WHO Classification of Digital Health Interventions](https://www.who.int/reproductivehealth/publications/mhealth/classification-digital-health-interventions/en/) - Taxonomy for categorizing digital health functionalities.

## Data Exchange & Interoperability

- [HL7 FHIR R4/R5](https://www.hl7.org/fhir/) - Fast Healthcare Interoperability Resources. Universal RESTful API standard. R4 is production; R5 adds subscriptions and native ICD-11 support.
- [SMART on FHIR](https://smarthealthit.org) - App launch and authorization framework with OAuth 2.0 scoping for FHIR-connected clinical applications.
- [OpenHIE](https://ohie.org) - Open Health Information Exchange reference architecture. Connects facility registries, terminology services, shared health records, and client registries.
- [OpenHIM](https://openhim.org) - Open Health Information Mediator. Middleware for routing, orchestrating, and logging health data transactions. Core of OpenHIE.
- [IHE Profiles](https://www.ihe.net/resources/profiles/) - mCSD (Care Services Discovery), PDQm (Patient Demographics Query), MHD (Mobile Access to Health Documents).
- [ADX](https://wiki.ohie.org/display/resources/ADX) - Aggregate Data Exchange. WHO standard for aggregate reporting, widely used with DHIS2.
- [Nigeria FHIR IG](https://github.com/Nigeria-FHIR-Community/NPHCDA-ImmunizationIG) - NPHCDA Immunization FHIR Implementation Guide. Supported by US CDC through AFENET, implemented by IntelliSOFT and DHIN.

## Terminology & Vocabulary

- [SNOMED CT](https://www.snomed.org) - 350,000+ clinical concepts. Free for LMICs via SNOMED International member licensing.
- [LOINC](https://loinc.org) - Logical Observation Identifiers Names and Codes. 100,000+ terms for lab tests and clinical observations. Free worldwide.
- [CIEL](https://openconceptlab.org) - Columbia International eHealth Laboratory. Curated concept dictionary mapping SNOMED, ICD, LOINC for resource-limited settings. Powers OpenMRS.
- [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/) - Drug nomenclature standard from U.S. National Library of Medicine.
- [GS1 Healthcare](https://www.gs1.org/industries/healthcare) - Medical product identification and supply chain standards. Supports UDI and drug serialization.
- [ATC Classification](https://www.who.int/tools/atc-ddd-toolkit) - WHO Anatomical Therapeutic Chemical classification for medicines.

## Clinical Data Models

- [OMOP CDM](https://ohdsi.github.io/CommonDataModel/) - Common Data Model for observational health data. Powers OHDSI network (800M+ patient records). OHDSI Africa chapter active.
- [CDISC](https://www.cdisc.org) - Clinical trial data standards (CDASH, SDTM, ADaM). Required for FDA/EMA submissions.
- [openEHR](https://openehr.org) - EHR data architecture using archetypes and templates. Separates clinical knowledge from technical implementation.
- [i2b2](https://i2b2.org) - Research data warehouse platform for clinical investigators.
- [FHIR Shorthand (FSH)](https://build.fhir.org/ig/HL7/fhir-shorthand/) - DSL for defining FHIR profiles and implementation guides.

## Digital Public Infrastructure (DPI)

Foundational infrastructure enabling secure, sovereign data exchange. See [DPI Africa](https://dpi.africa.com/) for continental context.

- [X-Road](https://x-road.global) - Estonia's open-source decentralized data exchange layer. Signed, logged, and encrypted transactions between government and health systems. Foundation for PAATHI/AIDA interoperability architecture.
- [MOSIP](https://mosip.io) - Modular Open Source Identity Platform. National digital ID for health enrollment and patient matching. Deployed in multiple African countries.
- [OpenCRVS](https://opencrvs.org) - Open-source civil registration and vital statistics. Birth/death registration feeding health data systems.
- [GovStack](https://govstack.global) - Digital government building blocks (identity, payments, messaging, health). Co-created by ITU, GIZ, Estonia, DIAL.
- [OpenG2P](https://openg2p.org) - Government-to-People social protection platform. Integrates with MOSIP for beneficiary identification.
- [Mojaloop](https://mojaloop.io) - Open-source real-time payment platform. Health payment interoperability and mobile money integration.

## African Health Information Platforms

Production-grade platforms forming the backbone of health systems across the continent.

- [DHIS2](https://dhis2.org) - District Health Information Software 2. **40+ African countries, 80+ globally.** Backbone of public health reporting and surveillance. Open source, HISP network.
- [OpenMRS](https://openmrs.org) - Open Medical Record System. **6,000+ facilities, 40+ countries.** Built for resource-limited settings with offline capability.
- [iHRIS](https://www.ihris.org) - Health workforce management. **30+ countries.** Tracks CHWs, nurses, and doctors.
- [mHero](https://www.mhero.org) - Two-way health worker communication via SMS/messaging. Integrates with iHRIS and DHIS2.
- [OpenLMIS](https://openlmis.org) - Supply chain management for vaccines, medicines, and medical supplies.
- [CommCare](https://www.dimagi.com/commcare/) - Mobile data collection for CHWs. **80+ countries**, robust offline support. By Dimagi.
- [Medic](https://medic.org) - Community health toolkit. **28,000+ CHWs** across Africa. SMS, voice, and app-based workflows.
- [Bahmni](https://www.bahmni.org) - Open-source hospital system (OpenMRS + Odoo + OpenELIS + dcm4chee). EMR, billing, lab, PACS.
- [OpenELIS Global](https://openelis-global.org) - Laboratory information system for public health and clinical labs.
- [LibreHealth](https://librehealth.io) - Open-source health IT community (EHR, radiology, toolkit).

## Developer Tools & SDKs

- [HAPI FHIR](https://hapifhir.io) - Open-source FHIR server/client (Java). Reference implementation with R4/R5 support.
- [ICD-11 ECT](https://github.com/ICD-API/ECT-React-samples) - Embedded Coding Tool for web apps. React/Angular/Vue via `@whoicd/icd11ect` npm package.
- [ICD-11 Docker](https://hub.docker.com/r/whoicd/icd-api) - Self-hosted ICD-11 API. `docker pull whoicd/icd-api`. No auth required. Critical for offline African deployment.
- [OpenConceptLab (OCL)](https://openconceptlab.org) - Terminology management platform for mapping between code systems.
- [Synthea](https://synthetichealth.github.io/synthea/) - Synthetic patient data generator. FHIR bundles for testing without real patient data.
- [Google Android FHIR SDK](https://github.com/google/android-fhir) - Offline-capable FHIR apps on Android. Critical for CHW mobile apps.
- [Medplum](https://www.medplum.com) - Open-source FHIR-native platform with developer-first APIs and React components.
- [FHIR Validator](https://github.com/hapifhir/org.hl7.fhir.core) - HL7 official validation tooling for conformance testing.
- [CQL](https://cql.hl7.org) - Clinical Quality Language for expressing clinical logic. Used in WHO SMART Guidelines.
- [onaio/fhir-web](https://github.com/onaio/fhir-web) - Web interface for administering FHIR-based digital health solutions.

---

# Landscape Intelligence

## African Health AI & Tech Companies

The following table profiles AI-enabled health companies active in Africa. We track: **AI type**, **clinical domain**, **key claims and evidence**, **regulatory status**, and **interoperability** with open standards. This is intended as a living intelligence resource.

> **Legend:** `Peer-reviewed` = published in indexed journal | `Pilot` = deployed in limited facilities | `Scale` = deployed nationally or across multiple countries | `Regulatory` = has CE/FDA/WHO PQ/SAHPRA clearance

### Clinical AI & Decision Support

| Company | HQ | AI Type | Domain | Scale & Evidence | Regulatory | Interop |
|---------|-----|---------|--------|-----------------|------------|---------|
| [EvidenceOS](https://evidenceos.com) | USA/Rwanda | Clinical decision support, NLP, auto-coding | TBI, neurology | ICD-11 auto-coding, biomarker integration, meta-analysis (28,612 patients, 32% CT reduction) | FDA SaMD pathway (in progress) | FHIR R4, ICD-11, OMOP |
| [Ubenwa](https://www.ubenwa.ai) | Nigeria/Canada | Signal processing, ML | Neonatology (birth asphyxia) | AI model detects asphyxia from newborn cry analysis. $2.5M raised (2022) | Research stage | Proprietary |
| [RxAll](https://rxall.net) | Nigeria | Hyperspectral AI | Drug authentication | Won Hello Tomorrow Global Challenge 2019 grand prize. AI-powered drug verification via handheld spectrometer | Research/pilot | Proprietary |
| [Babyl (Babylon)](https://www.babyl.rw) | Rwanda/UK | NLP, symptom assessment | Primary care, triage | National deployment in Rwanda. AI-powered triage and teleconsultation | CE marked (UK) | HL7 |
| [Ada Health](https://ada.com) | Germany | Probabilistic reasoning | Symptom assessment, triage | Peer-reviewed accuracy studies. Used in African health contexts | CE marked, Class IIa | FHIR-compatible |
| [Zuri Health](https://www.zurihealth.com) | Kenya | AI triage | Primary care | 16+ mobile operator partnerships across 7 countries. SMS/WhatsApp/app delivery | Not specified | SMS/WhatsApp APIs |
| [REMA](https://www.raborema.com) | Benin | AI diagnostic support | Multi-specialty | Remote assistance to 7,000+ physicians across West Africa. AI-driven error reduction | Not specified | Proprietary |
| [Ilara Health](https://www.ilarahealth.com) | Kenya | AI diagnostics | Point-of-care (malaria, etc.) | $4.2M raised. Equips clinics with portable ultrasounds and AI-powered malaria diagnostics | Not specified | Proprietary |
| [Jacaranda Health](https://www.jacarandahealth.org) | Kenya | NLP | Maternal health | SMS-based triage and clinical decision support for maternal care in East Africa | Not specified | SMS/DHIS2 |
| [Healthlane](https://www.healthlane.co) | Cameroon | Digital health platform | Preventive/primary care | 60K+ users. Y Combinator Winter 2020 | Not specified | Proprietary |
| [Waspito](https://waspito.com) | Cameroon | Telemedicine + AI | Integrated care | 30K+ users. Telemedicine, pharmacy, lab, delivery. $500K (Orange, 2020) | Not specified | Proprietary |

### Digital Health Platforms & EHR

| Company | HQ | Type | Domain | Scale & Evidence | Regulatory | Interop |
|---------|-----|------|--------|-----------------|------------|---------|
| [Helium Health](https://www.heliumhealth.com) | Nigeria | Cloud EHR | Hospital/clinic management | Largest EMR provider in West Africa. 5,000+ medical professionals, 150K+ patients/month | Not specified | Proprietary EMR |
| [Vezeeta](https://www.vezeeta.com) | Egypt | Digital healthcare platform | Patient-provider matching | $60M+ total funding. 3M+ bookings, 10K+ doctors | Not specified | Proprietary |
| [mPharma](https://www.mpharma.com) | Ghana | Data intelligence | Pharmacy/drug supply | $17M Series C. 850+ pharmacies, 155+ hospitals. Drug inventory management across multiple countries | Not specified | Proprietary |
| [Eden Care](https://www.edencare.rw) | Rwanda | Digital insurance | Health insurance | Digital health underwriter for East African health insurance | Not specified | Proprietary |
| [Bypa-ss](https://www.bypa-ss.com) | Multi-Africa | HIE platform | Health information exchange | HealthTag platform digitizing healthcare information exchange | Not specified | HIE standards |
| [Africa Health Holdings](https://www.africahealthholdings.com) | Ghana | Telemedicine | Primary care | MyCareMobile app. 200K+ annual patients | Not specified | Proprietary |
| [Healthtracka](https://www.healthtracka.com) | Nigeria | Digital diagnostics | Home health screening | At-home diagnostic testing with 1-3 day results. Techstars Toronto 2021, Google AI for Health 2024 | Not specified | Proprietary |

## AI Radiology & Imaging in Africa

AI-powered medical imaging is one of the most validated and deployed categories of health AI in Africa, particularly for TB screening.

| Company/Tool | Origin | AI Type | African Deployment | Evidence | Regulatory |
|-------------|--------|---------|-------------------|----------|------------|
| [CAD4TB (Delft Imaging)](https://www.delft.care) | Netherlands | Computer-aided diagnosis | **9 African countries** in national TB programs. South Africa, Kenya, Tanzania, Zambia confirmed | Peer-reviewed: performance compared well with human experts ([Nature Scientific Reports, 2021](https://www.nature.com/articles/s41598-021-03265-0)) | CE marked |
| [Qure.ai qXR](https://qure.ai) | India | Deep learning, chest X-ray, head CT | Multiple African countries for TB screening and trauma | Peer-reviewed: performed on par with expert readers, significantly better than intermediate readers | CE marked, FDA cleared |
| [Lunit INSIGHT CXR](https://www.lunit.io) | South Korea | Deep learning, chest X-ray | Deployed in African TB programs | Peer-reviewed: on par with expert readers in independent evaluation of 12 AI solutions | CE marked, FDA cleared |
| [Rology](https://www.rology.com) | Egypt | Teleradiology + AI | Egypt, MENA, expanding Africa | On-demand remote radiologist connection for hospitals | Not specified |
| [Dileny Technologies](https://www.dileny.com) | Egypt | AI breast imaging | Egypt | BE-SMART diagnostic workflow tool for breast cancer screening | Not specified |

> **Key reference:** [Independent evaluation of 12 AI solutions for TB detection](https://www.nature.com/articles/s41598-021-03265-0) -- Only 3 of 12 systems performed significantly better than intermediate human readers. CAD4TB, Qure.ai, and Lunit led the field.

## Supply Chain & Logistics AI

| Company | HQ | AI Type | Domain | Scale | Evidence |
|---------|-----|---------|--------|-------|----------|
| [Zipline](https://www.flyzipline.com) | USA/Rwanda | Autonomous drones, AI logistics | Blood, vaccine, medicine delivery | **1M+ deliveries, 70M+ autonomous miles, 4,800+ facilities, 49M people** across Rwanda, Ghana, Nigeria, Kenya, Cote d'Ivoire | Peer-reviewed: 61% faster delivery, 67% fewer blood expirations, 43% emergency orders ([SSIR](https://ssir.org/articles/entry/zipline-health-innovations-africa)) |
| [mPharma](https://www.mpharma.com) | Ghana | Predictive analytics | Drug supply chain | 850+ pharmacies, 155+ hospitals across Africa | $23.6M total funding |
| [DrugStoc](https://www.drugstoc.com) | Nigeria | Supply chain tech | Pharmaceutical distribution | Technology + financial solutions for medication access | Not specified |
| [DawaSwift](https://www.dawaswift.com) | Kenya/Canada | AI pharmacy | On-demand medicine delivery | Developing Healthipy AI insurance platform. Entrepreneur First backed | Not specified |
| [OpenLMIS](https://openlmis.org) | Open source | Logistics optimization | Vaccine/medicine supply chain | Multiple African country deployments for cold-chain management | N/A (open source) |

## Genomics & Precision Medicine

| Company/Initiative | HQ | Focus | Scale | Evidence |
|-------------------|-----|-------|-------|----------|
| [H3Africa](https://h3africa.org) | Pan-African | Genomics research consortium | Biobank and bioinformatics capacity across Africa | NIH and Wellcome Trust funded |
| [54gene](https://www.54gene.com) | Nigeria | African genomic diversity | Addresses representation gap in global genomics data | Research stage (pivoted to SystemBio) |
| [3X4 Genetics](https://www.3x4genetics.com) | South Africa | Nutrigenomics | Genetics-based health and nutritional genomics platform | Commercial product |
| [Nawah Scientific](https://www.nawahscientific.com) | Egypt | Research services | 100K+ samples analyzed, 3,500+ clients | Multidisciplinary research center |

## Accelerators & Cohort Programs

Programs accelerating African health tech companies. Useful for tracking emerging companies and validated pipelines.

| Program | Organizer | Year | Size | Focus |
|---------|-----------|------|------|-------|
| [Google for Startups Growth Academy: AI for Health](https://startup.google.com/programs/growth-academy/ai-for-health/emea/) | Google | 2024 | 24 startups (4 African) | AI for healthcare and wellbeing. African participants: Healthtracka (Nigeria), Thalia Psychotherapy (Kenya), TibuHealth (Kenya), Zoie Health (South Africa) |
| [HealthTech Hub Africa](https://thehealthtech.org/) | UNDP timbuktoo | 2025 | 21 startups | 10-month accelerator. Cohort from 11 countries including Kenya, Nigeria, Rwanda, Ghana, Egypt, Cameroon |
| [Digital Health Africa](https://digitalhealthafrica.org/) | DHA | Annual | Varies | Continental digital health innovation conference and innovation showcase |
| [Founders Factory Africa](https://www.foundersfactory.africa/) | FFA | Ongoing | Varies | Health tech vertical with investments in African health startups |

---

# Governance & Evidence

## Continental & Regional Frameworks

- [Africa CDC](https://africacdc.org) - Continental public health agency. Digital health strategy, surveillance infrastructure, pandemic preparedness across 55 AU member states.
- [AU Digital Transformation Strategy 2020-2030](https://au.int/en/documents/20200518/digital-transformation-strategy-africa-2020-2030) - Target: digital ID for 30% of Africans enabling universal health coverage.
- [AU Continental AI Strategy 2024-2030](https://au.int) - Adopted early 2025. Roadmap for responsible AI with precision medicine and digital health as strategic priorities.
- [Smart Africa Alliance](https://smartafrica.org) - 36-member intergovernmental alliance. AI for Health working group. [Digital Health White Paper](https://smartafrica.org/wp-content/uploads/2025/11/Digital-Health-White-paper-Designed-by-SA.pdf).
- [Malabo Convention](https://au.int/en/treaties/african-union-convention-cyber-security-and-personal-data-protection) - AU Convention on Cyber Security and Personal Data Protection. Ratified by 15 countries. Continental legal framework for health data governance.
- [African Medicines Agency (AMA)](https://au.int/en/ama) - Continental regulatory body treaty. Harmonized regulatory oversight for medicines and health products.
- [Africa Health Strategy 2016-2030](https://au.int/en/documents/20160202/africa-health-strategy-2016-2030) - AU framework for health systems strengthening.
- [DPI Africa](https://dpi.africa.com/) - Continental initiative for digital public infrastructure in health and other sectors.
- [ECOWAS Data Protection Framework](https://www.ecowas.int) - Supplementary Act for harmonized West African health data governance.
- [EAC Health Protocol](https://www.eac.int) - East African Community mutual recognition for health systems and cross-border data sharing.
- [SADC eHealth Strategy](https://www.sadc.int) - Southern African digital health and telemedicine framework.

## Regulatory Landscape by Country

Based on [Mapping the Regulatory Landscape of AI in Healthcare in Africa](https://pmc.ncbi.nlm.nih.gov/articles/PMC10484713/) (Frontiers in Pharmacology, 2023) -- a scoping review of 12 African countries. **No African country has specific AI legislation.** Regulation occurs through adjacent frameworks.

| Country | Data Protection | Digital Health Policy | AI in Medical Devices | Consumer Protection (Software) | Notable |
|---------|----------------|----------------------|----------------------|-------------------------------|---------|
| **Kenya** | Data Protection Act 2023 (Privacy-by-Design) | **Standalone E-Health Bill** (only country). Allows e-consent, e-dispensing, e-prescriptions | Not explicitly addressed | Potentially includes software | 2018 AI Taskforce appointed. Most advanced digital health legal framework |
| **South Africa** | POPIA (2013, effective 2020) | Standalone policy. Professional telemedicine guidelines | Included in medical device definition | Includes software. Wide "supplier" definition covers AI developers | PC4IR commission. SAHPRA now requires [AI/ML device evidence](https://medqair.com/regulatory-news/sahpra-issues-ai-ml-device-requirement/) |
| **Rwanda** | Law No 058/2021 (includes heir data rights, cessation rights) | Embedded in broader framework | Not explicitly addressed | Unique: regulatory body bears strict liability for approved products | Centre for 4IR with WEF |
| **Nigeria** | Data Protection Regulation 2019; Data Protection Bill 2020 | Policy framework exists | Not explicitly addressed | Potentially includes software | Largest health tech startup ecosystem |
| **Ghana** | Data protection legislation enacted | Allows e-dispensing, e-prescriptions. Telemedicine guidelines | Not explicitly addressed | "Movable property" definition may include software | Growing startup ecosystem |
| **Uganda** | Data Protection and Privacy Act 2019 | Policy framework. Software in medical device definition | **Software included** in device definition | Includes software | 2018 4IR Taskforce |
| **Tanzania** | Personal Data Protection Law 2022 | Policy exists | Not explicitly addressed | Potentially includes software | Transfer impact assessments required |
| **Zimbabwe** | Data Protection Act No 5 of 2021 | Professional telemedicine guidelines | Not explicitly addressed | Includes software | ARIPO member |
| **Cameroon** | No specific law (privacy embedded in cybersecurity, advertising, telecoms laws) | Embedded in healthcare framework | Not explicitly addressed | Negligence-based liability (unique) | CEMAC Directive ratified |
| **Malawi** | No enacted law (Data Protection Bill 2021 drafted) | Policy exists | Not explicitly addressed | **Software explicitly excluded** from consumer protection | Least developed framework |
| **Botswana** | Data Protection Act No 32 of 2018 | Standalone policy (sporadic implementation) | Not explicitly addressed | Potentially includes software | Information and Data Protection Commission |
| **The Gambia** | Information and Communications Act 2009 | Policy exists | Not explicitly addressed | Supplier responsible for recalls | Smallest market |

**Key takeaway:** Only South Africa, Kenya, and Uganda include software in medical device definitions. Nine of the twelve countries are ARIPO members, enabling regional patent registration. All offer patent and copyright protection for AI applications.

## International Standards & Compliance

Standards applicable to health AI built for or deployed in Africa.

- [ISO 13485](https://www.iso.org/standard/59752.html) - Quality management for medical devices. Required for CE marking.
- [IEC 62304](https://www.iso.org/standard/38421.html) - Medical device software lifecycle. Development and maintenance requirements.
- [ISO 14971](https://www.iso.org/standard/72704.html) - Medical device risk management. Essential for clinical AI risk assessment.
- [ISO 27001](https://www.iso.org/standard/27001) / [ISO 27799](https://www.iso.org/standard/62777.html) - Information security with health-specific extensions.
- [IEEE 2894-2024](https://standards.ieee.org/ieee/2894/10699/) - Responsible AI in healthcare standard.
- [EU AI Act](https://artificialintelligenceact.eu) - Classifies health AI as high-risk. Affects African exports to EU and sets global governance precedent.
- [FDA SaMD Framework](https://www.fda.gov/medical-devices/digital-health-center-excellence/software-medical-device-samd) - Software as a Medical Device regulatory pathway. IMDRF framework adopted globally.
- [WHO Regulatory Convergence](https://www.who.int/teams/regulation-prequalification) - Harmonization guidance for LMICs. Two pathways: abridged (if approved by WHO-listed authority) or comprehensive review.

## Research & Evidence Networks

- [OHDSI](https://ohdsi.org) - Observational Health Data Sciences and Informatics. African chapter building OMOP CDM capacity across the continent.
- [INTBIR](https://fitbir.nih.gov) - International Initiative for Traumatic Brain Injury Research. NIH-led TBI data commons. EvidenceOS integration partner.
- [INDEPTH Network](https://www.indepth-network.org) - Health and Demographic Surveillance System sites providing longitudinal data across Africa.
- [H3Africa](https://h3africa.org) - Pan-African genomics research consortium. NIH and Wellcome Trust funded, building biobank and bioinformatics capacity.
- [EDCTP](https://www.edctp.org) - European & Developing Countries Clinical Trials Partnership. Major clinical trials funder for Sub-Saharan Africa.
- [APHRC](https://aphrc.org) - African Population and Health Research Center. Leading African research institution on population and health.
- [KEMRI-Wellcome Trust](https://kemri-wellcome.org) - One of Africa's largest health research programs. Infectious diseases, child health, genomics.
- [AORTIC](https://aortic-africa.org) - African Organisation for Research and Training in Cancer.

---

# Ecosystem

## Community & Learning

- [OpenHIE Community](https://ohie.org/community/) - Architecture patterns and implementation experience for health information exchange.
- [FHIR Community (Zulip)](https://chat.fhir.org) - Global FHIR implementer community. Active channels for terminology, CDS, and regional implementations.
- [IntraHealth International](https://www.intrahealth.org) - Drives iHRIS development and health workforce strengthening across Africa.
- [PATH](https://www.path.org) - Global health innovation with deep African presence in digital health and diagnostics.
- [Digital Square](https://digitalsquare.org) - Coordinates global goods investments. Maintains the Global Goods Guidebook for LMICs.
- [RAIGH Academy](https://paathi.org) - PAATHI's workforce development pillar. Pan-African AI health informaticist training.
- [HELINA](https://www.helina-online.org) - Health Informatics in Africa. Pan-African professional association and biennial conference.
- [Digital Impact Alliance (DIAL)](https://dial.global) - Building block specifications and SDG Digital Investment Framework.
- [Masakhane](https://www.masakhane.io) - Grassroots African NLP community building MT for 2,000+ languages. Critical for multilingual health AI.
- [GIZ Digital Health](https://www.giz.de/en/worldwide/113944.html) - German development programs supporting digital health implementation in Africa.
- [HealthTech Hub Africa](https://thehealthtech.org/) - UNDP-backed accelerator for African health startups. Annual cohort program.

## Key Research Papers

Foundational research for understanding AI and digital health in Africa.

| Paper | Year | Key Finding |
|-------|------|-------------|
| [Mapping the regulatory landscape of AI in healthcare in Africa](https://pmc.ncbi.nlm.nih.gov/articles/PMC10484713/) | 2023 | No sui generis AI regulation in 12 African countries. Kenya most advanced. |
| [Artificial Intelligence for Healthcare in Africa](https://pmc.ncbi.nlm.nih.gov/articles/PMC8521850/) | 2021 | Maps AI applications from 1980s-present. Identifies diagnostics, drug authentication, HR prediction as key areas. |
| [Independent evaluation of 12 AI solutions for TB detection](https://www.nature.com/articles/s41598-021-03265-0) | 2021 | Only 3 of 12 AI TB tools performed better than intermediate readers (CAD4TB, Qure.ai, Lunit). |
| [State of AI in Healthcare: Sub-Saharan Africa](https://ceimia.org/wp-content/uploads/2024/07/state-of-ai-in-healthcare-sub-saharan-africa.pdf) | 2024 | CEIMIA report analyzing 60 active AI health initiatives across Africa. |
| [Challenges and opportunities of AI in African health space](https://pmc.ncbi.nlm.nih.gov/articles/PMC11748156/) | 2024 | Narrative review of barriers: data scarcity, infrastructure, regulatory gaps, workforce. |
| [AI in global health: unfair future for Sub-Saharan Africa?](https://pmc.ncbi.nlm.nih.gov/articles/PMC11823112/) | 2025 | Equity analysis of AI benefit distribution. Warns of widening gap without local capacity. |
| [Health information exchange policy and standards in Africa](https://pmc.ncbi.nlm.nih.gov/articles/PMC9931258/) | 2023 | Systematic review of HIE policies. Finds FHIR + DHIS2 as primary interoperability enablers. |
| [Do we need prequalification of AI as a medical device?](https://www.nature.com/articles/s41746-025-02151-7) | 2025 | Argues for WHO prequalification pathway to drive equitable AI adoption in LMICs. |

---

## Contributing

Contributions welcome. Please read the [contribution guidelines](CONTRIBUTING.md) before submitting a pull request.

### Guidelines

- **One resource per pull request.** Include a short description and why it is relevant to African digital health.
- **For company additions:** Include AI type, clinical domain, evidence base, and regulatory status where known.
- **Maintain alphabetical order** within each section.
- **Verify all links** are working and point to canonical URLs.
- New categories welcome if they contain 3+ entries.
- Flag outdated entries by opening an issue.

---

## About

This list is maintained by [PAATHI](https://paathi.org) and [EvidenceOS](https://evidenceos.com) as part of the mission to build sovereign, interoperable health infrastructure across Africa.

| Entity | Description | Jurisdiction |
|--------|-------------|-------------|
| [PAATHI](https://paathi.org) | Pan-African Alliance for Technology & Health Innovation | Rwanda (CLG) |
| [EvidenceOS](https://evidenceos.com) | Clinical AI operating system for evidence-based care | Delaware (C-Corp) |
| [CEAIH](https://ceaih.org) | Center for Evidence and AI in Health | United States (501c3) |
| [AIDA](https://paathi.org) | African Institute for Interoperability Solutions (PAATHI pillar) | Rwanda |

**PAATHI Charter Pillars:**
1. AI Safety & Ethics
2. RAIGH Academy (workforce development)
3. AIDA Infrastructure (interoperability)
4. AI Health Research

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [PAATHI](https://paathi.org) and [EvidenceOS](https://evidenceos.com) have waived all copyright and related or neighboring rights to this work.
