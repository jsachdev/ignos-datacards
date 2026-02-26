---
language:
  - en
datacard_version: 0.1.0
datacard_name: Datacard for NSTX-U Image and Video Diagnostic Data (2015–2016)
title: NSTX-U Image and Video Diagnostic Data (2015–2016)

datacard_creation:
  - created_by: ["Jai Sachdev"]
    created_date: 2026-02-26
    creation_method: manual

dataset_authors:
  - dataset_author_orcid: null
    given_name: NSTX-U Research Team
    family_name: Princeton Plasma Physics Laboratory
    affiliation: Princeton Plasma Physics Laboratory (PPPL)

dataset_contributors:
  - contributor:
      contributor_name: NSTX-U Research Team / Collaborators
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
    name: National Spherical Torus Experiment Upgrade (NSTX-U)

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

dataset_release_date: 2026-02-26

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

# NSTX-U began operations in 2015 and ceased operations in 2016 due to a failure.
data_collection_start_date: 2015-01-30
data_collection_end_date: 2016-08-10

dataset_info:
  features:
    - name: shot
      description: NSTX-U discharge identifier associated with the image/video acquisition.
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
  - User registration including DOE Foreign National Access Program
  - Proposal submission 
  - User/Collaboration agreement 
  - Data use and publication agreement 
  - Data license for any commercial use

maintenance: This dataset is archived and maintained by Princeton Plasma Physics Laboratory. The NSTX-U device started operations in 2015 and ceased operations in 2016 following a failure. Operations will recommence in 2026 but a new dataset will be created. Access and curation are subject to PPPL data management policies.

---

# DRAFT datacard for NSTX Image and Video Diagnostic Data (1999–2011)

## Dataset Description

**Last Updated:** 2026-02-26

### Developed by

NSTX-U imaging and video diagnostic teams at Princeton Plasma Physics Laboratory (PPPL), with contributions from the broader NSTX-U research program.

Contact: Stan Kaye (kaye@pppl.gov)

### Contributed by

NSTX-U research collaborators and diagnostic-specific teams (camera owners, diagnostic physicists, engineers, and data/controls staff) across the operational lifetime of NSTX-U.

### Dataset Short Description

This dataset contains image and video measurements acquired on the National Spherical Torus Experiment Upgrade (NSTX-U) at PPPL during NSTX-U operations (2015–2016). It includes high-speed camera data and other imaging/video diagnostics used to study plasma behavior, plasma–material interactions, visible emission, and transient events. NSTX-U supported multiple fast camera systems during operations.

### Timeframe of Data Collection

Data was collected during NSTX-U experimental operations, beginning with initial plasma operations in 2015 and extending through the NSTX-U era (2015–2016).

### Resources Used

- **Facility:** National Spherical Torus Experiment Upgrade (NSTX-U)
- **Institution:** Princeton Plasma Physics Laboratory
- **Funding:** U.S. Department of Energy, Office of Science (Fusion Energy Sciences)
- **Data systems and storage:** PPPL archival storage and imaging data management workflows (format and system vary by camera and time period)
- **Computing:** PPPL internal computing clusters afor data access, decoding, calibration, and analysis

## Sharing/Access Information

### Reuse restrictions placed on the data

Access to NSTX-U experimental data is subject to PPPL data access policies and DOE public access requirements. Access may require:
- User registration including DOE Foreign National Access Program
- Proposal submission 
- User/Collaboration agreement 
- Data use and publication agreement 
- Data license for any commercial use

### Recommended citation

```txt
@misc{NSTX_Imaging_2015_2016,
  title        = "{National Spherical Torus Experiment Upgrade (NSTX-U) Image and Video Diagnostic Data (2015-2016)}",
  author       = "{NSTX-U Research Team}",
  howpublished = "Princeton Plasma Physics Laboratory",
  year         = 2026,
  note         = "Access subject to PPPL data policy"
}
```

## More information

NSTX-U ceased operations in 2016 due to a failure. This dataset reflects the full operational lifetime of the original NSTX-U device from 2015-2016. A new dataset will be created when the NSTX-U operation is restarted in 2026.

