
# GLERL Contract Tasks
note: Several elements of this list have been begun or completed. This document is made as only a reference and for documentation of tasks to be completed and completed each week. It is updated as work on each task progresses    

## Office 

- Log hours for this week.
- Talk to admin re GSA driving training to start on training
- Complete IT Security Awareness training (require NOAA email-pending)

## OWG

- Read full README.md on OWG_DNN
    * If warranted, annotate pdf of Dan's paper and save locally in c/njc/docs/glerl_docs
- Review HPC Access
    * AWS credits cannot be accessed until July 5th at the earliest. Learn more about running scripts or launchign jupyter in No Tears cluster
    * Explore other options for HPC use (WHOI? NOAA?)
    * Always consider if this can be done with available computing resources. What is at GLERL and how do I access it?
- Optomize OWG Code
    * What model hyperparameters can be modified. With enough data can we keep 16?
    * New QC code implementing OpenCV2 for brightness and blur. Quanatatively (theta and historgram) establish thresholds  
    * Combine creation and serpeation into viewpaths with the intial copying of ReCON images to reduce processing time. 
    * Refresh underlying understanding of interpolation into csv.
    * Turn validation splitting code into function. Clean up the notebook and make a glerl_owg.py file 
        + Either split up prep_owg function and store with .csv interpolation function in one notebook/.py or combine them into a "master" function. 
- Run new OWG trials
    * Will I need to run wget linux commands to access entire GLERL archives or can I access directly in the lab? 
    * Multiyear trials, new QC code at mcy (or other site as reccomended). 
    * Will the model function better on more recent data?
## Field

- Talk to chief sci and review crusie plan for CSMI cruise from July 5-15
- Note potential Erie work  (or the 28th!) 
