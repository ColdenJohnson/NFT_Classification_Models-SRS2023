# NFT Image Analysis
## Project information
- **Author**: Colden Johnson, Computation and Design, Class of 2026, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to SRS2023 Innovate are advised and instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: I am deeply indebted to Professor Luyao Zhang for her invaluable feedback and patience.
- **Project Summary**:
Non-Fungible Tokens (NFTs) have gained significant popularity in recent years as a new form of digital asset. This article will focus on a dataset drawn from the article ‘\textit{Mapping the NFT revolution: market trends, trade networks, and visual features}’ (Nadini et al., 2021). This paper attempts to present a comprehensive analysis of NFT market data, combining data visualizations and image analysis.

First, we create visualizations to explore NFT trading patterns, specifically focusing on the trading cost and frequency of different collections. Building upon insights gained from data visualization, we then use image analyis techniques to extract meaningful features from NFT artwork. We employ image descriptors to capture the unique visual characteristics of NFT images, with the goal to enable efficient comparison and analysis of digital artworks. We also use the linked dataset to extract features to develop a classification algorithm that can accurately classify NFT images into one of 6 predefined image categories. The algorithm facilitates automated categorization of artworks based on their artistic style, image components, and other relevant criteria. To validate the effectiveness of our approach, we look at error rates using a test dataset of images, with the goal being to gauge accuracy of the proposed image descriptors and classification algorithm.

Combining data visualization and image analysis techniques helps gain valuable insights into the NFT market. The proposed approach is valuable in helping understand market dynamics and trends, understand image descriptors, and automatically classify NFT images.

  - [Summarize the Background/Motivation]
  - [Research Questions]
  - [Application Scenario (Data Source)]
  - [Methodology]
  - [Results]
  - [Intellectual Merits and Practical impacts of your project.]

## Table of Contents

| Contents | Description |
|--------|--------|
| [Data](https://github.com/SciEcon/SRS2023_NFT_Johnson#data) | View Raw and Processed Data Files |
| [Code](https://github.com/SciEcon/SRS2023_NFT_Johnson#code) | View Jupyter Notebook Code Files |
| [Spotlight](https://github.com/SciEcon/SRS2023_NFT_Johnson#spotlight) | View Generated Spotlight Figures |
| [About the Author](https://github.com/SciEcon/SRS2023_NFT_Johnson#more-about-the-author) | Read Author Bio and Project Background |
| [References](https://github.com/SciEcon/SRS2023_NFT_Johnson#references) | View References CSV File |

## Data

| File Name  | Variable Name | Description | Unit | Type |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| [Data_API.csv](https://github.com/SciEcon/SRS2023_NFT_Johnson/tree/main/data)  | Unique_id_collection  | Unique ID for a given NFT | ID | int |
|   | Price_crypto_USD  | Price of NFT at sale  | USD($) | int |
|   | Seller_address  | Addresses for seller of NFT | address | int |
|   | Buyer_address  | Addresses for buyers of NFT | address | int |
|   | Datetime_updated  | Identifies transaction with daily resolution | days | DateTime |
|   | Image_url_1  | URL to digital object associated with the NFT | URL | URL |
|   | ID_token  | ID of the NFT asset within a given smart contract | ID | int |
|   | Collection  | Corresponds to the collection to which the NFT belongs | Categorical (Collection) | str |
|   | Category  | Category in which the NFT belongs. Examples are: Art, Games, etc. | Categorical (Category) | str |

**Data Source:**
Nadini, M., Alessandretti, L., Di Giacinto, F. et al. Mapping the NFT revolution: market trends, trade networks, and visual features. Sci Rep 11, 20902 (2021). https://doi.org/10.1038/s41598-021-00053-8

- Data Source:
- Queried Data
- Processed Data


## Code
- Query Data
- Process Data
- Analyze Data
- ...

## Spotlight
- Posters
- Figures
![Figure_1](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/15862e2c-b465-4a5b-a512-7e99e7c05253)

![Figure_2](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/bc4f4318-af5a-492c-b0a1-2c84e251a724)

![Figure_3](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/7f8da240-93c4-4941-8ae7-d1b4c860ba99)

![Figure_4](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/27530afc-269b-4b6f-a57e-ed5d7537e66a)

![Figure_5](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/9e55440c-0bb6-4c5f-abdf-f0ef49115238)


- Slides
- Presentations
- Review articles
- Media appearance

## More about the Author

<img src="https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/a0b67354-b261-4375-9d60-35a8bf61eddf"  width="500" >


My name is Colden Johnson, I am a rising Sophomore student at Duke Kunshan University. I am considering a major in either Political Economy or Computation and Design with a track in Computer Science. My current research goals lie at the intersection of these two fields, and I am specifically interested in applying artificial intelligence and computation to address questions in the humanities.


- Final reflections 
  - intellectual growth
  - professional growth
  - living a purposeful life

## References

### Data Source
- Data Source Title and URL
### Code Source
- Code Source Title and URL
### Articles
- Article Source Title and URL
### Literature
- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Levin, Dan and Zhang, Luyao},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2022},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```

