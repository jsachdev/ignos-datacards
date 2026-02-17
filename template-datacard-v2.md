---
language:
- en # required, ISO language tag
datacard_version: 0.1.0 # required, version of the GENESIS datacard template
datacard_name: Datacard for ${DATASET_NAME} # required, name of the datacard
title: ${DATASET_NAME} # required, short, human-readable name of the dataset, aka pretty_name
datacard_creation:
  - created_by: [] # required, list of names of the person/people, or agent(s) that created the datacard in order of creation process, e.g. ["Claude Sonnet v 4", "John Smith"]. Include at least one, separate by commas, and add all that apply.
    created_date: {created_date} # required, date the datacard was created, format YYYY-MM-DD
    creation_method: {creation_method} # required, method used to create the datacard (e.g., manual, automated generation, or automated generation with human review)
dataset_authors:
  - dataset_author_orcid: {author_orcid} # required, repeat for each author
    given_name: {author_given_name} # required
    family_name: {author_family_name} # required
    affiliation: {author_affiliation} # optional, but recommended
dataset_contributors: # optional, but recommended, repeat for each contributor
  - contributor:
    contributor_ror_id: {contributor_ror_id} # optional, but recommended, either ror_id or orcid is required for each contributor
    contributor_orcid: {contributor_orcid} # optional, but recommended, either ror_id or orcid is required for each contributor
    contributor_name: {contributor_name} # optional, but recommended
dataset_contact_information:
  - orcid: {author_orcid} # required, repeat for each contact person
    given_name: {author_given_name} # required
    family_name: {author_family_name} # required
    email: {author_email} # required
    affiliation: {author_affiliation} # optional, but recommended
originating_research_organization_ror_id: {originating_research_organization_ror_id} # required, ROR ID of the organization that created the dataset.
  name: {originating_research_organization_name} # optional, but recommended, name of the organization that created the dataset
funding:
  - funder_name: {funding_grantor_name} # optional, but recommended, repeat for each funding source
    funder_ror_id: {funding_grantor_ror_id} # optional, but recommended
    funding_type: {funding_type} # optional, but recommended, e.g., grant, contract, in_kind
    grant_name: {funding_grant_name} # optional, but recommended
    grant_number: {funding_grant_number} # optional, but recommended
    solicitation_number: {funding_solicitation_number} # optional, but recommended, e.g. PAMS Award number and/or lab contract number
facilities:
  - ror_id: {facility_ror_id} # optional, but recommended, repeat for each facility used to create the dataset
    name: {facility_name} # optional, but recommended, name of the facility
tags:
- project: genesis # optional, but recommended, required to include genesis on all GENESIS project datasets
- science: lightsource # optional, but recommended to align with model and agent cards. what kind of science is this for (e.g., materials, biology, lightsource, fusion, climate, etc.)
- keywords: [] # required, keywords associated with the dataset. Include at least one, separate by commas, and add all that apply. Examples include: accelerator, atmospheric, audio, biology, climate, computer-vision, cosmology.
- release_review: #required, list of reviews that the dataset has undergone (must list at least one)
  - review_description: {review_description} # at least one is required, example values include not_reviewed, reviewed_general, reviewed_restricted, irb_reviewed, export_control_reviewed, institutional_review
  - review_institution_ror_id: {review_institution_ror_id} # optional, include ror_id of institution (institutional)_review, (irb)_reviewed that did the review if applicable.
_ dataset_release_date: {dataset_release_date} # optional, but recommended, date the dataset was released, format YYYY-MM-DD
- task_category: [] # optional, list all that apply, task categories associated with the dataset (e.g., multimodal, computer-vision, natural-language-processing, audio, tabular, time-series, reinforcement_learning, graph_learning, etc.) Separate by commas, and add all that apply.
- task_subcategory: [] # optional, but recommended, task subcategories associated with the dataset (e.g., benchmark, image-classification, object-detection, text-classification, named-entity-recognition, reinforcement_learning, robotics, text-to-speech, etc.) Separate by commas, and add all that apply.
- dataset_count_size:
  - dataset_count_category: # optional, include a size category for the dataset (n<1K, 1K<n<100K, 100K<n<1M, 1M<n<10M, 10M<n<100M, 100M<n<1B, 1B<n>100B, 100B<n<1T, n>1T) where n = number of instances (e.g., images, text documents, audio files, etc.).
  - dataset_count_unit: {dataset_count_unit} # optional, but recommended, unit for dataset size (e.g., files, images, sentences, audio recordings, etc.)
