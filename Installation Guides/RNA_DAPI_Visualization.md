# RNA & DAPI visualization
Visualize the RNA dots using Napari, CBR method of spot detection

# Defualt parameters:
```bash

SHOW_FOV_GRID = False           
image_size_default = 2048
MIN_CRA_COL_VALUE = 1.8
MAX_CRA_COL_VALUE = 5
SHOW_NUCLEI_LOCATIONS = False 
DISK_SIZE = 1  
DISK_SIZE_150 = 5
DISK_SIZE_141 = 5 
DISK_SIZE_NUCLEI = 4
SCALE_141 = 4
IMAGFE_SIZE_DEFAULT = 4928
DEFAULT_VISIBLE_DOTS = False  
MULTITHREAD = False  
multiprocessing_thread = 4
max_data_Size = 25000 
VISUALIZE_FEATURE_COLS = ['global_RNA_x', 'global_RNA_y', 'CBR', 'x', 'y']
NAN_VALUE = float("NaN" 
REMOVE_GENES_NOT_INTEREST = ["None", "none"]
CUT_OVERLAP = True 
Recon_size = 4928

````

# List of input arguments
```bash
 
"--rootdir",
help="The input directory containing the experiment data. ",
metavar="dir",
default="",

"--CUT_OVERLAP",
help="Whether cut the overlap x-y coordinates.",
action="store_true",
default=CUT_OVERLAP,

````
