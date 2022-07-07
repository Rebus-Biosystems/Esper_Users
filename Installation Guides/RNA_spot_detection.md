# RNA spot detection
Find dots (or dot-like objects) and write csv output file. This pipeline will process a given experiment folder to detect RNA dots.

# Defualt parameters:
```bash

RAW_IMG_FORMAT = "lout"
RAW_IMG_FORMAT_OLD = "lsgd"
skip_gene_list = ["A", "B", "C"]
start_cycle = 6
reference_cycle = "Cyc01"
IMAGE_Y_SIZE = 2048
DEFINED_RATIO_THRESH = 1.5
THREAD_COUNT = 16 
LOAD_PRESAVED_CLASS = True 
CELL_DATA = False 

# Contrast ration upper and lower limits
UPSAMPLING = 1 
CONTRAST_RATIO_THRESH = 1.35 
CONTRAST_RATIO_UPPER_THRESH = 100 
SPREAD_LOWER_THRESH = 0.4
SPREAD_UPPER_THRESH = 50
CONTRAT_RATIO_CSV_THRESH = 1.5 
NEIGHBORHOOD_SIZE_MAX = 5 * UPSAMPLING 
NEIGHBORHOOD_SIZE_MIN = 5 * UPSAMPLING 
NEIGHBORHOOD_SIZE = 5 #15
NEIGHBORHOOD_SIZE_2 = 25  #15
GAUSS_KERNEL_PREP = 55 
SCALE = 10000

# Cell_data default params
NEIGHBORHOOD_SIZE_CELL = 7 
NEIGHBORHOOD_SIZE_CELL_2 = 15

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
default=True,


"--verbose",
help="Logging utils verbose.",
action="store_true",
default=False,


"--multiprocess",
help="Using a multiprocessing in Python.",
action="store_true",
default=False,


"--threadcount",
help="Using a multiprocessing in Python, number of threads.",
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
help="This will indicate the defined CBR ratio threshold",
type=float,
default=DEFINED_RATIO_THRESH ,


"--IMAGE_Y_SIZE",
help="This will indicate the image size Y",
type=int,
default=IMAGE_Y_SIZE ,


"--LOAD_PRESAVED_CLASS",
help="Whether to load the presaved classes to speed up",
action="store_true",
default=LOAD_PRESAVED_CLASS,


"--CELL_DATA",
help="This will indicate that the experiment is a cell culture. The background looks different from the tissue",
action="store_true",
default=CELL_DATA ,

````
