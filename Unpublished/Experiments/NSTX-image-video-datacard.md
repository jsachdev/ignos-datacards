---
language:
  - en
datacard_version: 0.1.0
datacard_name: Datacard for NSTX Image and Video Diagnostic Data (1999–2011)
title: NSTX Image and Video Diagnostic Data (1999–2011)

datacard_creation:
  - created_by: ["Jai Sachdev"]
    created_date: 2026-02-17
    creation_method: manual

dataset_authors:
  - dataset_author_orcid: null
    given_name: NSTX Research Team
    family_name: Princeton Plasma Physics Laboratory
    affiliation: Princeton Plasma Physics Laboratory (PPPL)

dataset_contributors:
  - contributor:
      contributor_name: NSTX Research Team / Collaborators
      contributor_ror_id: https://ror.org/03vn1ts68
      contributor_orcid: null

dataset_contact_information:
  - orcid: null
    given_name: Stan
    family_name: Kaye
    email: kaye@pppl.gov
    affiliation: Princeton Plasma Physics Laboratory

originating_research_organization_ror_id: https://ror.org/03vn1ts68
originating_research_organization_name: Princeton Plasma Physics Laboratory (PPPL)

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
  - plasma-physics
  - spherical-tokamak
  - NSTX
  - imaging
  - video
  - high-speed-camera
  - computer-vision

release_review:
  - review_description: reviewed_restricted
    review_institution_ror_id: https://ror.org/03vn1ts68

dataset_release_date: 2026-02-17

task_category:
  - computer-vision
  - multimodal
  - time-series

task_subcategory:
  - scientific-imaging
  - video-analysis

dataset_count_size:
  dataset_count_category: 0 # [!TODO] Determine this
  dataset_count_unit: frames_or_videos_or_files

landing_page_url: https://nstx.pppl.gov
dataset_doi: null
publication_date: null

# NSTX began plasma ops in 1999 and later became NSTX-U after the upgrade period.
data_collection_start_date: 1999-02-12
data_collection_end_date: 2011-12-31

dataset_info:
  features:
    - name: shot
      description: NSTX discharge identifier associated with the image/video acquisition.
      dtype: int32
    - name: time
      description: Time coordinate(s) for frames relative to the shot timebase (seconds).
      dtype: float64
    - name: frame_index
      description: Frame number within a camera acquisition for a shot.
      dtype: int32
    - name: image_or_video
      description: Image frames and/or encoded video associated with specific diagnostics (format varies by system).
      dtype: image
    - name: camera_metadata
      description: Per-camera and per-shot metadata (e.g., frame rate, exposure, ROI/binning if available, timing alignment notes).
      dtype: sequence
    - name: calibration
      description: Calibration artifacts/coefficients when available (e.g., geometry mapping, intensity calibration notes).
      dtype: sequence

  splits:
    - name: full
      num_bytes: 0 # [!TODO] Determine this
      num_examples: 0 # [!TODO] Determine this

  example_instance: "Shot 141398, Camera 1, Frame 1" # [!TODO] Determine this

  download_size: 0 # [!TODO] Determine this
  dataset_unpacked_size: 0 # [!TODO] Determine this

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

# Datacard for NSTX Image and Video Diagnostic Data (1999–2011)

## Dataset Description

**Last Updated:** 2026-02-17

### Developed by

NSTX imaging and video diagnostic teams at Princeton Plasma Physics Laboratory (PPPL), with contributions from the broader NSTX research program.

Contact: Stan Kaye (kaye@pppl.gov)

### Contributed by

NSTX research collaborators and diagnostic-specific teams (camera owners, diagnostic physicists, engineers, and data/controls staff) across the operational lifetime of NSTX.

### Dataset Short Description

This dataset contains image and video measurements acquired on the National Spherical Torus Experiment (NSTX) at PPPL during NSTX operations (1999–2011). It includes high-speed camera data and other imaging/video diagnostics used to study plasma behavior, plasma–material interactions, visible emission, and transient events. NSTX supported multiple fast camera systems during operations.

### Timeframe of Data Collection

Data were collected during NSTX experimental operations, beginning with initial plasma operations in 1999 and extending through the NSTX era prior to the NSTX-U upgrade (1999–2011).

### Resources Used

- **Facility:** National Spherical Torus Experiment (NSTX)
- **Institution:** Princeton Plasma Physics Laboratory
- **Funding:** U.S. Department of Energy, Office of Science (Fusion Energy Sciences)
- **Data systems and storage:** PPPL archival storage and imaging data management workflows (format and system vary by camera and time period)
- **Computing:** PPPL internal computing clusters afor data access, decoding, calibration, and analysis

## Sharing/Access Information

### Reuse restrictions placed on the data

Access to NSTX experimental data is subject to PPPL data access policies and DOE public access requirements. Access may require:
- Collaboration agreement
- Proposal submission
- Data use agreement
- No commercial reuse is permitted without authorization.

### Recommended citation

```txt
@misc{NSTX_Imaging_1999_2011,
  title        = "{National Spherical Torus Experiment (NSTX) Image and Video Diagnostic Data (1999-2011)}",
  author       = "{NSTX Research Team}",
  howpublished = "Princeton Plasma Physics Laboratory",
  year         = 2026,
  note         = "Access subject to PPPL data policy"
}
```

## More information

NSTX ceased operations in 2011 and was subsequently upgraded to NSTX-U. This dataset reflects the full operational lifetime of the original NSTX device. This imaging/video dataset is commonly used alongside NSTX time-series data (e.g., MDSplus signals) for physics interpretation and analysis.

