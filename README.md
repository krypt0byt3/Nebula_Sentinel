# Nebula_Sentinel
Autonomous Threat Cognition: On-Device Language-Model Reasoning for Endpoint Threat Interpretation

Abstract:
The cybersecurity threat landscape is rapidly changing, with attackers leveraging Large Language Models to break into environments at machine speed. Most organizations, if not the industry, are actually focused on leveraging the cloud to perform inference and integrate cognition into workflows to try and keep up with the attackers. The main challenge of such integrations is the fact that the data must be accessible to frontier models and the cost of tokens could be significantly high. The cloud dependency, while not only costly, also requires breaking certain boundaries in terms of networks, data, trust, and privacy while attempting to operationalize security. Due to the fact that threats are moving at machine speed with the enhancement of large language models, the concept of moving the reasoning to the endpoint addresses requirements such as sovereign or air gap systems, while still taking advantage of cognition on the edge. This approach consists of leveraging an LLM or SLM closer to the data source, such as servers or endpoints, in an attempt to respond at machine speed and taking advantage of cognition.

What is Autonomous Threat Cognition?
This term was developed during research into the feasibility of incorporating an inference engine into a cybersecurity agent monitoring events on a system, while also enriching analysis via LLM/SLM reasoning on such events and determining if the activity constitutes a threat or benign activity based on the collected and processed data. Autonomous Threat Cognition enables the machine or agent to autonomously collect, process, and produce enriched analysis via inference on the endpoint.

What is Autonomous Threat Response? 
The ability to leverage an LLM/SLM to take response actions based on the reasoning or cognition during the enrichment of an event that poses a threat to the system. However, while the feature is partially built and is conceptually possible, at this time, due to inconsistency with LLMs/SLMs hosted locally (despite adjusting temperature and weights), it is not at a stage where it can be considered trustworthy. During research, it has been noted that the LLM/SLM may produce empty responses or inconsistent output. For this same reason, ATR is not recommended. In addition, bad analysis or reasoning by a language model could result in legitimate processes getting terminated, or network connectivity being severed, causing outages or other impact.


What is GOSSIP? 
Generative Observable Security Sharing Intelligence Protocol. While the idea has been around for quite some time, the goal was to make a decentralized system where the agents performing reasoning (in agent inference) can automatically generate indicators of compromise (IOCs), detection rules, and make other agents aware of such potential threats so that detection converges throughout the environment. This would make the agent fleet (nebula) self-learn threats to the environment.

Reference implementation:
Nebula Sentinel is a platform developed in Rust that has been under active testing for several months (March 2026). Inference on the agent has been successfully achieved, however, not without challenges. Some of the most notable challenges have been the fact that if the agent runs on a laptop, the battery is drained much faster (between 25-55%) compared to standard use. This is due to inference being expensive due to the amount of compute required. Both methods have been explored, CPU-based inference as well as GPU. CPU inference keeps the processor running well above 95% utilization, while GPU inference seems more stable. However, while running on battery, both methods are simply not ideal. For a workstation or server, the load seems more acceptable, as power is uninterrupted and compute seems more sustainable. This is the main finding when running ATC. A new angle is being explored and more will be published in the near future. 


Threat detection and enrichment framework via agent inference:
<img width="1380" height="1240" alt="image" src="https://github.com/user-attachments/assets/460a4751-fd80-498e-8a2f-848abbc717b7" />
