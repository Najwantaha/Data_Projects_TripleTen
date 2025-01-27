# Data Analysis Using SQL for Zuber

**Project Overview:**

This project involves analyzing ride data for Zuber, a new ride-sharing company launching in Chicago. The primary objective was to identify patterns in ride behavior, passenger preferences, and the impact of external factors (like weather) on ride frequency and duration. The analysis used SQL queries to extract and manipulate data from a database that contains taxi ride information for Chicago, which includes data from competitors in the area.

## Objective

The goal of this project was to understand how various external factors such as weather, day of the week, and location influenced ride frequency and duration. Specifically, the analysis focused on testing the hypothesis that weather conditions (such as rain) impact the duration of rides between the Loop and O'Hare International Airport.

### Key Questions:
- How do weather conditions affect the duration of rides between certain neighborhoods (e.g., from the Loop to O'Hare)?
- Are there any patterns that can be found in ride frequency during specific weather conditions, particularly on Saturdays?
- How can Zuber leverage this information to optimize ride services?

## Data Description

The analysis was conducted using the following tables in the database:

1. **neighborhoods** – Information about city neighborhoods.
    - `name`: Neighborhood name.
    - `neighborhood_id`: Unique identifier for the neighborhood.

2. **cabs** – Information about taxis.
    - `cab_id`: Unique identifier for the vehicle.
    - `company_name`: The company that owns the vehicle.

3. **trips** – Data on individual rides.
    - `trip_id`: Unique ride identifier.
    - `cab_id`: Vehicle operating the ride.
    - `start_ts`, `end_ts`: Ride start and end timestamps.
    - `duration_seconds`: Ride duration in seconds.
    - `distance_miles`: Ride distance.
    - `pickup_location_id`, `dropoff_location_id`: Pickup and dropoff neighborhood identifiers.

4. **weather_records** – Weather conditions at the time of the ride.
    - `record_id`: Unique weather record identifier.
    - `ts`: Timestamp for the weather record.
    - `temperature`: Temperature at the time of the record.
    - `description`: Brief description of the weather (e.g., "light rain," "clear skies").

## What Was Done and How

1. **Data Extraction and Cleaning:**
   - Wrote SQL queries to extract relevant data from the `trips`, `weather_records`, and `neighborhoods` tables.
   - Merged trip and weather data using timestamps to match weather conditions with ride details.
   - Cleaned and filtered the data to focus on rides from the Loop to O'Hare on Saturdays, across different weather conditions.

2. **Hypothesis Testing:**
   - Analyzed how the weather (rain vs. clear) influenced the duration of rides from the Loop to O'Hare, specifically on Saturdays.
   - Conducted statistical analysis to compare ride durations on rainy Saturdays versus clear days or other weather conditions.

3. **Pattern Identification:**
   - Used SQL aggregation functions to calculate average ride durations, distances, and frequencies under various conditions (e.g., temperature, weather description).

### Results

The analysis revealed that ride durations between the Loop and O'Hare were significantly longer on rainy Saturdays compared to other weather conditions. This suggests that weather conditions, particularly rain, might slow down traffic and increase ride duration.
On clear days, the average duration of rides was shorter, with rides taking less time to complete.

### Suggestions for Zuber and Future Improvements

Weather-Based Pricing Strategy:
Zuber could introduce dynamic pricing based on weather conditions to optimize pricing for both customers and drivers. For example, increase prices during rainy conditions to reflect the additional time or inconvenience.

Ride Optimization:
Implement predictive algorithms that account for weather conditions to predict and allocate drivers more efficiently during bad weather (e.g., rain on Saturdays). This could help minimize passenger wait times and improve service reliability.
