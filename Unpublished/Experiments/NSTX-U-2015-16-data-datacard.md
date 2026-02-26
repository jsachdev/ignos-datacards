---
language:
  - en
datacard_version: 0.1.0
datacard_name: Datacard for NSTX-U Experimental Data (2015-2016)
title: National Spherical Torus Experiment Upgrade (NSTX-U) Experimental Dataset

datacard_creation:
  created_by: ["Jai Sachdev"]
  created_date: 2026-02-26
  creation_method: manual

dataset_authors:
  - dataset_author_orcid: null
    given_name: NSTX Research Team
    family_name: Princeton Plasma Physics Laboratory
    affiliation: Princeton Plasma Physics Laboratory (PPPL)

dataset_contributors:
  - contributor_name: NSTX Research Team / Collaborators
    contributor_ror_id: https://ror.org/05sg23t46
    contributor_orcid: null

dataset_contact_information:
  - orcid: null
    given_name: Stan
    family_name: Kaye
    email: kaye@pppl.gov
    affiliation: Princeton Plasma Physics Laboratory

originating_research_organization_ror_id: https://ror.org/03vn1ts68
name: Princeton Plasma Physics Laboratory

funding:
  - funder_name: U.S. Department of Energy, Office of Science (Fusion Energy Sciences)
    funder_ror_id: https://ror.org/01bj3aw27
    funding_type: contract
    grant_name: Operation of PPPL / NSTX Program
    grant_number: DE-AC02-09CH11466
    solicitation_number: null

facilities:
  - ror_id: https://ror.org/03vn1ts68
    name: National Spherical Torus Experiment Upgrade (NSTX-U)

tags:
  project: genesis
  science: fusion

keywords:
  - fusion
  - tokamak
  - spherical-torus
  - plasma-physics
  - time-series
  - MDSplus
  - magnetic-confinement
  - NSTX-U

release_review:
  - review_description: reviewed_general
    review_institution_ror_id: https://ror.org/03vn1ts68

dataset_release_date: 2026-02-26

task_category:
  - time-series
  - tabular

task_subcategory:
  - benchmark
  - physics-analysis

dataset_count_size:
  dataset_count_category: O(10k)
  dataset_count_unit: plasma discharges

landing_page_url: https://nstx.pppl.gov
dataset_doi: null
publication_date: null

# NSTX-U began plasma ops in 2015 and ended in 2016 due to a failure.
data_collection_start_date: 2015-01-30
data_collection_end_date: 2016-08-10

dataset_info:
  features:
    - name: shot
      description: NSTX discharge identifier associated with the experimental data.
      dtype: int32
    - name: time
      description: Time coordinate for diagnostic signals
      dtype: float64
    - name: plasma_current
      description: Plasma current (Ip)
      dtype: float64
    - name: toroidal_field
      description: Toroidal magnetic field (Bt)
      dtype: float64
    - name: electron_density
      description: Line-averaged electron density
      dtype: float64
    - name: diagnostic_signals
      description: Raw and processed diagnostic signals from NSTX MDSplus trees
      dtype: sequence

  splits:
    - name: full
      num_bytes: varies by shot
      num_examples: O(10k)

  example_instance: "Shot 141398, including raw and processed diagnostic signals from NSTX MDSplus trees"

download_size: varies by shot
dataset_unpacked_size: varies by shot

source_datasets: []

arXiv: []

doi: []

license: other
license_name: DOE Public Access Policy
license_link: https://www.energy.gov/downloads/doe-public-access-plan

access_conditions:
  - User registration including DOE Foreign National Access Program
  - Proposal submission 
  - User/Collaboration agreement 
  - Data use and publication agreement 
  - Data license for any commercial use

maintenance: This dataset is archived and maintained by Princeton Plasma Physics Laboratory. The NSTX-U device started operations in 2015 and ceased operations in 2016 following a failure. Operations will recommence in 2026 but a new dataset will be created. Access and curation are subject to PPPL data management policies.

---

# DRAFT Datacard for National Spherical Torus Experiment Upgrade (NSTX-U) Experimental Dataset

