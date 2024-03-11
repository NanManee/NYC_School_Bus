# NYC-Bus-Breakdown-and-Delays

![Screenshot 2024-02-21 151706](https://github.com/NanManee/NYC_School_Bus/assets/156528525/7fa22ab3-13cf-40de-8b13-39ecbb03cb23)

### Data Source

The system for tracking bus breakdowns and delays gathers data from school bus vendors actively operating in the field in real-time. When bus personnel encounter delays during their routes, they're directed to communicate with the dispatcher at the central office of the bus vendor. Subsequently, the bus vendor's staff is prompted to access the Bus Breakdown and Delay system to document the incident and inform OPT. Customer service representatives at OPT utilize this system to update parents calling about bus service inquiries. The Bus Breakdown and Delay system is openly accessible and provides real-time updates, with all information inputted by school bus vendor staff.
- https://data.cityofnewyork.us/Transportation/Bus-Breakdown-and-Delays/ez4e-fazm/about_data
- Year 2016 - 2023
  
  
### Tools

Microsoft Excel - Data Cleaning, Data Analysis and Data visualization


### Inspecting Dataset

- The dataset contains 21 columns and 282,192 rows, including column names.
- Apply Filter for all columns to check for any errors, misspelling

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/35f59577-cfd6-48b5-9aca-27916f0a9a5c)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/c1d00b6e-ae7c-4634-8874-6819382d7ff4)


- I will only clean the columns that has data relating to the questions i need to answer.
- Transform data into separate columns.
  
![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/10645180-4591-4dcf-a77a-2e5492868896)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/885e3ff8-0292-42aa-8c52-d70207a83ea5)


- Now we have Date and time columns
  
![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/5e003adc-e1f8-41bf-9c43-e6d728c9b002)

- Select column 'Day' change from General to Number.

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/a64d3e10-a8df-4e20-8477-c5a20baa485f)


- Write Weekday() function to tansform to number of day in the week. Start with number 1 for Monday.

  
![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/eaaf4233-af4f-4a0b-9133-c997f04b9e4f)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/10b24bda-f99c-4298-a12e-15b7b8e06e67)


- Use filter, unselect everything, select only number 1, replace it with 'Monday'. Then replace 2 for Tuesday until 7 for Sunday.
  
![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/9096bdd8-b60e-491c-b5ce-05b26eb7f31c)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/1b52ed3a-c85a-4887-a5ec-a9dc59fe18e5)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/660aff56-4219-40ed-b7fc-e87765a25427)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/e0ba7b78-f3f6-40de-becb-869ce216848b)


### Standardize data

- Decluted repeated all company names in colum 'Bus Company name'.

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/63e8589d-2a2a-4ef8-9907-405cf7c42bd1)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/20277262-5544-4c26-bca4-24cabf8e7571)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/ca6626b9-bcac-4998-b6c2-4a6eaed9b716)


- Separate column 'How long Delayed' into Short Delay Time and Long Delay Time to find the avarage on each one later on.

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/9e11a816-5f02-4ce7-bb3d-dee89e5971c0)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/7929cbe0-afc9-426f-9ce4-79ad3449d224)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/90b2f595-2a58-4c70-9595-baf6e86de0ca)


- This dataset start year from 2016 - 2023, but on column 'Last Updated On' appears to have 1/1/1900, so I will delete them all.


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/a6916861-35db-4a69-8768-4f23a0489899)


![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/8ffca913-b2a3-4f11-bee4-89d623fc461d)



- Create pivot table and charts

![image](https://github.com/NanManee/NYC_School_Bus_Delay_Project/assets/156528525/998cd9d8-e0aa-457a-9a72-c6d8abea0efb)


















### Tableau Visualization:
https://public.tableau.com/app/profile/nanthawan.maneethong/viz/NYCSchoolBusDelays/Dashboard1

### Findings and Recomendations:

- The main cause of Bus delays is heavy traffic, which accounts for around 176,000 delays. The mojority of bus delays happen during the morning hours, causing as high as 214,000 delays, and during the afternoon about 50,000 delays. 
	- Highly recommend to regularly reviewing and adjusting routes based on changing traffic patterns and new developments.
	- Utilize software to plan and optimize routes based on real-time traffic conditions, road closures, and construction work. This can help in finding the quickest and most efficient paths.
	- Collaborate with local municipalities to establish dedicated school bus lanes on key routes during peak hours. This can significantly reduce delays caused by general traffic congestion.
	- Advocate for infrastructure improvements that facilitate smoother traffic flow, such as better road layouts, additional turning lanes, and improved signaling at intersections
  - Bus breakdowns mostly occur due to mechanical problems, resulting in almost 14,000 delays. Bus breakdowns happen during the morning hours, causing about 12,000 delays, and during the afternoon about 6,000 delays.
	- Highly recommend setting a regular maintenance schedule for all buses to prevent mechanical issues. This includes regular inspections, servicing, and timely replacement of worn-out parts.
	- Install advanced diagnostic systems on buses to detect potential mechanical issues before they lead to breakdowns. This proactive approach can significantly reduce the frequency of breakdowns.
	- Provide comprehensive training to drivers on how to identify early warning signs of mechanical problems and how to respond appropriately to prevent breakdowns.
	- Develop a clear protocol for drivers to follow in the event of a breakdown, including quick communication with dispatch, student assistance procedures, and efficient coordination with 	  	  maintenance teams.
	- Provide spare buses during peak hours to quickly replace any buses experiencing mechanical issues, minimizing delays for students.

- The top 5 companies with the highest delay times, ranging from 46 minutes to 1.30 hours, should be investigated further. 
	- Highly recommend investigating additional data of total trips and delay times for each bus company. 
	- Determininh whether to continue or discontinue services for specific bus companies should be made considering factors such as the severity and frequency of delays, the company's responsiveness 	  to improvement efforts, and the impact on students' overall satisfaction and convenience.

![image](https://github.com/NanManee/NYC_School_Bus/assets/156528525/f291c237-daea-456a-80c6-01d946894414)

