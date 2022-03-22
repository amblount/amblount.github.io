A lot of people reach out to me and ask what type of work do you do? What does it mean to work in data science? Other people mention things like, "machine learning, oh my!"

[Preparing for a transition into data science](https://blog.insightdatascience.com/preparing-for-the-transition-to-data-science-e9194c90b42c)

Let's start at the beginning, like most of my network I started out in software engineering, more specifically I was building web applications. Something like simple CRUD apps with a pleasing front-end (view layer). When I began I had a mentor who was a data engineer so we talked a lot about database design. I was working in rails at the time and I spent a whole lot of time understanding associations and how the way that you model the database impacts the flow of your application.


It took me a lot of time to create this schema for PreUni and understand how to break down the functionality that I wanted my user to have, into models for my database. If you think about the applications that you use the most often a poorly designed database could be at the center of slow performance or a host of other issues.

![preuni erd](/images/erd-preuni.jpg)

How does this relate to data science?

During my internship with Intel, I was building a web application which was intended to display data from a legacy database. It was a pretty regular project on the surface, maybe even simple, it was only intended to have one view. The problem here was getting the data. When you are working with a large company the way they store their data can be really complex and the way they modeled their database probably is not up to date with the current needs of the company. To say that in a different way, all of the data that you need is probably there but it is structured in a way that you need complicated algorithmic tricks to pull any meaning from this data at all. During this project I sat with the database administrator practically every single day to understand which tables in the database I needed to aggregate to get all of the information I needed. By the end of this project I filled around 3-500 page notebooks with data on how to get the information I needed!


### The rise of big data
<iframe width="560" height="315" src="https://www.youtube.com/embed/gx9IGKLi2e4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Long story short, my team had no idea how much data I was going to pull from the 30 joined tables and advanced SQL queries that I was running but when I did get some data back, it was a LOT of data. Like 9 BILLION records of data. You can not run SQL queries on a Microsoft SQL Server that return 9 Billion records. You need to use a distributed computing environment. After speaking with a data scientist at the company it was clear we needed HDFS and Spark. This means you need to restructure your back-end infrastructure and you NEED a data engineer


Data Engineering is at the intersection of business intelligence, data warehousing, and software engineering. As Maxime Beauchemin wrote in The Rise of Data Engineering, ETL and data modeling have changed, and that change is not just about Big Data. It’s distributed systems, stream processing, and computation at scale. It’s about working with data using the same practices that guide software engineering at large.

Virtually the answer to the distributed compute problem was HDFS and Hadoop.


This was started at Google and was brought to the rest of world via a research paper: "MapReduce: simplified data processing on large clusters"

[The rise of the data engineer free code camp](https://www.freecodecamp.org/news/the-rise-of-the-data-engineer-91be18f1e603?gi=9469a540563f)

When I first started learning about this process the Coursera Big Data certification with 5 courses, was the most useful- for anyone thinking of going into analytics or data science, I would highly recommend this specialization.


Hopefully, it is clear now that if you are working with Big Data you need HDFS or some sort of abstraction built on top of it.

Let's tie this into analytics and data science and the actual jobs and daily tasks that people are doing. We are virtually pulling insight from data. I think that the following video from the course on machine learning does a great job of describing what machine learning is and how the different topics, data science, analytics, predictive analytics apply.

#### Intro hadoop
<iframe width="560" height="315" src="https://www.youtube.com/embed/DEQNknALf_8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

From the course Big Data- Machine Learning, Machine Learning overview and applications.

Now that you understand generally how machine learning is used, we can come back to a high-level question of why is this important and how does this apply to business and a businesses needs?

Large corporations have been collecting data on their users, so they have a lot of information. Unfortunately, computers are not smart enough yet to completely understand data but machine learning systems like IBM's Watson can do some pretty amazing things with a data set and not much programming.


I uploaded a CSV with some Fitbit data and Watson was able to come up with questions about the data set and product analytics reports and data visualizations based on the data set. There was no need for me to understand advanced statistical analysis or big data algorithms because Watson understands this already. This example is from 2016, so I am sure the power of Watson has only gotten better over time. Although it would seem with advanced technology companies would simply pay for this powerful feature and not pay data scientists. Fortunately for all of you reading this, this is not the case.

[Big Data Specialization](https://www.coursera.org/specializations/big-data)


Many companies either can not afford or choose not to pay IBM to utilize this platform and so humans need to manually decide which algorithms to run and how to use them.

What skills do you need to do this?

[SQL](https://www.datacamp.com/courses/introduction-to-sql)
[Python](https://www.datacamp.com/tracks/data-scientist-with-python)
[R](https://www.datacamp.com/tracks/data-scientist-with-r)
[Statistics](https://ocw.mit.edu/courses/mathematics/18-05-introduction-to-probability-and-statistics-spring-2014/index.htm)
[Qualitative Research](https://www.coursera.org/learn/qualitative-research)
[Quantitative Research](https://www.coursera.org/learn/quantitative-research)
[Strategic Business Analytics](https://www.coursera.org/learn/strategic-business-analytics)
[Business Intelligence](https://www.coursera.org/learn/business-intelligence-tools)
[Algorithms](https://www.coursera.org/specializations/algorithms)
[Machine Learning](https://www.coursera.org/learn/machine-learning)


### [Qualitative Research]()

I will highlight this skill because it is the one skill that many people are not focusing on but I have found it is one of the most fundamental. When you are tasked with performing data analytics or data science projects it is important that you understand the domain you are working with and the customer you are trying to serve. When you understand these things about your target population you can think about the information or data that you need to improve the lives of those customers. Once you understand the data that you need you can start going through the process of collecting that data (ETL) and then pull insights from that data (analytics) through data visualizations like tableau or charts of some kind.

[Machine Learning with big data](https://www.coursera.org/lecture/big-data-machine-learning/machine-learning-overview-xmXhS)

### Blogs

[Information is beautiful](https://informationisbeautiful.net/)

### Data Visualization
[Tablaeu](https://www.coursera.org/learn/dataviz-visual-analytics)
[D3](https://d3js.org/)
[Alteryx]()

### The state of artificial intelligence

- fats ai
- open ai
- yoshua benio
- meta
- deep mind


Hope this helps.

Semi-pro tip: If you are new to the field of data science and analytics look at the LinkedIn profile of someone who has the job title at some of the companies you are interested in and check out their publications, courses and certifications. Some of these are free sites or courses that you can take and write about and given this person has the skillset you want this is one way to level-up.

