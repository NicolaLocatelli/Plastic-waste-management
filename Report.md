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
| Daichi | References  |


## Table of Contents  

1. [Introduction](#1-introduction)  
2. [Theoretical Framework](#2-theoretical-framework)  
3. [Methodology](#3-methodology)  
4. [Findings](#4-findings)  
5. [Discussion](#5-discussion)  
6. [Conclusions](#6-conclusions)  
7. [References](#7-references)  


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

Our first topic of interest  is related to the correlation of a country’s GDP and how their plastic waste management develops. Related to this concept, I would like to introduce the first relevant citation from the journal, which is titled”Plastics recycling: Challenges and opportunities”.  In this article, plastic waste management refers to the various methods used to reduce, reuse, and recycle plastic waste. Common strategies include mechanical and chemical recycling, incineration, and landfill disposal. Additionally, some countries have introduced strict regulations, such as plastic ban and circular economy policies, to combat the issue [[1](#ref1)].
In summary, economic growth, often measured by Gross Domestic Product (GDP), has been widely studied in relation to environmental degradation. It is interesting to note that the Environmental Kuznets Curve (EKC) suggests that pollution tends to rise with economic growth in the early stages but eventually declines as a country becomes wealthier and invests in sustainable policies [[2](#ref2)].

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

In relation to what i just mentioned, I want to state that we initially added more countries and continents, i'm referring to the US, China, India, Oceania; Some of these countries, especially the USA even offered interesting findings, but after including the education part of our research, we were obliged to take them out. We were not able to compare the plastic waste management and GDP data, and the related analysis that we had already made because we could not put it into correlation with the (missing) education data.
Furthermore, our analysis was again limited when trying to identify relationships between GDP, education, and plastic waste management. Even though different  statistical models were implemented they were still not necessarily able to give clear explanations for someone outside of our group that didn’t work with us through the whole project or even  establish causality. Additional limitations stem from  the fact that further elements such as policy enforcement, cultural attitudes, and technological advancements, may also play significant roles but were not explicitly analyzed due to data and time  constraints.
Lastly, data accuracy and completeness varied across different datasets. Some nations had for example missing or outdated records, requiring interpolation methods that may have introduced minor inaccuracies. Future research could benefit from a more meticulous analysis and polished data that could maybe employ the use of additional qualitative insights to complement the statistical findings


## 4 Findings


In our analysis, we examined the correlation between GDP, education levels, and plastic waste management in different regions. First, we compared GDP trends with plastic waste management efficiency across multiple countries from each continent level into micro level. First, we started to analyze this relationship from a macro level by looking at the general situation of the whole world.


1. Correlation Between GDP and Plastic Waste Management

At the world level, with the elevation of GDP, it still remains problematic with plastic waste management. On the other hand, from the perspective of the primary continent level , high-GDP countries like the United States and China generate significant plastic waste, but their management practices vary widely.


<img width="475" alt="スクリーンショット 2025-03-13 070559" src="https://github.com/user-attachments/assets/5b39551a-8c78-4256-8c7b-9c17a9a33f8f" />

[*F:01]
From the first set of data [*F:01], it can be seen that a significant rise in global GDP between 2000 and 2020. Simultaneously, the second dataset below indicates steady increases in all plastic waste management categories over the same period. On the whole, landfilled and mismanaged waste is still the dominant method of disposal, and recycling rates remain relatively low. The data suggests that it has not led to proportional improvements in sustainable plastic waste management from the perspective of worldwide view with the development of GDP.
This disparity raises important questions regarding whether wealthier economies are prioritizing sustainable waste management practices or if economic growth is merely amplifying waste-related issues. To explore this further, a more detailed analysis at the regional or national level will be conducted. 

<img width="251" alt="スクリーンショット 2025-03-14 184753 (17" src="https://github.com/user-attachments/assets/5b26f13c-18b8-4963-b544-d8e2d180662c" />

[*F:02]
Next step, we are going to analyze from the perspective of the primary region. Firstly, between 2000 and 2014, Asian countries experienced steady GDP growth, reflecting strong and consistent economic expansion. However, after 2014, economic trends became less stable, with fluctuations and a gradual downturn due to global challenges such as economic slowdowns and the COVID-19 pandemic in 2020.
In terms of waste management trends, it evolved alongside these economic changes. During the period of steady growth up to 2014, litter and mismanaged waste decreased, suggesting that as nations became more prosperous, they invested in waste management infrastructure and policies. Over time, reliance on landfills has declined, while recycling and incineration practices have expanded. This outcome reflects a growing commitment to sustainability in waste management across Asian countries.
![スクリーンショット 2025-03-14 184957](https://github.com/user-attachments/assets/ccc06bf6-195f-474a-9492-2403159a0545)

[*F:03]
Secondly, in the American continent, those countries have experienced a drastic surge in GDP. In contrast to Asian countries, improvements in plastic waste management have been characterized by a consistently high reliance on landfills, which has remained largely unchanged. However, recycling efforts have expanded. Here, it’s important to note that economic growth alone has not resolved the issue of mismanaged waste unlike our expectation we discussed before in the Americas. 

![スクリーンショット 2025-03-14 185025](https://github.com/user-attachments/assets/8aa084fe-145d-4598-9dc1-1baf85e1e452)

[*F:04]

I also want to add the interesting findings that we discovered that the USA is the  country showing high GDP but poor plastic waste management practices and development. Sadly, this is also as we will talk about in the limitations part. We couldn't really add this into our previous presentation which also included an education data set because we couldn't find a fitting correlation and a fitting data for education in the USA.
<img width="358" alt="スクリーンショット 2025-03-14 185111 (23" src="https://github.com/user-attachments/assets/2772dc8c-1628-406d-80e4-be93cdbb0fce" />

[*F:05]
Thirdly, Europe’s GDP grew steadily until 2008 but fluctuated following the financial crisis. During this period, landfill use declined significantly, while recycling and incineration increased. Unlike the previous regions discussed, Europe demonstrated notable improvements in plastic waste management despite economic fluctuations. Moreover, as the economy recovered, sustainability efforts resumed.
This trend underscores the link between economic prosperity and environmental initiatives while highlighting the disruptions caused by financial crises. Striking a balance between economic resilience and long-term sustainability is crucial for maintaining progress in waste management.











2. Correlation Between Education and Plastic Waste Management

Next, we examined the relationship between GDP trends and education levels across three primary regions. In a nutshell,  it is apparent  that countries with high education levels tend to have better waste management systems from our data set.Public awareness and environmental education campaigns have led to increased recycling rates and waste reduction in several regions. 
<img width="274" alt="スクリーンショット 2025-03-14 184924 (20" src="https://github.com/user-attachments/assets/47e98056-e0ba-41e7-8a9f-42098625bb78" />

[*F:06]
Firstly, in terms of education levels in Asia, these countries vary significantly across regions. East and Southeast Asia generally demonstrate higher and more stable education scores, reflecting strong educational systems. In contrast, South Asia shows lower median scores and greater variation, indicating inconsistencies in educational access and quality.
These differences in education levels appear to correlate with waste management practices. As you can see from the graph below, Countries with higher education scores, such as those in East Asia, tend to have more advanced waste management systems, including higher recycling rates and stricter regulations. Meanwhile, regions with lower education levels, such as parts of South Asia, often face challenges in plastic waste management due to limited recycling infrastructure and higher rates of improperly disposed waste.

![スクリーンショット 2025-03-14 184545](https://github.com/user-attachments/assets/52eaa245-40c9-4d96-bf4b-5bba4c693332)

[*F:07]
Next, education scores in the Americas show a wider distribution compared to Asia, as indicated by box and violin plots. Canada consistently ranks high, with scores comparable to Northern Europe, while countries such as Brazil, Mexico, and Colombia exhibit lower medians and greater variability.
Over a 20-year period, some nations, including Chile and Argentina, have shown gradual improvements in education scores. From an environmental perspective, the correlation between higher education levels and improved plastic waste management is more pronounced in the Americas than in Europe. This is due to the broader range of both education scores and waste management performance. For example, Canada combines high education scores with a well-developed recycling infrastructure and strong waste management policies.

<img width="487" alt="スクリーンショット 2025-03-14 184446 (12" src="https://github.com/user-attachments/assets/c5e75cf7-e013-4817-b667-24467606413c" />

[*F:08]
Finally, an analysis of education scores across various European countries reveals that Denmark, Finland, Germany, and Norway consistently rank among the highest, with scores typically above 94. The small range in their box plots indicates both high performance and consistent academic results.
From 2000 to 2020, the yearly score distribution remained stable or showed gradual improvement.
When comparing these education scores with plastic waste management data (analyzed separately), a pattern emerges: countries with strong education systems also tend to perform well in plastic recycling, waste reduction, and policy enforcement. While this suggests a positive relationship between education and effective waste management, it does not imply direct causation.

![スクリーンショット 2025-03-14 184611](https://github.com/user-attachments/assets/9f95c9e3-db8d-4536-80d8-091727150bb8)


[*F:09]
This bar chart highlights the Pearson correlation coefficient (r) between GDP and quality education for individual countries over two decades. We see values ranging from strongly positive to slightly negative:

 ● High Positive Correlations: In certain countries, a rising GDP is closely mirrored by improvements in education. This suggests effective policy channels that convert economic growth into tangible investments in schooling.
 ● Low or Negative Correlations: Some nations show minimal or even inverse relationships, indicating that economic gains are not always reinvested in the education sector—or that other structural factors (like inequality or governance) overshadow any direct GDP-to-education linkage. These findings reinforce that GDP alone is not a universal driver of better education.

## 5. Discussion

Interpretation of Findings:

Our analysis of plastic waste management in relation to GDP and education yielded mixed results, suggesting that economic growth alone is not a strong predictor of improved waste management. While some high-GDP countries showed better waste management practices, others continued to struggle with mismanagement despite economic expansion. This indicates that wealth alone does not guarantee effective plastic policies; rather other qualitative factors like government regulations, infrastructure, and societal awareness also play crucial roles.

GDP and Plastic Waste Management:

Economic growth did not always correlate directly with better plastic waste management. Although some high-income nations such as Germany, Sweden and Japan demonstrated strong waste management systems,  others like the USA, France and the UK, failed to implement effective strategies, highlighting the importance of additional factors such as regulatory frameworks and public awareness. The findings suggest that financial resources alone are insufficient in ensuring proper waste disposal and recycling; instead, a comprehensive approach that includes policy enforcement and infrastructural support is necessary.

Education and Plastic Waste Management:

A stronger correlation emerged between education levels and waste management efficiency. Regions with higher education scores, such as Europe, tended to have on average  lower rates of mismanaged plastic waste and higher recycling rates. Similarly, areas with lower education levels often struggled with persistent waste mismanagement despite economic growth. This pattern suggests that education plays a more significant role in fostering environmental awareness and promoting the implementation of effective waste management policies.

Regional Variations:

Significant regional variations were observed in plastic waste management practices. In Europe, countries with high education rates implemented effective policies, leading to increased recycling and reduced dependence on landfills. In contrast, Asia, including countries such as China and India, experienced substantial economic growth, yet waste management outcomes varied widely. While some nations made progress, others continued to face high mismanagement rates. In Oceania and the Americas, GDP growth was evident, but improvements in waste management remained inconsistent, further emphasizing that factors beyond GDP and education influence waste practices. The Middle East, North Africa (MENA), and Sub-Saharan Africa generally exhibited lower education levels, which correlated with higher mismanagement rates, reinforcing the notion that education might be a key driver in shaping sustainable waste management policies.

Implications of the Findings:

These findings challenge the assumption that economic prosperity alone leads to better environmental practices. Instead, even though more factors evidently influence plastic waste management practices, our findings still emphasize more the role of education as both a stronger link with better plastic waste developments and also as a mediator between economic growth and waste management; This means that policy interventions are necessary to ensure that economic resources are effectively allocated toward education sustainable waste management solutions, because knowing about the problem and knowing how to deal with it in a sustainable way are already big steps into better practices. Considering all the information that we were able to gather and analyze, a global shift in waste management strategies is required, prioritizing education, awareness, and policy enforcement rather than relying solely on financial growth as a determinant of environmental responsibility.





## 6. Conclusions

Our analysis revealed that GDP alone does not strongly correlate with effective plastic waste management. Despite higher economic resources, some wealthy nations continue to struggle with inefficient policies, due to a lack of public awareness, and ineffective recycling systems. This suggests that economic growth alone is not a reliable indicator of sustainable waste management practices. On the other hand, education appears to be a key mediator in improving plastic waste management. Countries with higher education levels generally demonstrate better waste management behaviors, likely due to increased awareness of environmental issues and stronger public participation in recycling initiatives. Since education is a low-cost and scalable approach, it presents a viable strategy for fostering sustainable waste practices globally.

Looking ahead, future research should explore qualitative aspects such as, how policy enforcement and cultural attitudes shape waste management. More importantly, countries must learn from successful case studies and apply these lessons to create sustainable, long term solutions for plastic waste. The challenge is big, but the solutions are within reach if we prioritise education, innovation, and investing in the right way by not forgetting to keep in consideration societal and cultural differences across the world.




## 7. References
<a id="ref1"></a>[1] Hopewell, J., Dvorak, R., & Kosior, E. (2009). "Plastics recycling: Challenges and opportunities." Philosophical Transactions of the Royal Society B: Biological Sciences, 364(1526), 2115-2126.  https://doi.org/10.1098/rstb.2008.0311
<a id="ref2"></a>[2] Grossman, G., & Krueger, A. (1995). "Economic growth and the environment." Quarterly Journal of Economics, 110(2), 353-377.https://doi.org/10.2307/2118443
[3] Kinnaman, T. (2014). "The economics of waste management." Journal of Environmental Economics and Management, 68(2), 273-289. https://digitalcommons.bucknell.edu/cgi/viewcontent.cgi?params=/context/fac_journ/article/1713/&path_info=WM7385.pdf 
[4] Ferronato, M., & Torretta, V. (2019). "Waste mismanagement in developing countries: A review of global issues." International Journal of Environmental Research and Public Health, 16(6), 1060.http://dx.doi.org/10.3390/ijerph16061060
[5] Cordier, M., Uehara, T., Baztan, J., Jorgensen, B., and Yan, H. (2021). Plastic pollution and economic growth: The influence of corruption and lack of education. Ecol. Econ. 182, 106930.
; https://doi.org/10.1016/j.ecolecon.2020.106930
[6] Soares, J., Miguel, I., Venancio, C., Lopes, I., and Oliveira, M. (2021). On the path to minimize plastic pollution: The perceived importance of education and knowledge dissemination strategies. Mar. Pollut. Bull. 171, 112890. https://doi.org/10.1016/j.marpolbul.2021.112890
[7] Vicente-Molina, M. A., Fernández-Sáinz, A., and Izagirre-Olaizola, J. (2013). Environmental knowledge and other variables affecting pro-environmental behaviour: Comparison of University students from emerging and advanced countries. J. Clean. Prod. 61, 130–138.  https://doi.org/10.1016/j.jclepro.2013.05.015


(2024). In: The ocean cleanup. URL: https://theoceancleanup.com/updates/global-plastics-treaty-why-legacy-plastic-cleanup-is-essential/ (plastic background)

(2018). In: Packaging Europe. URL: https://packagingeurope.com/plastic-packaging-time-to-pack-it-in/4595.article (packaging)

(2020). In: CBC. URL: https://www.cbc.ca/news/science/bottle-recycling-1.5416614 (bottles)

(2022). In: UNESCO. URL: https://oceanliteracy.unesco.org/plastic-pollution-ocean/ (ocean pollution)

(2020). In: PEW. URL: https://www.pewtrusts.org/en/research-and-analysis/articles/2020/07/23/science-study-shows-that-nearly-80-percent-of-the-annual-plastic-flow-into-the-environment (coast pollution)

(n. D.). In: Everyday Plastic. URL: https://www.everydayplastic.org/surveyold (headlines)

(n.D.). In: Freepik. URL: https://www.freepik.com/free-vector/clean-black-world-map-silhouette-style-template-design_68624446.htm#fromView=search&page=4&position=48&uuid=ffbef720-8e5f-44f0-b736-9c1d746893f8&query=world+map+ (worldmap)
 
Sources:
 
(2023). Environment education: A first step in solving plastic pollution. In: frontiers. URL: https://www.frontiersin.org/journals/environmental-science/articles/10.3389/fenvs.2023.1130463/full

Islam, S. (2023). Sustainable Development Data. In: kaggle. URL: https://www.kaggle.com/datasets/sazidthe1/sustainable-development-report?select=sdg_index_2000-2022.csv

Momeni, M. (2023). Plastic pollution. In: kaggle. URL: https://www.kaggle.com/datasets/imtkaggleteam/plastic-pollution?resource=download

(n.D.). Plastic pollution education: How awareness changes behaviours. In: TontoTon. URL: https://tontoton.com/plastic-pollution-education-how-awareness-changes-behaviors/
 
(n.D.). Plastikmüll und seine Folgen. In: Nabu. URL: https://www.nabu.de/natur-und-landschaft/meere/muellkippe-meer/muellkippemeer.html
 
(n.D.) The toxic impacts of plastic across it’s lifecycle. In: Center of International Environmental Law. URL: https://www.ciel.org/the-toxic-impacts-of-plastic-across-its-lifecycle/#:~:text=Using%20plastic%20consumer%20goods%20exposes,of%20animals%20and%20human%20tissue.
 
Tas, O. C. (2021). World GDP. In: kaggle. URL: https://www.kaggle.com/datasets/zgrcemta/world-gdpgdp-gdp-per-capita-and-annual-growths?resource=download

Use of AI:

For our project work we have made use of AI to help with data analysis issues, to give us ideas for the project outline as well as to help with phrasing.






