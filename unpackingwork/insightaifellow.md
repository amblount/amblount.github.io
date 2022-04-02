# Artificial Intelligence (A.I.) Fellow | Insight Data Science 	|	San Francisco, CA 	|	2018

  - What team or product did I work on?

This was a project based fellowship. I worked on understanding how reinforcement learning could improve emergency resident scheduling. This actually turned into a contraint optimization problem which is well known in the field of operations research.

  - What was the impact of this project or team in relation to the company?

This was my first attempt at a deep learning project and my first intorudction to reinforcement learning as a concept. One of my research interests is meta-learning which is based on the concepts from metalearning.

  - What did I work on?

<iframe width="560" height="315" src="https://www.youtube.com/embed/_sK_n_OHgHA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

##### Automating Scheduling for ED residents at UCSF

Data Journalism: I have been interested in [big data](https://www.youtube.com/watch?v=gx9IGKLi2e4) for a while now because I am fascinated by telling stories with data. I spent this past summer at the New York Times understanding data journalism by listening to writers explain their writing process and the investigative journalism that goes into it. Data journalism goes beyond re-telling facts and seeks to explore the utility behind the information. Once you aggregate your data and understand the metadata affiliated with your data set, you can decide what sort of statistical analysis to run on the data. Artificial intelligence mixes up this process a bit and lets the neural network gain an understanding of your data and imply how probable an outcome is. The foundation here is still statistics and probability without some of the manual work.

Hello Insight: This winter I decided I would spend time diving into an AI project end-to-end and that is why I decided to participate in the [Insight Data Science](https://insightfellows.com/data-science) fellowship as an [AI fellow](https://insightfellows.com/ai). During the first week of the fellowship, I explored projects and settled on a prompt to use reinforcement learning for control systems. The prompt was as follows:

Currently, rules (control policy) for the mechanical operations (control loops) of most sophisticated machinery are set by human experts, which require tremendous time and domain expertise. If we can teach machines to learn these rules and reduce the reliance on scarce human experts, that has far-reaching impacts across all manufacturing fields.

The complexity and diversity of control loops in hard technologies like metal 3D printing make them a good candidate for Reinforcement Learning (RL). RL algorithms usually require a lot of trials and it is expensive and dangerous to run physical trials. But combining RL with simulation will not only optimize the control policy for more efficiency and time saving, it also can disrupt manufacturing by developing new methods that require less complicated machinery.
Use case:

Scheduling of emergency medicine doctors in inner-city hospitals

Deliverable:
Deep reinforcement learning as a service platform that can learn a policy using a specific simulation environment or existing dataset. The service needs to interfaces with the engineer to gather the model and objective function and potentially take advantage of imitation learning and off-policy learning to improve the speed of convergence and gather bounds on each parameter to help reduce search space. The service should take advantage of asynchronous and parallel deep RL techniques to speed up the learning process as well. The accuracy of policy should exceed human generated policy.

How did I think about the problem: I have a lot of experience in the hospital given earlier in my undergraduate studies I majored in chemistry and planned to attend medical school. In preparation for that, I volunteered in different departments at different hospitals to understand what life was like as a physician. One experience that I pulled from when thinking about this problem was my internship experience at the University of California, Davis Medical Center in the Pediatric Emergency Department. I worked an overnight shift two days per week, and there are a few things that stood out for me.

The department was understaffed
Emergency room nurses and physicians were overworked
The UCD medical center has a certain number of nurses and doctors who are contracted to work in that particular facility. When schedules are being created for a particular facility you are only able to use the medical providers who are contracted to work there. If there are 150 shifts to fill in one medical center for a week and only 70 medical providers then the medical providers might be scheduled every day, and essentially under-worked.

Why don’t medical facilities hire more workers?: This would make sense if supply met demand, but in this case, it does not. In the case of nurses and doctors, these medical practitioners are specialized. Not only do these providers need to attend medical school or nursing school they also need to choose a specialty. For my project, we are thinking about Emergency Medicine as that specialty. The emergency department specializes in keeping people alive when something has gone wrong. You might think about patients who are suffering from a stroke or someone who has a heart attack and needs immediate treatment. The pediatric emergency department is even more of a rare case because pediatric patients (children) have organs and bones which have not yet fully developed and are more sensitive to slight environmental changes. All in all it takes a while to train an emergency medicine practitioner and there just aren’t very many.

<iframe width="560" height="315" src="https://www.youtube.com/embed/WHla_QmfV5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

In the USA today there are 5273 emergency departments and 39,547 [Emergency Medicine providers](https://www.aamc.org/data-reports/workforce/interactive-data/active-physicians-sex-and-specialty-2015). There are about [139 million](https://www.cdc.gov/nchs/fastats/emergency-department.htm) visits to the Emergency Department each year, which averages to around 380,821 visits each day. If all the physicians in the USA were working all day, then each of these physicians would be responsible for ~10 visits.

Problem: A reasonable Emergency Medicine (EM) shift lasts 8 hours but a typical shift lasts around 12 hours. There are work regulations limiting the space between shifts requiring there are at least 8 hours off between shifts. Given the scarcity of ED physicians and the amount of ED visits, there is more demand than supply and often the scheduling requirements are unmet and physicians are required to work more often than they should.

UCSF: For this particular project I worked with the University of California, San Francisco to understand the way their emergency department was organized and it turns out it is a very complicated system. I was specifically working on understanding the scheduling system for the medical residents who are not yet doctors. The residents have rotations throughout the year and only a segment of this schedule involves rotating through the ED. When a new round of residents is assigned placement within the UCSF program the program admins get a block of resident assignment detailing which residents will be available and which particular weeks they will be available. The schedule looks something like this:

![schedule](-ed-current-sched.png)

Resident availability for the year, broken down by week segmented by blocks
The rotation assignment in this spreadsheet are color coded and the pink and baby blue cells correspond to the time when the residents will be available to pick up shifts in the emergency department. This spreadsheet does not detail which particular shifts the residents will be working, there is an additional step which needs to be figured out to make that happen.

Preprocessing: The first step involved in making this data usable for any algorithm is cleaning the data. It is necessary to reformat this data in a way which clusters either the weeks and the residents available for that week or the residents and a list of all of the weeks they are available. This is an important step because we currently have data for every department in the hospital and when each resident will be in the emergency department, but we only care about when the residents will be available to work in the emergency department.

When looking at the data it is also clear that this csv is not going to be easy to work with given there are multiple data clusters on the same sheet and the columns and rows are not clearly organized. Even though all of the data is technically available we need to do a lot of manual work to get the data formatted in a way where we would be able to use it for the purposes of scheduling.

Future work: There needs to be some front-end framework or properly labeled CSV file where whoever is inputting the data can input this information into the csv in a way which would allow the clustering of the data to be usable by other teams. I spent quite a bit of time thinking through the proper database design techniques for this particular use case, but my design process did not only build for the initial preprocessing step it also included steps for creating relationships between residents, shifts, and facilities which we will get into a little later in the post.

Useful CSV format example:
With a list of residents, how can we think about modeling the entire system?

![schedule](/images/er-sched-erd.png)

##### Designing the entire database

What are the variables?
![schedule](/images/er-sched-variables.png)

Shifts
![schedule](er-scheduling-excel.png)

Dimensions?
![schedule](/images/er-sched-dimensions.png)

How many residents work each shift?
After assigning a letter to each shift, I then assigned another letter to each shift start and end time combination. Many of the facilities have the same start and end time combinations so we can assign the ‘shift’ to multiple facilities.

![schedule](/images/er-scheduling-board.jpeg)

Wireframe of white boarding session # 1
Solving the scheduling problem using reinforcement learning

  - Who did I work with?

UCSF Lead Resident to understand scheduling challenges

  - What assumptiosn did I make coming in?

I didn't know much about reinforcement learning.

  - What technology or tools did I use?

    - Google Colab
    - Google OR (operations research tools)
    - OR Tools [Scheduling](https://developers.google.com/optimization/scheduling/employee_scheduling)

  - What hurdles did this team face?

I had a problem setting of the shifts and residents in the system. Creating the OR space was challenging. The design of the problem given all of the constraints was a challenge.

  - What was the outcome of the project?

A calendar with shifts.

  - What external courses or educational resources did I use to skill up?

I read a bit more about reinforcement learning. Deep Mind has a nice course.
 - [Deep Mind: Introduction to Reinforcement Learning](https://deepmind.com/learning-resources/-introduction-reinforcement-learning-david-silver)
 - [Reinforcement Learning - an Introduction](http://www.incompleteideas.net/book/the-book-2nd.html) Richard Sutton - The Intro RL Book
