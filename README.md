# RAINFALL-PATTERN-CROP-SUITABILITY-ANALYSER
In this project comparisons among different regions’ rainfall patterns are made to asses whether or not certain crops can be grown in those regions.   
Monthly rainfall in mm from January to December : 
- Kampala = [120, 140, 180, 200, 220, 180, 90, 70, 60, 100, 110, 130] 
- Gulu = [ 8, 25, 75, 160, 190, 145, 170, 215, 175, 150, 60, 15] 
- Mbarara = [ 70, 85, 120, 140, 90, 25, 20, 55, 100, 125, 120, 90] 
- This code was edited with the aid of CODEX, an Artificial Intelligence powered tool.
### IMPLEMENTATION
- Created a Region class with rainfall as a NumPy array and has methods for annual total, mean, wettest/driest month, and coefficient of variation. 
- Created  a CropRule class that defines a suitable monthly rainfall range for maize, beans and milllet. Normal ranges for annual rainfall for maize and beans are 500-600mm and 300-500mm from the ministry of agriculture, animal industry and fisheries for millet 500-1000mm is the annual normal range from an article titled, “Finger millet production manual for Uganda. National Agricultural Research Organization”
by scovia adikini. The normal ranges were divided by 12 to come up with the figures below. this analysis is done under the assumption that monthly rainfall is uniform.
- Implemented the cosine similarity.
- Computed similarity/distance measures between every pair of regions using cosine similarity, Pearson correlation and Euclidean distance.
- Used scipy.signal to detect rainy seasons automatically and classified them. even when one is much wetter than the other.
- Illustrated the findings.
### FINDINGS, LIMITATIONS AND RECOMMENDATION
- Kampala had the highest average rainfall with the lowest coefficient of variation compared to Gulu and Mbarara. Mbarara had the least average rainfall compared to Gulu and Kampala. Gulu had the highest coefficient of variation in rainfall compared to Kampala and Gulu.
- In Kampala, only August and September were good for growing millet. In Gulu, March and November were good for millet and February was good for beans. In Mbarara, January and August were good for millet. All other months faced either a drought risk or waterlogging risk for the different crops.
- Cosine similarity looks at the overall trend in monthly rainfall data  and not the magnitude of each month’s rainfall level. For example, Kampala and Mbarara have the highest cosine similarity (0.8912) but a weak  Pearson correlation (0.2093) and had the shortest Euclidean distance meaning rainfall amounts were similar. Overall, Pearson correlations were weak.
- Uganda has a bimodal rain pattern in central western and southern parts (March-May, September-November). It has a unimodal rainfall pattern in the far  northern part(April-October). This is inconsistent with the findings from this analysis that found Kampala to have a unimodal rain pattern despite being in the central region of Uganda. Mbarara and Gulu had a bimodal rainfall pattern consistent with the Ugandan rain patterns.
##### ADVISORY NOTE FOR FARMERS IN GULU
- DISCLAIMER: Normal ranges for annual rainfall for maize and beans are 500-600mm and 300-500mm from the ministry of agriculture, animal industry and fisheries for millet 500-1000mm is the annual normal range from an article titled, “Finger millet production manual for Uganda. National Agricultural Research Organization”
by scovia adikini.
- The normal ranges were divided by 12 to come up with the figures below. this analysis is done under the assumption that monthly rainfall is uniform.
- Basing on the analysis, in Gulu, its advisable to grow beans because then, the available rainfall is sufficient . In march and November, it is safe to grow millet in the same region

