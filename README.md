# NYC-Bus-Breakdown-and-Delays

![Screenshot 2024-02-21 151706](https://github.com/NanManee/NYC_School_Bus/assets/156528525/7fa22ab3-13cf-40de-8b13-39ecbb03cb23)

### Data Source

The system for tracking bus breakdowns and delays gathers data from school bus vendors actively operating in the field in real-time. When bus personnel encounter delays during their routes, they're directed to communicate with the dispatcher at the central office of the bus vendor. Subsequently, the bus vendor's staff is prompted to access the Bus Breakdown and Delay system to document the incident and inform OPT. Customer service representatives at OPT utilize this system to update parents calling about bus service inquiries. The Bus Breakdown and Delay system is openly accessible and provides real-time updates, with all information inputted by school bus vendor staff.
- https://data.cityofnewyork.us/Transportation/Bus-Breakdown-and-Delays/ez4e-fazm/about_data
- Year 2016 - 2023


### Project Task

- Analyzing historical data from the system to identify common causes such as mechanical issues, traffic congestion, weather conditions, etc.
- Analyze the timestamp data from the system to determine if there are specific times of day or days of the week when delays and breakdowns are more common.
- Aggregate and analyze data from the system to identify bus companies that have reported the highest number of delay incidents over a certain period. This analysis can help identify potential areas for improvement or intervention.

### Questions to Answer


- Is there a particular time of day when school bus delays and breakdowns occur?
- What are the major reasons and causes of school bus delays and breakdowns?
- Which bus companies experience the most delays?

  
### Tools

- Microsoft Excel - Data Cleaning and Data Analysis
- Tableau - Data Visualization

### Inspecting Dataset

- The dataset contains 21 columns and 282,192 rows, including column names.
- Apply Filters to all columns to check for any errors, null, or misspellings.

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/35f59577-cfd6-48b5-9aca-27916f0a9a5c)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/c1d00b6e-ae7c-4634-8874-6819382d7ff4)



### Data Cleaning and Standardize data formatting across the table

- Check and Remove Duplicates, by select the whole table and checked for duplicate values.

- Transform the data into separate columns.
  

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/10645180-4591-4dcf-a77a-2e5492868896)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/885e3ff8-0292-42aa-8c52-d70207a83ea5)


- Now, we have date and time columns available.
  

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/5e003adc-e1f8-41bf-9c43-e6d728c9b002)


- Change the column 'Day' from General format to Number format.
  

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/a64d3e10-a8df-4e20-8477-c5a20baa485f)

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/10b24bda-f99c-4298-a12e-15b7b8e06e67)


- Apply the Weekday() function to transform the day into a number representing the day of the week, starting with 1 for Monday.


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/eaaf4233-af4f-4a0b-9133-c997f04b9e4f)



- Use the filter to unselect everything, then select only number 1 and replace it with 'Monday'. Repeat this process for numbers 2 through 7, replacing them with 'Tuesday' through 'Sunday', respectively.
  
  
![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/9096bdd8-b60e-491c-b5ce-05b26eb7f31c)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/1b52ed3a-c85a-4887-a5ec-a9dc59fe18e5)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/660aff56-4219-40ed-b7fc-e87765a25427)


- Now we have the day column available.


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/e0ba7b78-f3f6-40de-becb-869ce216848b)


- Remove repeated company names in the 'Bus Company Name' column to declutter the dataset.
  

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/63e8589d-2a2a-4ef8-9907-405cf7c42bd1)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/20277262-5544-4c26-bca4-24cabf8e7571)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/ca6626b9-bcac-4998-b6c2-4a6eaed9b716)


- Separate the column 'How long Delayed' into 'Short Delay Time' and 'Long Delay Time' to calculate the average delay time for each category later on.
  

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/9e11a816-5f02-4ce7-bb3d-dee89e5971c0)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/7929cbe0-afc9-426f-9ce4-79ad3449d224)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/90b2f595-2a58-4c70-9595-baf6e86de0ca)



