# **An_Analysis_of_Kickstarter_Campaigns**
Analyzing data for Kickstarter campaigns gloably using descriptive statistics, meansuring outcomes and trends and by specific geographic regions and interest.

## **Executive summary** 

This report uses powerful tools in Excel to explore crowdfunding data from Kickstarter campaigns around the world.  The report dives into data from theater productions, a large contributor to the Kickstarter platform, and distills outcomes in the US and UK to help maximize successful launches.  The report then analyzes Kickstarter campaigns more broadly by goal amounts to provide needed context for aspiring Kickstarter campaigns to make the most of the platform.


## **Analysis and Challenges**

#### Theater Productions

Theater campaigns make up more than half of all Kickstarter campaigns in the US and UK and are an important avenue for access to funding.  Timing clearly matters when a theater company plans to launch its campaign as demonstrated in the graphic below.  While theater companies regularly perform inside - think of the Nutcracker - clearly, there is something about the summer months that inspires the attention of audiences.   

![Theater Outcome](/Theater_Outcomes_vs_Launch.png)


#### Fundraising Goals

The fundraising goals initially set by artists are incredibly important to determine their success.  [Kickstarter’s model](https://www.kickstarter.com/how-it-works) is based on an all-or-nothing approach to securing crowdsourced funding.  As the chart below demonstrates, campaigns see declining levels of success as their fundraising goals become more ambitious.  This isn’t to say that high achievers are not able to see success, indeed there is a spike of successful campaigns evident between $40,000 - $45,000, but artists should take the data and seriously consider realistic fundraising goals for their projects.  

![Goals](/Outcomes_vs_Goals.png)

#### Challenges 

Two related challenges with the composition dataset became apparent throughout this project.  The first issue is that the goal amounts are not normally distributed, with some questionably high outliers included.  A more robust study would seek or normalize the data first and detail the steps taken to either include or exclude certain data.  The second challenge based on the nature of the data is that many projects simply never got off the ground, with over 500 campaigns garnering less than $5 in pledged funds.  This affected the range of data with a ‘bunched’ distribution around 0.  Further efforts could normalize the data by only including successful campaigns above a certain threshold, though at the cost of not making Kickstarter campaigns seem more successful than they actually are.  

  
## **Results**

#### Theater Productions

This report uses a pivot table to allow the viewer to drill down to a specific year and Country, as well as filter by if the outcome is successful, canceled, or even still live.  To do this, the yearly data was converted from Unix code and a separate column using `Years` in Excel was created to separate years from the inferred date.   

The report shows that May and June are by far the most successful months for theater Kickstart campaigns, while December and January are the least successful.  


#### Fundraising Goals

This portion of the report uses links to the main data by using `COUNTIFS` to target a specific result (successful, failed, etc.) as well as a fundraising target (ie. $1,000-to $5,000) by referencing the Kickstarter_Challenge data sheet.  The data points to a downward slide in success from a high of 75% to less than 30% as fundraising goals increase.  As mentioned earlier, the sharp uptick between 40,000 to 45,000 warrants further study.

More data comparing successful and failed campaigns comes from the descriptive statistics sheet that uses the linear regression `STDEV.P`.  This data shows that failed Kickstarter campaigns on average have a much higher fundraising goal, with a long tail of poorly designed campaigns with unrealistically high amounts.  

Last, the Edinburgh Research tab dives into specific data for a client that focuses on some highlights from the Edinburgh Fest Fringe using `VLOOPS` to pull qualitative & quantitative data on specific successful theater productions.   


#### Limitations of the data

While the data examined uses tens of thousands of campaigns from around the world, it is not meant to be exhaustive.  The trends presented are based on campaigns dating back from 2015 that may be less applicable given the reality of public safety measures and changes in consumer behavior since 2020.  More data since 2020 is needed to what changes have proven to be most successful for various artists.
