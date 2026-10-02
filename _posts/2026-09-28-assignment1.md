---
title: "Assignment 1"
last_modified_at: 2026-09-24T12:00:00-05:00
tags:
  - static sites
  - Markdown
  - Interactive Map
  - R
  - F26
---

## Background and Expectations 

Before beginning the analysis, I already knew that the UAE’s most populated cities are Abu Dhabi, Dubai, and Sharjah. I also had some background knowledge of the country’s history, including that the UAE was united in 1971 and is made up of seven emirates. Geographically, the UAE is located on the southeastern edge of the Arabian Peninsula and borders Saudi Arabia and Oman, with the Persian Gulf to the north and the Strait of Hormuz connecting it to the Gulf of Oman. I also knew that the UAE has large sandy deserts and dunes, as well as mountains, particularly toward the borders of Oman and around Al Ain. Having lived in the UAE for most of my life, I was also familiar with the country’s importance in oil and gas production and its growing diversity. 

For this analysis, I chose to explore three GeoNames feature codes: PPL, meaning populated place; TRB, meaning tribal area; and WLL, meaning well. Before mapping them, I hypothesized that populated places and tribal areas might be located near wells because wells can provide access to water in a dry environment. However, I realized that WLL can also include oil and gas wells, so the presence of a well on the map does not necessarily indicate access to freshwater. Because GeoNames does not provide further information on what type of well each individual point represents, I can not assume that there is a direct relationship between wells and human settlement based only on the map. I also initially expected tribal areas to be located more toward the southern areas of the UAE, which turned out to be different from what I found. 

The UAE dataset from GeoNames contained 8,585 rows, with major updates occurring in 2024 and 2012. The feature codes I chose were updated at different times: wells and tribal areas were largely updated in 2012, while populated places were largely updated in 2024. This approximately 12-year difference made me question whether the different layers are representing the UAE at the same point in time. For example, if the tribal-area data were updated today, I wonder whether some of these features would instead be classified as historical or heritage sites, or whether the number of tribal areas would change as the UAE has become increasingly urbanized. 

The main feature codes available in the dataset were PPLX, or section of populated place, with 1,983 rows; HTL, or hotel, with 1,577 rows; and WLL, or well, with 542 rows. I chose TRB because it immediately interested me. Since I have lived in such a modern and developed country for most of my life, I was surprised to see that GeoNames contained 81 tribal-area features. After experimenting with other codes such as oasis and area, I chose PPL because I wanted to compare the distribution of populated places with tribal areas. Following my professor’s suggestion, I then added WLL to see whether wells might reveal a spatial relationship between these different forms of human geography. 


<div style="width:100%; height:70vh;">
  <iframe
    src="{{ '/assets/maps/AE_featuremap.html' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy">
  </iframe>
</div>


## Computational Insights 

After filtering and mapping the three features using the Posit Cloud notebook, the first pattern I noticed was that wells were fairly dispersed across the country, with a slight concentration toward the northeastern part of the UAE, around areas such as Sharjah and Al Dhaid. Tribal areas, in contrast, were much more concentrated in the north, particularly around the older areas of Ras Al Khaimah and Fujairah. There were also around eight outliers much farther south. This was different from my original expectation that tribal areas would be more concentrated in the southern UAE.

I was also surprised that Bani YAS, which is considered a tribal confederation associated with Abu Dhabi, did not have a tribal-area point on the map. This made me question what GeoNames considers a “tribal area” and what information may be missing from the dataset. 

Populated places showed another interesting pattern. There were a few populated places around Abu Dhabi City, Al Ain, and Dubai, but I was particularly surprised by the density of PPL points around Fujairah and Ras Al Khaimah. One of the most unexpected concentrations appeared southwest of Abu Dhabi, where a curved line of populated-place points occurs near the Saudi Arabian border. 


<div style="width:80%; height:70vh;">
  <iframe
    src="{{ '/assets/images/LiwaArea.png' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy">
  </iframe>
</div>
Caption: Zooming into the southwestern UAE reveals a curved concentration of populated-place features toward the Saudi Arabian border

This area caught my attention because I recognized the name Liwa. Liwa is known for its desert festivals during the winter, and many people from Abu Dhabi and Dubai travel there to attend the festivals and see dune motorsports. Because I was curious about what the populated places around Liwa actually represented, I asked an Emirati friend who has been there. She explained that Liwa has many densely populated villages, which helped me understand that the PPL points on the map actually do represent the villages and smaller settlements rather than only large urban areas. It was interesting to see how these villages appear to form an almost curved line along a common street across the map. 

