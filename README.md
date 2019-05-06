# Electric Vehicle Presence Discovery


The purpose of this project is to identify if a household has an electric vehicle or not. This information will help energy companies identify the needs of the consumers.  
 
The abstract reviews the overall objectives. There is also a slide deck that discusses the final results and evaluation. 

All of the data is located in the data folder. There are many scripts. Below is the proper order and description of each script. 

1. Electricity Pre-Processing

    This script loads the dataids of all homes in thhe pecan street program that were invovled in the program during the full duration of 2016-2018. It includes their total energy use for that time. This script groups the homes so that instead of an observation per hour per home, it is one observation per home. This scirpt is for general purposes of viewing and processing this data to make it easier to work with. 
    
2. Merge data andd preprocessing

    This script loads the metadata. This is similar to a data dictionary. It has the unique identify for each home which is how it merges with the electricity information. It also includes general infornmation about the home such as year built, if it has electric vehicles, if it has solar panels, the location and total square footage. 
    
3. Explore

    This script is for exploratory data analysis. 
    
4. Model building oversampling pre train test split

     This script is used to run models where oversampling technique had been used prior to the train test split. Here oversampling was viewed more as a preprocessing step than as a modeling tool. 
     
 5. Model Building oversampling post train test split
 
    This script reurns the models but does not do any oversampling until after train test split and then only the train data. This allows for a view of how the model will run on the raw original data instead of processed data. 
    
 6. Undersampling
 
     This script reruns the modesl but with undersampling instead of oversampling. This allows for an understanding of how oversampling can bias  a dataset. 
     
 7. dailydata
 
     This script brings in a dataset of Janaury 2017 and has the electricity data grouped by day. This allows for information on if time component affects the model. This script also includes the features from metadata. It reruns the model to asses if daily instead of total for three years energy usage provides different information on the homes. 
     
8. Survey

   This script loads the surveys that the homes in the program could fill out in 2017. Many homes chose not to use the survey. This survey provides more insights into the homes. Here we can see that more than half of the people with EV that filled out the Survey say that they never charge their vehicle at home. This explains why the models are not very accuarte. You can not predict who has EV baed on home electricity use if they do not charge their vehicle at home. 
