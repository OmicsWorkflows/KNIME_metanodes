# KNIME_metanodes
KNIME_metanodes repository contains metanodes for [KNIME](https://www.knime.com/) analytics platform for various tasks like data processing, visualization and evaluation.

## Metanodes preparation guidelines
We make the KNIME metanodes with the following guidelines in mind:
- metanodes should be easy to be used also by the user with no programming/scripting skills
- metanodes are made to be generally applicable to almost any wide format data table
- metanodes aim to make more complicated operations in KNIME easier and reproducible together with the KNIME workflows
- metanodes utilize open-source tools and programs (their list should be mentioned in the metanode description) 
- utilize in-build KNIME nodes where possible
- metanodes should be documented
  - metanode description should contains purpose, used tools and libraries
  - purpose of individual nodes used inside the metanode should be clear
  - documented code
  - documentation should be done in a way to make it clear how metanodes works 'under the hood' to also less experienced but interested users and to make them easily modifiable and or reusable
- metanodes should be usable stand-alone (expect extra programs and libraries 
mentioned in the description)
  - i.e. all scripts needed for data processing should be embedded in the metanode
  - this should make them reproducible in standardized environment like docker 
  container running KNIME (e.g. [KNIME_docker_vnc](https://github.com/OmicsWorkflows/KNIME_docker_vnc))

## How to use the metanodes in KNIME workflows

The metanodes may need extra KNIME extensions and or e.g. python or R libraries to work properly. You can use the metanodes within dedicated docker container running KNIME ([KNIME_docker_vnc](https://github.com/OmicsWorkflows/KNIME_docker_vnc), link to the docker images: https://hub.docker.com/r/cfprot/knime/) that has all necessary extensions already installed. 

You can use the metanodes in your local KNIME installation as well, please, consult the metanode description in KNIME for the list of extra KNIME extensions and or libraries needed and install them prior the metanode usage. 

To use the metanodes in your KNIME workflow follow these steps:
1) download '_Metanodes templates' folder (or individual metanode's folder)
2) move metanode(s) copy into your KNIME workspace folder (e.g. 'D:\knime-workspace\' on Windows or '/home/user/knime-workspace' on linux)
3) start KNIME; in case the KNIME is already running, refresh the KNIME workspace to refresh the workspace content (right click on the workspace in the KNIME Explorer sub-window and select Refresh)
4) drag and drop selected metanode into your KNIME workflow
5) connect the preceding nodes to the metanode input ports
6) double click on the metanode to get form window
7) adjust the metanode's setting (to make the individual settings adjustable, make sure the "Change" check box on the left side is checked)
8) run the metanode
9) check the metanode outcome, reset if needed 

## General metanodes features
- metanodes are versioned individually
   - versioning is done based on https://semver.org/

## List of used programs and extensions and the respective licences

