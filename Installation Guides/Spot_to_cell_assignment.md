# Spot to cell assignment 
This pipeline will process a given experiment folder to assign the spots into the cells.

# Defualt parameters:
```bash

IMAGE_Y_SIZE = 2048
THREAD_COUNT = 14 
SHOW_PLOTS = False           
SAVE_CELL_ASSIGNMENT = True 
MAX_CELL_DISTANCE = 100 
ASSIGN_TO_FIRST_CYCLE = True 
REF_CYCLE_ASSIGNMENT = 1 
MIN_CBR_COL_VALUE = 1.75
MAX_CBR_COL_VALUE = 8
LOAD_PRESAVED_CLASS = True 
label_properties = ['centroid', 'area', 'perimeter', 'label']#, 'axis_major_length', 'axis_minor_length']
cell_specific_columns = ['assigned_cell', 'nucleus_area', 'nucleus_perimeter', 'global_nucleus_centroid_x', 'global_nucleus_centroid_y']

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
default=False,



"--threadcount",
help="Using a multiprocessing in Python.",
type=int,
default=THREAD_COUNT,



"--EEL",
help="This will indicate that the experiment is an EEL format vs HiFi",
action="store_true",
default=False,



"--SHOW_PLOTS",
help="This will indicate that the experiment should save the csv files for tables and spots",
action="store_true",
default=SHOW_PLOTS ,



"--IMAGE_Y_SIZE",
help="This will indicate that the experiment should save the csv files for tables and spots",
type=int,
default=IMAGE_Y_SIZE ,



"--SAVE_CELL_ASSIGNMENT",
help="This will indicate that the experiment is an EEL format vs HiFi",
action="store_true",
default=SAVE_CELL_ASSIGNMENT,



"--ASSIGN_TO_FIRST_CYCLE",
help="This will indicate that the spots are assigned to the first cycle dapi only",
action="store_true",
default=ASSIGN_TO_FIRST_CYCLE,



"--REF_CYCLE_ASSIGNMENT",
help="This will the cycle used as a reference for spot assignment to DAPI nuclei",
type=int,
default=REF_CYCLE_ASSIGNMENT,



"--MAX_CELL_DISTANCE",
help="This will indicate that the experiment should save the csv files for tables and spots",
type=float,
default=MAX_CELL_DISTANCE ,



"--MIN_CBR_COL_VALUE",
help="This will indicate the min ratio for CBR to drop",
type=float,
default=MIN_CBR_COL_VALUE ,



"--MAX_CBR_COL_VALUE",
help="This will indicate the upper end of the CBR thresholding",
type=float,
default=MAX_CBR_COL_VALUE ,



"--LOAD_PRESAVED_CLASS",
help="Whether to load the presaved classes to speed up",
action="store_true",
default=LOAD_PRESAVED_CLASS,


````
