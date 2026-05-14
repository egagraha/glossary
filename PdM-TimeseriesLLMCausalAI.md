# Glossary

1. Imputation and mathematical time-series topic  
2. LLM, prompt engineering, telematics, privacy, and causal graph topic  

# 1. Imputation and Mathematical Time-Series Glossary

## 1.1 Term Glossary

| Term | Definition |
|---|---|
| Alternative Data | Non-traditional data sources used in finance, such as satellite imagery, web-scraped sentiment, app-usage statistics, or other irregular external signals. |
| Bayesian Linear Regression | A probabilistic regression approach that estimates both predicted values and uncertainty using Bayesian inference. |
| Bayesian Multilevel Regression | A Bayesian regression model with hierarchical structure, allowing parameters to vary across groups or levels. |
| Bayesian Structural Time Series | A Bayesian state-space model that decomposes a time series into trend, seasonality, and regression components. |
| Bidirectional Long Short-Term Memory | A recurrent neural network that processes sequential data in both forward and backward directions. |
| Causal Discovery | The process of identifying possible causal structures among variables from data. In the imputation thesis, causal discovery is treated as a downstream motivation for producing complete and structurally faithful time series. |
| Causal Inference | The estimation or interpretation of cause-and-effect relationships after a causal structure has been assumed, learned, or validated. |
| Collinearity | A condition in which two or more variables are highly correlated, which can inflate model performance or create misleading structural relationships. |
| Composite Score | A model-selection score combining normalized RMSE, MAE, R², and WMAPE to compare imputation models across multiple metrics and missing rates. |
| Covariance Preservation | The ability of an imputation method to maintain the original covariance structure among variables, which is important for downstream causal discovery and risk modelling. |
| Data Leakage | A modelling problem where information that should not be available during prediction is indirectly used, causing overly optimistic results. |
| Deep Learning Imputation | Imputation using neural network models such as LSTM, GRU, Conv1D, Bi-LSTM, or LSTM-MHA to reconstruct missing time-series values. |
| Edge Deployment | Running a model close to the data source, such as on an in-vehicle computing unit or edge gateway. |
| Feature-wise Imputation | An imputation approach where each feature is treated as a target variable in turn, while the remaining features are used as predictors. |
| Fixed-Parameter Kalman Filter | A Kalman filter configuration where noise parameters are manually fixed rather than estimated from data. In the imputation thesis, this configuration fails on near-constant BEV signals. |
| Fog Deployment | Running computation on intermediate infrastructure between edge devices and cloud servers. |
| Gradient Boosting | A machine learning technique that builds an ensemble of weak prediction models, usually decision trees, in a sequential manner to reduce error. |
| Ground Truth | The original known values used as a reference when evaluating reconstructed or imputed values. |
| Kalman Filter | A statistical state-space method used to estimate hidden states in noisy sequential data. |
| Leaf-wise Tree Growth | A LightGBM tree-building strategy that expands the leaf with the largest potential loss reduction. |
| LightGBM | A gradient boosting algorithm based on decision trees, used in the imputation thesis for high-performing feature-wise imputation. |
| Long Short-Term Memory | A recurrent neural network architecture designed to capture temporal dependencies in sequential data. |
| Mask-and-Reconstruct Protocol | An evaluation procedure in which known values are artificially masked and then reconstructed by imputation models, allowing direct comparison with ground truth. |
| Mean Absolute Error | A metric that measures the average absolute difference between predicted and true values. |
| Mean Absolute Percentage Error | A relative error metric that can become unstable when true values are close to zero. |
| MinMax Scaling | A preprocessing method that rescales values into a fixed range, commonly [0, 1]. |
| Missing Data | Observations that are absent, corrupted, or unavailable due to sensor failure, transmission loss, irregular sampling, or other data-quality problems. |
| Missing Rate | The proportion or percentage of values removed, missing, or masked in a dataset. |
| Multivariate Time Series | A time series dataset containing multiple variables observed over time, such as speed, mileage, battery voltage, and energy consumption. |
| Multi-Head Attention | An attention mechanism that allows a model to attend to different parts of a sequence simultaneously. |
| Near-constant Signal | A signal with very low variation over time, such as remaining battery energy during parked periods. |
| Non-stationarity | A condition where the statistical properties of a time series change over time, for example due to vehicle mode switching. |
| Posterior Predictive Distribution | A probability distribution representing predicted values and uncertainty after observing data in a Bayesian model. |
| Quantitative Finance | A field applying mathematical, statistical, and computational methods to financial markets, risk modelling, and asset pricing. |
| Rauch-Tung-Striebel Smoother | A smoothing algorithm used with Kalman filtering to estimate latent states using the full observed sequence. |
| Regime Switching | A situation in which a system alternates between different operating states, such as electric and combustion modes in a hybrid vehicle. |
| Root Mean Squared Error | A metric measuring the square root of the average squared difference between predicted and true values. |
| Sequence-based Imputation | An imputation approach that uses windows of consecutive timesteps to reconstruct missing values by exploiting temporal context. |
| Sliding Window | A fixed-length sequence of consecutive observations used as input for sequence-based models. |
| State-Space Model | A mathematical model representing observed data as generated from hidden states that evolve over time. |
| Structural Hamming Distance | A graph comparison metric that counts the number of edge additions, deletions, or reversals needed to transform one graph into another. |
| Tick-data Synchronisation | The process of aligning asynchronously observed financial market transactions onto a common time grid. |
| Time Series | A sequence of observations recorded over time, where temporal order is central to analysis. |
| Time-Series Imputation | The process of estimating and filling missing values in a time series while preserving temporal structure and inter-variable relationships. |
| Usage-Based Insurance | An insurance model that uses driving behaviour or vehicle telematics data to assess risk or determine pricing. |
| Value-at-Risk | A financial risk measure estimating potential portfolio loss over a given time horizon and confidence level. |
| Vehicular Telematics | Vehicle-generated data collected from sensors and communication systems, including speed, acceleration, mileage, battery voltage, and energy consumption. |
| Weighted Mean Absolute Percentage Error | A relative error metric that uses aggregate absolute actual values as the denominator, making it more stable than MAPE for near-zero values. |
| Yield Curve Reconstruction | The process of estimating interest rates at unobserved maturities using available financial data. |
| Zero-inflated Feature | A variable containing many zero values, such as acceleration or distance during stationary vehicle periods. |

