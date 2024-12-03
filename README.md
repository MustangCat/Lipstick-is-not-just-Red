# Lipstick-is-not-just-Red
This project analyzes lipstick shades using clustering techniques to uncover dominant colors in the red and not-red groups. </br>
The goal is to identify shade distributions, compare groups, and extract actionable insights for brand and product-level decisions. </br>
The raw data used in this project was sourced from the GitHub repository [Lipsticks Detect](https://github.com/theBigDataDigest/lipsticks_detect) by [The Big Data Digest](https://github.com/theBigDataDigest).


## Data Structure
```json
{
  "brands": [
    {
      "name": "Brand Name",
      "series": [
        {
          "name": "Series Name",
          "lipsticks": [
            {
              "color": "#HEXCODE",
              "id": "Lipstick ID",
              "name": "Lipstick Name"
            }
          ]
        }
      ]
    }
  ]
}
```


## Data Manipulation

**1. Preprocessing** 

- Extract HEX Colors:
- Extracted color values for clustering.
- Group Lipsticks:Split lipsticks into red and not-red groups using custom RGB-based classification:
**Red:** High red dominance over green and blue.
**Not-Red:** All other shades.

**2. Clustering**

Performed k-means clustering separately for red and not-red groups to identify dominant shades:

**Red Group:**
Identified 5 clusters of dominant red shades.

**Not-Red Group:**
Identified 5 clusters of dominant non-red shades.

**3. Sorting**

Clustered shades were sorted by proportion in descending order for better visualization and comparison.


## Requirements

**Python 3.x**

**Libraries:**
- matplotlib
- numpy
- sklearn
- collections
