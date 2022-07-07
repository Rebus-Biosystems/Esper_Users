
<div align="center">
  <img src="https://rebusbio.com/wp-content/uploads/2022/04/cropped-logo-top-Rebus-Bio.png">
</div>

<div align="center">
  <img src="https://rebusbio.com/wp-content/uploads/2022/05/hero-apps-elucidate.jpg">
</div>

**`Documentation`** |
------------------- 

# Esper_Process 1.5 internal release documentation 

This document provides information on how to set up and utilzie the Python-based solution to run the automated spot detection pipeline end to end (v1.5).


# Installation guide:

## 1. Python version, requirements and environment setup 

```bash

Install Python 3.8.8 

````

### Create Python virtual environment for running the automated spot detection 

```bash

# Upgrade pip
python -m pip install --user --upgrade pip 

# Install python virtual environment
python -m pip install --user virtualenv 

# Create python virtual environment
python -m venv esper_15_env

# Instal the packages and requirements

````

## 2.1. Folder naming convention and data formats
This release will be able to address two different data formats from Esper, old format and the new format. In the old format, all raw data were stored in folders titled "CycXX" where as the new data format contains all data stored using the actual gene name. It is required to make sure the data folders are aligned with the following format: 
    
    Old Esper Data Format: 
    .
    root_folder
    ├── AcqData                   # Contains all the raw data acquired from the Esper system 
    │   ├── Cyc01R                # Individual cycle data
    │   ├── Cyc02R             
    │   ├── Cyc03R   
    │   ├── ... 
    │   ├── Cyc12R 
    ├── ProcessOutput             # The output data from Esper Process 1.4.1
    ├── SaoRecon                  # The contents are from SaoRecon algorithm using Esper Process 1.4.1
    ├── Results                   # The output from Esper Process 1.5 
    │   ├── CellxGene             # Cell by feature (gene) tables
    │   ├── Nuclei_Segmentations  # DAPI nuclei segmentation folder
    │   ├── QC_plots              # Contains QC plots for the detected dots, SNR information 
    │   ├── Registration          # Information associated with the FOV registartion, per FOV and all cycles
    │   ├── Spot_Cell_Assignment  # Individual FOV tables with associated cells assignment 
    │   ├── SpotTables            # Spot detection after the output of the spot detection algorithm 
    │   ├── Stitched_images       # Contains all stitched images, DAPI
    │   ├── Tables                # Contains all tables after stitching and spot assignment


    New Esper Data Format: 
    .
    root_folder
    ├── AcqData                         # Contains all the raw data acquired from the Esper system 
    │   ├── Cyc01_DJ19_c3.C.Ex532.lout  # Individual cycle data  
    │   ├── ... 
    │   ├── ...  
    ├── ProcessOutput             # The output data from Esper Process 1.4.1
    ├── SaoRecon                  # The contents are from SaoRecon algorithm using Esper Process 1.4.1
    ├── Results                   # The output from Esper Process 1.5 
    │   ├── CellxGene             # Cell by feature (gene) tables
    │   ├── Nuclei_Segmentations  # DAPI nuclei segmentation folder
    │   ├── QC_plots              # Contains QC plots for the detected dots, SNR information 
    │   ├── Registration          # Information associated with the FOV registartion, per FOV and all cycles
    │   ├── Spot_Cell_Assignment  # Individual FOV tables with associated cells assignment 
    │   ├── SpotTables            # Spot detection after the output of the spot detection algorithm 
    │   ├── Stitched_images       # Contains all stitched images, DAPI
    │   ├── Tables                # Contains all tables after stitching and spot assignment

## 2.2 Place the 'GeneTable.csv' in the root folder
The Esper Process software will look for the 'GeneTable.csv' file in the root folder to fill in the gene names as well as the cycles/lasers associated with each gene. 

** **Note that Windows does not recognize two filenames that identicial in lower case but given in a combination of lower/upper case as separate files and will mix them up. If the genem names are in a way that the same name repeats, better distinguish them using other annotation forms such as numbers or underscore sign ('_')** **

Visit https://docs.microsoft.com/en-us/windows/wsl/case-sensitivity 

The following table is an example GeneTable.csv file. The colum names indicate the cycle number, laser channel. The first column will identify the cycle number. 

| No.	| L595  | L647  |	L532  |
| --- | ----- | ----  | ----- |
| 1   |	  A   |   B   |   C   |
| 2   |   D   |   E   |   F   |
| 3   |   G   |	  H   |   I   |
| 4   |   J   |	  K   |   L   |
| 5   |   M   |	  N   |   O   |
| 6   |   P   |	  Q   |   R   |
| 7   |   S   |	  T   |   U   |
| 8   |   V   |	  W   |   X   |
| 9   |   Y   |	  Z   |   A2  |
| 10  |   B2  |	  C2  |   D2  |


## 3. Esper process 1.5 philosophy 
<img src="/Installation Guides/EsperProcess1.5_philisophy.jpg" alt="Alt text" title="Optional title">

## 4. Automated spot detection steps
<img src="/Installation Guides/EsperProcess1.5.jpg" alt="Alt text" title="Optional title">

## 4.1 Nuclei segmentation 
[Nuclei segmentation parameters guide](Installation%20Guides/nuclear_segmentation.md)

<img src="/Installation Guides/20220602_Esper Process Update-05.jpg" alt="Alt text" title="Optional title">

## 4.2 FOV registration from DAPI
[FOV registration parameters guide](Installation%20Guides/FOV_registration.md)

<img src="/Installation Guides/20220602_Esper Process Update-06.jpg" alt="Alt text" title="Optional title">

## 4.3 RNA spot detection
[RNA spot detection parameters guide](Installation%20Guides/RNA_spot_detection.md)

<img src="/Installation Guides/20220602_Esper Process Update-07.jpg" alt="Alt text" title="Optional title">

## 4.4 Spot detection quality metrics (QC)
[RNA spot detection QC parameters guide](Installation%20Guides/Spot_Detection_QC.md)

<img src="/Installation Guides/20220602_Esper Process Update-08.jpg" alt="Alt text" title="Optional title">

## 4.5 Spot to cell assignment 
[Spot to cell assignment parameters guide](Installation%20Guides/Spot_to_cell_assignment.md)

<img src="/Installation Guides/20220602_Esper Process Update-09.jpg" alt="Alt text" title="Optional title">

## 4.6 Spot table stitching
[RNA spot table stitching parameters guide](Installation%20Guides/Spot_Table_stitching.md)

<img src="/Installation Guides/20220602_Esper Process Update-10.jpg" alt="Alt text" title="Optional title">

## 4.7 Cellxgene matrix generation 
[Cellxgene matrix generation parameters guide](Installation%20Guides/Cellxgene_matrix_generation.md)

<img src="/Installation Guides/20220602_Esper Process Update-11.jpg" alt="Alt text" title="Optional title">

## 4.8 RNA visualization on Nuclei DAPI
[RNA & DAPI visualization parameters guide](Installation%20Guides/RNA_DAPI_Visualization.md)

<img src="/Installation Guides/20220602_Esper Process Update-12.jpg" alt="Alt text" title="Optional title">

## 5. Running the scripts to automatically fill the automated spot deteciton steps 
<img src="/Installation Guides/20220602_Esper Process Update-13.jpg" alt="Alt text" title="Optional title">
