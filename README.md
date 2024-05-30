# US Census Data Analysis

## Overview
This project focuses on accessing and analyzing data from the US Census Bureau using the American Community Survey (ACS). The analysis involves retrieving data via the Census Bureau API, cleaning and processing this data, calculating margins of error, and aggregating results by neighborhood profile areas (NPA). Python libraries such as Pandas, Numpy, and specialized census data libraries are used extensively.

## Prerequisites
To run this project, you need to have the following Python libraries installed:
- **Pandas**: For data manipulation and analysis.
- **Numpy**: For numerical operations.
- **OS**: For interacting with the operating system's file system.
- **censusdata**: For accessing and previewing US Census data.
- **Census**: For interfacing with the US Census Bureau API.

## Getting Started

### Environment Setup
1. **Library Imports**: Begin by importing the required libraries to your Python environment.
2. **Display Configuration**: Configure Pandas to display all rows and columns for better data visualization.
3. **Directory Setup**: Use OS library functions to set the working directory for your project.

### Accessing Census Data
1. **API Key Acquisition**: Obtain an API key from the US Census Bureau by signing up on their website.
2. **API Initialization**: Initialize the Census API using your API key to enable data retrieval.
3. **Variable Preview**: Utilize the `censusdata` library to preview available variables and understand the data structure.

### Data Download and Processing
1. **Define Parameters**: Specify the dataset type (e.g., ACS 5-year estimates), the year of interest, and the geographic scope (e.g., census tracts, block groups).
2. **Data Retrieval**: Fetch the data using the Census API and load it into a Pandas DataFrame.
3. **Data Cleaning**: Perform data cleaning tasks such as converting numerical data from string to integer format and handling error codes by replacing them with `NaN`.

### Calculating Margins of Error
1. **Identify Margin Variables**: Locate variables that represent margins of error, typically ending with 'M'.
2. **Square Margins**: Square these margin values as part of the error propagation process.
3. **Derived Margin Calculations**: Calculate margins of error for derived measures by summing the squared margins and taking the square root of the sum.

### Data Joining
1. **GEOID Creation**: Create a unique GEOID by concatenating state, county, census tract, and block group IDs.
2. **Crosswalk Data Integration**: Read the NPA Crosswalk data from a provided URL and prepare it for merging.
3. **Data Merge**: Join the ACS data with the NPA data using the created GEOID to facilitate analysis at the neighborhood level.

### Data Aggregation and Analysis
1. **Group by NPA**: Aggregate the data by Neighborhood Profile Areas (NPA) for localized analysis.
2. **Derived Estimates and MOEs**: Calculate aggregated estimates for derived proportions and compute the corresponding margins of error.

## Final Outputs
The final cleaned, processed, and aggregated data is ready for detailed analysis or visualization. This data can be used to derive insights at both a broad and granular level, focusing on various geographic and demographic variables.

## Contributions
Contributions to this project are welcome. You can fork the repository, make enhancements or fixes, and submit pull requests for review.

## License
This project is licensed under the MIT License, allowing for wide use and modification.

---

For detailed examples and step-by-step instructions, please refer to the individual Python scripts provided in this repository.
