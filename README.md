# Research Project: Barriers to Higher-Density Housing near Transit in College Park, MD

## Research Question

**What zoning, land use, and built environment factors limit opportunities for higher-density housing near the College Park MARC and Greenbelt Metro/MARC stations?**

This analysis explores residential land use efficiency and zoning constraints within a half-mile walking radius of the College Park and Greenbelt transit stations. The focus is on identifying parcels—especially in Calvert Hills, Old Town, and North College Park—that are underutilized based on existing zoning allowances. The broader aim is to support policy recommendations that promote sustainable and equitable transit-oriented development.

## Approach

### Data Acquisition

- Parcel-level property data including land use, structure size, and zoning classification.
- Cleaned zoning shapefiles with allowable densities.
- Transit buffer zones (half-mile walking distance from the MARC and Metro stations).
- College Park and neighborhood boundary shapefiles.

### Data Preparation

- Filter to include parcels within the defined half-mile walking areas.
- Ensure CRS alignment for spatial operations.
- Clip property and zoning data to station buffers.

### Merge and Join Data

- Merge property data with zoning data to associate each parcel with allowable density.
- Join with neighborhood and municipal boundaries for neighborhood-level insights.

### Utilization Ratio Calculation

- For each parcel, calculate the ratio of actual built density to the maximum allowable density.
- Flag parcels with low utilization ratios as underbuilt relative to zoning potential.

### Analysis

- Assess the number and proportion of underbuilt parcels within each neighborhood.
- Identify which zoning districts are most associated with underutilization.
- Explore whether zoning, physical constraints, or historical preservation contribute to low-density persistence.

### Visualization

- Generate maps that highlight underutilized parcels, zoning categories, and transit proximity.
- Visualize patterns by neighborhood and across the half-mile transit buffers.

## File Structure

## Data Sources
### - Prince George’s County GIS Open Data Portal: [https://gisdata.pgplanning.org/opendata/]
### - Zoning Ordinance (Density Allowances): [https://online.encodeplus.com/regs/princegeorgescounty-md/doc-viewer.aspx#secid-634]

## How to Run the Code

### Install Required Libraries

### Data Setup:
- Download the necessary Property_Info_Py shapefiles and place them in the data/ folder. [https://drive.google.com/drive/folders/18SFvOqeQhXGY8KrIgw38ZvlkBIADTXlW?usp=drive_link]
- Ensure all files are unzipped and in the correct format before running the notebook.

### Run the Notebook:
- Open main_analysis.ipynb in JupyterLab.
- Execute each cell in sequence to perform the data preperation and generate visualization.

## Outputs

### Summary of study area:
- Number of underbuilt parcels.
- Average utilization ratios.
- Zoning types associated with underutilization.

### Zoning map of parcels within a half-mile of College Park-U of Md and Greenbelt Metro stations.

## Notes
### - Be sure to use the correct CRS (EPSG: 2248 for PG County data or EPSG: 4326 for web-mapping).
### - If files are too large for GitHub, store and link them through

---

*This README was created for Exercise 04 of the URSP688Y course at the University of Maryland.*