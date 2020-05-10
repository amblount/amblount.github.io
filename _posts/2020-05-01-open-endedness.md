#### What is open-endedness and why do I care?

It's a field of machine learning focused on algorithms generating new more complicated algorithms in a never ending loop. 
If we think about how we will eventually get to a place where we have general artificial intelligence then this form of generating algorithms from other
algorithms is probably a good place to start. 

April 25, 2020 - An episode of the data exchange podcast interview with Kenneth Stanley spoke about the field of open-endedness is general. 
In this post I hope to explore some of the content he shared and a few additional links which could help those new to the field explore it in more
depth.

A link to the [shownotes](https://thedataexchange.media/algorithms-that-continually-invent-both-problems-and-solutions/) - Episode: Algorithms
that continually invent both problems and solutions.

Kenneth Stanley in this interview mentioned that he is starting a new research group @ Open AI focused on open-endedness and he is recruiting people with diverse background in neuroevolution, evolutionary algorithms and a solid knowledge base of machine learning and deep learning.

A brief history on neuroevolution, it stems from the evolution of the brain and it's development over time. Human intellect has developed over time not by planning every stage but through observing the environment and adapting to it. Although this seems like a brand new science it is actually complementary to training a neural network through stochastic gradient descent and this can be thought of as a way to improve the current state of the art (SOTA) approach we have to structuring reinforcement learning problems. 

5 Pieces of Prior work which contributed

1. POET [Paired Open-Ended Trailblazer: Endlessly Generating Increasingly Complex and Diverse Learning Environments and Their Solutiona](https://arxiv.org/abs/1901.01753) | [Jeff Video Explanation](https://www.youtube.com/watch?v=CsizpWJ-nD0&t=23s) | [Video Explanation](https://www.youtube.com/watch?v=8wkgDnNxiVs)

2. Enhanced POET [Enhanced POET: Open-Ended Reinforcement Learning through Unbounded Invention of Learning Challenges and their Solutions](https://arxiv.org/abs/2003.08536) | [Video Demo](https://www.youtube.com/watch?v=RX0sKDRq400) | [Video Explanation](https://www.youtube.com/watch?v=jxIkPxkN10U&t=133s)

3. Neuro-evolution Papers - Work don @ Uber AI Labs

  [Welcoming the Era of Deep Neural Evolution](https://eng.uber.com/deep-neuroevolution/)
  
  - [Deep Neuroevolution: Genetic Algorithms are a competitive Alternative for Training Deep Neural Networks For Reinforcement Learning](https://arxiv.org/abs/1712.06567)
    - Evolves DNNs with a simple, traditional, population-based genetic algorithm that performs well on hard deep RL problems. On Atari, the GA performs as well as evolution strategies and deep reinforcement learning algorithms based on Q-learning (DQN) and policy gradients (A3C).
    - The “Deep GA” successfully evolves networks with over four million free parameters, the largest neural networks ever evolved with a traditional evolutionary algorithm.
    - Suggests intriguingly that in some cases following the gradient is not the best choice for optimizing performance.
    - Combines DNNs with Novelty Search, an exploration algorithm designed for tasks with deceptive or sparse reward functions, to solve a deceptive, high-dimensional problem on which reward-maximizing algorithms (e.g. GA and ES) fail.
    - Shows the Deep GA parallelizes better than, and is thus faster than, ES, A3C, and DQN, and enables a state-of-the-art compact encoding technique that can represent million-parameter DNNs in thousands of bytes.
    - Includes results for random search on Atari. Surprisingly, on some games random search substantially outperforms DQN, A3C, and ES, although it never outperforms the GA.
    - [Video Explanation]()
  - [Safe Mutations for Deep and Recurrent Neural Networks through ourput Gradients](https://arxiv.org/abs/1712.06563)
    - Safe mutations through gradients (SM-G) greatly improves the efficacy of mutation in large, deep, and recurrent networks by measuring the sensitivity of the network to changes in particular connection weights.
    - Computes gradients of outputs with respect to weights instead of gradients of error or loss as in conventional deep learning, allowing random, but safe, exploratory steps
    - Both types of safe mutation require no additional trials or rollouts in the domain.
    - The result: deep networks (over 100 layers) and large recurrent networks now evolving effectively only through variants of SM-G.
  - [On The Relationship Between the OpenAI Evolution Strategy and Stochastic Gradient Descent](https://arxiv.org/abs/1712.06564)
    - Explores the relationship between ES and SGD by comparing the approximate gradient computed by ES with the exact gradient computed by SGD in MNIST under different conditions.
    - Develops fast proxies that predict ES expected performance with different population sizes.
    - Introduces and demonstrates different ways to speed up and improve the performance of ES.
    - Limited perturbation ES significantly speeds up execution on parallel infrastructure.
    - No-mini-batch ES improves the gradient estimate by replacing the mini-batch convention designed for SGD with a different approach customized for ES: A random subset of the whole training batch is assigned to each member of the ES population within each iteration of the algorithm.  This ES-specific approach provides better accuracy for ES with equivalent computation, and the learning curve is much smoother than even for SGD.
    - No-mini-batch ES reached 99 percent accuracy in a test run, the best reported performance of an evolutionary approach in this supervised learning task. 
    - Overall helps to show why ES would be able to compete in RL, where gradient information obtained through trials in the domain is less informative with respect to the performance objective than in supervised learning.  
  - [ES is more than just a traditional finite difference approximator](https://arxiv.org/abs/1712.06568)
    - Highlights an important distinction between ES and traditional finite differences methods, which is that ES optimizes for an optimal distribution of solutions (as opposed to one optimal solution).
    - One interesting consequence: Solutions found by ES tend to be robust to parameter perturbation.  For example, we show that Humanoid Walking solutions from ES are significantly more robust to parameter perturbation than similar solutions found by GAs and by TRPO.
    - Another important consequence:  ES is expected to solve some problems where conventional methods would become trapped, and vice versa.  Simple examples illustrate these different dynamics between ES and conventional gradient-following.
  - [Improving Exploration in Evolution Strategies for Deep Reinforcement Learning via a Population of Novelty Seeking Agents](https://arxiv.org/abs/1712.06560)
    - Adds the ability to encourage deep exploration in ES.
    - Shows that algorithms that have been invented to promote exploration in small-scale evolved neural networks via populations of exploring agents — specifically novelty search (NS) and quality diversity (QD) algorithms — can be hybridized with ES to improve its performance on sparse or deceptive deep RL tasks, while retaining scalability.
    - Confirms that the resultant new algorithms, NS-ES and a version of QD-ES called NSR-ES, avoid local optima encountered by ES to achieve higher performance on tasks ranging from simulated robots learning to walk around a deceptive trap to the high-dimensional pixel-to-action task of playing Atari games.
    - Adds this new family of population-based exploration algorithms to the deep RL toolbox.

4. [Go-Explore](https://www.youtube.com/watch?v=SWcuTgk2di8): A New Approach for Hard Exploration Problems  | [Paper](https://arxiv.org/abs/1901.10995)

5. [Generative Teaching Networks](https://eng.uber.com/generative-teaching-networks/) | [Video Explanation](https://www.youtube.com/watch?v=lmnJfLjDVrI)
