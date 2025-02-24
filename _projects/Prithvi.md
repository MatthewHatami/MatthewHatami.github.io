---
layout: single
title: "Transfer Learning in Remote Sesning Data"
excerpt: "Visualizing the Results of the Coastal Vulnerability Index through a Dynamic GIS Dashboard" 
permalink: /projects/prithvi/
category: PhD
image: /images/gisdashboard.jpg
---
# Exploring Coastal Vulnerability: An Interactive Dashboard  

As part of our research group at **iWERS**, within the **Department of Civil and Environmental Engineering at the University of South Carolina**, my colleagues have published a study on **integrated socio-environmental vulnerability assessment of coastal hazards**. While their original paper presents vulnerability maps as raster files, I have adapted these results into an interactive dashboard that simplifies interpretation and enhances accessibility.  

## **Why This Dashboard?**  
Understanding vulnerability at a granular level is crucial for decision-making. Raster files provide detailed spatial information, but they can be challenging for non-experts to interpret. To bridge this gap, I have **aggregated raster values over zip code areas**, making it easier to comprehend and analyze regional vulnerability patterns.  

### **Key Features of the Dashboard**  
1. **User-Friendly Selection**  
   - Start by choosing a **county**.  
   - Then, select a **zip code** within the chosen county.  

2. **Vulnerability Indices & Maps**  
   - View computed **vulnerability indices** for different risk factors.  
   - Explore maps that visualize the aggregated vulnerability across different zip codes.  

3. **Data-Driven Insights**  
   - The dashboard leverages **multi-criteria decision-making (MCDM)** and **probabilistic principal component analysis (PPCA)** to provide a **comprehensive vulnerability assessment**.  

### **Methodology in Brief**  
This dashboard builds upon the methodology outlined in the paper:  
- Vulnerability is assessed using five key groups: **biophysical, hydroclimate, socio-economic, ecological, and shoreline factors**.  
- Traditional raster-based results are **spatially aggregated** using zip code boundaries for easier comparison.  
- The **entropy weighting technique** is used to minimize bias in assigning importance to different vulnerability factors.  

## **Try It Yourself**  
I have embedded the dashboard into this blog, making it accessible to anyone interested in exploring coastal vulnerability in South Carolina.  

[**Click here to explore the dashboard**](https://uscgeography.maps.arcgis.com/apps/dashboards/fc7eef0cb3b844dea1dbbb7500b5dffd) 


By making these findings more accessible, I hope this tool will support planners, policymakers, and local communities in better understanding and mitigating coastal vulnerability.  

Let me know your thoughts! Feedback is always welcome.  

---
📄 **Reference**: [Original Research Paper](https://doi.org/10.1038/s41598-022-15237-z)  
