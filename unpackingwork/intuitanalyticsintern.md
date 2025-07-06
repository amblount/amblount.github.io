# Machine Learning Analytics Intern (Transaction Labeling Group) | Intuit | Mountain View, CA | Summer 2017

  * What company did I work with?
Intuit

Intuit Inc. – Company Overview

What it is:
Intuit Inc. is an American financial technology company best known for developing software that simplifies financial, accounting, and tax management for individuals and small to medium-sized businesses.

Founded:
1983 by Scott Cook and Tom Proulx in Palo Alto, California.

Headquarters:
Mountain View, California, USA.

Core Products:
	1.	TurboTax – Tax preparation software for individuals and businesses to file taxes easily.
	2.	QuickBooks – Accounting software used widely by small businesses to manage finances, payroll, and invoices.
	3.	Mint – A free personal finance app for budgeting, bill tracking, and credit monitoring.
	4.	Credit Karma – Acquired in 2020; offers free credit scores, credit monitoring, and personalized financial product recommendations.
	      5.	Mailchimp – Acquired in 2021; a marketing automation platform primarily      	  used for email marketing by small businesses.

* What industry is this company a part of?
Accounting software as a service (Saas)

* What was my role?
Data engineering intern

* What prepared me for that role?
Web development bootcamps where I worked on teams which built web apps scraping data from public APIs specifically financial data and learned how to display and organize that data. 

* How can you apply for that role?
Typically computer science undergraduates apply for roles at large technology companies in Silicon Valley to prepare to work as entry level software engineers upon graduation. 

Here are a few open roles I found on the website 
Read about the internship program 
https://www.intuit.com/careers/programs/internships/

Keep in mind that the internships occur during the summer and you apply September or January for the following summer. 

* Who were the stakeholders for my project?

All of the transaction data going out to other downstream products and services inside of the company INTUIT came through my team  [categorizations] team for labeling. Mint is the product that makes the most sense to someone who is not working directly on a data engineering team because lots of people use mint to watch their money. You might want to get a general understanding of how much money you are spending each month on food, clothes, or utilities and if your transactions are properly labeled it’s easy to get an understanding of that. Technically all downstream teams consuming transactional data with product managers were stakeholders for my project. 

Product manager - this person is working on a specific product let’s say income distribution graphs for the month and category labels within that for MINT. The product manager owns one aspect of the product and has multiple projects to improve or expand the product and functions based or user feedback. We will come back to user feedback.

Data engineering team - most data engineers are just cleaning up pipelines to enable analysts who query the data and present the data to use the data. Basically if there is no data available because where it is being stored from in the apps is inaccessible in some way, it’s not useful. Currently cloud compute services like Google GCP and azure enable so many other companies to pay a monthly fee and have someone else manage the storage of large amounts of data.

Analysts - analysts are really important team members given they find trends within the data and help make sense of this data. 📈 analysts sit on specific teams and their managers or other team members holding more important positions inform them about priorities within the company structure. Maybe the CEO states after reviewing specific user feedback they found that they want to expand the MINT product and the accuracy of food related transactions is very important. If that is the case the analyst could run a few queries based on data they recognize is readily available and get a broad understanding of what needs to be collected and think about how this data could be used to make certain assumptions or products. This starts with graphs or charts about what currently exists and after presenting this to product managers another meeting typically leads to another set of data queries and the process repeats. 

* What team or product did I work on?

Categorizations team

This team ingests all of the transaction data for all Intuit customers across products, labels the transaction and then sends the labeled transactions out to the appropriate groups. These groups then consume the transaction for their particular business use case. A few examples are the mint financial planning application where users can monitor the ways in which they are spending in hopes they can understand over spending in certain categories and make appropriate changes in line with their budgets.

* What was the impact of this project or team in relation to the company?

A few examples are the mint financial planning application where users can monitor the ways in which they are spending in hopes they can understand over spending in certain categories and make appropriate changes in line with their budgets. In this particular examples, through my analysis I noticed that the machine learning algorithm and data labeling process being used to label the transactions coming in was only correct 20% of the time because the other 80% of the time users would manually re-label the transactions.

* What did I work on?

Data pipeline 

As an intern on this team, I created a data pipeline sing SQL and Python to explore the data coming in each day and for each business unit understand the percentage of transactions which contained a label at all and of the transactions which did contain a label how often was that label correct. I created data visualizations using tableau and presented my findings during the intern summit to all of the product teams whose data I was collecting.

