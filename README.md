# Image Classification Algorithms for NFTs: a Comparative Analysis

Disclaimer: This article is a final deliverable from Prof. Luyao Zhang's project entitled "From 'Code is Law' to 'Code and Law': A Comparative Study on Blockchain Governance," supported by the 2023 Summer Research Scholarship (SRS) program at Duke Kunshan University. SciEcon wholeheartedly supports DKU's noble mission of advancing interdisciplinary research and fostering integrated talents. Our support is solely focused on promoting academic excellence and knowledge exchange. SciEcon does not seek any financial gains, property rights, or branding privileges from DKU. Moreover, individuals involved in this philanthropy event perform their roles independently at DKU and SciEcon.

## Project information
- **Author**: Colden Johnson, Computation and Design, Class of 2026, Duke Kunshan University
- **Research Mentor**: Prof. Luyao Zhang, Duke Kunshan University
- **Acknowledgments**: I am deeply indebted to Professor Luyao Zhang for her invaluable feedback and patience. I am also thankful to both Yiyang Zhang and Jiayi Wang for their constructive review and commentary.
- **Project Summary**:

Non-fungible tokens (NFTs) have gained significant popularity in recent years as a new form of digital asset. This research focuses on improving and innovatively applying a dataset drawn from the article 'Mapping the NFT Revolution: market trends, trade networks, and visual features’ (Nadini et al., 2021). In order to provide a comprehensive analysis of NFT market data, we both provide data visualization and compare various image analysis techniques.

Abstract: This research presents a comparative analysis of image classification algorithms for use in the NFT space, using a linked dataset comprising NFT images and their corresponding categorization. Initial exploratory visualizations were generated, providing insights into category distribution, temporal price trends, and the image dataset as a whole. Next, we conducted a comparative assessment of image classification methodologies, utilizing K-Nearest Neighbors (KNN), Convolutional Neural Networks (CNN), and CNN with transfer learning from ResNet50. The CNN approach demonstrates high efficacy, achieving 96.8% accuracy on validation data post-training using a subset of 25,000 images (fig. 2). KNN, which was used as a baseline model due to its comparative simplicity, also performed relatively well with a 93.7% accuracy (fig. 1). However, due to the relatively high accuracy even at low k-values, it is suspected that there may be some near-duplicate images in the dataset. In the future, these could be filtered out using image hash functions. Finally, the CNN incorporating transfer learning from ResNet50 recorded only a 91.1% accuracy(fig. 3), underscoring how this image classification task differs from standard image classification work. In the future, this could be improved by selecting a more tailored pre-trained image classification model to work with. This study presents a novel use for the dataset, as it has never been used to facilitate NFT image scraping and analysis. Additionally, looking at the comparative efficacy of three different image classification methodologies provides insights into the types of algorithms which are effective on NFT image datasets of this type, and is useful in informing future research on the topic. Subsequent research with this enhanced dataset could also benefit from incorporating image feature extraction and image sentiment analysis techniques.

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

- Queried Data
- Processed Data

## Spotlight
- Posters
- Figures

![Figure_2](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/15862e2c-b465-4a5b-a512-7e99e7c05253)
Figure 2: Average price in USD by collection. Note that this is a metric of average trading price, and not of total market cap.

![Figure_3](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/bc4f4318-af5a-492c-b0a1-2c84e251a724)
Figure 3: Average price in USD filtered by category. Categories are Metaverse, Utility, Art, Collectible, Games, and Other. This visualization only includes queried data and is not a truly accurate or proportional representation of the overall NFT market. For example, because all NFTs in the 'Gods Unchained' ecosystem have been queried, this has shifted the reflected average price and is not representative of, say, the average price of 'Gaming' type NFTs on OpenSea.

![Figure_4](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/7f8da240-93c4-4941-8ae7-d1b4c860ba99)
Figure 4: Average price in USD by market. Note that filtering by market often results in different average and median NFT category valuations. For example, the high trading price of 'Decentraland' inflates the average valuation of 'Metaverse' NFTs, and the relatively low value of 'Gods Unchained' deflates the average value of 'Gaming' NFTs.

![Figure_5](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/27530afc-269b-4b6f-a57e-ed5d7537e66a)
Figure 5: Average price in USD over time. This is measured by NFTs traded, grouped by week. Grouping by day does not significantly change the graph, and grouping by hour or minute creates misleading price fluctuation.

![Figure_6](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/9e55440c-0bb6-4c5f-abdf-f0ef49115238)
Figure 6: Average trading price in USD over time. Three similar categories, Metaverse, Art, and Collectible are simultaneously displayed.

![Figure_7](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/a665d85c-8f99-4477-915a-313d2c14003f)

Figure 7: A K-Nearest Neighbor (KNN) algorithm was used to create a baseline model due to its relative simplicity, and performed relatively well with a 93.7% accuracy. Notice how for low k-values the efficacy is validation error is relatively small, and also experiences a local minimum at a much higher k-value (k = 72).

![Figure_8](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/bb977f55-835d-4cbb-ab18-71db2dfd729e)

Figure 8: Using a CNN (Convolutional Neural Network) has high efficacy, achieving 96.8% accuracy on validation data post-training using a subset of 25,000 images. However, due to the relative gap between predicted training accuracy (approaching 100%) and relatively smaller validation accuracy, there could be some issues with overfitting. Adding more images to the training dataset could help resolve this issue.

![Figure_9](https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/2e4f20d8-75c6-45e3-8232-10ab64eca080)

Figure 9: The CNN incorporating transfer learning from ResNet50 had only a 91.1% accuracy. In contrast to the other trained CNN, training accuracy at no point reached 99%, indicating that the underlying ResNet50 model may be poorly adapted to this dataset.

- Slides
- Presentations
- Review articles
- Media appearance

## More about the Author

<img src="https://github.com/SciEcon/SRS2023_NFT_Johnson/assets/118926209/a0b67354-b261-4375-9d60-35a8bf61eddf"  width="500" >


My name is Colden Johnson, I am a rising Sophomore student at Duke Kunshan University. I am considering a major in either Political Economy or Computation and Design with a track in Computer Science. My current research goals lie at the intersection of these two fields, and I am specifically interested in applying artificial intelligence and computation to address questions in the humanities.

## References

### Data Source
Nadini, M., Alessandretti, L., Di Giacinto, F. et al. Mapping the NFT revolution: market trends, trade networks, and visual features. Sci Rep 11, 20902 (2021). https://doi.org/10.1038/s41598-021-00053-8

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

