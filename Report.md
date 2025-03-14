# Plastic waste management 
Date: 2025-03-13

Authors: Daichi Ryo, Nicola Locatelli.
| Name | Specific Contribution in this Report |
| ----------- | ----------- |
| Nicola | Introduction  |
| Nicola | Data analysis, writing methodology |
| Nicola | Discussion and conclusion |
| Daichi | Theoretical framework and findings |
| Daichi, Nicola | Data preprocessing, visualization |
| Daichi | References and appendix  |


## Table of Contents  

1. [Introduction](#1-introduction)  
2. [Theoretical Framework](#2-theoretical-framework)  
3. [Methodology](#3-methodology)  
4. [Findings](#4-findings)  
5. [Discussion](#5-discussion)  
6. [Conclusions](#6-conclusions)  
7. [References](#7-references)  
8. [Appendix](#8-appendix)

## 1 Introduction

### 1.1 Background:

Plastic pollution is one of the biggest environmental crises of our time. Every year, over 400 million tonnes of plastic waste are produced worldwide, yet only 9% of it gets recycled (Geyer et al., 2017). Mismanaged plastic waste ends up polluting oceans, harming wildlife, and contributing to climate change (Jambeck et al., 2015).

In this study, we aim to explore the relationship between societal factors and plastic waste management by addressing the question: “How do different parts of society affect plastic waste management and where can we see correlations for these tendencies?” The motivation behind this research stems from the observation that countries with higher economic outputs often have more resources to invest in environmental infrastructure; however, the effectiveness of these investments may also depend on the population’s education level and awareness regarding sustainability practices.

### 1.2 Objectives

This study investigates whether GDP alone can be considered as a strong predictor of plastic waste management efficiency or if perhaps education plays a more significant role. By examining global data on economic growth, education levels, and plastic waste trends, we aim to uncover the factors that truly drive sustainable waste management.
 
This research focuses on four main objectives:
1. To analyse to which extent a  higher GDP correlates with better plastic waste.
2. To identify regional differences in how countries handle plastic waste.
3. To assess the role of education in shaping waste management policies and behaviours.
4. To determine whether education could be a key mediator between economic progress and sustainability.
 
### 1.3 Research Question:

How do different parts of society affect plastic waste management and where can we see correlations for these tendencies?

 Sub-questions include:

• How does GDP growth influence plastic waste management policies?

• Which regions show the most effective sustainability strategies?

• Is there a link between higher education levels and better waste management?
           
 
By answering these questions, we aim to contribute to the broader discussion on sustainability and policy-making, offering insights that could shape future environmental strategies.

## 2 Theoretical Framework 

In order to shed light on what aspects lead to the most influential and efficient way to approach waste management, we are going to start by defining key concepts and analyze the problem through the analysis of two already existing researches; This foundation is going to allow us to delve more clearly into the chosen aspects of GDP and education.

Our first topic of interest  is related to the correlation of a country’s GDP and how their plastic waste management develops. Related to this concept, I would like to introduce the first relevant citation from the journal, which is titled”Plastics recycling: Challenges and opportunities”.  In this article, plastic waste management refers to the various methods used to reduce, reuse, and recycle plastic waste. Common strategies include mechanical and chemical recycling, incineration, and landfill disposal. Additionally, some countries have introduced strict regulations, such as plastic ban and circular economy policies, to combat the issue [1].
In summary, economic growth, often measured by Gross Domestic Product (GDP), has been widely studied in relation to environmental degradation. It is interesting to note that the Environmental Kuznets Curve (EKC) suggests that pollution tends to rise with economic growth in the early stages but eventually declines as a country becomes wealthier and invests in sustainable policies [2].

The second question is about how important education is to improve and achieve better waste management. We hypothesized that Educating and Elevating our awareness of plastic pollution could lead to mitigate environmental challenges we are facing. 
Recently, some related research was carried out, “Cordier et al. developed one worldwide socio-economic model to forecast the influence of lack of education plastic pollution by using the data of the World Bank and pointed out that the amount of inadequately managed plastic waste will decrease by 34% compared to the business-as-usual scenario (Cordier et al., 2021) [5] ”. Soares et al. presented a study on the perceived importance of education and knowledge dissemination strategies on the mitigation of plastic pollution (Soares et al., 2021)[6]. These articles is one of the few studies currently focusing on the pathway to minimize plastic pollution through environmental education” On top this statement, Vicente-Molina et al. (2013) concluded that a 1% increase in individual environmental knowledge leads to a 0.4% increase in environmental behavior among university students through model estimation."[7]
This supports the idea that environmental education directly influences pro-environmental behavior, leading to better waste management. Starting from these resources we wanted to analyze from a broader perspective, how much impact both GDP and education have had on the development of better plastic waste management practices. We are going to analyze different geographical regions and countries, and their GDP and education levels from the year  between 2000 to 2020. 

## 3 Methodology

Our methodology is structured into three core parts: data collection, data processing, and statistical analysis. Each phase was of course critical in ensuring the reliability and validity of our findings.

### 3.1 Data Collection 

We sourced three primary datasets from Kaggle:

-Plastic Waste Management Data: This dataset provides country-level data on how nations manage plastic waste, including metrics such as recycling rates and waste processing infrastructure.
-GDP Data: In order to measure a country’s fiscal strength, we extracted economic indicators, including GDP per capita and overall economic growth.
-Education Data: In order to assess overall academic proficiency of a country’s population, we included and analyzed Educational metrics, such as literacy rates and school enrollment figures. 
We decided to select these datasets for the insightful and complementary perspectives that they offer in relation to our research question. The plastic waste management dataset in fact offers direct insights into environmental practices, while the GDP and education datasets allow us to explore potential correlations with economic and social developments.

### 3.2 Data Analysis Methods

#### 3.2a Data Processing

The initial datasets contained raw data, that’s where we had to undergo a significant cleaning and preprocessing process:
-Descriptive Overview: We began with the use of the .describe() function in Python to obtain a statistical summary of each dataset. This step helped us identify central tendencies, outliers, and data distributions.
-Handling Missing Data: We needed to apply the .isnull() function to detect missing values, and we also used the .dropna() method to remove rows with irreparable data, to reduce the impact of these gaps, and to remove rows with irreparable data and used .interpolate() to fill in minor missing values.
-Data Transformation: To ensure consistency across datasets we had to convert certain columns to numeric formats using .astype(). We also applied the .melt() function to restructure the data, making it easier to merge datasets by country codes and names.
-Merging Datasets: A critical step of  data processing involves merging the three datasets based on common identifiers such as ‘Country Name’ and ‘Code’. This was achieved through the .merge() function in pandas, which allowed us to align the data temporally (covering the period 2000–2021) and geographically.

#### 3.2b Statistical Analysis

After preprocessing, we also performed a series of statistical tests to examine the relationships between the variables:

-Descriptive Statistics: The descriptive analysis provided an initial understanding of the data’s variability and central trends.
-Pearson’s Correlation Analysis: This test quantified the linear relationship between GDP, education, and plastic waste management practices. For example, a high positive Pearson correlation coefficient between GDP and waste management efficiency would suggest that wealthier nations tend to manage plastic waste more effectively.
-Regression Analysis: To further understand predictive relationships, we conducted regression analyses. This allowed us to explore how variations in GDP and education levels could predict changes in plastic waste management outcomes.
-Data Visualization: Graphical representations such as line graphs and bar charts were crucial. The line graphs illustrated the temporal trends in plastic waste management across different regions, while bar charts enabled a comparative analysis between regions like Europe, America, Asia, MENA, and Sub-Saharan Africa.
The data analysis process, as shown in our presentation, clearly demonstrated the step approach from data cleaning to the final statistical interpretations. Another very significant role was played by visualizations, they were fundamental because they allowed conveying the insights, like possible correlations or  regional discrepancies.


### 3.3 Limitations

When dealing with our methodology, several limitations affected the study. One major challenge was the complexity of processing and cleaning large datasets. The chosen  datasets contained extensive information spanning multiple years and countries, significant effort  was required to manage missing values, align timeframes, and ensure consistency altogether across different sources.
Another limitation was the selection of relevant countries and geographic regions. Given the diversity of nations in terms of economic development, policy frameworks, and cultural attitudes towards waste management, deciding which countries to compare resulted challenging. While we surely aimed for a balanced selection, some regions had more comprehensive data than others, this could have led to potential biases in regional comparisons.
In relation to what i just mentioned, I want to state that we initially added more countries and continents, im referring to the US, China, India, Oceania; Some of these countries, especially the USA even offered interesting findings, but after including the education part of our research, we were obliged to take them out. We were not able to compare the plastic waste management and GDP data, and the related analysis that we had already made because we could not put it into correlation with the (missing) education data.
Furthermore, our analysis was again limited when trying to identify relationships between GDP, education, and plastic waste management. Even though different  statistical models were implemented they were still not necessarily able to give clear explanations for someone outside of our group that didn’t work with us through the whole project or even  establish causality. Additional limitations stem from  the fact that further elements such as policy enforcement, cultural attitudes, and technological advancements, may also play significant roles but were not explicitly analyzed due to data and time  constraints.
Lastly, data accuracy and completeness varied across different datasets. Some nations had for example missing or outdated records, requiring interpolation methods that may have introduced minor inaccuracies. Future research could benefit from a more meticulous analysis and polished data that could maybe employ the use of additional qualitative insights to complement the statistical findings


## 4 Findings



