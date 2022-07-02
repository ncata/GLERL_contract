
# GLERL Contract Activity Log - Nicholas Catanzaro 2022

## Note: Each time represents the beginning of a new group of activities. Most are related or are broken up around meals, meetings, or short breaks.

## 06/23/2022: NOAA GLERL/remote

- 08:30: Clock in
    * Plan daily tasks and check email
- 09:30:
    * Arrive at GLERL.
    * Review previous summer's code from SSF repo owg folder.
    * Review recent ReCON webcam images.
    * Update startup.docx tasks
- 10:00:
    * Review figures from [Dan Buscombe's paper on OWG](https://doi.org/10.1016/j.coastaleng.2019.103593).
    * Plan edits to [Prepdata.ipynb](https://github.com/ncata/SSF/blob/main/OWG/Prepdata.ipynb)
- 11:00:
    * Review potential owg sites on and off ReCON network in Lake Erie
- 12:00:
    * Managed AWS account.
    * Reached out to AWS about redeeming grant credits (Point of contact is OoO until July 4th).
    * Began familiarizing myself with No Tears Cluster, general HPC terminology and usage, and requirements to ssh into a cluster in order to run jupyter. May be more useful to adapt .py scripts from Dan's OWG_DNN repo.
- 13:45:
    * IT helps install software (Atom, Git, Anaconda)
- 14:30:
    * Cloned glerl_owg repo to local machine.
    * Created blank activitylog.txt, glerl_owg.yml, and startup_goals.txt files. Populate then attempted to commit and push activitylog.txt to repo. Failed due to incorrect directory management. Troubleshooted.
- 15:30:
    * Meeting with Steve R. (Fedwriters) on first week.
- 15:45:
    * Read over tc information and watched tutorial
- 16:00:
    * Identified correct directory path and removed local github repository. Will reclone later when on network.
    * Updated and populated local files
- 16:30: Clock out

## 06/23/2022: NOAA GLERL/remote

- 09:00:
    * Set up files on directory in c drive to host local copy of glerl_contract repo
- 09:30:
    * Reviewd git commands and best practices to ensure that upstream data maintains integrity. Branches should not be needed.
- 10:30:
    * Reviewed and forwarded docs from Steve R.
    * Emailed re:tc info after unsuccesful login
- 11:00:
    * Cloned git repo to appropriate direcotory and pushed local directory.
    * Updated activitylog.md
    * Populated .yml file and push to repository
- 12:30:
    * Talked to Steve Ru. (GLERL)
    * Created glerl_contract python env
    * Accessed tc info and logged hours
    * Populated startup_goals.md
- 14:00:
    * Started WeeklyReport_06.24.txt
    * Confirmed partial details of field work
    * Transfered code between repos
    * Did a python excercise to update GitHub profile and bio
    * File management/typing up activity log and weekly report.

## 06/27/2022 NOAA GLERL/remote

- 09:30:
    * Plan current tasks and populate .md file
    * Arrive at GLERL/set up workspace and check repos
- 10:20:
    * Being work on Prepdata_glerl.ipynb. Dan's code did not only include water. Try to only crop to square.
    * Looked into new IQA metrics. BRISQUE was thought of last summer but ultimately not used, images probably not high enough resolution.
    * OpenCv [Laplacian variance](https://pyimagesearch.com/2015/09/07/blur-detection-with-opencv/) may work for blur detection. [Rodrigo Loza Classify Day and Night Images](https://www.youtube.com/watch?v=dfcrYIu5LNo) for brightness
    * Planned additional code changes
- 13:00:
    * Spoke with Steve and Ed about field schedule. Report to GLERL tomorrow at 0800 and plan to be on CSMI cruise helping with bio sampling.
    * Break for lunch
- 13:50:
    * Tested Laplacian Variance. Inconclusive. Could be an indicator of wave detectability rather than blurs but further testing is needed.
    * Tested Loza's code for brightness. Requires pre sorted day and night dirs. to find theta value. May be better to stick with np.intensity as a QC metric. More research into QC metrics is needed.
- 14:30:
    * Considered other systems for directory management
    * Spoke with Ed confirming CSMI cruise participation.
    * Updated working lists
    * Worked on Prepdata_glerl notebook
    * Installed necessary packages into python environment.
    * Planned OWG trials.
- 17:00:
    * Break to exercise
- 18:00
    * Logs/other documentation, timecard, clockout.

## 06/28/2022 NOAA GLERL-Toledo Light

- 08:00:
    * Travel to NCYC
- 09:00:
    * MOB and transit to field site
- 09:30:
    * Begin field ops; webcam and HAB sensor installation
- 14:00
    * Transit back to NCYC
- 15:00
    * Drive back to GLERL
- 16:00
    * Arrive at GLERL

## 06/29/2022 - Remote

- 09:00:
    * Consider timeline for running OWG trials. Get data from GLERL before ship out on CSMI and run while on cruise.
    Must ensure Jupyter will run w/o internet.
- 10:00:
    * Read CSMI cruise plan
    * Prepare notes for meeting with Steve R. (Fedwriters)
- 11:00:
    * Meeting with Steve R. Confirmed presence on CSMI cruise
    * Reviewed csv_interpolation notebook from SSF repo
- 12:00:
    * GLERL Summer Fellow Lunch and Learn
        + Listened to Craig speak about modeling and Steve Ru. talk about sink holes in Lake Huron offshore Alpena, MI.
- 13:00:
    * Break for Lunch
- 14:30:
    * QC code updates
    * Manual image review of view 2 in mcy 2021
    * QC efficacy tests
        + Is manual review worth it? Increased data volume and batch size? Run trial on 06/30 for testing.
    * Further image blurriness review. Everyone is using laplacian, but that doesn't work well for water droplets it seems.
- 16:30:
    * Updating and troubleshooting prepowgimgs function. Does not like to be run twice. Is there an rm_tree function in shutil?
    * With no attempted QC on water droplets, x images with 2.5% not viable due to water droplets.
        + How does this compare to a normal QC attempt?
    * Troubleshooting code again after it failed multiple times to correctly assign file paths.
- 19:30:
    * Sign off

## 06/30/2022 - Remote

- 09:00:
    * Workshopped ideas to change up code to avoid issues from yesterday
- 10:00:
    * Code works, though Jupyter nbs are starting to shut down. Going to save push and reset.
    * Testing code with former sharpness QC results in 1.5k images with 2.7% not viable due to water droplets
        + deleted records from yesterday. Must rerun function with no sharpness QC to compare methods.
- 11:00
    * Rerun sharpness code.
    * Rerun prepowgims and create a csv file. Resulted in ~1.5k available images but only 569 were found to be acceptable for csv use. This is not enough.
        + Could we combine multiple (or all) years of data available. Would OWG still perform? I think it is worth a try at least. Might be awful, might just work. That will be todays trial. Create folder and csv file, port over on usb to GPU computer, then run owg notebook from there.
- 12:00:
    * Break for lunch
- 13:20:
    * prep images for testing
    * Compare images manually
    * Assess new file management structures
- 15:00
    * Review theory of csv_interpolation nb.
        + Logic may be flawed. So many images are thrown out. Why? interpolators may not be the best tool for the job.
    * Ran multiple tests on the nb. Many images were listed as outside interpolation range for next to no reason. Is mcy a poor site? Must explore other site opportunities
    * Wrote new logic to accomplish what was done in interpolation. Will code tomorrow if necessary.  
- 17:00:
    * Sign out and wrap up.

## 07/01/2022

- 09:00:
    * Emails
    * Reveiew yesterday's logic
    * Plan updates to pre-interpolation code as well as code
        + More reliable WVHT recordings would allow for more images to enter the OWG via the exclusion of noiser DPD and MWDIR recordings.  
- 10:00:
    * Start coding new notebook
- 11:00:
    * Meeting with Steve R. (Fedwriters)
    * Sign timesheet
    * Continue coding
- 13:00:
    * Break for Lunch
- 14:00:
    * Coding, testing, and running, Prepcsv_glerl.ipynb
    * Identified local vs UTC difference that could have serious consquences if unresolved
    * Tested and troubleshoot first function in notebook
    * Added commetns and markdown cells to notebook
- 17:00
    * Sign off
