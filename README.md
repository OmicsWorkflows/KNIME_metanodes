# KNIME_metanodes
KNIME_metanodes repository contains metanodes for [KNIME](https://www.knime.com/) analytics platform for various tasks like data processing, visualization and evaluation.

## Metanodes preparation guidelines
We try to make KNIME metanodes with the following guidelines in mind:
- metanodes should be easy to be used the end user with no programming/scripting skills
- metanodes are made to be generally applicable to almost any wide format data table
- metanodes aim to make more complicated things in KNIME easier and reproducible 
together with the KNIME workflows
- metanodes utilize open-source tools and programs (their list should be mentioned 
in the metanode description) 
- utilize in-build KNIME nodes where possible
- metanodes should be documented
  - metanode description should contains purpose, used tools and libraries
  - purpose of individual nodes used inside the metanode should be clear
  - documented code
  - documentation should be done in a way to make it clear how metanodes works 
  'under the hood' to also less experienced but interested users and to make 
  them easily modifiable and or reusable
- metanodes should be usable stand-alone (expect extra programs and libraries 
mentioned in the description)
  - i.e. all scripts needed for data processing should be embedded in the metanode
  - this should make them reproducible in standardized environment like docker 
  container running KNIME (e.g. [KNIME_docker_vnc](https://github.com/OmicsWorkflows/KNIME_docker_vnc))

## How to use the metanodes in KNIME workflows

The metanodes may need extra KNIME extensions and or e.g. python or R 
libraries to work properly. You can use the metanodes within dedicated 
docker container running KNIME 
([KNIME_docker_vnc](https://github.com/OmicsWorkflows/KNIME_docker_vnc), 
link to the docker images: https://hub.docker.com/r/cfprot/knime/) that 
has all necessary extensions already installed. 

You can use the metanodes in your local KNIME installation as well, please, 
consult the metanode description in KNIME for the list of extra KNIME 
extensions and or libraries needed and install them prior the metanode usage. 

To use the metanodes in your KNIME workflow follow these steps:
1) download '_Metanodes templates' folder (or individual metanode's folder)
2) move metanode(s) copy into your KNIME workspace folder (e.g. 
'D:\knime-workspace\' on Windows or '/home/user/knime-workspace' on linux)
3) start KNIME; in case the KNIME is already running, refresh the KNIME 
workspace to refresh the workspace content (right click on the workspace 
in the KNIME Explorer sub-window and select Refresh)
4) drag and drop selected metanode into your KNIME workflow
5) connect the preceding nodes to the metanode input ports
6) double click on the metanode to get form window
7) adjust the metanode's setting (to make the individual settings adjustable, 
make sure the "Change" check box on the left side is checked)
8) run the metanode
9) check the metanode outcome, reset if needed 

## General metanodes features
- metanodes are versioned individually

## List of used programs and extensions and the respective licences

Metanodes are made within docker container running KNIME accessible via VNC 
(https://github.com/OmicsWorkflows/KNIME_docker_vnc). The current version 
of the docker environment contains the following list of programs. Version 
numbers and the licenses (see below) might differ based on your local installation. 
Please inspect your local installation and contact us if you can not locate your 
local version and or license terms associated to the used metanode(s).

##### Programs

- KNIME 3.6.1 (https://www.knime.com/)
  - The KNIME nodes consists of the following GNU GPL 3.0 License. 
  Licence terms are available here: https://www.knime.com/downloads/full-license
- Python 3.6.5 (https://www.python.org/)
  - The Python consists of the following Python 3.6 License. 
  Licence terms are available here: https://docs.python.org/3.6/license.html
- R 3.4.4 (https://www.r-project.org/)
  - The R consists of the following GNU General Public Licences. 
  Licence terms are available here: https://www.r-project.org/Licenses/

##### KNIME extensions on top of the standard KNIME Analytics Platform installation

- KNIME Python Integration (org.knime.features.python2.feature.group/3.6.1.v201808311614)
- KNIME Interactive R Statistics Integration (org.knime.features.r.feature.group/3.6.1.v201808311614)
- OpenMS 2.3.0 (de.openms.feature.feature.group/2.3.0.201712211252)
    - The OpenMS consists of the following BSD/3clause license. 
    Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- PIA 1.3.7 (de.mpc.pia.feature.feature.group/1.3.7.v201803061425)
    - The PIA consists of the following BSD/3clause license. 
    Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause

##### python packages
- numpy 1.15.1
    - The numpy consists of the following BSD/3clause license. 
    Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- pandas 0.23.4
    - The pandas consists of the following BSD/3clause license. 
    Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- seaborn 0.9.0
    - The seaborn consists of the following BSD/3clause license. 
    Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- statsmodels 0.9.0
    - The statsmodels consists of the following BSD/3clause license. 
    Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- matplotlib 2.2.3
    - The matplotlib consists of the following Python Software Foundation License (BSD compatible). 
    Licence terms are available here: https://matplotlib.org/users/license.html
- scipy 1.1.0
    - The scipy consists of the following BSD/3clause license. 
    Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause

##### R libraries

- Rserve
    - The Rserve consists of the following General Public License (GPL), version 2 license. 
    Licence terms are available here: https://www.r-project.org/Licenses/GPL-2
- preprocessCore
    - The preprocessCore consists of the following GNU Library General Public (LGPL) License, version 2 (or higher) license. 
    Licence terms are available here: https://www.r-project.org/Licenses/LGPL-2
- limma
    - The limma consists of the following General Public License (GPL), version 2 license. 
    Licence terms are available here: https://www.r-project.org/Licenses/GPL-2
- Biobase
    - The Biobase consists of the following Artistic-2.0 license. 
    Licence terms are available here: https://opensource.org/licenses/Artistic-2.0
- vsn
    - The vsn consists of the following Artistic-2.0 license. 
    Licence terms are available here: https://opensource.org/licenses/Artistic-2.0
- pcaMethods
    - The pcaMethods consists of the following General Public License (GPL), version 3 (or higher) license. 
    Licence terms are available here: https://www.r-project.org/Licenses/GPL-3
- impute
    - The impute consists of the following General Public License (GPL), version 2 license. 
    Licence terms are available here: https://www.r-project.org/Licenses/GPL-2
- imp4p
    - The imp4p consists of the following General Public License (GPL), version 3 license. 
    Licence terms are available here: https://www.r-project.org/Licenses/GPL-3

## Do you have a question or wants to get involved?
The project is maintained by people from several laboratories (see below), but each metanode has 'contact person' who should be contacted first in case of any question. You can also [create an issue here](https://github.com/OmicsWorkflows/KNIME_metanodes/issues/new).

If you want to contribute to the project, contact us at david.potesil@ceitec.muni.cz 

### Code of Conduct
This project and everyone participating in it is governed by the [Code of Conduct](../blob/master/code-of-conduct.md). By participating, you are expected to uphold this code. Please report any unacceptable behavior.

# Contributors

The project is maintained by people from several laboratories (in alphabetical order):
- [Vitezslav Bryja laboratory](http://www.sci.muni.cz/bryjalab/) 
  - Kristína Gömöryová
- [Proteomics - Zbyněk Zdráhal Research group](https://www.ceitec.eu/proteomics-zbynek-zdrahal/rg49)
  - David Potěšil

# Licence
This version of metanodes is available under the GNU GPL 3.0 License, unless stated otherwise. The full version of the license terms is available at https://www.gnu.org/licenses/gpl.html .