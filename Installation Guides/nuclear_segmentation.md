# Nuclei segmentation from DAPI channels. 

The default segmentaiton algorithm is Stardist. This pipeline will process a given experiment folder to segment the nuclei dapi.

# Default parameters:

```bash

IMAGE_Y_SIZE = 2048
SEGMENTTION_MODEL = "2D_paper_dsb2018" #"2D_versatile_fluo"
THREAD_COUNT = 12 
SHOW_PLOTS = False   
SEGMENT_FULL_STITCH = False
SAVE_SEGMENTATION_MASK = True 
SAVE_SEGMENTATION_METADATA = False   
RUN_SEGMENTATION_ALL_CYCLES = False   
LOAD_PRESAVED_CLASS = True 
UPPER_PERCENTILE = 99
LOWER_PERCENTILE = 5
dog_lower_param = 1
dog_upper_param = 50 

````

# Input Arguments: 

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
    help="Using a multiprocessing in Python.",
    type=int,
    default=THREAD_COUNT,
 

 
    "--EEL",
    help="This will indicate that the experiment is an EEL format vs HiFi",
    action="store_true",
    default=False,
 

 
    "--SAVE_SEGMENTATION_MASK",
    help="This will indicate that the experiment should save the segmentation mask",
    action="store_true",
    default=SAVE_SEGMENTATION_MASK,
     

 
    "--SAVE_SEGMENTATION_METADATA",
    help="This will indicate that the experiment should save the segmentation metadata",
    action="store_true",
    default=SAVE_SEGMENTATION_METADATA,
 

 
    "--RUN_SEGMENTATION_ALL_CYCLES",
    help="This will indicate that the experiment should run segmentaiton on all cycles vs only the first cycle",
    action="store_true",
    default=RUN_SEGMENTATION_ALL_CYCLES,
 

 
    "--SHOW_PLOTS",
    help="This will indicate that the experiment should show the debugging plots ",
    action="store_true",
    default=SHOW_PLOTS,
     

 
    "--IMAGE_Y_SIZE",
    help="This will indicate the image size in the Y direction",
    type=int,
    default=IMAGE_Y_SIZE,
     

 
    "--SEGMENTTION_MODEL",
    help="This will indicate the image size in the Y direction",
    type=str,
    default=SEGMENTTION_MODEL,
     

 
    "--SEGMENT_FULL_STITCH",
    help="This will indicate that the experiment should run the segmentation on a fully stitched mask",
    action="store_true",
    default=SEGMENT_FULL_STITCH,
     

 
    "--UPPER_PERCENTILE",
    help="This will indicate the upper percentile for identifying the normalization factors",
    type=float,
    default=UPPER_PERCENTILE,
     

 
    "--LOWER_PERCENTILE",
    help="This will indicate the lower percentile for identifying the normalization factors",
    type=float,
    default=LOWER_PERCENTILE,
    

 
    "--LOAD_PRESAVED_CLASS",
    help="Whether to load the presaved classes to speed up",
    action="store_true",
    default=LOAD_PRESAVED_CLASS,
 
