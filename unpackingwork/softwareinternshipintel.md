# Software Engineering Intern (Hardware Architecture Group) |       Intel | Hillsboro, OR | Spring 2017

* What company did I work with?

Intel Corporation – Company Overview

Founded:
1968 by Robert Noyce and Gordon Moore (the originator of Moore’s Law).

Headquarters:
Santa Clara, California, USA.

Core business areas:
	1.	Microprocessors:
	•	Supplies the majority of central processing units (CPUs) used in PCs, laptops, data centers, and servers.
	•	Known for its Intel Core (i3, i5, i7, i9) and Xeon processor lines.
	2.	Chipsets and Motherboard Components:
	•	Provides chipsets that connect CPUs with other system components.
	3.	Integrated Graphics:
	•	Produces Intel UHD and Iris integrated graphics for mainstream computing.
	4.	Networking and Connectivity:
	•	Offers networking components, Ethernet solutions, and wireless connectivity products.
	5.	Memory and Storage:
	•	Previously produced NAND flash memory (sold its NAND business to SK hynix in 2021) but continues research in other memory technologies.
	6.	Data Centers and AI:
	•	Supplies high-performance processors and accelerators for cloud computing, AI workloads, and edge computing.
	7.	Foundry Services:
	•	Recently expanding into Intel Foundry Services (IFS) to manufacture chips for other companies, competing with TSMC.

* What industry is this company a part of?

What it is:
Intel is one of the world’s largest semiconductor companies, renowned for designing and manufacturing microprocessors and integrated circuits used in computers and many electronic devices.

* What was my role?
Software engineering internship

* What prepared me for that role?
This was my first technical internship EVER. Before this role I was a computer science undergraduate student at the University of California Davis. This was an internship I started in the winter term shortly after I completed a web development Bootcamp. I had some experience in web development and I knew a bit about algorithms so that was enough for me to build something useful using data for a hardware team.

* How can you apply for that role?
The website is up to date I would search around to try and find a role that is similar to your interests.
https://intel.wd1.myworkdayjobs.com/External/page/f7af6f4ab7131001ecc380a588ca0000

* Who were the stakeholders for my project?
Platform architecture Group - I worked for a hardware team that owned the production of certain microprocessors. If you think about microprocessors the way you think about iPhones you realize there are:

- storage size and compute power
- Year it came out
- Version number 

Every iPhone has a chip or a microprocessors and they also contain all of this information and more. My PI or principal investigator gave me a list of chips that were important to him and my project entailed understanding what data was being collected about the chips and what that data was exactly. 

* What team or product did I work on?
Platform architecture group which sits in Hillsboro Oregon 

* What was the impact of this project or team in relation to the company?
The hardware engineers on the team were in charge of improving the microprocessors every iteration.  

Example: 2015 version of chip A should be better than 2014 version of chip A which is used on smart refrigerators. What those improvements are exactly in terms of hardware I couldn’t tell you.

I am not very familiar with all of the aspects of the hardware side of the team because I was so focused on the software side of the team.

* What did I work on?

I worked as a software engineering intern on this team of hardware architects. Each architect owned a particular set of products which span many versions. A particular chip for instance could have 17 different versions which have all been put into production. For each instance of a version of the chip which is being used there are fuses which are turned on or off depending on the chips use. The data on each instance of each version of the chip for one particular product is stored in the one legacy database which the company manages.

My project included creating a data model which would track all of the version of one particular product and determine which fuses were turned on or off in each version alternation to understand the fuses which could be removed from production in the finalized version of the product to reduce the cost associated with production. I created a backend API to pull data from the oracle database using SQL, Express JS, and a few Microsoft NPM packages to help connect authenticate my API to the internal database.

* Who did I work with?

Team Manager - this was technically the manager of the interns on his team. He assigned me the project and would sporadically check in with me about how things were going. 

PI - principal investigator, this is the person who was technically responsible for my project and who explained the ins and outs of what exactly we were looking for. My manager understood the end goal of the project but could not as in depth about the technical specifications of the entire project.

Data Engineering Manager - in the company at the time there was one data engineering team and that team owned all of the data engineering pipelines and understood how to access legacy data across products. This person ended up being very important for my project given I had to go to him to figure out how to collect information for my products and he could explain what the very high level tables were in the database and what the symbols and naming conventions for those tables meant. 