* Who did I work with?

One data engineer specifically who created the data pipelines for the categorizations team. The big idea is I would help her improve the pipelines, but it didn’t work out that way. It turns out I was much more interested in the analysis aspect of the job and the product management part of the job, so I spent most of my time interviewing the product managers on my team and taking notes from those conversations and I interviewed a few data scientists to understand how they got into the field: their educational backgrounds and such. The long and short of many of those conversations turned out to be PhD in statistics leads to a data scientist role. Turns out classic machine learning algorithms are just basic statistical models and we have the compute and software to run those classic models on large data sets in the cloud at this point. Some companies around this time had outdated data infrastructure so this made it much more difficult for data engineers to actually clean data and move it around. 

* What assumptions did I make coming in?
During my interviews I made it clear I wanted to join a data and machine learning team because that is where my interests were. I had some experience with web apps and moving small scale data around but I wasn’t really sure how to work with large data sets and so this was an ongoing area of learning I had to go through for myself. I did find the big data courses on Coursera useful, but every team I worked with had different software and different infrastructure they were using so I had to understand the specific challenges for each team.

* What did I learn in the first 4 weeks of this project?
I learned how the company was organized on the data side. The data science it’s had their building and they were working on implementing algorithms that would help improve the company workflow on a large scale. Enterprise product managers typically gave the, direction on what to work on next. I also learned that Intuit gives interns lots of perks like an apartment and a cool cafeteria those are awesome. 

* What did I learn in second 4 weeks of the project?
I learned that I hated data engineering when the data is dirty and you are forced to use Hadoop and C to clean it and make pipelines. You might join certain teams and realize how much work there is to do and also realize that you are NOT the person do do this work because your interests don’t align with the daily tasks of the job. Given this learning came quickly I found the data engineer on my team, who pressed the importance of Tableau as a tool and explained how some analysts build an entire career with that one skill. we will come back to that at another time. 

* What did I learn in the last 4 weeks of the project?
I learned how to explain the project END TO END. There are so many non- technical skills that I learned from this internship and we will explore those in the next part of this blog, but because we had an intern summit coming up and I needed to present the project at the intern summit I needed to give the 2 minute explanation of the project for other teams to understand what I did. I learned I am really great at that. Most of the time as a data engineering someone will ask you to create a pipeline and you won’t even understand what the point of the pipeline is and why you need to create that pipeline in the first place. If you have an ambition to remain behind the scenes this works and this is fine but let’s say you want to become something else, specifically if you have a knack for storytelling like I do it becomes very clear something like being an analyst or a product manager makes more sense given how much I appreciate doing the research and present the end goals.

* What hurdles did this team face?
Data infrastructure - this team did not have their data in the cloud and was using legacy infrastructure making it extremely difficult for the one data engineer on the team to do all of the work by herself.

* Were there any senior leaders who stood out as possible mentors or people I would want to work with in the future?

Alladin was awesome.. will come back to this story.

* Proprietary information takeaways…
Working with a company who was so familiar with transactional data and organized it in such a way that it was useful to many products was super cool because we didn’t have many products using financial data in such a way at the time. I am now sure if Intuit ever sold any of its models to places like Bank of America but I know that some of the smaller companies now are able to connect with Bank of America and parse income and transaction history to start to make sense of credit history and spend trends now.

* Important team meetings?
Nothing stands out as really important right now, I remember listening to the CEO at the time talk about how cool the internship was and how excited he was to work with the company. He seemed like an enthusiastic leader. I think it might say something about the fit for me at that company that there is not one meeting that stood out as important at the time given how many products and services were in production. Clearly I was in the wrong meetings and working with the wrong team.

* Perks of this internship
Apartment & 24 hour gym

* Where did I succeed?
Making connections with people who were much further along in their careers than me and using those connections to learn more about corporate America. 

* Where did I fail?
I was not a great data engineer on that team, the work seemed pointless and never ending. 

* What did I learn about the tech ecosystem here specifically?
 Some companies are referred to as the big 4
1. Netflix
2. Facebook
3. Google
4. Amazon
I would also include Microsoft in this group. The companies that are not in this group do not have a technological framework in place that makes them competitive like really competitive. Intuit has done a bunch for accounting software Saas as a space but they didn’t change the financial tech sector like say PayPal at the time, they are just another Saas financial tech company, but they are a large player in the space. 
