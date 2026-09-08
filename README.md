[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.on008610-blue)](https://doi.org/10.82901/nemar.on008610)

# Raw Macaque Electrophysiology Dataset

## Overview
This dataset contains intracranial electrophysiology recordings from macaque VPL thalamus, acquired with a NeuroNexus V1x32-Edge (Vector Array) single-shank probe (32 sites, 100 µm pitch, 177 µm² iridium sites) on a Blackrock Cerebus system, during two conditions:

- Focused ultrasound (FUS) neuromodulation, with sonication targeted at either:
  - VPL thalamus (co-located with the recording array), or
  - insular cortex (recording remains in VPL)
- Tactile stimulation of the hand contralateral to the recording hemisphere (right-hemisphere VPL array → left-hand stimulation, unless a session notes otherwise)

FUS target (VPL vs insular cortex) and tactile stimulation side are recorded in each run’s `events.tsv` `stim_site` column—treat that as the authoritative per-trial record.

The data support the following publication:
Zheng, N., Yang, P.F., Phipps, M.A. et al. Transcranial focused ultrasound modulates spiking, LFP, and BOLD activity in the primate thalamus. *Nat Commun* (2026). https://doi.org/10.1038/s41467-026-75826-8

## Subjects
Species: *Macaca fascicularis* and *Macaca mulatta*  
Subject identifiers have been anonymized.  
Additional subject information is provided in `participants.tsv`.

## Experimental design
Extracellular electrophysiology was recorded from: VPL  
Focused ultrasound was targeted to: VPL or insular cortex  

The experiment included the following conditions:
- Focused ultrasound stimulation
- Tactile stimulation

Event timing and stimulation parameters are provided in the corresponding `events.tsv` files.

## Electrophysiology acquisition
Recording system: Blackrock Microsystems  
Recording hardware: CerePlex Direct with CerePlex M headstage  
Electrode/probe: NeuroNexus V1x32-Edge  
Number of channels: 32  
Sampling frequency: 30 kHz (spikes), 1 kHz (LFP)  
Recording hemisphere: Right  
Recording location: VPL  

## Data format
Raw Blackrock files were read with NPMK (`openNSx`, `openNEV`) in MATLAB and written to NWB using MatNWB.

File types may include:
- `.nwb`: raw electrophysiology recording and metadata
- `.tsv`: participant, channel, electrode, and event tables
- `.json`: metadata describing corresponding files

## Data included
sub-01:
- Spikes dataset: FUS stimulation in VPL (`ses-ieeg01`)
- LFP dataset: FUS stimulation in VPL (`ses-ieeg02`)
- Tactile stimulation (left hand) (`ses-ieeg03`)

sub-02:
- Spikes dataset: FUS stimulation in VPL (`ses-ieeg01`)
- LFP dataset: FUS stimulation in VPL (`ses-ieeg02`)
- Spikes dataset: FUS stimulation in insular cortex (`ses-ieeg03`)
- Tactile stimulation (left hand) (`ses-ieeg04`)

## Funding
This work was supported by NIH grants:
- NINDS RF1 NS126144
- NIBIB 1U18EB02935

## Contact
Li Min Chen  
Vanderbilt University Institute of Imaging Science, Vanderbilt University  
limin.chen@vanderbilt.edu

Li Min Chen
Department of Radiology and Radiological Sciences, Vanderbilt University Medical Center
limin.chen@vumc.org

## License
CC0