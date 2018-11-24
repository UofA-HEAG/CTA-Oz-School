# Installation Instructions

We recommend to bring a laptop with a UNIX-based operating system (MacOS or Linux).
To install the software, you will need approx. 3GB of free disk space.
The different data sets will require additional disk space:  
* Galactic plane survey (8.3 GB)
* Galactic centre survey (4.4 GB)
* Extragalactic survey (2.5GB)
* AGN monitoring program (4.7GB)

## Datasets
We will provide copies of the data set during the meeting.

## Installation of python
I strongly recommend to use python via anaconda. Therefore, I will describe the installation of python via anaconda in the following.

#### MacOS
-	Download the Graphical Installer of anaconda 3.6 from https://www.anaconda.com/download/#macos
-	Follow the instructions

#### Linux
-	Download anaconda 3.6 from https://www.anaconda.com/download/#linux
-	In terminal:

```
bash Anaconda3-*-Linux-*.sh
<Enter>
yes
~/.local/anaconda3
yes
```
-	Restart terminal

#### Update (for both MacOS and Linux)
-	In terminal:
`conda update anaconda`
 
## Installation of gammapy
We will use gammapy to analyse the CTA data. You can find its documentation here: http://docs.gammapy.org/dev/install/index.html

To avoid messing up with other python projects you might be working on, I recommend to create a virtual environment for this tutorial. Therefore, download the file `environment.yml` and then:

`conda env create -f environment.yml`

This will create an environment with the name cta-oz, including gammapy. To access this environment, you have do activate it (every time you open a new terminal):

source activate cta-oz

In case, you don't want to install this environment, but only gammapy:

`conda install -c conda-forge gammapy`

In case, you don't use anaconda:

`python -m pip install gammapy`

#### Check Installation

To check the installation, type in the terminal:

```
python
import gammapy
print(gammapy.__version__)
print(gammapy.__path__)
exit()
```

If you get error messages, please check if you have done everything as described – otherwise please contact Sabrina.
