# Changelog

All notable changes to the KOVA3 dataset are recorded here.

Releases follow the versioning and correction policy in
[docs/versioning.md](docs/versioning.md). Published release paths are
immutable; corrections produce a new release rather than modifying an existing
one.

## [Unreleased]

Preparing the initial KOVA3 release (`v3.0.0`) from 10,988 Korean whole-genome
cohort records, in two tiers: an open allele-frequency layer and a
controlled-access layer holding the participant-level sequencing data.

Outstanding before launch:

- Joint genotyping run and export of the open tier
- Exact unique and unrelated sample counts after deduplication and QC
- Consent and governance evidence per cohort (consent instrument, IRB approval), recorded in docs/cohorts.md
- Data Use Agreement finalized after legal review, before the controlled tier opens
- Sample QC exclusion thresholds, and the rule that assigns a projected
  sample to an ancestry cluster
- Reconciliation of the data dictionary against the produced VCF header
- Per-sample manifest of read-level formats held for the controlled tier

Changed:

- Controlled tier: read-level data (FASTQ, CRAM) are excluded for the National
  Integrated Bio-Big Data (KOBIC) cohort at the data owner's request; its
  per-sample gVCF and multi-sample VCF genotypes remain. Korea10K CRAM is being
  prepared in addition to FASTQ.
- Controlled tier layout: participant-level objects are grouped by cohort under
  `data/<cohort>/{fastq,cram,gvcf}/` and keep the provider's file names
  (Korea4K renamed at upload); the per-sample manifest maps samples to keys.
- Tutorial notebooks
- S3 buckets and Registry of Open Data entry

<!--
Template for each released version:

## [vX.Y.Z] - YYYY-MM-DD

### Added
### Changed
### Fixed
### Superseded
-->