## 1.2 Abbreviation Glossary

| Abbreviation | Full Form | Definition |
|---|---|---|
| BEV | Battery Electric Vehicle | A vehicle powered entirely by an electric battery and motor system. |
| Bi-LSTM | Bidirectional Long Short-Term Memory | A recurrent neural network that processes sequential data in both forward and backward directions. |
| BLR | Bayesian Linear Regression | A probabilistic regression model used for prediction and uncertainty estimation. |
| BMLR | Bayesian Multilevel Regression | A hierarchical Bayesian regression model allowing group-level variation. |
| BSTS | Bayesian Structural Time Series | A Bayesian state-space model using components such as trend, seasonality, and regression. |
| B-RF | Bayesian Random Forest | A Bayesian or Bayesian-approximation version of Random Forest used to estimate uncertainty over predictions. |
| B-XGB | Bayesian XGBoost | A Bayesian or Bayesian-approximation version of XGBoost used to estimate uncertainty over boosted-tree predictions. |
| CAN-bus | Controller Area Network bus | A vehicle communication system that allows electronic control units and sensors to exchange data. |
| Conv1D | One-Dimensional Convolutional Neural Network | A neural network architecture used to detect local temporal patterns in sequential data. |
| DAG | Directed Acyclic Graph | A directed graph without cycles, often used to represent causal relationships. |
| DL | Deep Learning | A class of machine learning methods based on multi-layer neural networks. |
| EKF | Extended Kalman Filter | A nonlinear extension of the Kalman filter using linearization around current estimates. |
| FCI | Fast Causal Inference | A causal discovery algorithm capable of handling latent confounders. |
| GES | Greedy Equivalence Search | A score-based causal discovery algorithm that searches over possible graph structures. |
| GRU | Gated Recurrent Unit | A recurrent neural network architecture similar to LSTM but with fewer gates. |
| HMC | Hamiltonian Monte Carlo | A Bayesian sampling method used to estimate posterior distributions efficiently. |
| KF | Kalman Filter | A state-space filtering method used for sequential estimation under noise. |
| LSTM | Long Short-Term Memory | A recurrent neural network architecture designed for learning temporal dependencies. |
| LSTM-MHA | Long Short-Term Memory with Multi-Head Attention | A hybrid neural architecture combining recurrent sequence modelling with attention. |
| MAE | Mean Absolute Error | The average absolute difference between predicted and true values. |
| MAPE | Mean Absolute Percentage Error | A relative error metric that can be unstable for near-zero values. |
| MAR | Missing At Random | A missing-data mechanism where missingness depends on observed variables but not directly on the missing value itself. |
| MCAR | Missing Completely At Random | A missing-data mechanism where missingness is independent of observed and unobserved values. |
| MCDA | Multi-Criteria Decision Analysis | A decision-analysis approach used to compare alternatives across multiple criteria. |
| ML | Machine Learning | A field of AI in which models learn patterns from data to make predictions or decisions. |
| MNAR | Missing Not At Random | A missing-data mechanism where the missing value itself influences the probability of being missing. |
| NUTS | No-U-Turn Sampler | An adaptive Markov Chain Monte Carlo algorithm used for Bayesian posterior sampling. |
| OBD-II PID | On-Board Diagnostics II Parameter ID | A standardized identifier used to request vehicle diagnostic or sensor values. |
| PC | Peter-Clark Algorithm | A constraint-based causal discovery algorithm using conditional independence tests. |
| PHEV | Plug-in Hybrid Electric Vehicle | A vehicle combining an internal combustion engine with a rechargeable electric drivetrain. |
| R² | Coefficient of Determination | A metric indicating the proportion of variance explained by a model. |
| RMSE | Root Mean Squared Error | The square root of the average squared prediction error. |
| SCR | Solvency Capital Requirement | A regulatory capital requirement under Solvency II for insurance companies. |
| SHD | Structural Hamming Distance | A graph error metric counting edge additions, deletions, or reversals. |
| UBI | Usage-Based Insurance | An insurance approach based on observed driving behaviour or vehicle usage. |
| UKF | Unscented Kalman Filter | A nonlinear Kalman filter variant using deterministic sampling to approximate nonlinear transformations. |
| VaR | Value-at-Risk | A financial risk metric estimating potential loss at a given confidence level. |
| WMAPE | Weighted Mean Absolute Percentage Error | A relative error metric that is more stable than MAPE for near-zero-valued features. |
| ZLB | Zero Lower Bound | A financial condition where interest rates are close to zero. |

