# Analyses of LFP data collected from Medtronic's PC+S System

I developed this script between 2018-2019 to analyze subject-level data from the
PC+S project at Mass General Hospital/Harvard Medical School. The data to be 
analyzed are in [Python MNE](https://mne.tools/stable/index.html)'s fif format. 
The PC+S system produces Local Field Potential (LFP) data in text files. 
In our analyses pipeline a collection of transfer scripts converts text data to 
.fif files using BIDS formatted metadata that include an anonymized identifier 
and time/visit information. The transfer scripts are not included here as I did 
not author those scripts.

For the present analyses we collected LFP data from sensing implants in striatum
and a cortical area located near supplementary motor area. Each implant sends 
data from two channels, therefore the analyses include four channels of data:
- Cortical Left
- Cortical Right
- Striatal Left
- Striatal Right

The PC+S system recorded data from the implants 4 times a day on average. The 
script relies heavily on session metadata to pick each day's data and aggregate 
LFPs per days. Time-domain LFPs are converted to frequency-domain. Finally, 
behavioral/affective scores derived from clinical questionnaries are then 
correlated with frequency-domain LFP measures.

At the time the study consisted of only one patient, so the analyses are not 
concerned with group level data and aggregate statistics. 

I included some plot examples produced from the scripts. Exact clinical scores
are not included here due to privacy. No metadata files are included in this 
repo.
