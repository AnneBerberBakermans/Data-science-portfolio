# Overview 

Name: Anne Berber Bakermans

SUID: 5898659222

email: abbakerm@syr.edu

Resume; See file Resume.Ber-Bakermans.docx

# Table of content 
1. Collect, store, and access data by identifying and leveraging applicable technologies
2. Create actionable insight across a range of contexts (e.g. societal, business, political),
using data and the full data science life cycle
3. Apply visualization and predictive models to help generate actionable insight
4. Use programming languages such as Rand Python to support the generation of
actionable insight
5. Communicate insights gained via visualization and analytics to a broad range of
audiences (including project sponsors and technical team leads
6. Apply ethics in the development, use and evaluation of data and predictive models (e.g.,
fairness, bias, transparency, privacy)
7. Overall learning goals
8. Strenght and Weaknesses
9. Life-long learning


# 1. Collect, store, and access data by identifying and leveraging applicable technologies

For our final project in IST 652: Scripting for Data Analytics, we analyzed Citi Bike rentals in New York City to find patterns in how people use the bike-sharing system. We focused on July, August, and September because these months had the highest number of rides. Since the data for each month was stored in a separate file, we had to gather, clean, and combine them before we could start analyzing. Each month had around 4–5 million rows, so organizing the data properly was very important to avoid issues when working with such large files.

To make our analysis more useful, we also included weather data. At first, we merged weather data with all three months, but later, we decided to focus only on September because that month had the most rides. To compare the two datasets, we added an hour column to the Citi Bike data so we could match each ride with weather conditions at that time. This helped us see how factors like temperature, humidity, and wind speed affected ridership. Our goal was to provide useful insights that could help improve the Citi Bike system in New York City.

Since we were working with large datasets, we needed to use different tools and techniques to make the process more manageable. First, we downloaded the Citi Bike data from the official website and cleaned it by:

- Fixing date and time formats to make sure they were consistent
- Removing missing values and duplicate entries to avoid errors
- Standardizing column names so they were easier to work with
- Converting coordinates into numerical values
- Filtering out negative trip durations, which were mistakes in the data
- 
For the weather data, we removed unnecessary columns and kept only useful details like temperature, humidity, and wind speed. We also added extra information, such as the week number and the week-of-the-month, to help with the analysis. Finally, we merged the Citi Bike and weather datasets by matching the time and date, creating a well-structured dataset that linked bike trips with weather conditions.

This project showed us how important it is to collect and organize data before starting an analysis. When we first began working with the files, our laptops kept freezing because of how large the datasets were. Without the right tools, working with big data can become overwhelming and frustrating.

We used Pandas for data processing and Datetime functions to organize time-based information. These tools helped us turn raw data into clear and useful insights. By the end of our project, we were able to see how weather and time of day impacted Citi Bike usage. This kind of analysis can help city planners and Citi Bike managers make better decisions about bike availability, station locations, and service improvements.

See document 1-code.ipynb

# 2. Create actionable insight across a range of contexts (e.g. societal, business, political), using data and the full data science life cycle

One of the classes that really focused on gaining insights across different contexts was Responsible AI (IST644). In one of our first assignments, we worked with the Adult Income dataset from the UCI Machine Learning Repository. This dataset looks at whether a person earns more than $50K per year, based on factors like education, occupation, and marital status. Since income prediction relies on demographic information, it raises important questions about fairness and bias in AI models.

This assignment showed how data science can be used to create actionable insights in different areas—society, business, and policy. In a societal context, it highlighted how AI can reinforce inequalities if models aren’t carefully built. In a business setting, understanding income trends could help companies improve hiring policies. From a political perspective, it raised questions about wage gaps and economic mobility.

We started with Exploratory Data Analysis (EDA) to understand the dataset and uncover patterns in income levels. We looked at key factors such as:
- Age – Are older individuals more likely to earn above $50K?
- Hours worked per week – Does working more actually lead to higher income?
- Education level (education_num) – How does education impact earning potential?
- After exploring the data, we built a logistic regression model to predict whether someone earns more than $50K per year. This model helped us see which factors had the - strongest influence on income.

This assignment really showed how data science can be applied to different areas. In business, companies use similar models for salary predictions or workforce planning. Governments might analyze this kind of data when making policies about wages and education. On a societal level, it showed how AI can either help reduce bias or unintentionally reinforce existing inequalities.

The biggest takeaway was that data science isn’t just about making predictions.It’s about making fair and meaningful decisions. This assignment made it clear that when working with real-world data, we have to think about how our models impact people and ensure that our insights are responsible and useful across different contexts.

See document 2-code.ipynb

# 3.Apply visualization and predictive models to help generate actionable insight

For our Introduction to Data Science class, I worked on a homework assignment analyzing food scarcity data. Some communities in the U.S. struggle to get healthy and affordable food because they live far from supermarkets or grocery stores. This limited access can make it difficult for people to maintain a balanced diet. There are many ways to measure food store access and define areas that lack these resources. In our assignment, we focused on one specific measure—how far people had to travel to reach a supermarket.

The dataset included a variable called LAPOP1_10, which represented the number of people in each U.S. county who lived more than 1 mile away (for urban areas) or more than 10 miles away (for rural areas) from a supermarket. This measure helped identify populations at risk of food insecurity.

Before analyzing the data, I needed to clean it. This involved converting values into numeric form and removing missing data (NA values). Once the data was cleaned, I performed exploratory data analysis (EDA) to better understand the dataset. For example, I found out which county had the smallest population. I then created a new variable called insecurityRatio, which we calculated by dividing LAPOP1_10 by Pop2010 (the total county population). This ratio showed the percentage of people in each county who lived too far from a supermarket and were therefore at risk of food insecurity. By creating this ratio, I made it easier to compare food insecurity across different counties.

To combine multiple datasets, I needed a common column to merge them properly. The dfIns dataset contained a column called Largest_city, while the pop dataset had a city column. However, city names alone were not unique, as different states could have cities with the same name. To solve this, I created a new column called city_state by combining the city and state names. This allowed us to accurately merge the two datasets.

Once the data was merged, I used different types of graphs to visualize food insecurity across the U.S.:

- A map of the U.S. with points representing each city, where color indicated the insecurity ratio.
- A bar chart comparing the food insecurity ratio by state.
- A scatter plot showing state populations.
- A heat map where each state’s color represented its level of food insecurity.

Key Takeaways
The biggest takeaway from this homework was how useful visualizations can be for understanding data. Simply looking at numbers in a table can make it hard to see patterns, but graphs and maps help make the information clearer. For example, My ggplot visualizations helped show which areas had the highest food insecurity, making the data more meaningful. This assignment showed how important data visualization is in turning raw data into useful insights.

See document 3-code.pdf

# 4. Use programming languages such as Rand Python to support the generation of actionable insight

For Homework 4 in the Scripting for Data Analytics course, I worked with a large dataset containing crime reports from Chicago between 2018 and 2021. The task required me to process and analyze the data and extract two meaningful insights from it.

For my first analysis, I focused on identifying which types of crimes occurred most frequently. After processing the data, I found that theft was the most common crime, with a total of 209,507 theft incidents reported. I then wanted to see if there was a year with more thefts than others, so I examined the data over the years and found that 2018 had the highest number of thefts. I also looked at which police beat had the most thefts, and it turned out that Beat 1834 had the highest concentration. This showed that this area was more prone to thefts than others in the city. Additionally, I explored the location descriptions of the thefts and discovered that most of them took place on streets, suggesting that street-level crimes were more frequent. Another important finding was that most of these thefts involved amounts of $500 or less, meaning lower-value thefts were more common than larger, more serious ones.

After analyzing these findings, I decided to dive deeper into the overall crime trends between 2018 and 2021. I looked at the total number of reported crimes each year and found that it dropped from 268,324 in 2018 to 207,863 in 2021, showing a clear decrease in the number of crimes over time. I also examined the number of arrests made each year, and found that the total number of arrests dropped from 53,757 in 2018 to 25,839 in 2021. While this decrease in arrests seemed to correspond with the decline in reported crimes, I noticed something interesting. The arrest rate, which is the percentage of crimes that led to arrests, improved slightly from 20.03% in 2018 to 21.50% in 2019, but then it sharply declined to 12.43% by 2021, even though fewer crimes were reported.

This sharp drop in the arrest rate might be linked to the COVID-19 pandemic, which affected police operations and made it harder for them to make arrests. However, without more detailed data on how the pandemic impacted crime and law enforcement in Chicago, it’s difficult to draw any definitive conclusions.

From my analysis, several key insights emerged:

No Arrests: A significant portion of the crimes each year did not lead to arrests. This suggests that there may be gaps in the law enforcement process, such as lack of evidence, lower priority given to certain crimes, or issues in tracking and apprehending suspects.

Missing Location Data: Some of the crimes in the dataset were missing location information. This makes it harder to map crime hotspots and understand the geographic trends of criminal activity, especially at the neighborhood level.

Unresolved Crimes: There was a smaller subset of crimes that lacked both arrest records and location data. These cases are particularly concerning because they represent significant gaps in both resolving the crime and tracking where it occurred, which is important for understanding crime patterns.

To address these issues and improve the quality of crime data, I suggest the following measures:

Improved Data Collection: A key solution would be to enhance the way location data is collected. Ensuring that every crime is properly geo-coded and that location information is recorded accurately will allow for more detailed crime mapping, making it easier to identify high-crime areas and trends over time.

Focus on Unresolved Cases: Another useful step would be to investigate the categories of crimes that were not followed by arrests, especially those that were missing both arrest and location data. Understanding why these cases remain unresolved could help law enforcement agencies prioritize certain types of crimes or improve their investigative processes.

Integrate Arrest and Location Data: Combining arrest data with geographic data could help us identify areas where crimes are more likely to go unresolved. By understanding these patterns, police can better allocate resources to areas with higher rates of unresolved or unnoticed crimes. Additionally, this data could be used for predictive policing, where patterns from historical data are used to predict where future crimes may occur, allowing law enforcement to proactively respond.

See document 4-code.ipynb

# 5. Communicate insights gained via visualization and analytics to a broad range of audiences (including project sponsors and technical team leads

For our final presentation in ACC 652 (Accounting Analytics), my group chose Vail Resorts as the company to analyze. We began by providing a brief overview of the company and explaining its global presence to give context for those unfamiliar with Vail Resorts. Next, we identified three key questions we wanted to answer about the company, with my focus being on how Vail Resorts generates revenue from different business areas, such as lift tickets, lodging, retail, and dining, a concept known as "revenue diversification."

Using data from Vail Resorts' 10-K filings (detailed financial reports filed with the SEC), we analyzed how much revenue the company generates from each area and whether any segments were growing faster than others. This analysis was important for understanding how shifts in one revenue stream could impact the company’s overall financial stability.

To present these findings, I created four clear and effective visuals. The first visual was a bar chart that compared the revenue from mountain activities (like lift tickets) and lodging. The second and third visuals were line charts that tracked these revenue streams over time, with color differentiation to make the trends easier to follow.

I made sure to keep the visuals simple and focused, ensuring that the analysis could be easily followed. By focusing on key trends, like growth in specific revenue segments, I highlighted insights that were critical for understanding the company’s financial health and how different business areas contributed to overall performance. This allowed for a focused, data-driven discussion on how revenue diversification impacts the company’s stability and future growth.

This is important because looking at how Vail Resorts makes money from different areas helps us understand how stable the company is and how it can grow. By seeing which parts of the business, like lift tickets, lodging, retail, and dining, are making the most money, we can figure out where the company is doing well and where it might be struggling. This kind of analysis helps show if the company relies too much on one area and if that could cause problems in the future. For those making decisions at the company, this information is helpful for planning, making smart investments, and making sure the business stays strong even if some areas face challenges. Understanding which parts of the business are growing helps the company focus on what’s working and improve what’s not.

See document 5-code.pptx

# 6. Apply ethics in the development, use and evaluation of data and predictive models (e.g., fairness, bias, transparency, privacy)

In our Responsible AI class (IST 644), we worked with a dataset that focused on data science STEM salaries. We used two main methods, LIME and SHAP, to understand how the model makes predictions and to check if it treats everyone fairly.

LIME (Local Interpretable Model Explanations) LIME helps us figure out what factors are most important in the model’s predictions. For this analysis, we looked at the 3rd row in the dataset, which showed information about salaries in data science STEM roles. The main factors that influenced the salary prediction were base salary and stock grant value. LIME uses colors to show how each factor impacts the result:

Blue means it pushes the prediction toward a lower salary ("less than medium").
Orange means it pushes the prediction toward a higher salary ("more than medium"). In this case, the prediction for the 3rd row was "less than medium."
SHAP (Shapley Additive Explanations) SHAP looks at how much each factor, like base salary, stock grant value, bonus, and years of experience, affects the salary prediction. The key factors SHAP found were similar to those identified in LIME, showing both methods agree on what matters most for salary predictions.

Fairness and Bias Analysis We also looked at whether the model treated different groups fairly, especially focusing on race and gender. We found some differences:

Race: Black individuals were less likely to have higher salary predictions compared to other racial groups.
Gender: Female individuals were less likely to get higher salary predictions compared to male individuals.
False Positive Rates by Group We also checked how often the model made incorrect predictions (false positives) for different racial groups:

- Hispanic: 0.07
- More than two races: 0.05
- White: 0.11
- Asian: 0.12
- Black: 0.17 (the highest)
- The higher false positive rate for Black individuals (0.17) shows that the model is less accurate for this group, which could indicate bias in the model’s predictions.

Ethics in Model Development Our analysis raised some important ethical issues:

Fairness: The model seems to treat Black individuals and females unfairly, as shown by the higher false positive rates and fewer predictions for higher salaries.
Bias: There are clear racial and gender biases in the model, and it’s important to address these to make the model fairer.
Transparency: Tools like LIME and SHAP help us understand how the model makes decisions, but more work is needed to ensure fairness in the salary predictions.
Improvement: The model needs to be improved to avoid bias and make salary predictions fairer and more accurate for all racial and gender groups.

This analysis highlights the need to include fairness, transparency, and bias reduction in building and assessing predictive models, so we can create systems that are both ethical and trustworthy. 

See document 6-code.ipynb

# 7. Overall learning goals

I can see that my knowledge of data science has grown significantly in different areas.  I decided to take all the Data Science courses and choose electives more focused on Data Analytics. When I started this degree, I wasn’t sure exactly what I wanted to do or which path to take. I was always interested in analytics, but I was surprised by how much I enjoyed coding and spending hours figuring out different codes. The classes I took in my first semester were Data Administration Concepts & Database Management, Quantitative Reasoning for Data Science, Introduction to Data Science, and Business Analytics. Each class taught me something new.

In my first semester, I want to highlight two classes. First, Data Administration Concepts & Database Management. 
At first, I struggled with working with an external database and learning more advanced SQL. It was challenging, but with help from my professors and classmates, it became easier the more time I spent on it and the more I understood it. In this class, we finished by creating a project where we designed a database-driven solution to improve the public transportation system of New Syracusedam (a database we built ourselves). Using Python and SQL, we analyzed data on ridership, vehicle performance, and station usage. When I started this class, I didn’t think I would be able to do this. Working on this real-world project helped me learn better and collaborate with others on my coursework.

Another class I want to highlight is Introduction to Data Science. I really enjoyed this course because it went back to the basics of coding and data science, ensuring we fully understood what we were doing. At the end of the class, we had a project that was quite challenging. As a team, we started analyzing the data without much direction. While some initial exploratory data analysis (EDA) is always helpful, I learned that having a clear plan from the start is very important.
The dataset we worked with was large, and even though we could explore it, we quickly realized we needed a strategy to handle it properly. After struggling at first, we sat down as a team, created a plan, and adjusted it as needed. Being thrown into the project without clear guidance actually helped emphasize how important it is to plan ahead. You can always make changes along the way, but you need to have a goal in mind and a clear approach to working with the data.

Another class I want to highlight is one I took over the summer: Managing Data Science Projects. This course lasted four full days, and at first, I was unsure how an entire class could fit into such a short time. However, it did not disappoint. The way the material was taught and the information we covered were very helpful.
We went through the entire process of managing data science projects and explored different methods for doing so. This was extremely useful, and even as I moved into my second semester, the lessons from this class helped me a lot. I was able to apply the frameworks I learned to my bigger projects, making them more structured and manageable.

In my second semester, I took Accounting Analytics, Scripting for Data Analytics, Responsible AI, and Applied Machine Learning. Applied Machine Learning was definitely a challenging but enjoyable class. We explored different machine learning techniques in depth and ended the course with a project analyzing Airbnb data.
Our project focused on detecting fake or fraudulent Airbnb listings. We built a model that analyzed listing details such as price, location, and host information to identify patterns and spot anything unusual that could indicate fraud. The goal was to provide Airbnb platform managers with a tool to screen and flag suspicious listings, helping to keep guests and hosts safe. This project brought together everything we had learned, allowing us to apply machine learning techniques in a real-world scenario. The most exciting part was that we actually found a listing that appeared to be the same property listed by two different hosts, both using the same license ID. This was unusual since Airbnb assigns a unique license ID per host and property.

# 8. Strenght and Weaknesses
Looking back at my time in the Master’s in Applied Data Science program, I can see how much I've grown, both in my strengths and areas where I had to put in extra effort.
One strength I developed was my ability to learn new technical skills quickly. Coming into the program, I had a general interest in data analytics, but I didn’t expect to enjoy coding as much as I did. I found myself getting lost in coding challenges and spending hours working through problems, which made me realize I actually enjoyed it. As I worked on different projects, especially those that involved machine learning and real-world data, I became more confident in my technical abilities.

Another strength I noticed was my ability to adapt. There were many times when I faced challenges that were new to me, like working with SQL and external databases. At first, it felt overwhelming, but with help from my professors and classmates, I figured it out. I learned that if I kept pushing forward and asked questions when needed, I could handle tough situations. I also learned how to approach problems step by step, which helped me grow stronger in coding and problem-solving.
However, balancing school and athletics was challenging at times. As a student-athlete, I had to manage not only my coursework but also training and games. It was tough to find enough time for both, especially when deadlines were tight. In the beginning, I struggled to stay on top of everything, but I eventually learned to manage my time better. I started breaking projects down into smaller tasks and planning out my days so I could give both my studies and athletics the attention they needed.

Another weakness I faced was understanding how to handle big data science projects. While I could analyze data and build models, I sometimes felt unsure about how to organize larger projects. It wasn’t until I took the Managing Data Science Projects class that I realized the importance of planning. This class showed me that managing a project is about more than just coding; it’s about making a plan, setting goals, and staying organized. Once I started applying these lessons, I noticed my projects ran more smoothly and were more efficient.

Looking back, the program pushed me to improve my technical skills and my ability to manage projects. It also helped me become better at balancing my time between school and athletics. I’ve learned that while coding and problem-solving are key, being organized and having a clear plan are just as important.

# 9. Life-long learning
I’ve learned that learning never really ends. In the world of data science, there’s always something new to discover—whether it’s a new tool, technique, or idea. I’ve realized that staying curious and always striving to learn more is key to being successful.
Being a student-athlete also taught me the value of life-long learning. Sports showed me that progress comes from putting in the effort and listening to feedback. Whether it’s improving in sports or my studies, I’ve learned that small daily improvements really add up.

In data science, I see the same principle. The more I engage in projects or try new things, the more I expand my skills. I’ve also come to appreciate how valuable it is to learn from others—whether it’s teammates, classmates, or mentors. I’m excited to continue learning and growing, and I look forward to applying everything I’ve learned to real-world situations.