landing_page_url: {landing_page_url} # optional, URL of the dataset landing page, catalog or repository page where the dataset can be accessed, e.g. https://zenodo.org/records/6515019. In-flight datasets may not have a landing page at the time of datacard creation, but should be added when available.
dataset_doi: {dataset_doi} # optional, but recommended, DOI of the dataset. Example: 10.5281/zenodo.6515019
publication_date: {publication_date} # optional, date the dataset was published or made publicly available, format YYYY-MM-DD 
data_collection_start_date: {data_collection_start_date} # optional, but recommended, date the data collection or generation started
data_collection_end_date: {data_collection_end_date} # optional, but recommended, date the data collection or generation ended
dataset_info:
  features:
    - name: {feature_name} # optional, but recommended, repeat for each feature
      description: {feature_description} # optional, but recommended, a brief description of the feature
      dtype: {data_type}  # optional, but recommended, string, int32, float32, image, audio, sequence
  splits:
    - name: train # optional, but recommended, if the dataset is not split into train/validation/test, or if the dataset is not a dataset (e.g., a single file), then just include one split with name "full"
      num_bytes: {bytes}
      num_examples: {count}
    - name: validation # optional, but recommended, if the dataset does not have a validation split, remove this section
      num_bytes: {bytes}
      num_examples: {count}
    - name: test # optional, but recommended, if the dataset does not have a test split, remove this section
      num_bytes: {bytes}
      num_examples: {count}    
  example_instance: {example_instance} # optional, but recommended, provide an example instance from the dataset, or a link to one if the dataset is too large to include an example instance directly in the datacard
  download_size: {total_bytes} # required, total size in bytes of the dataset download
  dataset_unpacked_size: {total_bytes} # required, total size in bytes of the dataset on disk when uncompressed
source_datasets: 
  - name: {source_dataset_name} # optional, repeat for each source dataset
    doi: {source_dataset_doi} # optional, but recommended
    source_dataset_landing_page: {source_dataset_landing_page} # optional, but recommended if doi is not provided
arXiv: [] # optional, arXiv IDs of papers describing the dataset or associated papers
doi: [] # optional, DOIs of papers describing the dataset or associated papers
license: {spdx_license_id} # optional, use an SPDX license identifier https://spdx.org/licenses/
license_name: {license_name}  # optional, if license = other (license not in https://hf.co/docs/hub/repositories-licenses), specify an id for it here, like `my-license-1.0`. if not delete this line
license_link: {license_link}  # optional, if license = other, specify "LICENSE" or "LICENSE.md" to link to a file of that name inside the repo, or a URL to a remote file. if not delete this line
access_conditions: [] # optional, but recommended, list of conditions to fulfill to gain access to the dataset (Examples: ["Fully Open"]; ["CITI Training", "Proposal Process: Contact [CONTACT INFORMATION]"]; ["Collaboration Required: GlueX Collaboration"], ["Data Use Agreement: [DOI FOR DATA USE AGREEMENT]", etc. Separate by commas, and add all that apply.
maintenance: {maintenance_information} # optional, but recommended, free text field to provide information about the sustainability and maintenance of the dataset. For example, "This dataset is maintained through the [PROJECT NAME OR SOLICITATION NUMBER] project. There is no expectation of updates beyond the initial release, or maintenance after the graduation of the last phD student involved in the project. For questions about the dataset, please contact the dataset contact."

---

[!TODO] <INSTRUCTIONS: Replace all [!TODO], INSERT: ..., and REPLACE: ... placeholder tags with the appropriate information for your dataset. Be sure to remove the header TODO and INSTRUCTION tags once you have completed the datacard.>
[!TODO] <INSTRUCTIONS: The sections and questions in the markdown section of this datacard template are meant to be a guide for the types of information that should be included in a datacard. You can choose to answer all, some, or additional questions as appropriate for your dataset. The goal is to provide enough information for users to understand the dataset and its context, but you can use your judgment to determine what information is most relevant and important to include.>
[!TODO]<INSTRUCTIONS: yaml_metadata_key: [KEY_NAME] tags indicate that the information for that section can be found in the corresponding key in the YAML metadata at the top of this file, and is for use in the human and the automated generation of markdown section of the datacard. You can choose to either manually copy the information from the YAML metadata into the markdown sections below then adjust, or you can leave the placeholders and use them to use an automation tool (such as an LLM) to populate the markdown sections from the YAML metadata. If you choose to automatically populate the markdown sections from the YAML metadata, make sure to replace yaml_metadata_key: [KEY_NAME] tags in each relevant markdown section before sharing the datacard, and note the LLM or agent used to do this in the datacard_creation section of the YAML frontmatter metadata.>


# Datacard for [!TODO]${DATASET_NAME}

## Dataset Description

