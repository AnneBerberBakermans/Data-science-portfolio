• Collect, store, and access data by identifying and leveraging applicable technologies
• Create actionable insight across a range of contexts (e.g. societal, business, political),
using data and the full data science life cycle
• Apply visualization and predictive models to help generate actionable insight
• Use programming languages such as Rand Python to support the generation of
actionable insight
• Communicate insights gained via visualization and analytics to a broad range of
audiences (including project sponsors and technical team leads
• Apply ethics in the development, use and evaluation of data and predictive models (e.g.,
fairness, bias, transparency, privacy)



Collect, store, and access data by identifying and leveraging applicable technologies

Using Tools to Collect and Organize Data: Citi Bike and Weather Analysis
For our final project in IST 652: Scripting for Data Analytics, we analyzed Citi Bike rentals in New York City to find patterns in how people use the bike-sharing system. We focused on July, August, and September because these months had the highest number of rides. Since the data for each month was stored in a separate file, we had to gather, clean, and combine them before we could start analyzing. Each month had around 4–5 million rows, so organizing the data properly was very important to avoid issues when working with such large files.

To make our analysis more useful, we also included weather data. At first, we merged weather data with all three months, but later, we decided to focus only on September because that month had the most rides. To compare the two datasets, we added an hour column to the Citi Bike data so we could match each ride with weather conditions at that time. This helped us see how factors like temperature, humidity, and wind speed affected ridership. Our goal was to provide useful insights that could help improve the Citi Bike system in New York City.

Collecting and Organizing the Data
Since we were working with large datasets, we needed to use different tools and techniques to make the process more manageable. First, we downloaded the Citi Bike data from the official website and cleaned it by:

Fixing date and time formats to make sure they were consistent
Removing missing values and duplicate entries to avoid errors
Standardizing column names so they were easier to work with
Converting coordinates into numerical values
Filtering out negative trip durations, which were mistakes in the data
For the weather data, we removed unnecessary columns and kept only useful details like temperature, humidity, and wind speed. We also added extra information, such as the week number and the week-of-the-month, to help with the analysis. Finally, we merged the Citi Bike and weather datasets by matching the time and date, creating a well-structured dataset that linked bike trips with weather conditions.

Why This Matters
This project showed us how important it is to collect and organize data before starting an analysis. When we first began working with the files, our laptops kept freezing because of how large the datasets were. Without the right tools, working with big data can become overwhelming and frustrating.

We used Pandas for data processing and Datetime functions to organize time-based information. These tools helped us turn raw data into clear and useful insights. By the end of our project, we were able to see how weather and time of day impacted Citi Bike usage. This kind of analysis can help city planners and Citi Bike managers make better decisions about bike availability, station locations, and service improvements.

Create actionable insight across a range of contexts (e.g. societal, business, political),
using data and the full data science life cycle


