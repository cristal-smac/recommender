# Recommender-system  

In this recommender system, we try to filter the satisfied service recommendation for service costomers. The proposed method bases 
on recommenderation feedback, Beta probability density function, Monte Carlo method, random walk algorithm, roulette wheel algorithm. 
Their functions in the proposed model are detailed introduced as follows:

# Recommendation feedback: 
The feedback are stored in agents' memory. Every agent remenbers the sequential query, the corresponding service provider and feedback. Here the feedback result could be either success or failure (The same to satisfied and unsatisfied.)
# Beta probability density function: 
An interaction between two agents can be viewed as an independent trail and each interaction has two possible feedback outcomes:success or failure. Beta probability density function is a mapping feedback to trust value. The trust value 
also indicates the probability that one agent move to this neighbouring agent. 
# Monte Carlo method, random walk algorithm:
The method is used to calculate the Pagerank Values of all available recomendations. In the process, the trust value is regarded as the hyperlink matrix in random walk process, and in this article we choose the third algorithm in  Monte Carlo methods in #PageRank computation: When oneintertion is suffericient#. We ran a random walk {X-{t}} starts at a random node "rw" times, it can go to a neighbouring node with probability c and terminates with probability 1-c or it stops when the random walk reaches at a danging node. It is reasonable because we believe agents should not give information if they have no experiences.
# Roulette wheel algorithm:
We use roulette wheel algorithm to filter the satisfied agents or recommendations. In the service recommender system, agents have limited energy and space to provide service for all service costomers. At the same time, if the top-ranking agent is choosen all rounds, the new agent will never have opportunities to give service, to gain trust value.
# An example:
The proposed model is applied to the field of medical recommender system. In the simulation setting, there are several agents act as doctors, they have uneven levels of skills in Orthopedics, Dentistry, ENT which are configured beforehand with probability. The more expericenced the doctors, the higher probability that agent will be assigned. But the preset probability is not known to the public. We ran several tests to show how the model works and its efficiency. Each round, the protocol for agents' query procedure are as follows:

1: An agent generates a query for service; and 

2: Each agent transmits the request to its reliant trustees; and 

3: An agent responses rapidly once it receives the query; and

4: Analyzing the trust value by trust relationship; and

5: Filter a service provider by roulette wheel algorithm; and

6: Update memory by remembering the feedback outcome.

First, we ran a test to show that the concept of trust makes great sense in improving the preformances of the recommender system. Then we analyzed the effect the some preset probability, including forgetting factor, the reset probability in random walk process and the amount to use roulette wheel aggorithm when making decisions. Finally, the coherence between the total number of providing treatments and the preset probability is tested. Because of randomness when providing services, each test has been ran for 10 times and the average result is shown in the result comprison. In the example, the effectiveness of adopting the concept of trust in recommender system is shown.



