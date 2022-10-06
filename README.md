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

* __you can get the self-hosted runner from "Settings > Actions > Runners" and see the status of your runner__
![Screenshot 2022-10-06 at 4 52 49 PM](https://user-images.githubusercontent.com/9972259/194268268-2b4e54c9-5814-43f5-addd-785d3bb0daba.png)

* __you can find the status of all your action__ 
![Screenshot 2022-10-06 at 4 53 16 PM](https://user-images.githubusercontent.com/9972259/194269052-c04f9428-2193-4e13-b4ea-cca956686d83.png)

* __you can find the logs of your actions__
![Screenshot 2022-10-06 at 4 57 42 PM](https://user-images.githubusercontent.com/9972259/194269507-abe0f97b-b6cd-4a8b-b283-402871f1536c.png)

* __you can run multiple runners at the same machine__
<img width="820" alt="Screenshot 2022-10-06 at 4 54 38 PM" src="https://user-images.githubusercontent.com/9972259/194269974-61a292fb-d95e-406f-9210-550ca7b34668.png">



