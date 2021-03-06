---
title: Getting started with ∂a∂i for Windows Users
subtitle: Learn how to install ∂a∂i under a Windows environment
summary: Learn how to install ∂a∂i under a Windows environment
authors: 
- admin
tags: []
categories: []
date: "2019-02-05T00:00:00Z"
lastMod: "2019-09-05T00:00:00Z"
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ""
  focal_point: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

<b>Note: This post was written before the Windows Subsystem for Linux (WSL) was released. I now highly recommend Windows users interested in dadi (or bioinformatics of any kind) use Anaconda via the WSL instead of trying to work with Windows natively. See [here](https://towardsdatascience.com/setting-up-a-data-science-environment-using-windows-subsystem-for-linux-wsl-c4b390803dd) for a guide on how to set this up for yourself!
</b>
### Original post:

∂a∂i is a powerful and flexible population genetics model-fitting package for Python 2.X written by [Ryan Gutenkunst](http://gutengroup.mcb.arizona.edu/). It is a popular tool used in population and evolutionary genetics research for evaluating the fit of demographic models to DNA polymorphism data.

∂a∂i is slightly unusual that it is a Python package rather than a standalone piece of software. This makes using ∂a∂i an interactive process, particularly if one uses a dynamic coding platform such a Jupyter notebook. 

∂a∂i also has extremely handy functions that allow you to call the program *ms* by Richard Hudson via Python in order to simulate data. So *ms* and a working Python 2.7 (32 bit) installation are both prerequisites, which in turn have other prerequisites.

I normally use Mac OS and/or a Linux computing cluster for my day-to-day scientific computing. However, I recently installed ∂a∂i and all its dependencies from scratch on my Windows 10 PC. It was bit of a saga, and I wanted to share the exact steps I took, so as to ease the process for others.

Things that need to be installed (if you don't have them already):

- Anaconda 2.7 (32 Bit version)
- Cygwin
- The gcc compiler
- ms
- ∂a∂i

## Install Anaconda 2.7 (32 bit)

Anaconda is a pre-packaged version of Python maintained by Continuum Analytics. It includes a number of useful scientific packages, utilities, and a package manager in a single installation.

1. Uninstall any previous versions of Anaconda + restart Windows.

2. Install using the **32 bit** Anaconda installer available [here](https://www.continuum.io/downloads).

3. Restart windows.

## Install Cygwin + gcc compiler

ms requires compilation from source. If you do not have a compiler installed, installing Cygwin will allow you to quickly install the gcc compiler. Cygwin also gives access to many Linux-like utilities.


1. To install Cygwin, Follow Steps 1 & 2 [here](http://preshing.com/20141108/how-to-install-the-latest-gcc-on-windows/). 

2. After installing Cygwin, move the setup-x86_64.exe file you used to install Cygwin to the folder where you chose install Cygwin. Navigate to that folder in a command prompt. To install gcc, type:

		setup-x86_64.exe -q -P wget -P gcc-g++ -P make -P diffutils -P libmpfr-devel -P libgmp-devel -P libmpc-devel

3. Add the cygwin64/bin folder to your [system path](http://www.zdnet.com/article/windows-10-tip-point-and-click-to-edit-the-system-path-variable/).

## Install Richard Hudson's *ms*

1. Download and extract the zipped version of *ms* from the [ms website](https://uchicago.app.box.com/s/l3e5uf13tikfjm7e1il1eujitlsjdx13). 

2. Navigate to the folder where you extracted *ms*, and run:

		gcc -o ms ms.c streec.c rand1.c -lm

3. Add the folder containing ms.exe (the *ms* folder) to your [system path](http://www.zdnet.com/article/windows-10-tip-point-and-click-to-edit-the-system-path-variable/).

## Install the latest version of ∂a∂i

1. Go here: https://bitbucket.org/gutenkunstlab/dadi/downloads/ and choose "download repository" (not the .exe). 

2. Extract the contents to a folder (anywhere).

3. Navigate to the extraction folder in a command prompt. Then type:

		python setup.py install
		
Scan the output of this command for errors. Depending on the state of your system, you may need to install Visual Studio 9.0 C++ (follow the URL given in error message).
		
## Run the ∂a∂i example analysis

To confirm your installation works, run the example analysis provided in the repository you downloaded.

1. Copy the "example/YRI_CEU" folder from the extracted repository to a new folder (anywhere).

2. Open the Jupyter application.

3. In the file browser tab Jupyter opens, navigate to the newly created YRI_CEU folder and Create a new Python 2 notebook. This will open a new tab with a Python 2 notebook.

4. Open the 'YRI_CEU.py' script from the Jupyter file browser. This will open the script in a separate browser tab.

5. Copy,  paste and run (logically-selected) chunks of code from the .py to your new Python 2 notebook. 

6. Check for error messages + troubleshoot if necessary.


## Finished!

If the gods have smiled on you, you should now how a functioning installation of ∂a∂i. Before diving into an analysis, I highly recommend the following references by Ryan Gutenkunst et al.:

## Reading list

1. [The original paper describing ∂a∂i.](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1000695)

2. [The ∂a∂i manual.](https://bitbucket.org/gutenkunstlab/dadi/downloads/)

3. [A paper describing the use of the Godambe Information Matrix for model comparison in ∂a∂i.](https://academic.oup.com/mbe/article-lookup/doi/10.1093/molbev/msv255)

4. [A recent paper about integrating two-locus statistics into ∂a∂i.](http://www.genetics.org/content/early/2017/04/13/genetics.117.201251)

