---
title: Publications
layout: default
nav_order: 3
---

# Publications

{: .note-title }
> Space-efficient Population Protocols for Exact Majority on General Graphs
>
> [Joel Rybicki](https://rybicki.github.io/), Jakob Solnerzik, [Olivier Stietel](https://ostietel.github.io/) and R.V.
> - 🎙️ *SODA*, 2026
> <details markdown="block">
> <summary>Abstract</summary>
> 
> $$\newcommand{\trel}{\tau_\mathrm{rel}}$$ We study exact majority consensus in the population protocol model. In this model, the system is described by a graph $$G = (V,E)$$ with $$n$$ nodes, and in each time step, a scheduler samples uniformly at random a pair of adjacent nodes to interact. In the exact majority consensus task, each node is given a binary input, and the goal is to design a protocol that almost surely reaches a stable configuration, where all nodes output the majority input value.
> 
> We give improved upper and lower bounds for exact majority in general graphs. First, we give asymptotically tight time lower bounds  for general (unbounded space) protocols. Second, we obtain new upper bounds parameterized by the relaxation time $$\trel$$ of the random walk on $$G$$ induced by the scheduler and the degree imbalance $$\Delta/\delta$$ of $$G$$. Specifically, we give a protocol that stabilizes in $$O\left( \tfrac{\Delta}{\delta} \tau_{\mathsf{rel}} \log^2 n \right)$$ steps in expectation and with high probability and uses  $$O\left( \log n \cdot \left(  \log\left(\tfrac{\Delta}{\delta}\right) + \log \left(\tfrac{\trel}{n}\right) \right) \right)$$ states in any graph with minimum degree at least $$\delta$$ and maximum degree at most $$\Delta$$.
> 
> For regular expander graphs, this matches the optimal space complexity of $$\Theta(\log n)$$ for fast protocols in complete graphs [Alistarh et al., SODA 2016 and Doty et al., FOCS 2022] with a nearly optimal stabilization time of $$O(n \log^2 n)$$ steps. Finally, we give a new upper bound of $$O(\trel \cdot n \log n)$$ for the stabilization time of a constant-state protocol.
> 
> 
> </details>

{: .note-title }
> Minimal Leader Election Under Weak Communication
>
> R.V. and [Isabella Ziccardi](https://sites.google.com/view/isabellaziccardi/)
> - 🎙️ [*PODC*, 2025](https://doi.org/10.1145/3732772.3733559)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> We propose a protocol to solve Leader Election within weak communication models such as the beeping model or the stone-age model.  Unlike most previous work, our algorithm operates on only six states,  does not require unique identifiers, and assumes no prior knowledge of  the network's size or topology, i.e., it is uniform. We show that under  our protocol, the system almost surely converges to a configuration in  which a single node is in a leader state. With high probability, this  occurs in fewer than $$O(D^2 \log n)$$ rounds, where $$D$$ is the network diameter. We also show that this can be decreased to $$O(D \log n)$$ when a constant factor approximation of $$D$$ is known. The main drawbacks of our approach are a $$\tilde{\Omega}(D)$$ overhead in the running time compared to algorithms with stronger requirements, and the fact that nodes are unaware of when a  single-leader configuration is reached. Nevertheless, the minimal  assumptions and natural appeal of our solution make it particularly  well-suited for implementation in the simplest distributed systems,  especially biological ones.
> 
> 
> </details>

{: .note-title }
> Fast and Robust Information Spreading in the Noisy PULL Model
>
> Niccolò D'Archivio, [Amos Korman](https://amoskorman.cs.haifa.ac.il/), [Emanuele Natale](https://natema.github.io/ema-webpage/) and R.V.
> - 📯 [*PODC*, 2025](https://doi.org/10.1145/3732772.3733543) (Brief Announcement)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> Understanding how information can efficiently spread in distributed systems under stochastic and noisy communication conditions is a fundamental question in both biological research and artificial system design. When the communication pattern is stable, allowing agents to control whom they interact with, noise in communication can often be mitigated through redundancy or more sophisticated coding techniques. In contrast, previous work has shown that noisy communication has fundamentally different consequences on well-mixed systems. Specifically, Boczkowski et al. (2018) considered the noisy $$\mathcal{PULL}(h)$$ model, in which in each (parallel) round, each agent passively receives observations of the messages held by $$h$$ randomly chosen agents, where each message can be viewed as any other message in the alphabet $$\Sigma$$ with probability $$\delta$$. The authors proved that in this model, the basic task of propagating a  bit value from a single source to the whole population requires $$\Omega(\frac{n\delta}{h(1-\delta\mid\Sigma\mid)^2})$$ rounds. For example, for one-to-one interactions ($$h=1$$) and constant $$\delta$$, this lower bound is exponentially higher than the time required to reliably spread information over a stable complete network, thus exemplifying how the loss of structure in communication can undermine the system's ability to effectively counteract noise. 
> 
> The current work shows that the aforementioned lower bound is almost tight. In particular, in the extreme case where each agent observes all other agents in each round, which can be related to scenarios where each agent senses the average tendency of the system, information spreading can reliably be achieved in $$\mathcal{O}(\log n)$$ time, assuming constant noise. We present two simple and highly efficient protocols, thus suggesting their applicability to real-life scenarios. Notably, they also work in the presence of multiple conflicting sources and efficiently converge to their plurality opinion. The first protocol we present uses 1-bit messages but relies on a simultaneous wake-up assumption. By increasing the message size to 2 bits and removing the speedup in the information spreading time that may result from having multiple sources, we also present a simple and highly efficient self-stabilizing protocol that avoids the simultaneous wake-up requirement.
> 
> Overall, our results demonstrate how, under stochastic communication, increasing the sample size can compensate for the lack of communication structure by linearly accelerating information spreading time.
> 
> </details>

{: .note-title }
> On the Limits of Information Spread by Memory-less Agents
>
> Niccolò D'Archivio and R.V.
> - 📰 [*Distributed Computing*, 2025](https://doi.org/10.1007/s00446-025-00500-z)
> - 🎙️ [*DISC*, 2024](https://doi.org/10.4230/LIPIcs.DISC.2024.18)
> - 📯 [*PODC*, 2024](https://doi.org/10.1145/3662158.3662813) (Brief Announcement)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> We address the self-stabilizing bit-dissemination problem, designed to capture the challenges of spreading information and reaching consensus among entities with minimal cognitive and communication capacities. Specifically, a group of $$n$$ agents is required to adopt the correct opinion, initially held by a single informed individual, choosing from two possible opinions. In order to make decisions, agents are restricted to observing the opinions of a few randomly sampled agents, and lack the ability to communicate further and to identify the informed individual. Additionally, agents cannot retain any information from one round to the next. According to a recent publication by Becchetti et al. in SODA (2024), a logarithmic convergence time without memory is achievable in the parallel setting (where agents are updated simultaneously), as long as the number of samples is at least $$\Omega(\sqrt{n \log n})$$. However, determining the minimal sample size for an efficient protocol to exist remains a challenging open question. As a preliminary step towards an answer, we establish the first lower bound for this problem in the parallel setting. Specifically, we demonstrate that it is impossible for any memory-less protocol with constant sample size, to converge with high probability in less than an almost-linear number of rounds. This lower bound holds even when agents are aware of both the exact value of $$n$$ and their own opinion, and encompasses various simple existing dynamics designed to achieve consensus. Beyond the bit-dissemination problem, our result sheds light on the convergence time of the "minority" dynamics, the counterpart of the well-known majority rule, whose chaotic behavior is yet to be fully understood despite the apparent simplicity of the algorithm.
> 
> </details>

{: .note-title }
> Abundant Resources can Trigger Reduced Consumption: Unveiling the Paradox of Excessive Scrounging
>
> R.V. and [Amos Korman](https://amoskorman.cs.haifa.ac.il/)
> - 📰 [*PNAS*, 2024](https://doi.org/10.1073/pnas.2322955121)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> In ecological contexts, it is conventionally expected that increased food availability would boost consumption, particularly when animals prioritize maximizing their food intake. This paper challenges this conventional wisdom by conducting an in-depth game-theoretic analysis of a basic foraging model, in which animals must choose between intensive food searching as producers or moderate searching while relying on group members as scroungers. Our study reveals that, under certain circumstances, increasing food availability can amplify the inclination to scrounge to such an extent that it leads to a reduction in animals’ food consumption compared to scenarios with limited food availability. We further illustrate a similar phenomenon in a model capturing free-riding dynamics among workers in a company. We demonstrate that, under certain reward mechanisms, enhancing workers’ production capacities can inadvertently trigger a surge in free-riding behavior, leading to both diminished group productivity and reduced individual payoffs. Our findings provide intriguing insights into the complex relationships between individual and group performances, as well as the intricate mechanisms underlying the emergence of free-riding behavior in competitive environments.
> 
> 
> </details>

{: .note-title }
> The Minority Dynamics and the Power of Synchronicity
>
> [Luca Becchetti](http://www.diag.uniroma1.it/~becchett/), [Andrea Clementi](https://www.mat.uniroma2.it/~clementi/), [Francesco Pasquale](https://www.mat.uniroma2.it/~pasquale/), [Luca Trevisan](https://lucatrevisan.github.io/), R.V. and [Isabella Ziccardi](https://sites.google.com/view/isabellaziccardi/)
> - 🎙️ [*SODA*, 2024](https://doi.org/10.1137/1.9781611977912.144)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> We study the minority-opinion dynamics over a fully-connected network of $$n$$ nodes with binary opinions. Upon activation, a node receives a sample of opinions from a limited number of neighbors chosen uniformly at random. Each activated node then adopts the opinion that is least common within the received sample.
> 
> Unlike all other known consensus dynamics, we prove that this elementary protocol behaves in dramatically different ways, depending on whether activations occur sequentially or in parallel. Specifically, we show that its expected consensus time is exponential in $$n$$ under asynchronous models, such as  asynchronous $$GOSSIP$$. On the other hand, despite its chaotic nature, we show that it converges within $$O(\log^2 n)$$ rounds with high probability under synchronous models, such as synchronous $$GOSSIP$$.
> 
> Finally, our results shed light on the bit-dissemination problem, that was previously introduced to model the spread of information in biological scenarios. Specifically, our analysis implies that the minority-opinion dynamics is the first *stateless* solution to this problem, in the parallel *passive-communication* setting, achieving convergence within a poly-logarithmic number of rounds. This, together with a known lower bound for sequential stateless dynamics, implies a parallel-vs-sequential gap for this problem that is nearly quadratic in the number $$n$$ of nodes. This is in contrast to all known results for problems in this area, which exhibit a linear gap between the parallel and the sequential setting.
> 
> </details>

{: .note-title }
> On the Role of Memory in Robust Opinion Dynamics
>
> [Luca Becchetti](http://www.diag.uniroma1.it/~becchett/), [Andrea Clementi](https://www.mat.uniroma2.it/~clementi/), [Amos Korman](https://amoskorman.cs.haifa.ac.il/), [Francesco Pasquale](https://www.mat.uniroma2.it/~pasquale/), [Luca Trevisan](https://lucatrevisan.github.io/) and R.V.
> - 🎙️ [*IJCAI*, 2023](https://doi.org/10.24963/ijcai.2023/4)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> We investigate opinion dynamics in a fully-connected system, consisting of $$n$$ identical and anonymous agents, where one of the opinions (which is called *correct*) represents a piece of information to disseminate. In more detail, one *source* agent initially holds the correct opinion and remains with this opinion throughout the execution. The goal for non-source agents is to quickly agree on this correct opinion, and do that robustly, i.e., from any initial configuration. The system evolves in rounds. In each round, one agent chosen uniformly at random is *activated*: unless it is the source, the agent pulls the opinions of $$\ell$$ random agents and then updates its opinion according to some rule. We consider a restricted setting, in which agents have no memory and they only revise their opinions on the basis of those of the agents they currently sample. As restricted as it is, this setting encompasses very popular opinion dynamics, such as the *voter model* and *best-of-$$k$$ majority* rules. 
> 
> Qualitatively speaking, we show that lack of memory prevents efficient convergence. Specifically, we prove that no dynamics can achieve correct convergence in an expected number of steps that is sub-quadratic in $$n$$, even under a strong version of the model in which activated agents have complete access to the current configuration of the entire 
> system, i.e., the case $$\ell=n$$. Conversely, we prove that the simple voter model (in which $$\ell=1$$) correctly solves the problem, while almost matching the aforementioned lower bound. 
> 
> These results suggest that, in contrast to symmetric consensus problems (that do not involve a notion of correct opinion), fast convergence on the correct opinion using stochastic opinion dynamics may indeed require the use of memory. This insight may reflect on natural information dissemination processes that rely on a few knowledgeable individuals.
> 
> </details>

{: .note-title }
> Distributed Alignment Processes With Samples of Group Average
>
> [Amos Korman](https://amoskorman.cs.haifa.ac.il/) and R.V.
> - 📰 [*IEEE TCNS*, 2023](https://doi.org/10.1109/TCNS.2022.3212640)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> This paper studies a stochastic alignment problem assuming that agents can sense the general tendency of the system. More specifically, we consider $$n$$ agents, each being associated with a real number. In each round, each agent receives a noisy measurement of the system's average value and then updates its value. This value is then perturbed by random drift. We assume that both noise and drift are Gaussian. We prove that a distributed weighted-average algorithm optimally minimizes the deviation of each agent from the average value, and for every round. Interestingly, this optimality holds even in the centralized setting, where a master agent can gather all the agents' measurements and instruct a move to each one. We find this result surprising since it can be shown that the set of measurements obtained by all agents contains strictly more information about the deviation of Agent $$i$$ from the average value, than the information contained in the measurements obtained by Agent $$i$$ alone. Although this information is relevant for Agent $$i$$, it is not processed by it when running a weighted-average algorithm. Finally, we also analyze the drift of the center of mass and show that no distributed algorithm can achieve drift that is as small as the one that can be achieved by the best centralized algorithm.
> 
> </details>

{: .note-title }
> Early Adapting to Trends: Self-Stabilizing Information Spread using Passive Communication
>
> [Amos Korman](https://amoskorman.cs.haifa.ac.il/) and R.V.
> - 📰 [*Distributed Computing*, 2024](https://doi.org/10.1007/s00446-024-00462-8)
> - 🎙️ [*PODC*, 2022](https://doi.org/10.1145/3519270.3538415)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> How to efficiently and reliably spread information in a system is one of the most fundamental problems in distributed computing. Recently, inspired by biological scenarios, several works focused on identifying the minimal communication resources necessary to spread information under faulty conditions. Here we study the  self-stabilizing *bit-dissemination* problem, introduced by Boczkowski, Korman, and Natale in [SODA 2017]. The problem considers a fully-connected network of $$n$$ *agents*, with a binary world of *opinions*, one of which is called *correct*. At any given time, each agent holds an opinion bit as its public output. The population contains a *source* agent which knows which opinion is correct. This agent adopts the correct opinion and remains with it throughout the execution. We consider the basic $$\mathcal{PULL}$$ model of communication, in which each agent observes  relatively few randomly chosen agents in each round. The goal of the non-source agents is to quickly converge on the correct opinion, despite having an arbitrary initial configuration, i.e., in a self-stabilizing manner. Once the population converges on the correct opinion, it should remain with it forever. Motivated by biological scenarios in which animals observe and react to the behavior of others, we focus on the extremely constrained model of *passive communication*, which assumes that when observing another agent the only information that can be extracted is the opinion bit of that agent. We prove that this problem can be solved in a poly-logarithmic in $$n$$ number of rounds with high probability, while sampling a logarithmic number of agents at each round. Previous works solved this problem faster and using fewer samples, but they did that by decoupling the messages sent by agents from their output opinion, and hence do not fit the framework of passive communication. Moreover, these works use complex recursive algorithms with refined clocks that are unlikely to be used by biological entities. In contrast, our proposed algorithm has a natural appeal as it is based on letting agents estimate the current tendency direction of the dynamics, and then adapt to the emerging trend. 
> 
> </details>

{: .note-title }
> On the Role of Hypocrisy in Escaping the Tragedy of the Commons
>
> [Amos Korman](https://amoskorman.cs.haifa.ac.il/) and R.V.
> - 📰 [*Scientific Reports*, 2021](https://doi.org/10.1109/TCNS.2022.3212640)
> <details markdown="block">
> <summary>Abstract</summary>
> 
> We study the emergence of cooperation in large spatial public goods games. Without employing severe social-pressure against "defectors", or alternatively, significantly rewarding "cooperators", theoretical models typically predict a system collapse in a way that is reminiscent of the *tragedy-of-the-commons* metaphor. Drawing on a dynamic network model, this paper demonstrates how cooperation can emerge when the social-pressure is mild. This is achieved with the aid of an additional behavior called "hypocritical", which appears to be cooperative from the external observer's perspective but in fact hardly contributes to the social-welfare. Our model assumes that social-pressure is induced over both defectors and hypocritical players, but the extent of which may differ. Our main result indicates that the emergence of cooperation highly depends on the extent of social-pressure applied against hypocritical players. Setting it to be at some intermediate range below the one employed against defectors allows a system composed almost exclusively of defectors to transform into a fully cooperative one quickly. Conversely, when the social-pressure against hypocritical players is either too low or too high, the system remains locked in a degenerate configuration.
> 
> </details>