# 2. LLM, Prompt Engineering, Telematics, Privacy, and Causal Graph Glossary

## 2.1 Term Glossary

| Term | Definition |
|---|---|
| Acceleration_kmh2 | A vehicle telematics variable representing acceleration in km/h², used to analyse driving behaviour and energy demand. |
| Adjacency Matrix | A matrix representation of a directed graph where each entry indicates whether a relationship exists from one feature to another. |
| Analytical Utility | The usefulness of an LLM output for the intended analytical task, such as recovering correct causal or directed graph relationships. |
| Batteryvoltage | A telematics feature representing the electrical voltage of the vehicle battery. |
| Causal Discovery | The process of identifying directed cause-and-effect relationships among variables. In the four theses, LLMs are tested as tools for generating candidate causal structures from telematics data. |
| Causal Graph | A directed graph showing assumed or expert-defined causal relationships among variables. |
| Chain-of-Thought Prompting | A prompting strategy that asks the model to reason step by step before producing the final response. |
| Confusion Counts | Counts used in graph evaluation, including true positives, false positives, false negatives, and true negatives. |
| Consensus Graph | A graph produced by aggregating edges predicted across multiple model and prompt configurations. It shows recurring model beliefs but does not guarantee correctness. |
| Contextual Prompting | A prompting strategy that adds domain-specific context, such as EV telematics and vehicle physics, to improve model output. |
| Data Fingerprint | A compact dataset summary containing descriptive statistics and correlations, used as LLM input instead of the full dataset. |
| Data Leakage | The unintended exposure of sensitive values, behavioural patterns, or private information in model outputs. |
| Directed Edge | A directed relationship from one variable to another, for example `speed_kmh -> energyconsumptionaverage`. |
| Directed Graph | A graph composed of nodes and arrows, where arrows indicate the direction of influence or relationship. |
| Distance_m | A Tesla EV telematics feature representing travelled distance in meters. |
| Edge Count | The number of directed relationships predicted or extracted from an LLM output. |
| Edge-Level Analysis | Evaluation of individual predicted relationships to identify correct, false, missing, or reversed edges. |
| Edge Parser | A component that extracts structured directed relationships from raw LLM outputs. |
| Electricenergyremaining | A Tesla EV feature representing remaining usable electric energy. |
| Electricremaining | A telematics feature representing remaining electric range or remaining electric energy proxy. |
| Energyconsumptionaverage | A telematics feature representing average energy consumption over time or distance. |
| Expert-Defined Ground Truth | A manually defined reference graph based on domain knowledge, vehicle physics, or literature. |
| Few-Shot Prompting | A prompting strategy that provides examples before the actual task to guide model response format or reasoning. |
| Fleet Monitoring | The use of vehicle data to monitor operations, sustainability, diagnostics, maintenance, or performance. |
| Graph Recovery | The task of reconstructing a directed graph from model-generated edges and comparing it with a reference graph. |
| Ground Truth | The reference graph or structure used to evaluate model-generated outputs. |
| Hybrid Vehicle | A vehicle combining an internal combustion engine with an electric drivetrain. |
| In-Context Learning | The ability of a model to perform a task using information provided directly in the prompt, without changing model parameters. |
| Inference-Time Privacy | Privacy risk that occurs during model use when sensitive prompt content is exposed or inferred in the output. |
| Instruction Prompting | A prompting strategy that gives explicit task instructions, rules, or formatting requirements. |
| Knowledge Graph | A structured representation of entities and relationships, which can be created from parsed model-generated edges. |
| Least-to-Most Prompting | A decomposition strategy that breaks a complex task into simpler subproblems and solves them progressively. |
| Local Inference | Running an LLM on local hardware rather than sending sensitive data to an external API or cloud system. |
| Meta Prompting | A prompting strategy that gives high-level task guidance and allows the model to choose its own reasoning approach. |
| Mileage | A telematics variable representing total distance travelled by the vehicle. |
| No-Instruction Control | A baseline prompt condition with minimal extra guidance beyond the main task. |
| Normalization | A preprocessing step that rescales numerical features into a common range, often [0, 1]. |
| Output Parsing | The process of converting raw LLM-generated text into structured machine-readable outputs such as directed edges. |
| Plan-and-Solve Prompting | A prompting strategy in which the model first creates a plan and then solves the task step by step. |
| Policy-First Structured Prompting | A strategy that places explicit causal-discovery rules before the main task. |
| Prompt Decomposition | A prompting approach that divides a complex task into smaller reasoning stages before final output generation. |
| Prompt Engineering | The design of prompts, examples, roles, constraints, and reasoning instructions to influence LLM behaviour. |
| Prompt Scope | The breadth of the requested model output. A narrow prompt scope can reduce sensitivity leakage by restricting what the model is allowed to generate. |
| Prompt Sensitivity | The tendency of LLM outputs to change when prompt wording, structure, or framing changes. |
| ReAct Prompting | A prompting strategy that interleaves reasoning and action-like steps. |
| Rephrase and Respond | A prompting strategy where the model first rephrases the question and then answers the rephrased version. |
| Role Prompting | A prompting strategy that assigns the model a role or persona, such as automotive analyst, technician, or fleet manager. |
| Sensitivity Leakage | The exposure of sensitive values, behavioural patterns, location-related inferences, or private information from input data in the model output. |
| Skeleton-of-Thought Prompting | A decomposition strategy that provides a structured internal outline before the final answer, such as separating energy-state, driving-behaviour, and cross-group relations. |
| Sochighlevel | A telematics feature representing a high-level state-of-charge indicator. |
| Speed_kmh | A vehicle speed variable measured in kilometers per hour. |
| Step-Back Prompting | A prompting method that first asks the model to consider a higher-level principle before solving the specific task. |
| Structural Evaluation | Evaluation of predicted graph structure by comparing edges, directions, and adjacency matrices against a ground truth. |
| Style Prompting | A prompting strategy that asks the model to respond in a particular style or expert persona. |
| Telematics | The collection and analysis of vehicle-generated data such as speed, acceleration, battery state, mileage, energy consumption, and operational behaviour. |
| Tesla EV Dataset | A Tesla electric-vehicle dataset used in graph-recovery experiments involving features such as remaining electric energy, speed, acceleration, mileage, and distance. |
| Time Series Data | Data recorded sequentially over time. Vehicle telematics data is treated as time series because readings are collected at repeated time intervals. |
| Zero-Shot Prompting | A baseline prompting strategy where the model receives the task without examples or demonstrations. |

