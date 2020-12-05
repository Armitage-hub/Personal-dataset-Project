# Personal-dataset-Project

# Motivation
-The question that I set out to answer would be my personal wonder if the amount of extremely high temperatures in each county in Washington has any relationship with wildfires that took place in our state from 2009 - 2013. I chose to go with two datasets from thee Washington State Department of Health and went with the # of extreme hot days in each county as well as the # of wildfires in each county from 2009 - 2013. Oregon's wildfires that happened in September made me curious on the causes of wildfires in general, and if the global climate has anything to do with it, more specifically, the amount of extremely hot days. I decided to use our local data from our state to see if there is any relationship between the two variables, and if they correlate.  

# Data Sources
I combined two datasets from the Washington State Department of Health website and stumbled upon groupings for the # of extremely hot days per census block from 2009 - 2013 and the amount of wildfires in each county from 2009 - 2013. The derivation for the # of extremely hot days is based on the "number of days each year from 2000 onward that the maximum temperature exceeded the 99th percentile threshold at each station." The derivation for the # of wildfires is just the sum of all the wildfires that have occured in each county. I downloaded 5 different datasets per year for the # of extremely hot days  and 5 dataset for wildfires per county (all merged), all fitting within the yearly parameters. 

# Processing Steps
I gathered all of the data sets for five different datasets per year for the # of ectremely got days per year from 2009-2013 and they were all merged into one .csv file. I looked over the datasets by skiming all of the entries and tried to make sense on how the data is split. Since they are all split into census blocks, I had to use a method of making the data more comprehensible and more comparable to the # of wildfires data, as that dataset is split up by just county names and not census blocks. The steps that I needed to take for the census blocks was to use the groupby() function and aggregating the data by just county name and taking the mean of all of the amount of hot days over the amount of census blocks per county. I could not just sum every day up for each county, because that brings innaccurate results. The raw and processed data for extremely hot days consist of all five datasets and grouped county name with mean respectively. For the second dataset (# of wildfires) raw data consisted of also five data sets merged together for each year from 2009-2013 and has repeated county names, # of burned acres, # of fires, and percent area burned. For the processed data, I just decided to use one column, and the one I chose would be the number of fires. On the python notebook, I decided to use the same strategy of processing the data so it fits with the comparison of the other dataset by using the groupby() function for the county names, as well as aggragating # of fires burned by mean as well, to make the data more comparable to the other dataset given. The last step that I took would be merging both columns together, (avg # of extremely hot days and avg # of fires burned) making it easier to apply certain analytical tools to the new, trimmed dataset.
