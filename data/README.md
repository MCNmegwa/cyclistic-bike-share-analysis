# Data Directory

This folder should contain the Cyclistic bike trip data for analysis.

## 📥 How to Get the Data

### Source
Download the data from [Divvy Bikes Trip Data](https://divvy-tripdata.s3.amazonaws.com/index.html)

### Required Files
You need the following 12 monthly CSV files (June 2021 - May 2022):

- `202106-divvy-tripdata.csv` (June 2021)
- `202107-divvy-tripdata.csv` (July 2021)
- `202108-divvy-tripdata.csv` (August 2021)
- `202109-divvy-tripdata.csv` (September 2021)
- `202110-divvy-tripdata.csv` (October 2021)
- `202111-divvy-tripdata.csv` (November 2021)
- `202112-divvy-tripdata.csv` (December 2021)
- `202201-divvy-tripdata.csv` (January 2022)
- `202202-divvy-tripdata.csv` (February 2022)
- `202203-divvy-tripdata.csv` (March 2022)
- `202204-divvy-tripdata.csv` (April 2022)
- `202205-divvy-tripdata.csv` (May 2022)

### File Structure
Place all CSV files in this directory:
```
data/
├── 202106-divvy-tripdata.csv
├── 202107-divvy-tripdata.csv
├── ... (and so on)
└── 202205-divvy-tripdata.csv
```

### Update File Paths
After downloading, update the file paths in `google-capstone-project.Rmd`:

**Current path:**
```r
df_jun_2021 <- read.csv('../input/cyclist-trip-data-june-21-to-june-22/202106-divvy-tripdata.csv')
```

**Update to:**
```r
df_jun_2021 <- read.csv('data/202106-divvy-tripdata.csv')
```

Repeat for all 12 months.

## ⚠️ Important Notes

- **Size:** The CSV files are large (~100-200 MB each)
- **Git:** These files are in `.gitignore` and won't be uploaded to GitHub
- **License:** Data is provided by Motivate International Inc. under [this license](https://ride.divvybikes.com/data-license-agreement)
- **Privacy:** The data is anonymized and doesn't contain personally identifiable information

## 📊 Data Structure

Each CSV file contains the following columns:
- `ride_id`: Unique identifier for each trip
- `rideable_type`: Type of bike (classic, electric, docked)
- `started_at`: Trip start date and time
- `ended_at`: Trip end date and time
- `start_station_name`: Starting station name
- `start_station_id`: Starting station ID
- `end_station_name`: Ending station name
- `end_station_id`: Ending station ID
- `start_lat`: Starting latitude
- `start_lng`: Starting longitude
- `end_lat`: Ending latitude
- `end_lng`: Ending longitude
- `member_casual`: Rider type (member or casual)

## 🔄 Alternative: Use Smaller Sample

If you want to test the code without downloading all files:
1. Download just 1-2 months of data
2. Modify the R code to only load those months
3. Note that results will differ from the full analysis

---

**Need Help?** See the main [README.md](../README.md) for more information.
