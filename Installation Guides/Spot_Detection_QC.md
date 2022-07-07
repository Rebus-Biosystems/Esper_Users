# Spot detection QC
# RNA spot detection QC
QC the detected spots on the image and save figures.

This pipeline will process a given experiment folder to perform QC on the detectd RNA dots or fiducial markers.

# Defualt parameters:
```bash

RAW_IMG_FORMAT = "lout"
RAW_IMG_FORMAT_OLD = "lsgd"
IMAGE_Y_SIZE = 2048
DEFINED_RATIO_THRESH = 2
THREAD_COUNT = 8

MAX_RATIO_DF = 5
MIN_RATIO_DF = 1.3
DATA_SAMPLING_FRACTION = 0.1 
TABLE_SAMPLING_FRACTION = 0.25
MIN_SIGNAl_INTENSITY = 700
MAX_SIGNAL_INTENSITY = 10000

SAVE_COMBINED_PLOTS = True   
SAVE_INDIVIDUAL_PLOTS = True 
SAVE_COORDINATES = True 
SAVE_SCATTER_VIOLINS = True  
SAVE_CYCLE_FOV_BOXPLOTS = True 
fig_size_default_hist2d = (16,16)

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

"--SAVE_FEATURES_POINTS",
help="This will indicate that the experiment should save the csv files for tables and spots",
action="store_true",
default=True ,

"--DEFINED_RATIO_THRESH",
help="This will indicate that the experiment should save the csv files for tables and spots",
type=float,
default=DEFINED_RATIO_THRESH ,

"--IMAGE_Y_SIZE",
help="This will indicate that the experiment should save the csv files for tables and spots",
type=int,
default=IMAGE_Y_SIZE ,

"--DATA_SAMPLING_FRACTION",
help="This will indicate that the fraction of the data used for plotting. Larger fraction means more time it takes",
type=float,
default=DATA_SAMPLING_FRACTION,

````
