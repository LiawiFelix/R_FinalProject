Topic: Corona 52 Week in 2020 Animated Plot
Team Member: 0716103 潘建琿,0716106 洪德輝,0716336 郭志龍

Library Used:\
-maps\
-dplyr\
-scales\
-ggplot2\
-animation\

Dataset:
https://data.europa.eu/euodp/en/data/dataset/covid-19-coronavirus-data

In this project we use maps library to get the world maps coordinate to map it. Using the world maps, we map thecorona virus infected distribution using the dataset. Because the some of the corona dataset region name didn't match with the available maps data. So we change the corona dataset region to match with the world map data(at line 26 to 198). In the world map data some region are separated therefore to match with our corona dataset we merge those region. some of the example are : "Saint Kitts" and "Nevis" are merged into "Saint Kitts and Nevis". This task is being done at line 205 to 218. After matching the corona dataset region name with the world map we left join the dataset.

Since in the corona dataset some of the country year-week (Week 1-Week 52(not always 52, depends with the available weeks)) doesn't always start from the Week 1 in the plotting it will cause the resulting join dataset when to be plotted there is an empty space. To avoid the world map plotting to be empty, first we plot the world map and then we plot the join dataset which plot the corona distribution on top of the world map.

In this project we plot 52 Weeks(maximum available weeks) of corona infected distribution. To plot the 52 Weeks we use for loops and using unique yearly-weeks data from the dataset we plot each week plot and put it into a list. After we get the 52 weeks dataset we use animation library to compile all the 52 plot into one GIF File. The GIF file will be saved on the workspace directory and can open it anytime.
