---
language:
  - en
datacard_version: 0.1.0
datacard_name: Datacard for NSTX Experimental Data (1999-2011)
title: National Spherical Torus Experiment (NSTX) Experimental Dataset

datacard_creation:
  created_by: ["Jai Sachdev"]
  created_date: 2026-02-17
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
    name: National Spherical Torus Experiment (NSTX)

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
  - NSTX

release_review:
  - review_description: reviewed_general
    review_institution_ror_id: https://ror.org/03vn1ts68

dataset_release_date: 2026-02-17

task_category:
  - time-series
  - tabular

task_subcategory:
  - benchmark
  - physics-analysis

dataset_count_size:
  dataset_count_category: 100K<n<1M  # [!TODO] Check this
  dataset_count_unit: plasma discharges

landing_page_url: https://nstx.pppl.gov
dataset_doi: null
publication_date: null

# NSTX began plasma ops in 1999 and later became NSTX-U after the upgrade period.
data_collection_start_date: 1999-02-12
data_collection_end_date: 2011-04-30

dataset_info:
  features:
    - name: shot
      description: NSTX discharge identifier associated with the image/video acquisition.
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
      num_bytes: 5000000000000 # [!TODO] Check this
      num_examples: 700000 # [!TODO] Check this

  example_instance: "Shot 141398, including raw and processed diagnostic signals from NSTX MDSplus trees"

download_size: 5000000000000 # [!TODO] Check this
dataset_unpacked_size: 7000000000000 [!TODO] Check this

source_datasets: []

arXiv: []

doi: []

license: other
license_name: DOE Public Access Policy
license_link: https://www.energy.gov/downloads/doe-public-access-plan

access_conditions:
  - Proposal Process
  - Collaboration Required
  - Data Use Agreement

maintenance: This dataset is archived and maintained by Princeton Plasma Physics Laboratory. The NSTX device ceased operations in 2011 following its upgrade to NSTX-U. No new data will be added. Access and curation are subject to PPPL data management policies.

---

# Datacard for National Spherical Torus Experiment (NSTX) Experimental Dataset

## Dataset Description

*Last Updated*: 2026-02-17

### Developed by
National Spherical Torus Experiment (NSTX) Research Team at Princeton Plasma Physics Laboratory (PPPL), with contributions from the broader NSTX research program.

Contact: Stan Kaye (kaye@pppl.gov)

### Contributed by

NSTX research collaborators and diagnostic-specific teams across the operational lifetime of NSTX.

### Dataset Short Description

This dataset contains experimental plasma discharge data from the National Spherical Torus Experiment (NSTX), a spherical tokamak operated at Princeton Plasma Physics Laboratory from 1999 to 2011. The dataset includes time-resolved measurements from magnetic, kinetic, and equilibrium diagnostics stored in MDSplus trees, covering approximately 700,000 plasma discharges. [!TODO] Check this

### Timeframe of Data Collection

Data were collected between February 1999 and April 2011 during active NSTX operations. The data correspond directly to plasma discharges performed on the NSTX device during that operational period.

### Resources Used

- **Facility:** National Spherical Torus Experiment (NSTX)
- **Institution:** Princeton Plasma Physics Laboratory
- **Funding:** U.S. Department of Energy Office of Science (Fusion Energy Sciences)
- **Data systems and storage:** MDSplus data acquisition and archival system
- **Computing:** PPPL internal computing clusters afor data access, decoding, calibration, and analysis

## Sharing/Access Information

Access to NSTX experimental data is subject to PPPL data access policies and DOE public access requirements. Access may require:
- Collaboration agreement
- Proposal submission
- Data use agreement
- No commercial reuse is permitted without authorization.

### Recommended citation

```txt
@misc{NSTX_Experimental_Data,
  title        = "{National Spherical Torus Experiment (NSTX) Experimental Dataset (1999-2011)}",
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

Data were collected using calibrated diagnostic instruments installed on NSTX, including:
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

NSTX ceased operations in 2011 and was subsequently upgraded to NSTX-U. This dataset reflects the full operational lifetime of the original NSTX device.
