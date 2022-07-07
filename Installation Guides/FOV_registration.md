# Register FOVs in the experiment folder. 

The algorithm is based estmating an approximatae placement of the frames given their adjacent shifts and fov name structure.
Following the rough estimation of the fov placement, the shifts between adjacent fovs are estimated accordingly using 
- First a feature-based matching algorithm. If the RMS error between the rough location of the new fov and the estimated map is large then:
- Matching using a phase cross-correlation algorithm, which is slower than the feature-based matching
- If the second method does not work either, the rough estimate is chosen as the desired FOV placement 
The routin can save several output images, via command line arguments given below:
- Saving rough estimate for each cycle
- Saving the stitched images for each cycle 
- A Json otput that contains all registrations for the entire run. The json file can be saved/load via Pandas dataframe
- The Json output format is: FOV, Cycle and Transformation           

# Default parameters:

```bash

fov_size_default = 1366 
NUM_IMG_STITCH_MAX = 75 
DAPI_NORMALIZATION_FACTOR = 55
N_RANDOM_ESTIMATE = 10
# RESIZE_FACTOR = 2
MIN_CBR_THRESH = 2 
RESIZE_FACTOR_COARSE = 4
expected_error_margin = 10 
FEATURE_MATCH_RATIO = 0.9
UPPER_PERCENTILE = 85
LOWER_PERCENTILE = 15
DEBUG = False   
MODULO = 2048

````

# Input arguments summary:

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



"--IMAGE_Y_SIZE",
help="This will indicate that the experiment should save the csv files for tables and spots",
type=int,
default=IMAGE_Y_SIZE ,



"--SHOW_PLOTS",
help="This will indicate that the experiment is an EEL format vs HiFi",
action="store_true",
default=SHOW_PLOTS,



"--COARSE_STITCH_FIRST_CYCLE",
help="This will indicate to perform coarse stitching",
action="store_true",
default=COARSE_STITCH_FIRST_CYCLE,



"--COARSE_STITCH_ALL_CYCLES",
help="This will indicate to perform coarse stitching on all cycles",
action="store_true",
default=COARSE_STITCH_ALL_CYCLES,



"--SAVE_STITCH_CYCLES",
help="This will indicate to perform coarse stitching on all cycles",
action="store_true",
default=SAVE_STITCH_CYCLES,



"--SAVE_STITCH_FIRST_CYCLE",
help="This will indicate to perform coarse stitching on all cycles",
action="store_true",
default=SAVE_STITCH_FIRST_CYCLE,



"--LOAD_PRESAVED_CLASS",
help="Whether to load the presaved classes to speed up",
action="store_true",
default=LOAD_PRESAVED_CLASS,

````
