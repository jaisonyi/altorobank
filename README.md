# altorobank
sample integration with ASC4Auto using Github Action Runner

# AppScan Source for Automation with Github Action Runner sample - Overview

To do this you have to have 
1. Git download and install on your machine
2. Go to the project/repository and get the self-host runner installer
3. Setup and configure Self-hosted runner on your machine 
4. Configure for your workflow and your scan script at Github
5. Run your workflow 

## Notes
The following 4 files in the repo are required:

* __main.yml__ <--- This is the pipeline configuration, notice in line 18, we call appscansrccli to run "scanscript.scr". Also notice line 9: (pool: 'Default') is the agent pool where my self-hosted 2016 windows server machine is located. 
* __scanscript.scr__ <--- Runs AppScan Source CLI, will point to the .paf and ppf files to initialize the application 
* __AltoroJ_1.paf__ <---- Need to be pre-generated in AppScan Source for Analysis (think of this as putting in the appscan-config.xml in the context of ASC)
* __AltoroJ_1.ppf__ <---- Need to be pre-generated in AppScan Source for Analysis (think of this as putting in the appscan-config.xml in the context of ASC)
