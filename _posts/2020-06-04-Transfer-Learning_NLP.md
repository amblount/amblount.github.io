# Transfer Learning and NLP

I am two weeks into teaching the data science track for the virtual summer program and we are just starting to get into the details of the project. One student in particular 
I am working with want to work with NBA data and understand player performance. It has been a real journey getting the student to think about how to define performance and what metrics
are important when trying to prove that a player has improved and what that means. We started exploring the different player positions and what is important for each position.
The first player we took a deep dive into was Chris Mullen who was a power forward and shooting guard. I was unfamiliar with the player positions before this conversation so I
spent some time looking at a [wikipedia article](https://en.wikipedia.org/wiki/Basketball_positions) to learn more about each of the positions and what the players were responsible for in terms of performance in each game. 

I had an inclination that we might be able to use NLP to understand more about what makes a great basketball player, specifically what makes a great shooting guard by fine-tuning 
a language model on the text from the wikipedia article on basketball positions and maybe even a few articles written about shooting guards. I have never done this before, but I think it could be useful.
We might be able to create some sort of question answering system that would help me as a novice learn more about what would make a great shooting guard.

My student also mentioned a new metric I was unfamiliar with the 50-40-90 scoring rubric.

From [wikipedia](https://en.wikipedia.org/wiki/50%E2%80%9340%E2%80%9390_club) -

> "The "50–40–90 club" is an informal statistic used to rate athletes in the National Basketball Association (NBA) and Women's National Basketball Association (WNBA). It requires a player to achieve all three criteria of 50% field goal percentage, 40% three-point field goal percentage and 90% free throw percentage by the end of the regular season.[1] To qualify, a player must attain the statistical minimums for any league-leading title; since 2013, the NBA requires 300 field goals, 82 three-pointers and 125 free throws by the end of the season.[2][3] In NBA and WNBA history, only nine players have recorded a 50–40–90 season. The latest player, the WNBA's first, was Elena Delle Donne in 2019.[4]"

> "50–40–90 indicates a great all-around attacking performance and is considered the gold standard for shooters.[5] Only Steve Nash (four times) and Larry Bird (twice) have had repeat 50–40–90 seasons. Nash's lifetime 49–43–90 regular season average is the closest anyone has come to achieving a career 50–40–90 mark.[6] Nash's lifetime 47–40–90 playoff average is the closest anyone has come to achieving a career 50–40–90 mark in the playoffs.[7] Dirk Nowitzki is the only member that falls short of the updated minimum requirement for three-pointers; he finished with 72 threes in 2007, before the change in requirements in 2013."

I decided to start with FastAI- and found a [great lecture](https://www.youtube.com/watch?v=5gCQvuznKn0&list=PLtmWHNX-gukKocXQOkQjuVxglSDYWsSh9&index=10&t=0s) from the code first introduction to natural language processing course.
