Installation of latest acquisitionQC (includes all data QC functions)
Prerequisites: 
•	Anaconda Individual Edition Python version 3.8
•	Git 2.32.0 with Git Credential Manager Core
•	Access to https://github.com/opticalbiosystems/

22.	Make Repos folder on Desktop
23.	Open Anaconda Prompt
24.	chdir Desktop\Repos
25.	git clone https://github.com/opticalbiosystems/acquisitionQC.git
a.	Use your Github credentials
26.	chdir acquisitionQC
a.	You should be in the directory containing setup.py
27.	conda create -y -n explorer python=3.8
28.	conda activate explorer
29.	If pip not installed, conda install pip
30.	pip install --upgrade pip --user
31.	pip install .
32.	Copy .bat files to Desktop and .py files to folders on Desktop that match the paths in .bat files
