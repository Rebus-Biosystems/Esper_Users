# CellxGene generation module
This pipeline will process a given experiment folder to generate a cellxgene matrix.

# Defualt parameters:
```bash

IMAGE_Y_SIZE = 2048
THREAD_COUNT = 12
Calculate_THRESH_Params = False  
GEN_QC_PLOTS = True  
NUM_DOWNSAMPLE = 1
NUM_RAND_GENES = 4
DPI = 300 
MULTI_PROCESS = False  
REASSIGN_DISTANCE_TO_CELL = False 
MAX_DISTANCE_TO_CELL = 100
MIN_DISTANCE_TO_CELL = 0 

````

# List of input arguments
```bash

 
"--rootdir",
help="The input directory containing the experiment data. ",
metavar="dir",
default="",
 

 
"--outdir",
"-o",
help="Specify the output directory for results files. "
"If this is not specified then the files are written to the tmp dir.",
metavar="dir",
 

 
"--quiet",
help="Logging utils quiet.",
action="store_true",
default=False,
 

 
"--verbose",
help="Logging utils verbose.",
action="store_true",
default=False,
 

 
"--multiprocess",
help="Using a multiprocessing in Python.",
action="store_true",
default=MULTI_PROCESS,
 

 
"--threadcount",
help="Using a multiprocessing in Python.",
type=int,
default=THREAD_COUNT,
 

 
"--EEL",
help="This will indicate that the experiment is an EEL format vs HiFi",
action="store_true",
default=False,
 

 
"--IMAGE_Y_SIZE",
help="This will indicate that the experiment should save the csv files for tables and spots",
type=int,
default=IMAGE_Y_SIZE ,
     

 
"--Calculate_THRESH_Params",
help="Whether to recalculate the thresholding parameters",
action="store_true",
default=Calculate_THRESH_Params,
 

 
"--GEN_QC_PLOTS",
help="Whether to generate the Cell QC plots",
action="store_true",
default=GEN_QC_PLOTS,
     

 
"--MIN_DISTANCE_TO_CELL",
help="This will indicate that minimum distance between the spot and cells",
type=float,
default=MIN_DISTANCE_TO_CELL ,
     

 
"--MAX_DISTANCE_TO_CELL",
help="This will indicate that maximum distance between the spot and cells",
type=float,
default=MAX_DISTANCE_TO_CELL ,
     

 
"--REASSIGN_DISTANCE_TO_CELL",
help="This will indicate that the processing needs to reassign the spot t0o cell distance",
action="store_true",
default=REASSIGN_DISTANCE_TO_CELL,
 

````
