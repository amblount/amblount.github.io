# Software Engineering Intern (Data Engineering Team)   |  New York Times | Manhattan, NY | Summer 2018

At a high level, here is what I did.

+ Wrote Python script to move metadata from Google Sheets to BigQuery to explore use cases for new GCP product datahub.
+ Developed orchestration workflow to schedule Python DAG script execution using Airflow, and automated authentication process.

  - What team or product did I work on?

I worked with the Data Governance Team, which is a smaller team of product leads who own the meta-data related to major projects within the organization. The Data Governance team creates the standards for data quality stores in BigQuery (the online cloud database) to ensure that the data is being properly labeled and that no stale data is being maintained (someone has to be in charge of deleting or re-naming things). A good high level overview of the purpose of this team would be the equivalent of an internal diectory of employees. When you start working with a large company you might want to understand the organizational chart. This is the document or sructure within the company that informs everyone who the stakeholders are or who reports to whom and is in charge of what. You can take a look at the [people](https://www.nytco.com/company/people/) section of the company to get an idea of who does what.

Read more about the data governance initiatives at the Times, [here](https://open.nytimes.com/how-the-new-york-times-thinks-about-your-privacy-bc07d2171531)

The New York Times is a major news publication in New York City, (Manhattan) and is notorious for producing extremely high quality journalistic pieces of writing. From the company [website](https://www.nytco.com/company/)

> The New York Times is dedicated to helping people understand the world through on-the-ground, expert and deeply reported independent journalism.

I worked with the engineering sector of the company that is charge of the web and mobile electronic versions of the publication. Many old school long time subscribers get the Sunday paper delivered in physical form to their doorstep but because of modern times and the prevalence of smart phones most people are subscribing online and reading the paper on an e-reader like a kindle or i-pad. Because of this change the NYT has become a technology company that needs to support features and use cases for online readers.

> Since 1851, The New York Times has been on the ground reporting stories from around the globe that no one else was telling. How we tell those stories has changed, but our mission to seek the truth and help people understand the world has remained constant.

This company has been producing papers for a long time and a whole lot of articles have been written about a ton of topics. This translates to a lot of data. Each article has a name and a topic that users need to be able to filter through. If you think about all of the current sections of the newspaper that are worth reading:

- fashion
- modern living
- art
- music
- film
- cooking

To name a few, every article has a lot of meta-data involved with it and there is a need for that information to be sorted and easily queryable. This is why the data enginering team is important and what they are actually responsible for maintaining.

  - What was the impact of this project or team in relation to the company?

**Data migration**
The old school physical paper is virtually out the window but as is the physical data warehouse. During 2018 the company decided to shut down the physical data warehouse that stores all of the legacy data from forever. So they had a few floors in a building they were renting each month where they housed a lof of computers. Those computers stored all of the information that company has collected from forever! That s a lof of data, and they decided to move it ALL to the cloud. They decided to migrate from local data servers which were owned and managed by the Times to rented storage space from Google Cloud Services. 

  - What did I work on?

I was just an intern during this time so I wasn't in charge of a huge project. There was an entire data engineering team! They were working on most of the heavy lifting I was in charge of helping one of the senior program managers on the data governance team migrate the meta-data she held dear in a google sheer to affiliated tables of data already living in the cloud using BigQuery. 

[The Goods Paper](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45390.pdf): 
The goods paper shared insight into a new product that was emerging within Google Cloud.

#### [Google Catalog](https://cloud.google.com/data-catalog/docs/concepts/overview)
The Goods paper eventually turned into Google catalog the product now available on GCP. At this time in development the product was in Beta and the NYT was a beta testing customer. We had 3 google product specialists on site to help answer technical questions from the data engineering team and two product managers, one working specifically on Data Catalog to help us test implementation.

  - Who did I work with?

I spent a lot of time thinking about Data Science and Research and I thought it was incredible that you could actually have a career in data as a researcher. I didn't think about what I wanted to do as a career but I did think about the fact that I wanted to think about thinking and problem solving a lot. I spoke with so many senior team members around the office about what it was like to be a professor or a researcher as a career and what it looks like to earn a PhD. 

#### The Journalists
If you read my [blog post about podcasting](https://amblount.github.io/podcasting) back in 2015, you know that I was introduced to Kara Swisher for the first time in person in San Francisco. Well, she announced that she was joining the times as an [opinion writer](https://www.nytco.com/press/kara-swisher-to-contribute-to-opinion/) and I lost my SHIT! She has come a long way because now she has a [column](https://www.nytimes.com/column/kara-swisher), it makes sense. Anyway back in the day when I was a superfan and heard she was coming I organized a conversation between Kara and Michael Barbaro, which was a FUCKING BIG DEAL! 

> They are journalism superheros. Put some **RESPECT** on my name

<img src="/images/nyt/karaswishermichaelbarbaro.jpg" alt="swisher" width="600"/>

  - What assumptiosn did I make coming in?


  - What technology or tools did I use?

    - SQL
    - BigQuery
    - Google Sheets API

  - What hurdles did this team face?
  - What was the outcome of the project?
  - What external courses or educational resources did I use to skill up?

I had to learn a ton about Dev-Ops. I didn't know anything about that. Tools like Kafka. This is when I got into the data conferences and blogs because I realized there was so much shit I didn't know. 
