![delhivery-website-1024x683](https://github.com/user-attachments/assets/da66ffbf-3ead-453f-b239-a035ee5195d0)


# About The Case Study

## Feature Engineering Case study
### Problem statement:
* Delhivery aims to establish itself as the premier player in the logistics industry. This
case study is of paramount importance as it aligns with the company's core objectives
and operational excellence.
* It provides a practical framework for understanding and processing data, which is
integral to their operations. By leveraging data engineering pipelines and data analysis
techniques, Delhivery can achieve several critical goals.
* First, it allows them to ensure data integrity and quality by addressing missing values
and structuring the dataset appropriately.
* Second, it enables the extraction of valuable features from raw data, which can be
utilized for building accurate forecasting models.
* Moreover, it facilitates the identification of patterns, insights, and actionable
recommendations crucial for optimizing their logistics operations.
* By conducting hypothesis testing and outlier detection, Delhivery can refine their
processes and further enhance the quality of service they provide.


### Column Profiling:
* data - tells whether the data is testing or training data
* trip_creation_time – Timestamp of trip creation
* route_schedule_uuid – Unique ID for a particular route schedule
* route_type – Transportation type
  * FTL – Full Truck Load: FTL shipments get to the destination sooner, as the truck
is making no other pickups or drop-offs along the way
  * Carting: Handling system consisting of small vehicles (carts)
* trip_uuid - Unique ID given to a particular trip (A trip may include different source and
destination centers)
* source_center - Source ID of trip origin
* source_name - Source Name of trip origin
* destination_cente – Destination ID
* destination_name – Destination Name
* od_start_time – Trip start time
*  od_end_time – Trip end time
* start_scan_to_end_scan – Time taken to deliver from source to destination
* is_cutoff – Unknown field
* cutoff_factor – Unknown field
* cutoff_timestamp – Unknown field
* actual_distance_to_destination – Distance in kms between source and destination
warehouse
* actual_time – Actual time taken to complete the delivery (Cumulative)
* osrm_time – An open-source routing engine time calculator which computes the
shortest path between points in a given map (Includes usual traffic, distance through
major and minor roads) and gives the time (Cumulative)
* osrm_distance – An open-source routing engine which computes the shortest path
between points in a given map (Includes usual traffic, distance through major and minor
roads) (Cumulative)
* factor – Unknown field
* segment_actual_time – This is a segment time. Time taken by the subset of the
package delivery
* segment_osrm_time – This is the OSRM segment time. Time taken by the subset of the
package delivery
* segment_osrm_distance – This is the OSRM distance. Distance covered by subset of
the package delivery
* segment_factor – Unknown field


#### Analysis on the Data set has been executed on the Jupyter notebook.



## Work Flow on Data Set

______________________________________________________________________________
##### 1. Basic data cleaning and exploration:
* Handle missing values in the data.
* Converting time columns into pandas datetime.
* Analyze structure & characteristics of the dataset.

______________________________________________________________________________
##### 2. Feature Engineering: Extract features from the below fields:
* Calculate time taken between od_start_time and od_end_time and keep it as a
feature named od_time_diff_hour. Drop the original columns, if required.
* Destination Name: Split and extract features out of destination. City-place-code (State)
* Source Name: Split and extract features out of destination. City-place-code (State)
* Trip_creation_time: Extract features like month, year, day, etc.

______________________________________________________________________________
##### 3. In-depth analysis:
* Grouping and Aggregating at Trip-level
  * Groups the segment data by the trip_uuid column to focus on
aggregating data at the trip level.
  * Apply suitable aggregation functions like first, last, and sum specified in
the create_trip_dict dictionary to calculate summary statistics for each
trip.
* Outlier Detection & Treatment
  * Find any existing outliers in numerical features.
  * Visualize the outlier values using Boxplot.
  * Handle the outliers using the IQR method.
* Perform one-hot encoding on categorical features.
* Normalize/ Standardize the numerical features using MinMaxScaler or
StandardScaler.
  
______________________________________________________________________________
##### 4. Hypothesis Testing:
* Perform hypothesis testing / visual analysis between :
  * actual_time aggregated value and OSRM time aggregated value.
  * actual_time aggregated value and segment actual time aggregated
value.
  * OSRM distance aggregated value and segment OSRM distance
aggregated value.
  * OSRM time aggregated value and segment OSRM time aggregated
value.
* Note: Aggregated values are the values you’ll get after merging the rows on the
basis of trip_uuid.


______________________________________________________________________________
##### 5. Business Insights & Recommendations
* Patterns observed in the data along with what you can infer from them.
  * Check from where most orders are coming from (State, Corridor, etc.)
  * Busiest corridor, avg distance between them, avg time taken, etc.
* Actionable items for the business.


Recommendation and insights of the data analysis has been added in the PDF.


