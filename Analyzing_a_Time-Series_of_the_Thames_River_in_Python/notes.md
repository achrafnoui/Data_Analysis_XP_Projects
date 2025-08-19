Analysing a timeseries of The Thames river in python
Instructor: DataCamp Team
Data : the height of the thames river over the last century
primary goal : practice exploring a dataset

secendary goal : learn about autocorreclation and other time series analysis techniques
why : timeseries anaylysis is one of the most common type of analysis and flooding events are on the rise

key notes from the video project :
    - the river data is splited into 13 files ,each file is a point of tidal gauges , in this project we mainly gonna go for the london bridge point
    - python packages used in this shit : pandas , seaborn , matplotlib ,
    - the dataset of the london point contains : date and time , water level in meters  , flag = 1 high water / 0 low water
    - task 1 : imort and fix the data for analysis
    - lb = pd.read_csv('Data/10-11_London_Bridge.txt') 115503 rows
    - sniff around with lb.info and lb.describe
    - we drop a column named (HW=1 or LW=0) , it was a fuck up by pandas whem importing the shit
    - no null values found in the dataset
    - rename the columns for easier exploring : datetime , water_level , is_high_tide
    - fix the column dtype : 'datetime' to datetime , water_level to float
    - create df[month]= get it from df[datetime]
    - create df[year]= get it from df[datetime]
    - create a python fucntion that sun all of our works on cleaning the data : def cleaning_data() , so the next time we boot the jupyter notebook we don't have to run million blocks of shit
    - task 2 : analyse the london bridge data to get a sense of the water level
    - we plot the distribution of the water level in high tide and low tide using plt.hist()
    - same shit but now with box plot with sns.boxplot
    - box plot is way more readable than histplot
    - the box plot reveals a lot of upper outliers in lowtide plot , water usually is between -2 and -3
    - the box plot reveals a lot of lower outliers in hightide plot , water usually is between 3 and 3.7
    - we use df.describe to get the exact numbers instead of guessing them from the box plot
    - next we gonna count the numbers of alldays where high tide , and the count of days where the water level was above 75percentile in those all high days
    - we calculate the ratio of that shit ratio = very high tides day / all high tides days of the year
    - plot that shit with bar plot
    - we see an increasing amount of percentage takeover from 1890 till 2000 , it started as 3% but now skyrockited to 35% , someday it will cause a fucking disaster if you don't pull your shit together
    - next thing we gonna do the same shit with low tide
    - in low tide version , there is no changing ratio overtime , everything is cool and under control
    - task 3 : assess the monthly trends in 1927-1928-1929 ( the time of a fuckup disaster )
    - we create a dataframe called water_level wich contains the flag / time / median vaule of water level / month / year
    - in the data we got , the water level sometimes is mesured multiple times a day , wich leads us to use .resample('M').median() to calculate the median value of the month
    - we plot that shit in one plot , 3 plot line are created each of them represent a year , in the plot figure we draw a red line of the median vaule to know when the shit started to fuck up
    - we plot that shit twice , one in low tide mode , and other one in high tide mode
    - during low tide days , the water level usually spikes around october till the end of december
    - during low tide days , the water level usually spikes around august till the end of november
    -.resample() is something new to me , as this is the first time i analyse shit in time series
    - i have a strong feeling that i can do the work as a template and pass it on some diffrent points of the river to get even more analysis of the river on all of its body
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -
    -

