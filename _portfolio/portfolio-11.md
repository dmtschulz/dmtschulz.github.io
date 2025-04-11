---
title: "Weighted K-Means for Facility Placement"
excerpt: "Using weighted k-means clustering to simulate optimal placement of factories based on population density. <br/><img src='https://raw.githubusercontent.com/dmtschulz/weighted-kmeans-factory-placement/main/plots/centroid_animation.gif' width=500>"
collection: portfolio
---

### Weighted K-Means for Facility Placement

This project simulates optimal placement of production facilities based on global population data, using a **weighted k-means algorithm**.  
We cluster high-density regions and minimize transportation cost by placing centroids (factories) near demand centers.

**Key Highlights:**
- Weighted K-Means with population as weight map
- EM iterations visualized as a GIF (animation of centroid movement)
- Data from [SEDAC Global Population](http://sedac.ciesin.columbia.edu/)
- Centroid initialization proportional to population
- Visual overlay of country contours and clusters

![Clustering Animation](https://raw.githubusercontent.com/dmtschulz/weighted-kmeans-factory-placement/main/plots/centroid_animation.gif)
*(Weighted K-Means clustering over world population heatmap)*

**Tools Used**:  
Python, NumPy, SciPy, Matplotlib, ImageIO

**GitHub**: [Check out the repository](https://github.com/dmtschulz/weighted-kmeans-factory-placement)
