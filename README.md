# Cyclistic Bike-Share Analysis
### Google Data Analytics Professional Certificate - Capstone Project

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![RStudio](https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=rstudio&logoColor=white)
![Tidyverse](https://img.shields.io/badge/Tidyverse-1A162D?style=for-the-badge)

## 📋 Table of Contents
- [Overview](#🎯overview)
- [Business Task](#business-task)
- [Data Source](#data-source)
- [Tools & Technologies](#tools--technologies)
- [Analysis Process](#analysis-process)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [Files](#files)
- [How to Run](#how-to-run)
- [Author](#author)

## 🎯 Overview

This capstone project is the culmination of the **Google Data Analytics Professional Certificate** program. The analysis examines bike-sharing patterns in Chicago's Cyclistic bike-share program, which features **5,824 bicycles** across **692 stations**.

The project demonstrates proficiency in the complete data analysis process using the **6-phase framework**: Ask, Prepare, Process, Analyze, Share, and Act.

## 💼 Business Task

**Primary Objective:** Understand how annual members and casual riders use Cyclistic bikes differently to inform marketing strategies aimed at converting casual riders to annual members.

### Key Questions
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

### Stakeholders
- **Lily Moreno** - Director of Marketing
- **Cyclistic Executive Team** - Decision-makers for marketing program approval
- **Marketing Analytics Team** - Responsible for data-driven insights

## 📊 Data Source

- **Provider:** [Divvy Bikes](https://divvy-tripdata.s3.amazonaws.com/index.html)
- **Period:** June 2021 - May 2022 (12 months)
- **Records:** 5,860,776 trips
- **Format:** CSV files
- **License:** Made available by Motivate International Inc. under [this license](https://ride.divvybikes.com/data-license-agreement)
- **Credibility:** First-party data from a reliable source, free from bias

## 🛠️ Tools & Technologies

### R Packages Used
```r
tidyverse    # Data manipulation and analysis
readr        # Efficient data reading
ggplot2      # Data visualization
lubridate    # Date and time handling
skimr        # Data structure exploration
janitor      # Data cleaning
stringr      # String manipulation
dplyr        # Data transformation
```

### Analysis Environment
- **RStudio** - Primary development environment
- **R Markdown** - Documentation and reproducible analysis
- **Tableau** - Dashboard creation (for stakeholder presentation)

## 📈 Analysis Process

### 1. **Ask Phase**
- Defined business objectives
- Identified key stakeholders
- Formulated guiding questions

### 2. **Prepare Phase**
- Collected 12 months of trip data
- Verified data credibility and licensing
- Assessed data structure and completeness

### 3. **Process Phase**
- **Data Cleaning:**
  - Converted date-time formats for consistency
  - Combined 12 monthly datasets into single dataframe
  - Removed invalid entries (negative ride lengths, outliers)
  - Handled missing values in station names

- **Data Transformation:**
  - Created `ride_length` metric
  - Extracted temporal features: date, day, day_of_week, month, year
  - Standardized categorical variables

### 4. **Analyze Phase**
- Conducted descriptive statistical analysis
- Compared member vs. casual rider behavior across:
  - Ride duration
  - Day of week patterns
  - Monthly trends
  - Bike type preferences
  - Station usage

### 5. **Share Phase**
- Created visualizations using ggplot2
- Developed comprehensive R Markdown report
- Prepared Tableau dashboard for executive presentation

### 6. **Act Phase**
- Synthesized insights into actionable recommendations
- Aligned findings with business objectives

## 🔍 Key Findings

### Usage Patterns

| Metric | Casual Riders | Member Riders |
|--------|--------------|---------------|
| **Total Rides** | 2,481,631 | 3,192,283 |
| **Average Ride Length** | 26 minutes | 13 minutes |
| **Peak Usage** | Weekends | Weekdays |
| **Peak Month** | July | September |

### Behavioral Insights

1. **Ride Duration**
   - Casual riders take **2x longer trips** on average (26 min vs 13 min)
   - Maximum ride length: ~24 hours for both groups
   - Casual riders show more recreational usage patterns

2. **Temporal Patterns**
   - **Casual riders:** Peak on weekends, suggesting leisure use
   - **Member riders:** Consistent weekday usage, indicating commuting behavior
   - Summer months (June-August) show highest casual ridership

3. **Bike Type Preferences**
   - Both groups prefer **classic bikes**
   - Members **do not use docked bikes**
   - Electric bikes are popular among both segments

4. **Station Usage**
   - Top 5 starting stations differ significantly between groups
   - Casual riders favor tourist/recreational areas
   - Members use stations near residential/commercial zones

## 💡 Recommendations

### Strategy 1: Weekend Membership Plan
**Rationale:** Casual riders peak on weekends
- Introduce a **weekend-only membership** at a lower price point
- Target casual riders who primarily use bikes for leisure

### Strategy 2: Targeted Promotional Campaigns
**Timing:** June, July, August (peak casual months)
- Offer **subsidized annual memberships** during summer
- Highlight benefits: savings, convenience, priority access
- Use digital media channels for targeted advertising

### Strategy 3: Location-Based Marketing
**Focus:** Top 5 casual rider starting stations
- Deploy **on-site promotions** at high-traffic casual stations
- Weekend discount offers exclusively at these locations
- Station staff to engage riders about membership benefits

### Strategy 4: Fleet Optimization
**Action:** Increase classic bike availability
- Ensure adequate **classic bike supply** at casual rider stations
- Monitor and adjust based on demand patterns
- Improve bike availability during peak weekend hours

### Expected Impact
- **Conversion Rate Increase:** 15-20% of casual riders
- **Revenue Growth:** Higher predictable income from memberships
- **Customer Lifetime Value:** Longer engagement through annual plans

## 📁 Files

```
cyclistic-bike-share-analysis/
│
├── google-capstone-project.Rmd    # Main R Markdown analysis file
├── README.md                       # Project documentation
├── requirements.txt                # R package dependencies
├── .gitignore                     # Git ignore file
└── visualizations/                # Output charts and graphs (if rendered)
```

## 🚀 How to Run

### Prerequisites
- R (version 4.0 or higher)
- RStudio (recommended)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/cyclistic-bike-share-analysis.git
cd cyclistic-bike-share-analysis
```

2. Install required packages:
```r
install.packages(c("tidyverse", "readr", "ggplot2", "lubridate", 
                   "skimr", "janitor", "stringr", "dplyr"))
```

3. Download the data:
   - Visit [Divvy Bikes Trip Data](https://divvy-tripdata.s3.amazonaws.com/index.html)
   - Download trip data from June 2021 to May 2022
   - Place CSV files in appropriate directory

4. Open and run the R Markdown file:
```r
# In RStudio
rmarkdown::render("google-capstone-project.Rmd")
```

## 📊 Sample Visualizations

The analysis includes multiple visualizations:
- Member vs Casual ride counts
- Bike type usage by membership
- Weekly riding patterns
- Monthly trend analysis
- Average ride length comparisons
- Top station usage patterns

## 🎓 Skills Demonstrated

- ✅ Data cleaning and preprocessing
- ✅ Exploratory data analysis (EDA)
- ✅ Statistical analysis
- ✅ Data visualization with ggplot2
- ✅ R programming and R Markdown
- ✅ Business intelligence and insights generation
- ✅ Stakeholder communication
- ✅ Strategic thinking and recommendations

## 🏆 Certification

This project was completed as part of the **Google Data Analytics Professional Certificate** program offered through Coursera.

**Certificate Date:** June 13, 2022

## 👤 Author

**Miracle Nmegwa**

- GitHub: [@MCNmegwa](https://github.com/MCNmegwa)
- LinkedIn: [Miracle Nmegwa](https://linkedin.com/in/miracle-nmegwa)
- Email: nmegwamiracle@gmail.com

## 📄 License

This project uses publicly available data from Divvy Bikes under their [data license agreement](https://ride.divvybikes.com/data-license-agreement).

The analysis code is available under the MIT License.

## 🙏 Acknowledgments

- **Google** and **Coursera** for the Data Analytics Professional Certificate program
- **Divvy Bikes** (Motivate International Inc.) for providing the trip data
- **Cyclistic** case study (fictional company based on real data)

---

⭐ If you found this analysis helpful or interesting, please consider giving it a star!

## 📧 Questions?

Feel free to open an issue or reach out directly for any questions about the analysis or methodology.
