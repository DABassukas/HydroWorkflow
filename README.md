# Clustering water samples based on main anions and cations

![MedSAL](https://medsal.eu/wp-content/uploads/2019/10/cropped-Logo.png)

This project provides the basis in order to perform a reproducible clustering on water samples which can facilitate the detection of hydrochemical End-members . It has been created in the framework of the [MedSal project](https://medsal.eu/).

It currently includes following steps:

-   Step 1: Data import

-   Step 2: Data quality assessment and filtering based on the Charge Balance Error

-   Step 3: Cluster analysis

-   Step 4: Data visualization

At the time being, two different workflows exist based on the type of input data. Input data are either excel/csv files that get imported or through direct access to the [MedSal Database](https://www.uhydro.de/medsaldba). Differences regarding the features are summarized in the table below:



|                         | .xlsx              | 
|-------------------------|--------------------|
|__Data quality assessment__ |                 |
| Charge balance error    | :heavy_check_mark: | 
|__Cluster analysis__     |                    |   
| Data preparation        | :heavy_check_mark: | 
| Clustering              | :heavy_check_mark: | 
| Dendrogram              | :heavy_check_mark: | 
| Cluster map             | :heavy_check_mark: | 
|__Data visualization__   |                    | 
| Piper plot**            | :heavy_check_mark: | 
| Shoeller plot           | :heavy_check_mark: | 
| Ion ratios              | :heavy_check_mark: | 
| Isotope data            | :heavy_check_mark: | 

**Code from: <https://github.com/markolipka/ggplot_Piper>


### .xlsx data input

1) Create an .xlsx containing your water analyses. For the script to run the following variables must be provided with the exact column names shown below ( The column order is irrelevant). Longitude and Latitude in Decimal Degrees - WGS 84, ions in mg/L and isotopic data in per mil.



| Sample | Latitude | Longitude | Cl | HCO3 | SO4 | Ca | Mg | Na | K |
|--------|----------|-----------|----|------|-----|----|----|----|---|




   Other variables that can be included and are by default incorporated in the script are:

| d2H | d18O | D_Excess | NO3 | Br | CO3 |
|-----|------|----------|-----|----|-----|

   Deuterium, d18O and Deuterium excess should be provided together!




2) Find the **r Provide the instructions for your run** chunk

-   Provide the path to the .xlsx containing your data to the

    water_analysis \<- read_excel( ''C/.../your_data.xlsx'')

-   Choose the clustering parameters and the number of clusters

-   Specify map corners. The two map corners represent the coordinates of the upper left and lower right points of a rectangle covering the your study area.

3) Knit!
