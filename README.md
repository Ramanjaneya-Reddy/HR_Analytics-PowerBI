                                              Abstract
With the emergence of HR Analytics in organizations; gathering, interpreting, and measuring of HR data has become easy. 
It acts as a tool which is a combination of statistical techniques that enable the collection, interpretation, measurement, and forecasting of data.
It enlightens solutions to organizational problems and makes accurate decisions.
HR Analytics provides various opportunities to businesses as forecast workforce requirements enable HR to achieve corporate goals and improve organizational performance which helps businesses in finding success. 
In this project, I tried to visualize the retrenchment rate and promotion rate in a company.

                                          Methodology Used
1. Start
2. Integrating data source with power query
3. Querying data onto the navigator
4. Editing the queries on the table
5. Shaping the data according to requirements
6. Merging queries from different tables
7. Creating visuals (charts, graphs, maps, etc) using different metrics in table
8. Loading the Report onto the Power BI Desktop

                            Creating measures using DAX (Data Analysis Expressions)
1. % Due For Promotion = DIVIDE([Due For Promotion],[Total Emp],0)
2. % female = DIVIDE([Female],[Total Emp],0)
3. % high rated = DIVIDE([High rated],[Total Emp],0)
4. % low rated = DIVIDE([Low rated],[Total Emp],0)
5. % male = DIVIDE([Male],[Total Emp],0)
6. % Not Due = DIVIDE([Not Due],[Total Emp],0)
7. % On service = DIVIDE([On Service],[Total Emp],0)
8. % will be retrenched = DIVIDE([Will be retrenched],[Total Emp],0)
9. Due For Promotion = if(isblank(CALCULATE([Total Emp],’HR Analytics Data’[Promotion Status]=”Due for Promotion”)),0,CALCULATE([Total Emp],’HR Analytics Data’[Promotion Status]=”Due for Promotion”))
10. Female = CALCULATE([Total Emp],’HR Analytics Data’[Gender]=”female”)
11. High rated = CALCULATE([Total Emp],’HR Analytics Data’[Performance Rating]=”High Rating”)
12. Low rated = CALCULATE([Total Emp],’HR Analytics Data’[Performance Rating]=”Low Rating”)
13. Male = CALCULATE([Total Emp],’HR Analytics Data’[Gender]=”male”)
14. Not Due = if(isblank(CALCULATE([Total Emp],’HR Analytics Data’[Promotion Status]=”Not Due”)),0,CALCULATE([Total Emp],’HR Analytics Data’[Promotion Status]=”Not Due”))
15. On Service = if(ISBLANK(CALCULATE([Total Emp],’HR Analytics Data’[Retrenchment Status]=”On service”)),0,CALCULATE([Total Emp],’HR Analytics Data’[Retrenchment Status]=”On service”))
16. Total Emp = COUNTROWS(‘HR Analytics Data’)
17. Will be retrenched = if(ISBLANK(CALCULATE([Total Emp],’HR Analytics Data’[Retrenchment Status]=”Will be retrenched”)),0,CALCULATE([Total Emp],’HR Analytics Data’[Retrenchment Status]=”Will be retrenched”))

                                                   Summary
We have successfully performed exploratory analysis on the HR analytics data set.
This dashboard gives a clear idea about employees of 3 departments in a company.
There are 72 employees due for promotion of which 47 are from research and development, 23 are from sales and the rest 2 are from the hr department. 
There are 117 employees who will be retrenched of which 74 are from research and development, 36 from sales, and 7 from the hr department. 
If we take job roles 44 will be retrenched, and 22 are due for promotion in total 0f 102 managers. 
Of a total of 80 research directors 20 will be retrenched, and 8 are due for promotion.
Of 326 sales executives, 20 will be retrenched and 16 are due for promotion. 
No sales representative will be retrenched. Neither human resources nor sales representatives are due for promotion.
