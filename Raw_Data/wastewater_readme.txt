
This dataset provides a complete time history of metrics calculated using SARS-CoV-2 concentrations in wastewater.
Source: https://data.cdc.gov/Public-Health-Surveillance/NWSS-Public-SARS-CoV-2-Wastewater-Metric-Data/2ew6-ywp6/about_data

The wastewater_full.csv contains data updated on 10/28/2024. We will follow up with updated data in a few weeks to check the reproducibility of the code.


wwtp_jurisdiction: State, DC, US territory, or Freely Associated State jurisdiction name (2-letter abbreviation) in which the wastewater treatment plant provided in 'wwtp_id' is located.

wwtp_id: A unique identifier for wastewater treatment plants. This is an arbitrary integer used to provide a unique, but anonymous identifier for a wastewater treatment plant. This identifier is consistent over time, such that the same plant retains the same ID regardless of the addition or subtraction of other plants from the data set.

reporting_jurisdiction: The CDC Epidemiology and Laboratory Capacity (ELC) jurisdiction, most frequently a state, reporting these data (2-letter abbreviation)

sample_location: Sample collection location in the wastewater system, whether at a wastewater treatment plant (or other community level treatment infrastructure such as community-scale septic) or upstream in the wastewater system.

sample_location_specify: A unique identifier for "upstream" sample locations. Specifically, when 'sample_location' is "upstream", this field has a non-empty value, which provides a unique, but anonymous identifier for the upstream sample collection sites. This identifier is consistent over time, such that the same sample collection site retains the same ID regardless of the addition or subtraction of other sample collection sites from the data set.

key_plot_id: A unique identifier for the geographic area served by this sampling site, called a sewershed. This is an underscore-separated concatenation of the fields 'wwtp_jurisdiction', 'wwtp_id', and, if 'sample_location' is "upstream", then also 'sample_location_specify', and sample_matrix.

county_names: The county and county-equivalent names corresponding to the FIPS codes in 'county_fips'.

county_fips: 5-digit numeric FIPS codes of all counties and county equivalents served by this sampling site (i.e., served by this wastewater treatment plant or, if 'sample_location' is "upstream", then by this upstream location). Note that multiple sampling sites or treatment plants may serve a single county, and that a single sampling site or treatment plant may serve multiple counties. Counties listed may be entirely or only partly served by this sampling site.

population_served: Estimated number of persons served by this sampling site (i.e., served by this wastewater treatment plant or, if 'sample_location' is "upstream", then by this upstream location).

date_start: The start date of the interval over which the metric is calculated. Intervals are inclusive of start and end dates.

date_end: The end date of the interval over which metric is calculated. Intervals are inclusive of start and end dates.

ptc_15d: The percent change in SARS-CoV-2 RNA levels over the 15-day interval defined by 'date_start' and 'date_end'. Percent change is calculated as the modeled change over the interval, based on linear regression of log-transformed SARS-CoV-2 levels. SARS-CoV-2 RNA levels are wastewater concentrations that have been normalized for wastewater composition. 

detect_prop_15d: The proportion of tests with SARS-CoV-2 detected, meaning a cycle threshold (Ct) value <40 for RT-qPCR or at least 3 positive droplets/partitions for RT-ddPCR, by sewershed over the 15-day window defined by 'date_start' and "date_end'. The detection proportion is the percent calculated by dividing the 15-day rolling sum of SARS-CoV-2 detections by the 15-day rolling sum of the number of tests for each sewershed and multiplying by 100.

percentile: This metric shows whether SARS-CoV-2 virus levels at a site are currently higher or lower than past historical levels at the same site. 0% means levels are the lowest they have been at the site; 100% means levels are the highest they have been at the site. Public health officials watch for increasing levels of the virus in wastewater over time and use this data to help make public health decisions. 

sampling_prior: Indicates whether the site was collecting wastewater samples before or on December 1, 2021.

first_sample_date: The first date samples were collected at a site.