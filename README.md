**Eric Diep, CS 725 - Homework 9**

# Introduction
Water is essential to human survival. Having access to water is nice, but having access to clean water is better. Without clean water, the opportunity for diseases and infection increases. Most importantly, children growing up should have access to clean water because their immune system is still developing. Diarrhoeal diseases is the most common killer among children. According to UNICEF, in 2016, diarrhoeal diseases was the cause of approximately 8% of all deaths among children under 5. The question I attempt to answer with a visualization is can we identify correlation between having access to basic drinking water and sanitation, and mortality for children under 5 years caused by diarrhoeal diseases in South American countries? 

# Data
The datasets were provided as CSV files found on World Health Organization website. The datasets used are [basic and safely managed sanitation services data by country](http://apps.who.int/gho/data/node.main.WSHSANITATION?lang=en), [basic and safely managed drinking water services data by country](http://apps.who.int/gho/data/node.main.WSHWATER?lang=en), and [causes of child death; Proportion of deaths by cause](http://apps.who.int/gho/data/view.main.ghe3002015-SUR?lang=en).

In the datasets, basic and safely managed sanitation services / drinking water services, each contain a list of alphabetically ordered countries. For each country, there are columns populated with the percentage of population using either basic or managed sanitation services. These percentage values are further split between rural and urban areas. The dataset has values between the years 2000 and 2015.

The last dataset, causes of child death, contain a list of causes of death among children under 5 years. For each causes, there are columns populated with the percentage of children under 5 years who passed because of the cause. There are further categories for under 5: 0 - 27 days, 1 - 59 months, 0 - 4 years. The dataset has values between the years 2000 and 2016.

As stated from my [notebook for homework 7](https://git-community.cs.odu.edu/ediep/CS725-HW7/blob/master/NOTEBOOK.md), the aspect to highlight for the sanitation and drinking water services is the percentage of population in rural areas with access to basic drinking and sanitation services. Specifically for South American countries. The aspect to higlight for the causes of child death dataset is the percentage of children under 5 years who died because of diarrhoeal diseases in the South America countries. Mortality caused by diarrhoeal diseases is selected from the list of causes because it is the leading cause of child mortality when drinking water and sanitation is not well kept.

The dataset for causes of child death had further age categories under 5 years. I wanted to know the total percentage of child death caused by diarrhoeal diseases, so I added the values for 0 - 27 days, and 1 - 59 months. The value populating 0 - 4 years column was not added because I assumed it was included in the value populating the 1 - 59 months since 59 months is 4.9 years. The value populating the column 0 - 27 days is added to the value populationg 1 - 59 months to account for children before 1 month.

From these three datasets, the story to show is as access to basic drinking water and sanitation increases, the percentage of children under 5 years dying because of diarrhoeal diseases will decrease.

# Visualization
The final visualization is a single graph displaying multiple lines. Each line represents the categories: access to basic drinking services, access to basic sanitation services, and child mortality caused by diarrhoeal diseases. On the graph, the user is able to mouseover the graph to view the values for each categories in each year. Since the question is in regards to South American countries, there is a drop-down selection to allow the user to change the country to view the graph for the other South American countries. This visualization aids in answering the question, can we identify correlation between having access to basic drinking water and sanitation, and mortality for children under 5 years caused by diarrhoeal diseases in South American countries? Using the visualization, we can compare the trend of child mortality between countries, and identify if child mortality is decreasing or increasing depending on how access to drinking water and sanitation services trends.

# Design Decision
The multiple lines in one chart aids in spotting trends. The label at the end of the line allows to user to focus on graph rather than needing to look elsewhere for a legend. The red dots during mouseover movement highlights the values for each category. The values appearing next to the points gives an actual value for the user to view rather than having them guess the value.

# Development Process
In total, about 19 hours was spent on developing the visualization. The aspects which took to most time was finding a good question to answer by a visualization, finding the data necessary to answer the question, figuring out how the data needed to be formatted or split, and debugging the code.

# References
- [Basic and safely managed sanitation services Data by country by World Health Organization](http://apps.who.int/gho/data/node.main.WSHSANITATION?lang=en)
- [Basic and safely managed drinking water services Data by country by World Health Organization](http://apps.who.int/gho/data/node.main.WSHWATER?lang=en)
- [Causes of child death; Proportion of deaths by cause by World Health Organization](http://apps.who.int/gho/data/view.main.ghe3002015-SUR?lang=en)
- [UNICEF - Common Water and Sanitation Related Disease](https://www.unicef.org/wash/index_wes_related.html)
- [d3-time-format](https://github.com/d3/d3-time-format)
- [Multi-Series Line Chart by Mike Bostock](https://bl.ocks.org/mbostock/3884955)
- [Update data with button press by d3noob](http://bl.ocks.org/d3noob/7030f35b72de721622b8)
- [Multi-Series Line Chart with Multi-Mouseover by Eric Bunch](http://bl.ocks.org/eric-bunch/0bdef4942ac085a93fa6bd31452cd55c)