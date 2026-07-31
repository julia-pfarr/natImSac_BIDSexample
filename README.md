# Example BIDS Physio-EyeTracking Dataset - Binocular Recordings

This repo serves as an example for the BIDS Physio-EyeTracking specification (binocular recordings). 

The sourcedata was retrieved from https://github.com/mszinte/natImSac. Only the Eye Tracking data of the original dataset as well as only a few participants with only 2 of total 10 runs were kept for this example dataset. 

Sourcedata was converted to raw data according to the BIDS Physio-EyeTracking specification using the [eye2bids](https://github.com/bids-standard/eye2bids) converter tool. 

### Project information

By : Martin SZINTE
Project : natImSac
With : Guillaume Masson, Jason Samonds & Nicholas Priebe Version: 1.0

Experiment in which human participant free view natural images to determine saccade and fixation statistics. Published paper: https://doi.org/10.1523/ENEURO.0287-23.2023

### Getting the data

This dataset is managed with [DataLad](https://www.datalad.org/). The `.tsv.gz` physio and physioevents files are tracked via git-annex and stored on an OSF remote, so cloning the repo alone only gets you the file metadata, not the actual file contents.

1. Install DataLad (see detailed instructions in the [datalad handbook](https://handbook.datalad.org/en/latest/intro/installation.html)):

   ```bash
   pip install datalad
   ```

2. Install the `datalad-osf` extension, which is required to retrieve annexed content from the OSF remote:

   ```bash
   pip install datalad-osf
   ```

3. Clone the dataset:

   ```bash
   datalad clone https://github.com/julia-pfarr/natImSac_BIDSexample.git natImSac_BIDSexample
   cd natImSac_BIDSexample
   ```

4. Retrieve the actual data content:

   ```bash
   # get everything
   datalad get .

   # or get a specific file/subject
   datalad get sub-01/beh/sub-01_task-FreeView_run-01_recording-eye1_physio.tsv.gz
   ```