## 2.2 Abbreviation Glossary

| Abbreviation | Full Form | Definition |
|---|---|---|
| AI | Artificial Intelligence | A field of computing concerned with systems that perform tasks requiring human-like intelligence. |
| API | Application Programming Interface | A software interface that allows applications or systems to communicate; used in the theses for local model calls through Ollama. |
| CoT | Chain of Thought | A prompting strategy that encourages step-by-step reasoning before producing the final answer. |
| DAG | Directed Acyclic Graph | A directed graph with no cycles, used to represent causal structures. |
| DL | Deep Learning | A machine learning approach based on multi-layer neural networks. |
| EV | Electric Vehicle | A vehicle powered by an electric motor and battery system. |
| F1 | F1 Score | The harmonic mean of precision and recall. |
| FDR | False Discovery Rate | The proportion of predicted edges that are incorrect. |
| FN | False Negative | A ground-truth edge that the model failed to predict. |
| FP | False Positive | A predicted edge that does not exist in the ground-truth graph. |
| GDPR | General Data Protection Regulation | The European Union regulation governing personal data protection, relevant to vehicle location and behavioural data. |
| HEV | Hybrid Electric Vehicle | A vehicle that combines an internal combustion engine with an electric drivetrain. |
| KG | Knowledge Graph | A graph-based representation of entities and their relationships. |
| LLM | Large Language Model | A neural language model capable of processing and generating natural language or structured text. |
| MHA | Multi-Head Attention | An attention mechanism that allows a model to attend to multiple representation subspaces. |
| ML | Machine Learning | A field of AI in which models learn patterns from data. |
| NLP | Natural Language Processing | A field of AI focused on understanding and generating human language. |
| OBD | On-Board Diagnostics | A vehicle diagnostic system used to retrieve operational and sensor data. |
| PHM | Prognostics and Health Management | A field focused on system health monitoring, failure prediction, and maintenance decision support. |
| PID | Parameter ID | An identifier used in vehicle diagnostics to request specific sensor values. |
| PdM | Predictive Maintenance | Maintenance based on predicting faults, failures, or degradation before they occur. |
| Qwen | Qwen Model Family | An open-weight language model family developed by Alibaba and evaluated in one thesis. |
| RAG | Retrieval-Augmented Generation | A method combining language generation with external information retrieval. |
| RaR | Rephrase and Respond | A prompting method where the model first rephrases the question and then answers it. |
| ReAct | Reasoning and Acting | A prompting strategy that combines reasoning steps with action-like steps. |
| RLHF | Reinforcement Learning from Human Feedback | A model-alignment technique using human preference feedback to improve model behaviour. |
| RMSE | Root Mean Square Error | An error metric used to measure the difference between predicted and actual values. |
| RQ | Research Question | A formal question that guides a thesis or research study. |
| SHD | Structural Hamming Distance | A graph error metric counting edge additions, deletions, or reversals needed to match the ground truth. |
| SFT | Supervised Fine-Tuning | A training method using labelled instruction-response examples. |
| SLR | Sensitivity Leakage Rate | A binary metric indicating whether sensitivity leakage is detected in an LLM output. |
| SoC | State of Charge | A battery measure indicating available charge, commonly expressed as a percentage. |
| SoT | Skeleton of Thought | A prompt decomposition strategy that uses a structured reasoning outline before producing the final answer. |
| TN | True Negative | A non-edge correctly not predicted by the model. |
| TP | True Positive | A predicted edge that exists in the ground-truth graph. |
| UBI | Usage-Based Insurance | An insurance model using driving behaviour or telematics data for risk assessment or pricing. |
