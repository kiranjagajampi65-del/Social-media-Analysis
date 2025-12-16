 📊  Social-media-Analysis Dashboard 

A complete analysis of Meta Ads (Facebook & Instagram) performance using Power BI. This project uncovers how different ad formats, audiences, budgets, and time periods influence engagement, clicks, and conversions — helping marketing teams improve ROI and make data-driven decisions

Project Overview

This Power BI dashboard provides an interactive view of Meta Ads performance across Facebook and Instagram. It helps understand how ads perform by showing clear insights into ad formats, audience demographics, locations, budget usage, and performance trends over time.

The dashboard tracks important metrics such as impressions, clicks, engagement, conversions, CTR, engagement rate, conversion rate, and ROI. These insights help marketing teams see what is working well, identify areas that need improvement, and make better, data-driven decisions to improve ad performance and return on ad spend.

Key strength: The campaigns perform very well in creating awareness and engagement.
Key opportunity: Improving the conversion stage so that high interest leads to more purchases.



-The ads were shown 216,000 times, so they reached a large number of people.
-25,400 users clicked on the ads, showing strong interest in the content.
-Users shared the ads 1,300 times, which shows organic engagement.
-2,600 comments were posted, meaning people actively interacted with the ads.
-In total, there were 29,000 engagements (clicks, shares, and comments combined).
-The CTR of 11.76% is very good and much higher than the usual industry average.
-The engagement rate of 13.56% shows that the audience liked the ads.
-The ads generated 1,300 purchases, resulting in real customer conversions.
-The conversion rate is 5.21%, which is good but can still be improved.
-The purchase rate is only 0.61%, meaning many users did not complete the purchase.
-A total of $2.5 million was spent on advertising campaigns.
-The average budget per campaign was $50.7K, showing that multiple campaigns were running



📅 Calendar-Based Engagement Insights
Engagement activity is mapped across the days of June to identify performance patterns over time.
The data shows clear engagement spikes between the 19th–21st and 25th–27th, indicating periods of heightened user interaction.

These peaks likely align with campaign launches, promotions, or special offers, suggesting that time-bound marketing activities significantly influence engagement levels.

*Ad Type Performance Explanation*

Video ads received 46K impressions and 5K clicks and delivered the best overall performance. They achieved the highest click-through rate at 11.9% and the highest engagement rate at 13.7%, making them the most effective format for driving both interest and conversions.

Stories ads generated the highest reach with 72K impressions and 8K clicks. Their CTR of 11.8% and strong purchase and conversion rates show that this format is very effective for engagement and visibility, especially among mobile users.

Image ads recorded 51K impressions and 6K clicks. While their engagement rate remains healthy, their conversion and purchase rates are slightly lower compared to video and stories ads. This suggests that image ads are better suited for awareness rather than driving purchases.

Carousel ads delivered 48K impressions and 6K clicks. Their performance is consistent but slightly weaker in conversions when compared to video and stories ads. Carousel ads are useful for showcasing multiple products but may require stronger messaging to improve conversion results.

Overall, video ads perform the best, followed closely by stories ads. Image and carousel formats support reach and awareness but should receive a smaller share of the budget if the main goal is conversions and ROI.


👥 Audience Engagement Analysis
Gender-Wise Engagement

Female: 43% (highest engagement)
Male: 22%
Other/Not Specified: 35%
Insight: Better results with female audience → Ads should focus more on women.
Age Group Performance
Highest engagement: 20–30 years
Significant drop after 35+
Insight: Primary audience = young adults (18–30).

Domain Knowledge Document – Meta Ad Performance Dataset
📌 1. About the Data

This dataset represents Meta Ads Performance Data, similar to how Facebook and Instagram record interactions between users and ads.
It includes:

Campaign-level data

Ad-level data

User demographic data

Event-level interaction logs

The purpose of this dataset is to analyze and optimize:

Impressions → How many times ads were viewed

Clicks → User engagement

Purchases (Conversions) → Marketing effectiveness

CPM, CPC, CTR, ROAS → Cost and efficiency metrics

Audience Insights → Gender, age, country, interests

This dataset is ideal for building a Power BI Dashboard to evaluate campaign performance, budget utilization, and engagement patterns.

📌 2. Use of Each Table
Table 1: ad_events
Stores event-level logs: impressions, clicks, shares, comments, purchases
Fact table in the model (main table for KPIs)
Helps analyze when and how users interact with ads

Table 2: ads
Contains metadata for each ad creative
Includes targeting criteria and the platform where the ad runs
Supports analysis by ad type and platform (e.g., Instagram vs Facebook)

Table 3: campaigns

Defines campaign strategy, budget, start/end dates
Essential for calculating cost KPIs (CPC, CPM, ROAS)

Table 4: users

Stores demographic and interest data
Used for audience segmentation


📌 3. Table & Field Details
Table 1: ad_events
Purpose: Captures every user interaction with an ad.