Metanodes are made within docker container running KNIME accessible via VNC (https://github.com/OmicsWorkflows/KNIME_docker_vnc). The current version of the docker environment contains the following list of programs. Version numbers and the licenses might differ based on your local installation. Please inspect your local installation and contact us if you can not locate your local version and or license terms associated to the used metanode(s). Some applications may be provided to the metanodes separately, these are mentioned in Other applications section.  

#### Programs

- [KNIME](https://www.knime.com/)
  - The KNIME nodes consists of the following GNU GPL 3.0 License. Licence terms are available here: https://www.knime.com/downloads/full-license
- [Python](https://www.python.org/)
  - The Python consists of the following Python 3 License. Licence terms are available here: https://docs.python.org/3/license.html
- [R](https://www.r-project.org/)
  - The R consists of the following GNU General Public Licences. Licence terms are available here: https://www.r-project.org/Licenses/

#### KNIME extensions on top of the standard KNIME Analytics Platform installation

- KNIME Python Integration
- KNIME Interactive R Statistics Integration
- [OpenMS](http://www.openms.de/)
    - The OpenMS consists of the following BSD/3clause license. Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- [PIA](https://github.com/mpc-bioinformatics/pia)
    - The PIA consists of the following BSD/3clause license. Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause

#### Python 3 packages (alphabetical order)
- the follwoing list is not complete, mentions only selected packages without their dependencies etc.
- please see the requirements.txt file for the given KNIME docker environment version for more details and concrete versions
- [dash](https://github.com/plotly/dash)
    - The dash-bio consists of the following MIT license. Licence terms are available here: https://github.com/plotly/dash/blob/master/LICENSE
- [dash-bio](https://github.com/plotly/dash-bio)
    - The dash-bio consists of the following MIT license. Licence terms are available here: https://github.com/plotly/dash-bio/blob/master/LICENSE
- [matplotlib](https://matplotlib.org/)
    - The matplotlib consists of the following Python Software Foundation License (BSD compatible). Licence terms are available here: https://matplotlib.org/users/license.html
- [numpy](http://www.numpy.org/)
    - The numpy consists of the following BSD/3clause license. Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- [pandas](https://pandas.pydata.org/)
    - The pandas consists of the following BSD/3clause license. Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- [peptides](https://github.com/althonos/peptides.py)
    - The peptides consists of the following GPL-3.0 license. Licence terms are available here: https://github.com/althonos/peptides.py/blob/main/COPYING
- [scipy](https://www.scipy.org/)
    - The scipy consists of the following BSD/3clause license. Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- [seaborn](https://seaborn.pydata.org/)
    - The seaborn consists of the following BSD/3clause license. Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause
- [statsmodels](https://www.statsmodels.org/stable/index.html)
    - The statsmodels consists of the following BSD/3clause license. Licence terms are available here: https://opensource.org/licenses/BSD-3-Clause


#### R libraries (alphabetical order)

- [Biobase](https://bioconductor.org/packages/release/bioc/html/Biobase.html)
    - The Biobase consists of the following Artistic-2.0 license. Licence terms are available here: https://opensource.org/licenses/Artistic-2.0
- [imp4p](https://cran.r-project.org/web/packages/imp4p/index.html)
    - The imp4p consists of the following General Public License (GPL), version 3 license. Licence terms are available here: https://www.r-project.org/Licenses/GPL-3
- [impute](http://www.bioconductor.org/packages/release/bioc/html/impute.html)
    - The impute consists of the following General Public License (GPL), version 2 license. Licence terms are available here: https://www.r-project.org/Licenses/GPL-2
- [limma](https://bioconductor.org/packages/release/bioc/html/limma.html)
    - The limma consists of the following General Public License (GPL), version 2 license. Licence terms are available here: https://www.r-project.org/Licenses/GPL-2
- [Peptides](https://cran.r-project.org/web/packages/Peptides/index.html)
    - The Peptides consists of the following General Public License (GPL), version 2 license. Licence terms are available here: https://www.r-project.org/Licenses/GPL-2
- [pcaMethods](https://www.bioconductor.org/packages/release/bioc/html/pcaMethods.html)
    - The pcaMethods consists of the following General Public License (GPL), version 3 (or higher) license. Licence terms are available here: https://www.r-project.org/Licenses/GPL-3
- [plotly](https://cran.r-project.org/web/packages/plotly/index.html)
    - The plotly consists of the following MIT license and License file. Licence terms are available here: https://cran.r-project.org/web/licenses/MIT and https://cran.r-project.org/web/packages/plotly/LICENSE
- [preprocessCore](https://www.bioconductor.org/packages/release/bioc/html/preprocessCore.html)
    - The preprocessCore consists of the following GNU Library General Public (LGPL) License, version 2 (or higher) license. Licence terms are available here: https://www.r-project.org/Licenses/LGPL-2
- [proDA](https://const-ae.github.io/proDA/)
    - The proDA consists of the following GPL-3 license. Licence terms are available here: https://www.r-project.org/Licenses/GPL-3
- [Rserve](https://cran.r-project.org/web/packages/Rserve/index.html)
    - The Rserve consists of the following General Public License (GPL), version 2 license. Licence terms are available here: https://www.r-project.org/Licenses/GPL-2
- [UpSetR](https://cran.r-project.org/web/packages/UpSetR/index.html)
    - UpSet application (https://caleydo.org/tools/upset/) (The UpSet application consist of the following MIT license. Licence terms are available here: https://github.com/VCG/upset/blob/master/LICENSE)
- [vsn](https://bioconductor.org/packages/release/bioc/html/vsn.html)
    - The vsn consists of the following Artistic-2.0 license. Licence terms are available here: https://opensource.org/licenses/Artistic-2.0

#### Other applications

- [Reactome API](https://reactome.org/ContentService/)
  - Selected API of the Reactome pathway database, for more details see documentation of individual metanodes
  - The Reactome API consists of the two Creative Commons licenses: Creative Commons Public Domain (CC0) License and Creative Commons Attribution 4.0 International (CC BY 4.0) License. Licence terms are available here: https://reactome.org/license

- [UpSet](http://vcg.github.io/upset/about/)
  - Local copy of the project is under the Applications subfolder.
  - The UpSet application consists of the following MIT license. Licence terms are available here: https://github.com/VCG/upset/blob/master/LICENSE

- [UniProt API](https://www.uniprot.org/help/api)
  - selected API of the UniProt knowledge database are utilized
  - The UniProt API consists of the following Creative Commons Attribution (CC BY 4.0) License. Licence terms are available here: http://creativecommons.org/licenses/by/4.0/


## Do you have a question or wants to get involved?
The project is maintained by people from several laboratories (see below), but each metanode has 'contact person' who should be contacted first in case of any question. You can also [create an issue here](https://github.com/OmicsWorkflows/KNIME_metanodes/issues/new).

If you want to contribute to the project, contact us at david.potesil@ceitec.muni.cz.

### Code of Conduct
This project and everyone participating in it is governed by the [Code of Conduct](../master/code-of-conduct.md). By participating, you are expected to uphold this code. Please report any unacceptable behavior.

# Contributors

The project is maintained by people from several laboratories (in alphabetical order):
- [Laboratory of cellular communication](http://www.sci.muni.cz/bryjalab/), Department of Experimental Biology, Faculty of Science, Masaryk University, Brno, Czech Republic 
  - Kristína Gömöryová
- [Proteomics Research group](https://www.ceitec.eu/proteomics-zbynek-zdrahal/rg49), Central European Institute of Technology, Masaryk University, Brno, Czech Republic
  - Michal Cupák
  - Karolina Kryštofová
  - David Potěšil
- former collaborators
  - Anna Schneiderová

# Licence
This version of metanodes is available under the GNU GPL 3.0 License (see the [LICENSE](../master/LICENSE) file for details), unless stated otherwise.