The **Dataset Description** section provides basic details about the dataset. This includes the authors, funding sources, and dates of the data collection.

*Last Updated*: [!TODO]<INSERT: YYYY-MM-DD>

### Developed by

[!TODO] <INSERT: Developed by is a person or group that was primarily responsible for the creation and design of the dataset. It suggests a leading role, such as a Principal Investigator, in the development of the dataset. Provide the Name, [ORCID](https://orcid.org/), affiliation ([ROR ID](https://ror.org/)) and email address of the person or group responsible for the dataset.> <yaml_metadata_key: authors, dataset_contact_information>

### Contributed by

[!TODO] <INSERT: Contributed by are a person, or group provided input or support to the datasets development but may not have been the primary creators. Contributions can include sample collection, processing, analysis, documentation, and-or submission of the dataset. This suggests collaboration, where multiple parties might have played various roles in the dataset development. Provide the Name, [ORCID](https://orcid.org/), affiliation ([ROR ID](https://ror.org/)) and email address of the person or group responsible for the dataset.> <yaml_metadata_key: contributors>

### Dataset short description

[!TODO] <REPLACE: the Examples of the short description with a brief summary of the dataset, typically one or two sentences long. This description should provide a high-level overview of the content, purpose, and scope.>

Examples:  

+ Dataset: Characterization and automated optimization of laser-driven proton beams from converging liquid sheet jet targets
+ Simulations of the aftermath of a neutron star merger.

### Over what timeframe was the data collected or generated? Does this timeframe align with when the underlying phenomena or events occurred (e.g., recent simulation of historical accelerator configurations)? If not, describe the timeframe of the original events or conditions represented by the data.

[!TODO]<INSERT: Provide single date, range, or approximate date; suggested format YYYY-MM-DD, and, if appropriate, describe alignment with underlying phenomena or events> <yaml_metadata_key: data_collection_start_date, data_collection_end_date>

### What resources were used? For example, what funding, facility time, computing resources, and datasets were used to create the dataset? Provide answers in the sections below.

[!TODO] <INSERT: Provide a list of the resources used to create the dataset, including funding sources, facilities, computing resources, and any other relevant resources. Facilities can include user facilities, national laboratories, research institutions, and other organizations that provided access to equipment, data, or expertise. Funding sources can include government agencies, private foundations, industry partners, and other organizations that provided financial support for the dataset creation. Computing resources can include high-performance computing clusters, cloud computing platforms, and other computational resources used for data processing and analysis. Include [ROR ID](https://ror.org/), grant numbers, contract numbers, or other identifiers as appropriate.> <yaml_metadata_key: funding, facilities>

## Sharing/Access Information

The section outlines the terms for sharing and reusing the dataset, and how the dataset has been cited or used in other works.

### Reuse restrictions placed on the data: 

[!TODO] <INSERT: Description of reuse restrictions. Will the dataset be shared under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)? If so, please describe this license and/or ToU, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms or ToU, as well as any fees associated with these restrictions.> <yaml_metadata_key: license, license_name, license_link>

### Provide DOIs, citations (bibtex format), or links and descriptions of relationships to ancillary data sets. 

[!TODO] <INSERT: Provide citations for ancillary data sets in [bibtex format](https://www.bibtex.com/g/bibtex-format/). Please include either a `doi` or `url` field in the citation.> <yaml_metadata_key: source_datasets>

### Recommended citation for this dataset (in bibtex format):

[!TODO]<REPLACE: Provide an example citation for the dataset in [bibtex format](https://www.bibtex.com/g/bibtex-format/). Please include either a `doi` or `url` field in the citation.> <yaml_metadata_key: dataset_doi, landing_page_url>

```txt
@misc{Smith2020,
  title     = "{<EXAMPLE REPLACE>: Training Dataset}",
  author    = "Smith, John and Doe, Jane",
               https://mpp-hep.github.io/EXAMPLETRAININGDATASET/",
  howpublished = "(Version v2) [Data set]. Zenodo",
  year      =  2020,
  note     = "https://doi.org/10.5281/zenodo.XXXXXX", 
}
```

## Data & File Overview

 The **Data & File Overview** section provides an overview of dataset collection characteristics, including file listings, their relationships, and the collection timeframe, providing users with a comprehensive understanding of the dataset's structure and content.

### List all files (or folders, as appropriate for dataset organization) contained in the dataset.

[!TODO] <INSERT: Provide a brief description of each file or folder, including its purpose and contents. If the dataset is large, consider providing a summary or representative sample of the files.>

### Describe the relationship(s) between files.

[!TODO] <INSERT: Indicate if certain files are subsets of others, if they are related by time or location, or if they represent different versions or formats of the same data.>

### Describe any additional related data collected that was not included in the current data package.

[!TODO] <INSERT: For example, indicate if there are raw data files, calibration files, or metadata that are stored separately or were not included in the dataset for any reason.>

### Are there multiple versions of this dataset? 

[!TODO] <INSERT: If yes, what files were updated and why? Otherwise, answer Not applicable.>

## Methodological Information

This section provides detailed information about the methods and procedures used to collect, process, analyze, and validate the data.

### How was the data for each instance obtained or generated? 

[!TODO] <INSERT:For example, raw experimental measurements from user facilities, processed, physics-ready experimental data, outputs from computational simulations, or data derived from prior datasets? If the data was derived, list and describe the source(s).> 


### For each instrument, facility, or source used to generate and collect the data, what mechanisms or procedures were used for the data collection?

[!TODO] <INSERT: For example, hardware apparatuses or sensors, manual human curation, software programs, software APIs?>

### To create the final dataset, was any preprocessing/ cleaning/ labeling of raw data done?

[!TODO] <INSERT: If yes, describe the steps taken to preprocess, clean, or label the raw data to create the final dataset. Preprocessing, cleaning, and labeling can include simple pipelines (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values), or more complex workflows including noise reduction and filtering, calibration, reconstruction and event building, simulation post-processing, meta-data enrichment (e.g., adding uncertainty estimates).>

### Is the software that was used to preprocess/ clean/ label the data available? 

[!TODO] <INSERT: If so, please provide a [bibtex format](https://www.bibtex.com/g/bibtex-format/), PID, link, or other access point, along with descriptions of any required packages or libraries to run the scripts.> 

### Describe any standards and calibration information, if appropriate. 

[!TODO] <INSERT: Describe any standards and calibration information relevant to the dataset.>


### Describe the environmental and experimental conditions relevant to the dataset.

[!TODO] <INSERT: Provide information about environmental and experimental conditions relevant to the dataset. For example, temperature, humidity, pressure, or other conditions that might affect the data.>

### Describe any quality-assurance procedures performed on the data.

[!TODO] <INSERT: Provide information about any quality-assurance procedures performed on the data. For example, were there any validation or verification steps taken to ensure the accuracy and reliability of the data?>

## Data-Specific Information

This section provides additional context and details specific contents and structure of each contained dataset or file, including data type, variables, dimensions, naming conventions, missing data codes, and any specialized formats.

[!TODO]<REPEAT this section as needed for each dataset (or file, as appropriate).>

### What data does each instance within the dataset consist of (for each modality, if appropriate)? "Raw" data (e.g., unprocessed text or images) or features?

[!TODO] <INSERT: In either case, please provide a description.>

### Number of variables:

[!TODO] <INSERT: Provide the number of variables (features, columns) in the dataset or file.><yaml_metadata_key: dataset_info.features>

### Number of cases/rows:

[!TODO] <INSERT: Provide the number of cases (instances, rows) in the dataset or file.>

### Provide a list variable name(s), description(s), unit(s), and value labels as appropriate for each variable in the dataset/file.

[!TODO] <REPLACE: Replace the example table with a table listing each variable in the dataset/ or file, along with its description, unit, and any value labels if applicable.>

For example:
| Variable Name | Description               | Unit      | Value Labels                |
|---------------|---------------------------|-----------|-----------------------------|
| temp          | Temperature measurement   | Celsius   | N/A                         |
| status        | Operational status        | N/A       | 0 = Off, 1 = On            |  


### Codes used for missing data:

[!TODO] <INSERT: Replace the example table of codes used to represent missing data in the dataset or file.>

For example:
| Code | Description               |
|------|---------------------------|
| -999 | Data not collected        |
| -888 | Measurement error         |

### Specialized formats or other abbreviations used:

[!TODO] <INSERT: Describe any specialized data formats, abbreviations, or conventions used in the dataset or file. For example, if the dataset is in a specific file format (e.g., ROOT, HDDM, HDF5), or if there are any domain-specific abbreviations used in variable names or values.>

### Please provide a sample of the dataset/file, or a citation (bibtex format) or link where one may review an reasonably digestable example of the contents (optional).

[!TODO] <INSERT: Provide a sample of the dataset or file, or a citation (in bibtex format) or link to where one can review an example of the contents. This can help users understand the structure and content of the dataset.><yaml_metadata_key: dataset_info.example_instance>

## More information (optional)

[!TODO] <INSERT: Provide any additional information you think it is important to communicate, but does not clearly fit under any other heading. This could include information about future plans for the dataset, acknowledgments, or any other relevant details.>