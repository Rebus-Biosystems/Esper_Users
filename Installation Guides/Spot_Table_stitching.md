# Stitch RNA tables together using the FOV registration output 
This pipeline will stitch RNA tables after cell assignment and FOV registration. 

# Defualt parameters:
```bash

SHOW_TABLES_FULL = False             
SHOW_141 = False     
SHOW_BOTH = False      
USE_REGISTRATION_FILE = True 
SHOW_FOV_GRID = False           
image_size_default = 2048
MIN_CRA_COL_VALUE = 1.75
MAX_CRA_COL_VALUE = 8
PERFORM_CBR_FILT = False 
global PERFORM_CBR_FILTERING
PERFORM_CBR_FILTERING = True  
SHOW_NUCLEI_LOCATIONS = False 
DISK_SIZE = 2   
DISK_SIZE_NUCLEI = 4
SCALE_141 = 4
IMAGE_SIZE_SAO_DEFAULT = 4928

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
 

 
"--USE_DAPI_TO_FILTER",
help="This will indicate that the experiment uses DAPI cell location to filter outside boundaries",
action="store_true",
default=False,
 

 
"--SAVE_FEATURES_POINTS",
help="This will indicate that the experiment should save the csv files for tables and spots",
action="store_true",
default=True ,
     

 
"--DEFINED_RATIO_THRESH",
help="This will indicate that DEFINED_RATIO_THRESH to filter stuff",
type=float,
default=DEFINED_RATIO_THRESH ,
     

 
"--MIN_CRA_COL_VALUE",
help="This will indicate MIN_CRA_COL_VALUE to filter out stuff",
type=float,
default=MIN_CRA_COL_VALUE ,
  

 
"--MAX_CRA_COL_VALUE",
help="This will indicate MAX_CRA_COL_VALUE to filter out stuff",
type=float,
default=MAX_CRA_COL_VALUE ,
           

 
"--IMAGE_Y_SIZE",
help="This will indicate IMAGE_Y_SIZE",
type=int,
default=IMAGE_Y_SIZE ,
     

 
"--STITCH_RESULTS",
help="This will indicate to whether perform stitching ",
action="store_true",
default=STITCH_RESULTS,
 

 
"--STITCH_CELL_ASSIGNED_TABLES",
help="This will indicate to whether perform stitching on the cell assigned tables ",
action="store_true",
default=STITCH_CELL_ASSIGNED_TABLES,
     

 
"--PERFORM_CBR_FILTERING",
help="This will indicate to whether perform stitching on the cell assigned tables ",
action="store_true",
default=PERFORM_CBR_FILT,
     

 
"--SHOW_TABLES_FULL",
help="This will indicate to whether visualize the spot tables in Napari",
action="store_true",
default=SHOW_TABLES_FULL,
 

 
"--SHOW_141",
help="This will indicate to whether visualize the spot tables in Napari using 1.4.1 software output",
action="store_true",
default=SHOW_141,
 

 
"--SHOW_BOTH",
help="This will indicate to whether visualize the spot tables in Napari to compare 1.4.1 and automated spots output together",
action="store_true",
default=SHOW_BOTH,
 
````