## Dataset Description

*Last Updated*: 2026-02-26

### Developed by
National Spherical Torus Experiment Upgrade (NSTX-U) Research Team at Princeton Plasma Physics Laboratory (PPPL), with contributions from the broader NSTX-U research program.

Contact: Stan Kaye (kaye@pppl.gov)

### Contributed by

NSTX-U research collaborators and diagnostic-specific teams across the operational lifetime of NSTX-U.

### Dataset Short Description

This dataset contains experimental plasma discharge data from the National Spherical Torus Experiment Upgrade (NSTX-u), a spherical tokamak operated at Princeton Plasma Physics Laboratory from 2015 to 2016. The dataset includes time-resolved measurements from magnetic, kinetic, and equilibrium diagnostics stored in MDSplus trees, covering approximately O(10k) plasma discharges.

### Timeframe of Data Collection

Data was collected between January 2015 and August 2016 during active NSTX-u operations. The data correspond directly to plasma discharges performed on the NSTX-U device during that operational period.

### Resources Used

- **Facility:** National Spherical Torus Experiment Upgrade (NSTX-U)
- **Institution:** Princeton Plasma Physics Laboratory
- **Funding:** U.S. Department of Energy Office of Science (Fusion Energy Sciences)
- **Data systems and storage:** MDSplus data acquisition and archival system
- **Computing:** PPPL internal computing clusters afor data access, decoding, calibration, and analysis

## Sharing/Access Information

Access to NSTX-U experimental data is subject to PPPL data access policies and DOE public access requirements. Access may require:
- User registration including DOE Foreign National Access Program
- Proposal submission 
- User/Collaboration agreement 
- Data use and publication agreement 
- Data license for any commercial use

### Recommended citation

```txt
@misc{NSTXU_Experimental_Data,
  title        = "{National Spherical Torus Experiment Upgrade (NSTX-U) Experimental Dataset (2015-16)}",
  author       = "{NSTX Research Team}",
  howpublished = "Princeton Plasma Physics Laboratory",
  year         = 2026,
  note         = "Access subject to PPPL data policy"
}
```

## Data & File Overview

The dataset consists of MDSplus trees organized by shot number. Each shot contains:
- Magnetic diagnostics
- Kinetic diagnostics
- Plasma current and field measurements
- Equilibrium reconstructions
- Auxiliary heating signals
- Diagnostic calibration metadata

Each shot is stored as a structured hierarchy within MDSplus.

## Methodological Information

### Data Acquisition

Data were collected using calibrated diagnostic instruments installed on NSTX-U, including:
- Magnetic probes
- Flux loops
- Thomson scattering
- Neutral beam diagnostics
- Spectroscopy systems
- Equilibrium reconstruction systems
Signals were digitized, timestamped, and stored in MDSplus trees.

### Preprocessing

Some signals may include:
- Calibration corrections
- Time alignment adjustments
- Reconstruction algorithms (e.g., EFIT01)
- Derived parameters (e.g., betaN, elongation)
Processing methods evolved over the operational period and are documented in associated technical reports.

### Reproducibility

NSTX experimental data are reproducible in the sense of traceability and re-processability. All raw measurements are archived in MDSplus trees and can be re-analyzed using documented calibration and reconstruction procedures. Re-running reconstruction algorithms may yield numerically different results depending on software versions; however, scientific conclusions are expected to remain functionally reproducible.

## Data-Specific Information

Each shot contains time-series signals sampled at diagnostic-dependent rates.

Example variables:

| Variable Name | Description | Unit |
|---------------|-------------|------|
| time | Time coordinate | s |
| Ip | Plasma current | A |
| Bt | Toroidal field | T |
| nebar | Line-averaged density | m^-3 |

Missing data may appear as NaN or diagnostic-specific sentinel values.

## More information

NSTX-U ceased operations in 2016 due to a failure. This dataset reflects the full operational lifetime of the original NSTX-U device from 2015-2016. A new dataset will be created when the NSTX-U operation is restarted in 2026.