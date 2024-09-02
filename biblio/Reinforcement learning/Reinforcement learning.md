# Reinforcement learning
#ReinfocementLearning #QLearning #ModelBased #Learning

---

## Reinforcement Learning and link with psychology
---

> **Reinforcement Learning :** reinforcement learning is a computational framework that was developed in psychology and artificial intelligence to formalize how agents learn to select actions to acquire reward and avoid punishment. 

### Subdivisions of RL algorithms

RL algorithms are subdivided into two broad categories of algorithms :
    
- **Algorithms for prediction :** predict the outcome of a situation. It's _value-based_
- **Algorithms for control :** guide you through the situation. It's _Policy-based_.

### Types of RL approaches

There's two types of RL approaches :
- **Model-free reinforcement learning** associated with habits and skills, and relies on trial-and-error learning, storing, or caching the values of past actions and inflexibly repeating actions that have led to higher values.
- **Model-based reinforcement learning** associated with goal-directed actions and involves the generation of predictions through a computationally expensive process that depends on an internal model of the environment.

### Link with psychology

RL algorithms are linked with two fields of psychology :

- **Classical (or Pavlovian) conditioning :** linked to _predicting algorithms_ for predictions of upcoming stimuli, whether or not the stimuli are rewarding or punishing
- **Instrumental (or operant) conditioning :** an agent is rewarded or punished depending on its actions. Hence, the agent learns to maximize rewards or minimize punishments

### Classical (or Pavlovian) conditioning

> **Classical conditioning :** introduced by Pavlov, type of unconscious and automatic learning. It consists in taking a neutral stimulus and pairs it with an unconditioned stimulus that produces an unconditioned response. The neutral stimulus is now a conditioned stimulus that provokes a conditioned 


- **Unconditioned Stimulus (US) :** stimulus that leads to an automatic response that has never been trained (e.g. cold breeze makes you shiver)
- **Neutral Stimulus (NS) :** a stimulus that doesn't trigger a response (e.g. the sound of a fan (ventilo) doesn't makes you shiver)
- **Conditioned Stimulus (CS) :** a stimulus that was before neutral and now it produces a response (e.g. you never paid attention to a dog, once you get bit by a dog and then you pay attention to a dog. Dog is now a conditioned stimulus)
- **Unconditioned Response (UR) :** automatic response that occurs without thinking
- **Conditioned Response (CR) :** response learnt where before no response as existing