Field	Description	Example	Usage
event_id	Event identifier	100234	Primary key
ad_id	Linked ad ID	501	Join with ads table
user_id	Linked user ID	U_1204	Join with users table
timestamp	Exact event time	2025-03-12 14:30:00	Build date hierarchy
day_of_week	Day name	Tuesday	Compare weekday vs weekend
time_of_day	Segment of day	Afternoon	Engagement trend
event_type	Impression/Click/Purchase	Click	Funnel analysis



Table 2: ads

Purpose: Defines targeting and creative-level details.

Field	Description	Example	Usage
ad_id	Unique ad ID	501	Primary key
campaign_id	Campaign reference	C_101	Join to campaigns
ad_platform	Facebook/Instagram/etc	Instagram	Compare platforms
ad_type	Image/Video/Story/Carousel	Video	Creative performance
target_gender	Targeted gender	Female	Targeting accuracy
target_age_group	Targeted age bracket	25–34	Compare vs actual
target_interests	Targeted interest groups	Fashion	Interest matching

Usage:
Helps evaluate ad creative performance and targeting accuracy.

Table 3: campaigns

Purpose: Stores campaign-level strategy data.

Field	Description	Example	Usage
campaign_id	Unique ID	C_101	Primary key
name	Campaign name	Spring Promo 2025	Reporting
start_date	Launch date	2025-03-01	Time analysis
end_date	End date	2025-03-31	Duration analysis
duration_days	Derived: campaign length	30	Campaign pacing
total_budget	Campaign budget	50,000	CPC, CPM, ROAS

Usage:
Budget tracking → CPM, CPC, ROAS, pacing analysis

Table 4: users

Purpose: Provides demographic segmentation.

Field	Description	Example	Usage
user_id	Unique ID	U_1204	Join to ad_events
user_gender	Gender	Male	Gender analysis
user_age	Age	27	Custom segmentation
age_group	Age classification	25–34	Compare age buckets
country	User country	India	Geographic insights
location	City/state	Bangalore	Regional targeting
interests	User's interests	Tech, Travel	Interest matching

Usage:
Helps identify if ads reached the intended audience or a different segment.

📌 4. How the Tables Work Together

This dataset follows a Star Schema Model:

Fact Table

ad_events → All KPIs derived here

Dimension Tables
ads → Creative & platform details
campaigns → Budget & timeframe
users → Demographics & interests

Relationships

ad_events.ad_id → ads.ad_id
ads.campaign_id → campaigns.campaign_id
ad_events.user_id → users.user_id

This structure enables:

Platform-wise analysis
Ad format analysis
Demographic insights
Budget vs performance tracking

Funnel analysis (Impression → Click → Purchase)


📈 Dashboard Charts & Requirements

1. Donut Chart – Target Gender
Shows metric split by gender (from ads table)
Metric changes dynamically
Purpose: Identify which gender contributes more to a metric.

2. Bar Chart – Target Age Group
Shows performance across age groups
Metric changes dynamically
Purpose: Find most responsive age group.

3. Map – Country Performance
Shows metric by country (from users table)
Bubble size/color → performance
Purpose: Identify top-performing countries geographically.

4. Calendar Heat Map – Monthly Activity
Based on timestamp in ad_events
Darker color → higher activity
Purpose: Analyze seasonal/peak ad trends.

5. Weekly Trend – Stacked Column by Ad Type

X-axis → Week number
Stacks → Ad types
Y-axis → Metric
Purpose: Compare ad-type performance weekly.

6. Area Chart – Hourly Activity Trend

X-axis → Hour (0–23)
Y-axis → Metric
Purpose: Identify best posting hours based on engagement.

7. Matrix – Ad Type vs Platform

Rows → Ad types
Columns → Platforms
Values → Selected metric
Purpose: Compare performance across ad formats & platforms.





📚 3. Domain Knowledge Document (Simple Explanation)
About the Data

This dataset represents how Facebook/Instagram track ads.
It helps measure:
How many people saw the ad
How many clicked
Who purchased
Which audience responds best
Which platform works better
ROI and budget efficiency
What Each Table Does (Short Summary)
ad_events: Stores all user interactions → Used for metrics like impressions, clicks, purchases.
ads: Stores ad details → Helps compare platforms, ad types, target groups.
campaigns: Stores budget + duration → Helps calculate CPM, CPC, ROAS.
users: User demographics → Helps analyze audience segmentation.


📌 Conclusion

This Meta Ads Dashboard gives a clear and easy understanding of how Facebook and Instagram ad campaigns are performing. Instead of looking at scattered numbers, everything is brought together in one place, making it simple to see what is working and what needs improvement.
The analysis shows that the ads are doing very well in terms of reach and engagement. People are clicking, liking, sharing, and interacting with the ads, which means the creatives and targeting are effective. However, the dashboard also reveals that fewer users are completing purchases, highlighting an opportunity to improve the conversion journey after the click.
With this dashboard, marketing teams can:
Better understand who their audience is and how different age groups, genders, and locations respond
Use the budget more wisely by investing in high-performing ad formats like Video and Stories
Easily spot strong and weak campaigns and take quick action
Improve conversion performance by identifying where users drop off
Make confident decisions based on data, not assumptions

Overall, this project demonstrates how a simple and clean analytics solution can help businesses improve ad performance, reduce wasted spend, and achieve better results from their marketing efforts.