* What assumptions did I make coming in?
I didn’t have any assumptions given this was my first internship ever. I was very excited about the fact that I was working on a real technical team and I would have a real technical project. I didn’t know much about hardware and I didn’t understand anything about how large corporations function through teams. 

* What did I learn in the first 4 weeks of this project?

How to take notes and how to ask follow up questions. During my first meeting with my PI we went into a conference room and with a white board and he started to explain the project. I brought my cell phone and a notebook. I recorded the conversation. This was one of the smartest moves I ever made because I could hear from his mouth the high level overview of the project. He used terms I didn’t understand and he explained hardware concepts that I was unfamiliar with. Because I recorded the conversation I was able to go back and review this information and take notes 📝 then respond with follow up questions. 

The web development Bootcamp taught me maybe the most important lesson of my professional career: how to google…
If you currently don’t understand a concept that is ok, but you need to be able to get to a point where you contextualize information about the concept in some way that relates the concept to something you do understand. Once you can do that you can research related concepts or sub concepts that help you understand the broader topic on a deeper level.

You may not understand HOW smart refrigerators use microprocessors from Intel but if you think about the computer interface and buttons you press to understand what is inside something that is simpler to understand and visualize you can then start breaking down how the refrigerator gets information from inside the fridge and “remembers” what is inside and does something useful with that data.

I learned very quickly that inside every company there are certain information gurus who understand the project you are working on but don’t have the time to dive into it the way an intern can. Interns are always assigned grunt work or moonshot projects depending on your skills and abilities. The way the project becomes a project in the first place is someone on some team noticed something was broken or needs help expanding that thing and at some point wrote it down or made an effort in some way to devote more time to that thing. That person has their own deliverables and responsibilities which they need to be accountable for and so they can handoff the project to an intern. Sometimes your manager is not actually the person who “discovered” the project and it’s someone else. When you go down the rabbit hole and begin to understand who might know more and who designed the project you can book time with that person and you will discover a gold mine of information which opens the pearly gates to success in your project. The data administrator was that person for me.

* What did I learn in second 4 weeks of the project?

During this project I learned a lot about data modeling give I worked directly with the database administrator to understand what data was available and the way that this data was being stored in the database. This was the first time that I was exposed to data governance topics. I also worked with big data for the first time given the database I was working with contained 500,000 tables and my query returned 9,000,000,000 records and crashed the server. I then consulted with a data scientist in another department to understand the proper ways to use parallel processing and HDSF to distribute the computer resources and get my job to complete successfully.

* What did I learn in the last 4 weeks of the project?
I learned how to talk about data ingestion and parallel processing.
This internship explored: data modeling, data ingestion and processing, job scheduling and orchestration, and data engineering.
You can hear me speak more about this experience during a live talk where I share what I learned: https://www.youtube.com/watch?v=rtYRcegtNxc&t=4s

* What hurdles did this team face?
The team did not understand the magnitude of data that was being collected. Once it was clear how much data was being collected the team needed to decide how to process that data and even make sense of it or analyze it.

* Were there any senior leaders who stood out as possible mentors or people I would want to work with in the future?
The data administrator was very knowledgeable about his job given he worked with the company for so long. Given what I know now about data parsing strategies and techniques it doesn’t seem like this guy was innovative in any way it felt more like he was an information hoarder without the capacity to properly document what was going with the data. Hopefully that company has done a bit more work to distribute this knowledge to other teams so that if he leaves someone else will have access to a general understanding of how the data infrastructure works internally. Scary to think that only one guy in a corporation as large as intel only had one person who could potentially document pipelines and an intern?

* Proprietary information takeaways…
Microprocessors produce a lot of data, and each microprocessor can have a bunch of versions. There are product owners who could potentially use this information in some way but I am not sure who or how they were using it in the past.

* Important team meetings?
None come to mind.

* What was the outcome of the project?
This project was handed back to my PI and he became aware of the information being collected and what tables that information was coming from. the outcome for him was a data pipeline and all he needed to do was run the query after I set up the tables and appropriates calls and even the parallel processing with the data engineering team.

* What external courses or educational resources did I use to skill up?
A lot of my I web development knowledge was useful but I didn’t get to a point where I needed to do any analysis. Understanding a bit more about parallel processing and how that works would be useful for this role. There are courses about big data that are useful for learning this. 
