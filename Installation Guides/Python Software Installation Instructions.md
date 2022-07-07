# Esper_Process

Software (Python) Installation Instructions
How to setup environment 

Image Processing v1.4 Segmentation
Prerequisites: 
•	Anaconda Individual Edition Python version 3.8

1.	Open Anaconda Prompt
2.	conda create --name Segmentationv14 --file Segmentationv14-spec-file.txt
3.	conda activate Segmentationv14
4.	If pip not installed, conda install pip
5.	pip install --upgrade pip --user
6.	pip install -r Segmentationv14-requirements.txt --no-deps
Esper Process v1.5
Description


Installation
Prerequisites: 
•	Anaconda Individual Edition Python version 3.8
•	Git 2.32.0 with Git Credential Manager Core
•	Access to https://github.com/opticalbiosystems/

1.	Make Repos folder on Desktop
2.	Open Anaconda Prompt
3.	chdir Desktop\Repos
4.	git clone https://github.com/opticalbiosystems/acquisitionQC.git
a.	Use your Github credentials
5.	git clone https://github.com/opticalbiosystems/imageprocessing.git
6.	git clone https://github.com/opticalbiosystems/slicedimage.git
7.	conda create -y -n imageprocess15 python=3.8
8.	conda activate imageprocess15
9.	If pip not installed, conda install pip
10.	pip install --upgrade pip --user
11.	chdir imageprocessing
a.	You should be in the directory containing setup.py
12.	git checkout mcai-rebus-new-SaoRecon-format
13.	pip install .
14.	chdir acquisitionQC
a.	You should be in the directory containing setup.py
15.	pip install .
16.	chdir slicedimage
a.	You should be in the directory containing setup.py
17.	pip install .
18.	python -m ipykernel install --user --name=imageprocess15
19.	pip install pywin32==225
20.	Copy imageprocessing_20210520.py and Test-New-Esper-SaoRecon-Format.ipynb to a folder if you want to use those pipelines
Installation Guides
Esper Process v1.6
Description


Installation
Prerequisites: 
•	Anaconda Individual Edition Python version 3.8
•	Git 2.32.0 with Git Credential Manager Core
•	Access to https://github.com/opticalbiosystems/

1.	Make Repos folder on Desktop
2.	Open Anaconda Prompt
3.	chdir Desktop\Repos
4.	git clone https://github.com/opticalbiosystems/acquisitionQC.git
a.	Use your Github credentials
5.	git clone https://github.com/opticalbiosystems/imageprocessing.git
6.	git clone https://github.com/opticalbiosystems/slicedimage.git
7.	conda create -y -n imageprocess16 python=3.8
8.	conda activate imageprocess16
9.	If pip not installed, conda install pip
10.	pip install --upgrade pip --user
11.	chdir imageprocessing
a.	You should be in the directory containing setup.py
12.	git checkout mcai-rebus-watchdog-compatible
13.	pip install .
14.	chdir acquisitionQC
a.	You should be in the directory containing setup.py
15.	pip install .
16.	chdir slicedimage
a.	You should be in the directory containing setup.py
17.	pip install .
18.	python -m ipykernel install --user --name=imageprocess16
19.	pip install pywin32==225
20.	Copy ModularizeImageProcessing.ipynb to a folder if you want to use the modules in a Jupyter notebook
21.	Or use WatchdogScripts with the Watchdog software