Steps for classical conditioning :
1. A UC results in an UC (food triggers dog's salivation)
2. NS stystematically paired with the US (bell + food)
3. the NS becomes a CS and the UR becomes a CR by the CS

### Instrumental conditioning

## Reinforcement Learning models
---
Sources :
- [Reinforcement learning (Scolarpedia)](http://www.scholarpedia.org/article/Reinforcement_learning)
- [[@gueguen_dynamique_2017]] (thesis)
- [[@diederen_dopamine_2021]]
- [Temporal difference learning](https://www.engati.com/glossary/temporal-difference-learning)

### Model-free vs. Model-based RL

Key variables for RL models :
- Several states = $s$
- Several actions = $a$
- Matrix of transition rules = $P$
- Reinforcer associated to each transition = $r$

For **Model-Based** algorithm, the transition matrix $P(s, a, s')$ describing the probability of going from a state $s$ to $s'$ with action $a$ and the function for reinforcement $r(s, a)$ are known in advance. This type of algorithm _do not belong to the family of RL algorithms_.

Conversely, for **Model-Free** algorithms, the functions $P$ and $r$ are not known in advance, therefore a process of adaptation is required to optimize the strategy of choice. Two popular algorithms :

- **Temporal difference learning (TD) :** introduce to solve the problem of prediction
- **Q-learning :** extension of the TD to solve both the problem of prediction and the problem of control

### Rescorla-Wagner

> Learning slows down as the reinforcer (i.e. the obtained reward or avoided punishment) becomes more predictable. Said differently, the PE decrease toward zero. It is a _VALUE_ algorithm that is not updated according to the action.

Definition of the Rescorla-Wagner (RW) 1972 RL model:
$$y_{n} = y_{n-1} + \alpha \times \delta_{n}$$

Where $y$ is the prediction of reward value updated each trial $n$ as a function of the size of the RPE $\delta$ and the constant learning-rate $\alpha$. The smaller the learning rate, the less importance is given to the prediction error.

For example, if we expect to get 10€ but we received 16€, the PE is $16-10=6$€. If the learning rate is $\alpha=0.5$, we will update our next prediction of reward to $10 + 0.5 \times (16 - 10)=13$\€. If the PE is equal to zero, then $y_{n-1}=y_{n}$ which means that the future predicted reward is the same as the precedent trial therefore there is no more learning.

### Temporal difference learning

> The TD-learning is an update of the RW since the central learning rule is based on correcting errors. However, the updating rule in the TD is also considering the current state of the agent (_STATE-VALUE_). The value of a state is defined as a weighted sum of all possible rewards.

RW lacks of time description and prediction of future rewards. To solve this issue, Sutton and Barto (1980) introduced the **temporal difference** (TD) which states that temporally closer rewards have more influence in the predictions compare to those more distant in the future. For example, I prefer to receive 1€ now instead of 1.5€ in two months even if $1.5 > 1$. More precisely, the aims of the TD is to predict the total reward expected over the future i.e. a long term utility. TD aims to predict a combination of the immediate reward and its own reward prediction at the next moment in time The PE becomes a temporally dependent weighted sum.

Key equations :
- **Global consequence :** is equal to the cumulative sum of all of the reinforcer $R_{t}$, with priority given to the closer rewards : $$R_{t} = r_{t+1} + \gamma_{1}.r_{t+2}+...+\gamma_{T-t-1}.r_{T}$$
- **Value of a state :** the value of a state $s$, written $V(s)$, is equal to the global consequence from this state : $$V(s)=R_{t}(s_{t}=s)$$. It predicts the reinforcement obtained starting from this state.
- **Updating value state :** the updated value of a state is the sum between the previous value of that state plus the prediction error modulated by the learning rate :\\ $$V(s_{t}) \leftarrow V(s_{t}) + \alpha.[R_{t} - V(s_{t})]$$ where $0<\alpha<1$. If $\alpha=0$, $V_(s{t})$ is unchanged while $\alpha=1$ the state is strongly updated. The difference $$R_{t} - V(s_{t})$$ is the prediction error i.e. the difference between the reinforcement obtained minus the one expected. If the one obtained is equal to the expected, there's no update of the state
- **Trial-by-trial value update :** formulated this way, the _global consequence_ is a sum of all future rewards, there's no progressive update. This equation can be rewritten to : $$R_{t}=r_{t+1}+\gamma.V(s_{t+1})$$The updated value becomes : $$V(s_{t}) \leftarrow V(s_{t}) + \alpha.\delta_{t}$$ with  $$\delta_{t}=[r_{t+1}+\gamma.V(s_{t+1})-V(s_{t})]$$the prediction error term.

### Q-learning

> Q-learning is an update of the TD learning to solve the problem of control i.e. the choice of an optimal strategy. Said differently, it updates the value of a state, given an action (_STATE-ACTION-VALUE_).


- **Considering actions :** The Q-values now depends both on the current state and action : $$Q(s, a)=R_{t}(s_{t}=s|a_{t}=a)$$
- **Q-value update (SARSA or updated Q-learning) :** the q-values are updated with this equation :
$$Q(s_{t}, a_{t}) \leftarrow Q(s_{t}, a_{t}) + \alpha.[r_{t+1}+\gamma.Q(s_{t+1}, a_{t+1})-Q(s_{t},a_{t})]$$
- **Q-value update :** the q-values are updated with this equation :
$$Q(s_{t}, a_{t}) \leftarrow Q(s_{t}, a_{t}) + \alpha.[r_{t+1}+\gamma.max_{a}[Q(s_{t+1}, a) - Q(s_{t}, a_{t})]]$$The main difference with the SARSA version is that by taking the maximum across actions it makes the learning process independent of the policy $\pi$. To estimate action values precisely, it is necessary to explore all possible actions. The simplest rule for decision is to take the action with the highest q-values

### Softmax : action selection rule

Subjects are sometimes exploring (random action selection) or exploiting (keeping the same action). During exploration, it is possible that subjects select the worst possible action. A solution to estimate the probability of each action, is to transform q-values (i.e. the value of a state given an action) into probabilities. Then, the best action (or the most probable one) is the one with the highest Q-value. The _softmax_ rule, using a Gibbs distribution, is the most used one to transform Q-values into probabilities. For $n$ actions $a_{1}, a_{2}, ..., a_{n}$ at a trial $t$, the probability to chose the action $a_{1}$ ($P(a_{1})$) is given by :


$$P(a_{1}) = \frac{e^{Q_{t}(a_{1})/\beta}}{\sum_{i=1} ^{n} e^{Q_{t}(a_{i})/\beta}}$$

Some properties :
- The sum $P(a_{1}) + P(a_{2}) + ... + P(a_{n})$ is equal to one
- The $\beta$ parameter ($\beta>0$) is known as the _temperature_. When $\beta \rightarrow \infty$, each exponential is equal to one and therefore, the probability of an action is equal to $1/n$. Therefore, larger $beta$ make possible actions equiprobable (exploration). When $\beta \rightarrow 0$, the probability of selecting an action strongly depends on the Q-value associated to this action. Therefore, low $\beta$ encourage exploitation behavior.
- Small example on beta : $qvals = [10, 20, 145, 12]$. For $\beta=10^{6}$, $P=[.25, .25, .25, .25]$ (exploration) while for $\beta=10^{-6}$, $P=[0, 0, 1, 0]$ (exploitation)
- In python : $scipy.special.softmax(beta * Q, axis=1)$ where $axis=1$ specifies actions are stored as columns in the Q-matrix and therefore the sum over the actions should be one

