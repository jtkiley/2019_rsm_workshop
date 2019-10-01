
# Workshop: Text Analysis and Machine Learning at RSM

The workshop is divided into six blocks, each with two 75 minute segments, with breaks between segments.


## Schedule

block | topic | day | time
---|------|-----|-----
0a | Introduction | Monday | 9:00-10:15
0b | Setup, Anaconda, and Jupyter | Monday | 10:30-11:45
1a | Python basics I | Monday | 13:00-14:15
1b | Python basics II | Monday | 14:30-15:45
2a | Data handling | Monday | 17:00-18:15
2b | Review and self-study tracks | Monday | 18:30-19:45
3a | Data retrieval I | Tuesday | 9:00-10:15
3b | Data retrieval II | Tuesday | 10:30-11:45
4a | Text analysis I | Wednesday | 9:00-10:15
4b | Text analysis II | Wednesday | 10:30-11:45
5a | Supervised learning | Wednesday | 13:00-14:15
5b | Unsupervised learning | Wednesday | 14:30-15:45


## Materials

There is a notebook and slide deck for each section.
The slides are available in zip archives containing Keynote and Powerpoint versions in the [releases](https://github.com/jtkiley/2019_rsm_workshop/releases) section.
Please note that the Keynote slides are the ones actually presented.

Also, there is an `environment.yml` file for setting up your Anaconda environment, using the instructions below.


## Install software

1. Install [Anaconda, Python 3.7 version](https://www.anaconda.com/distribution/).
1. (optional, but encouraged) Install Microsoft Visual Studio Code. The Anaconda installer asks if you would like to install it.
1. (experts-only alternative) Install miniconda instead of the GUI version. While there are direct download versions, you would typically use a package manager (e.g., brew on macOS, apt on Ubuntu). Similarly, you could install VS Code with your package manager as well.


## Importing the Anaconda environment.

1. Open the Anaconda Navigator app.
1. On the left, click Environment.
1. At the bottom of the resulting main window, click Import.
1. In the resulting popup, click the folder icon, navigate to the `environment.yml` file, and click Open.
1. Back in the import popup, the environment name should be filled in automatically from the file, `workshop` in this case. Click Import.
1. Wait for the packages for the environment to be downloaded and installed. This could take a few minutes.

**Note:** there is also a file named `environment_full.yml`.
This file is much more specific about particular software versions, and it is largely specific to both macOS and particular hardware.
I include it for documentation reasons, but you should generally use the more general (i.e. compatible) `environment.yml`.


## Install the Jupyter Lab Extension for Plotly

1. Open a terminal (on Windows, use the prompt labeled either "Anaconda Prompt" or "Anaconda (64-bit)" in the start menu).
1. Activate the `workshop` environment using the command `conda activate workshop`.
1. Install the extension using this command:

```jupyter labextension install @jupyterlab/plotly-extension```

**Note:** Officially, this jupyterlab plugin is being deprecated in favor of ones written by the plotly developers. [These instructions](https://github.com/plotly/plotly.py#jupyterlab-support-python-35) describe the installation for those plugins, though they did not work (with the pinned versions) in my testing (using the latest jupyterlab). A comment on an [issue](https://github.com/plotly/plotly.py/issues/1659) describes them as working if installed unpinned.


## Install TextBlob text corpora and spacy word models.

1. Open a terminal (on Windows, use the prompt labeled either "Anaconda Prompt" or "Anaconda (64-bit)" in the start menu).
1. Activate the `workshop` environment using the command `conda activate workshop`.
1. Install the corpora using the command `python -m textblob.download_corpora`. There may be warnings or errors that are not relevant for our purposes, but you should see a series of successful downloads.
1. Install the spacy English models using the command `python -m spacy download en_core_web_lg`.


## Resolving Potential Setup Issues

In a prior version of this workshop, it seemed that Anaconda was not reliably installing the `nytimesarticle` package used in block 3b. To resolve this issue, do the following:

1. Open a terminal (on Windows, use the prompt labeled either "Anaconda Prompt" or "Anaconda (64-bit)" in the start menu).
1. Activate the `workshop` environment using the command `conda activate workshop`.
1. Install the package using the command `pip install nytimesarticle`. There may be warnings or errors that are not relevant for our purposes, so long as you see that `nytimesarticle` was installed successfully.


## About Jason

Jason T. Kiley is an Assistant Professor and Spears Fellow at Oklahoma State University.
His research examines the interplay of audience perceptions of firms, impression management, and their associations with outcomes, including recent publications in the Academy of Management Journal and Strategic Management Journal.
As part of his work, he works to advance the use of software to increase the range, efficiency, and rigor of conducting empirical research.
He is a co-organizer of the annual AOM Content Analysis PDW, and his published and in-progress work often uses state-of-the-art content analysis techniques, including recent work with semantic text analysis and machine learning.
