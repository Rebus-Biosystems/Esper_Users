Description
Esper data visualization and QC software that is built on napari. The data that can be visualized in napari includes: S image pyramids, detected RNA spots, cell segmentation results, and spot-to-cell assignments.

Current Status
As of August 2021, Esper Explorer consists of a couple .bat files, a couple .py scripts, and the acquisitonQC.

The .bat files are the UI. Users can edit the parameters (e.g. pick a gene to visualize) in a text editor and then run the .bat file to view their data without ever having to touch Python.

The .py scripts are what the .bat files call using the Esper Explorer’s Python executable.

The acquisitionQC package contains all the core functions that convert Esper data into formats that can be viewed in napari.

Future 
•	Use a forked version of the open source napari project that has been reskinned with Rebus Esper branding
•	Launch napari from a GUI window, rather than .bat files
•	Add feature where data edits in napari can be saved to disk and used for re-processing
o	E.g. Edit segmentation results and then re-run PerCellAnalysis
•	Package acquisitionQC so that installation is from a single file (e.g. wheel) rather than a git repo
•	Package acquisitionQC and any other scripts so that source code is not easily readable
•	Add a license/copyright that satisfies the license requirements of the Python packages used
•	Rename acquisitionQC to a more general name like esperQC now that it does more than just QC of acquired images
