[![Medium Badge](https://img.shields.io/badge/Medium-Read%20on%20Medium-black?style=flat-square&logo=medium)](https://medium.com/@apirat-apiromyanard/are-all-red-lipsticks-the-same-see-what-the-data-says-9901ed125e0d)

# Lipstick-is-not-just-Red
- This project analyzes lipstick shades using clustering techniques to uncover dominant colors in the red and not-red groups. </br>
- The goal is to identify shade distributions, compare groups, and extract actionable insights for brand and product-level decisions. </br>
- The raw data used in this project was sourced from the GitHub repository [Lipsticks Detect](https://github.com/theBigDataDigest/lipsticks_detect) by [The Big Data Digest](https://github.com/theBigDataDigest).


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


## Methodology
The methodology used in this project involves several key steps to analyze and classify lipstick shades based on their RGB values:

1. **Data Collection**
The raw data was collected from the GitHub repository Lipsticks Detect by The Big Data Digest. The dataset includes information about various lipstick brands, series, and individual shades, including their hexadecimal color codes (`#RRGGBB` format).

2. **Data Preprocessing**

The dataset was parsed to extract relevant information, such as:

  - **Brand Name:** The name of the brand.
  - **Series Name:** The specific product line of the lipstick.
  - **Lipstick Shade** Information: Each shade’s ID, name, and color (in hexadecimal format).
  - **Hexadecimal color codes** were converted to RGB values to facilitate color-based classification.

3. **Color Analysis**

    - Each lipstick's RGB value was analyzed to determine whether red is the dominant color. This was done by comparing the red component with the green and blue components.

    - **A shade was classified as:**

      - Red-Dominant if the red component was significantly higher than both green and blue.
      - Non-Red-Dominant if either green or blue had a comparable or higher value than red.

    - **Classification Output**

        - The shades were categorized into two lists:
      
            - Red-Dominant Shades
            - Non-Red-Dominant Shades

        
    - The results were printed and stored, providing a clear distinction between shades based on their RGB characteristics.

4. **Results**

    The script outputs two main classifications:

      - Red-Dominant Shades: Lipsticks where red is the primary color component.

      - Non-Red-Dominant Shades: Lipsticks with other dominant colors (e.g., pink, orange).

    Example output:

      - Red-dominant shades: `#D62352`, `#DC4B41`, `#B22146`

      - Non-red-dominant shades: `#A25356`, `#E06C68`, `#842C71`

![image](https://github.com/user-attachments/assets/e1056f38-118b-4306-b99e-9d6bc62dce0a)


## Wrap-Up

**Dominance of Not-Red-Dominant Shades** 

The analysis reveals that **not-red-dominant shades** make up approximately **70% of the total lipstick collection across all four brands.** This indicates a clear trend: while red remains iconic, there is a noticeable shift in consumer preferences towards shades that offer greater versatility and subtlety. Consumers are increasingly interested in experimenting with colors beyond the classic red, leading to a demand for more diverse and unique options.

**Strategic Diversification by Brands** 

At the series level, the analysis highlights a deliberate strategy by brands to offer a wide variety of not-red-dominant shades. This approach demonstrates a nuanced understanding of modern consumers, who seek individuality and versatility in their makeup choices. Lipsticks are no longer viewed as a simple beauty product but as a way to express personality, evoke emotions, and project specific characteristics.
![image](https://github.com/user-attachments/assets/b1ca3ae6-2bd1-4bc5-8387-fa7d0540ec6d)


**Emerging Market Trends**

Brands are capitalizing on this shift in preferences to remain competitive by expanding their portfolios beyond traditional red shades. The growing popularity of subtle and experimental colors points to an evolving market landscape where customer-centric innovation drives product development.

## Requirements

**Python 3.x**

**Libraries:**
- matplotlib
- numpy
- sklearn
- collections
