# altorobank
sample integration with ASC4Auto using Github Action Runner

AppScan Source for Automation with Github Action Runner sample - Overview
To do this you have to have

Git download and install on your machine
Go to the project/repository and get the self-host runner installer
Setup and configure Self-hosted runner on your machine
Configure for your workflow and your scan script at Github
Run your workflow
Notes
The following 4 files in the repo are required:

main.yml <--- This is the pipeline configuration, notice in line 18, we call appscansrccli to run "cli_script.txt". Also notice line 9: (pool: 'Default') is the agent pool where my self-hosted 2016 windows server machine is located.
scanscript.scr <--- Runs AppScan Source CLI, will point to the .paf and ppf files to initialize the application
AltoroJ_1.paf <---- Need to be pre-generated in AppScan Source for Analysis (think of this as putting in the appscan-config.xml in the context of ASC)
AltoroJ_1.ppf <---- Need to be pre-generated in AppScan Source for Analysis (think of this as putting in the appscan-config.xml in the context of ASC)