- This dataset spans from 2016 to 2023. However, in the 'Last Updated On' column, there are entries with the date 1/1/1900, which appear to be incorrect. Therefore, I will delete them all.


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/a6916861-35db-4a69-8768-4f23a0489899)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/8ffca913-b2a3-4f11-bee4-89d623fc461d)



- I will only clean the columns that have data relating to the questions I need to answer.
- After completing the data cleaning process, the dataset is now prepared for upload into Tableau, where it will be utilized to generate comprehensive data visualizations for analysis and presentation of findings.



# Tableau Visualization:
https://public.tableau.com/app/profile/nanthawan.maneethong/viz/NYCSchoolBusDelays/Dashboard1



### Findings and Recomendations:



### 1. The main cause of Bus delays is heavy traffic, which accounts for around 176,000 delays. The mojority of bus delays happen during the morning hours, causing as high as 214,000 delays, and during the afternoon about 50,000 delays. 


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/15ac7116-8282-49f1-a77e-db98f4ebc8c4)
![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/54b34004-4111-4847-b567-a6d5bd20915e)



	- Highly recommend to regularly reviewing and adjusting routes based on changing traffic patterns and new developments.
	- Utilize software to plan and optimize routes based on real-time traffic conditions, road closures, and construction work. This can help in finding the quickest and most efficient paths.
	- Collaborate with local municipalities to establish dedicated school bus lanes on key routes during peak hours. This can significantly reduce delays caused by general traffic congestion.
	- Advocate for infrastructure improvements that facilitate smoother traffic flow, such as better road layouts, additional turning lanes, and improved signaling at intersections
   
### 2. Bus breakdowns mostly occur due to mechanical problems, resulting in almost 14,000 delays. Bus breakdowns happen during the morning hours, causing about 12,000 delays, and during the afternoon about 6,000 delays.


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/9cb82909-78c6-4352-b13f-ebdadc13dfb1)


	- Highly recommend setting a regular maintenance schedule for all buses to prevent mechanical issues. This includes regular inspections, servicing, and timely replacement of worn-out parts.
	- Install advanced diagnostic systems on buses to detect potential mechanical issues before they lead to breakdowns. This proactive approach can significantly reduce the frequency of breakdowns.
	- Provide comprehensive training to drivers on how to identify early warning signs of mechanical problems and how to respond appropriately to prevent breakdowns.
	- Develop a clear protocol for drivers to follow in the event of a breakdown, including quick communication with dispatch, student assistance procedures, and efficient coordination with maintenance teams.
	- Provide spare buses during peak hours to quickly replace any buses experiencing mechanical issues, minimizing delays for students.
 

### 3. The companies with the highest delay times, ranging from 46 minutes to 1.30 hours, should be investigated further. 


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/824f45f6-b02e-4b5c-9a3e-56c4bf52421c)


	- Highly recommend investigating additional data, gather and analyze historical data on delay times for the company in question. Assess the frequency, duration, and impact of delays on the overall service.
	- Compare delay times of the company with industry standards and benchmarks to determine if they significantly deviate from the norm.
	- Engage in dialogue with the bus company to understand the root causes of delays and their efforts to address them. Evaluate their responsiveness and commitment to improving service.
	- Contractual Obligations: Review the terms of the contract with the bus company to determine if there are specific clauses related to service performance and termination conditions.
	- Based on the comprehensive analysis and assessment, make an informed decision on whether to continue or terminate the contract with the bus company. Ensure the decision-making process and communicate the rationale to all relevant parties.
	- If the decision is made to terminate the contract, initiate the necessary contractual procedures in accordance with legal and regulatory requirements. Consider any potential contractual penalties or termination clauses.
	- Continuously monitor the performance of the selected bus company and evaluate the effectiveness of the decision. Adjust strategies as needed to ensure ongoing improvement in transportation services.