This also made me think differently about what I had initially assumed a “populated place” would look like. Since I am most familiar with the UAE’s major cities, I was unconsciously associating the population with large urban areas. The map showed me that GeoNames captures a much wider range of settlements. 

Overall, I think the distribution of wells looks relatively realistic based on what I know about the UAE. In school, I learned that oil and gas wells are distributed across different parts of the country and are not located inside major cities such as Abu Dhabi City or Dubai City. However, because GeoNames does not specify what type of well each WLL represents, this can count as a limitation when trying to interpret the relationship between wells and human settlement. 

One part of the dataset that seems less well represented is the distribution of populated places around Sharjah compared with Fujairah. Sharjah has a much larger population than Fujairah, but the map shows more PPL points in Fujairah. This made me wonder what qualifications GeoNames uses to classify something as a populated place. Does it include an equal representation of villages, small settlements, neighbourhoods, or historical settlements? This made me realize that the number of PPL points cannot simply be interpreted as a direct representation of population size. 

This connects to the “Do Maps Lie?” video because it made me think about how easy it is to look at a map and immediately treat its visual patterns as an accurate representation of reality. The map is showing me something accurate about the dataset, but I still need to ask who created the data, why particular features were included, how they were classified, and what might be missing. The video emphasizes that maps can influence how we interpret information, even when the map itself appears objective. In my case, seeing many PPL points around Fujairah could have easily led me to assume that Fujairah has more populated places than Sharjah in a meaningful demographic way, when the data may just be simply classifying smaller settlements differently. 

This connects to Kitchin and Lauriault’s argument that data is never simply “raw.” They explain that data is produced through categories, standards, technologies, institutions, and practices that influence what is recorded and represented. My experience with the PPL and WLL codes showed me how this can happen. A point labeled “populated place” or “well” seems straightforward, but the label does not really tell me everything about what the point represents. 


## GeoNames as a Data Assemblage 

Geonames can be understood as a data assemblage because data is constructed from information gathered from different sources and shaped by human decisions about what geographic features are included, how they are classified, and how they are represented spatially. Kitchin and Lauriault describe a data assemblage as the different institutions, infrastructures, practices, people, standards, and forms of knowledge that contribute to producing and managing data (8-9).

This helped me understand why the differences I noticed in the UAE dataset are important. For example, the fact that PPL, TRB, and WLL were updated at different times means that these features may not represent exactly the same moment in the UAE’s development. GeoNames classifies features according to its own system of classification, meaning that the UAE is being represented through a particular data structure rather than simply being copied directly from the physical world. 

The absence of a GeoNames ambassador for the UAE may also be one factor that shapes how the UAE is represented in the dataset. An ambassador could help verify local information, provide local sources, or address questions about specific features. More generally, the representation of the UAE may depend on which sources GeoNames has access to, who provides information, how features are classified, and when they are updated. 

GeoNames itself states that its data is provided without guarantee of accuracy, timeliness, or completeness. This helped me understand that some of the inconsistencies I noticed are not mistakes that make the dataset useless or unreliable. Instead, they are part of what makes the dataset interesting to analyze. The differences between the data and what I know about the UAE allow me to question where the information came from and what may be missing. 

Looking at the sources used by GeoNames, I also noticed that it draws information from multiple geographic information systems rather than relying on one UAE-specific source. For example, it uses sources such as the U.S. National Geospatial-Intelligence Agency and the U.S. Board on Geographic Names. At the same time, the UAE has its own developing national and emirate-level geographic-names databases. 

Kitchin and Lauriault argue that data assemblages are constantly changing as technologies, institutions, knowledge, and practices change. This made me think about the 2012 and 2024 updates in my dataset. The GeoNames map I interacted with is not necessarily a full picture of the UAE. If the dataset is updated, reclassified, or combined with other sources in the future, the map and patterns I see could also change.


## Transferability

As a political science major, I found this assignment useful because I learned how to navigate new coding and mapping techniques. I learned how to use a Posit Cloud notebook, run different packages, filter a dataset, observe spatial patterns, and think about where data comes from and how it's gathered. 

As I continue developing my interests in international relations, I think this type of mapping could become useful in future assignments and research projects. Being able to map different features across countries could help me compare geographical patterns and better understand how physical space, political history, and populations interact. More importantly, this assignment taught me that when I see a map, I should not automatically assume that it represents the full reality of a place. 

READY FOR GRADING