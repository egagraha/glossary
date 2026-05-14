# Glossary
## Table of Contents
- [1. Imputation and Mathematical Time-Series Glossary](#1-imputation-and-mathematical-time-series-glossary)
- [2. LLM, Telematics, Privacy, and Causal Graph Glossary](#2-llm-telematics-privacy-and-causal-graph-glossary)
- [3. Prompting Strategy Registry from the Notebook](#3-prompting-strategy-registry-from-the-notebook)
- [4. Ollama LLM Model Tested in the Silicon M1 Max 32GB Machine](#4-ollama-llm-model-tested-in-the-silicon-m1-max-32gb-machine)
- [5. Ollama Model Reference List](#5-ollama-model-reference-list)


## 1. Imputation and Mathematical Time-Series Glossary

| Term/Abbreviation | Description |
|---|---|
| Alternative Data | Non-traditional data sources used in finance, such as satellite imagery, web-scraped sentiment, app-usage statistics, or other irregular external signals. |
| BEV | Battery Electric Vehicle. A vehicle powered entirely by an electric battery and motor system. |
| Bi-LSTM | Bidirectional Long Short-Term Memory. A recurrent neural network that processes sequential data in both forward and backward directions. |
| BLR | Bayesian Linear Regression. A probabilistic regression model used for prediction and uncertainty estimation. |
| BMLR | Bayesian Multilevel Regression. A hierarchical Bayesian regression model allowing group-level variation. |
| B-RF | Bayesian Random Forest. A Bayesian or Bayesian-approximation version of Random Forest used to estimate uncertainty over predictions. |
| BSTS | Bayesian Structural Time Series. A Bayesian state-space model that decomposes a time series into components such as trend, seasonality, and regression effects. |
| B-XGB | Bayesian XGBoost. A Bayesian or Bayesian-approximation version of XGBoost used to estimate uncertainty over boosted-tree predictions. |
| CAN-bus | Controller Area Network bus. A vehicle communication system that allows electronic control units and sensors to exchange data. |
| Causal Discovery | The process of identifying possible causal structures among variables from data. In the imputation thesis, causal discovery is treated as a downstream motivation for producing complete and structurally faithful time series. |
| Causal Inference | The estimation or interpretation of cause-and-effect relationships after a causal structure has been assumed, learned, or validated. |
| Collinearity | A condition in which two or more variables are highly correlated, which can inflate model performance or create misleading structural relationships. |
| Composite Score | A model-selection score combining normalized RMSE, MAE, R², and WMAPE to compare imputation models across multiple metrics and missing rates. |
| Conv1D | One-Dimensional Convolutional Neural Network. A neural network architecture used to detect local temporal patterns in sequential data. |
| Covariance Preservation | The ability of an imputation method to maintain the original covariance structure among variables, which is important for downstream causal discovery and risk modelling. |
| DAG | Directed Acyclic Graph. A directed graph without cycles, often used to represent causal relationships. |
| Data Leakage | A modelling problem where information that should not be available during prediction is indirectly used, causing overly optimistic results. |
| Deep Learning Imputation | Imputation using neural network models such as LSTM, GRU, Conv1D, Bi-LSTM, or LSTM-MHA to reconstruct missing time-series values. |
| DL | Deep Learning. A class of machine learning methods based on multi-layer neural networks. |
| Edge Deployment | Running a model close to the data source, such as on an in-vehicle computing unit or edge gateway. |
| EKF | Extended Kalman Filter. A nonlinear extension of the Kalman filter using linearization around current estimates. |
| FCI | Fast Causal Inference. A causal discovery algorithm capable of handling latent confounders. |
| Feature-wise Imputation | An imputation approach where each feature is treated as a target variable in turn, while the remaining features are used as predictors. |
| Fixed-Parameter Kalman Filter | A Kalman filter configuration where noise parameters are manually fixed rather than estimated from data. In the imputation thesis, this configuration fails on near-constant BEV signals. |
| Fog Deployment | Running computation on intermediate infrastructure between edge devices and cloud servers. |
| GES | Greedy Equivalence Search. A score-based causal discovery algorithm that searches over possible graph structures. |
| Gradient Boosting | A machine learning technique that builds an ensemble of weak prediction models, usually decision trees, in a sequential manner to reduce error. |
| Ground Truth | The original known values used as a reference when evaluating reconstructed or imputed values. |
| GRU | Gated Recurrent Unit. A recurrent neural network architecture similar to LSTM but with fewer gates. |
| HMC | Hamiltonian Monte Carlo. A Bayesian sampling method used to estimate posterior distributions efficiently. |
| ICE | Internal Combustion Engine. A conventional engine type that may operate alongside an electric drivetrain in hybrid vehicles. |
| KF | Kalman Filter. A statistical state-space filtering method used to estimate hidden states in noisy sequential data. |
| Leaf-wise Tree Growth | A LightGBM tree-building strategy that expands the leaf with the largest potential loss reduction. |
| LightGBM | A gradient boosting algorithm based on decision trees, used in the imputation thesis for high-performing feature-wise imputation. |
| LSTM | Long Short-Term Memory. A recurrent neural network architecture designed to capture temporal dependencies in sequential data. |
| LSTM-MHA | Long Short-Term Memory with Multi-Head Attention. A hybrid neural architecture combining recurrent sequence modelling with attention. |
| MAE | Mean Absolute Error. The average absolute difference between predicted and true values. |
| MAPE | Mean Absolute Percentage Error. A relative error metric that can be unstable for near-zero values. |
| MAR | Missing At Random. A missing-data mechanism where missingness depends on observed variables but not directly on the missing value itself. |
| Mask-and-Reconstruct Protocol | An evaluation procedure in which known values are artificially masked and then reconstructed by imputation models, allowing direct comparison with ground truth. |
| MCAR | Missing Completely At Random. A missing-data mechanism where missingness is independent of observed and unobserved values. |
| MCDA | Multi-Criteria Decision Analysis. A decision-analysis approach used to compare alternatives across multiple criteria. |
| MinMax Scaling | A preprocessing method that rescales values into a fixed range, commonly [0, 1]. |
| Missing Data | Observations that are absent, corrupted, or unavailable due to sensor failure, transmission loss, irregular sampling, or other data-quality problems. |
| Missing Rate | The proportion or percentage of values removed, missing, or masked in a dataset. |
| ML | Machine Learning. A field of AI in which models learn patterns from data to make predictions or decisions. |
| MNAR | Missing Not At Random. A missing-data mechanism where the missing value itself influences the probability of being missing. |
| Multivariate Time Series | A time series dataset containing multiple variables observed over time, such as speed, mileage, battery voltage, and energy consumption. |
| Multi-Head Attention | An attention mechanism that allows a model to attend to different parts of a sequence simultaneously. |
| Near-constant Signal | A signal with very low variation over time, such as remaining battery energy during parked periods. |
| Non-stationarity | A condition where the statistical properties of a time series change over time, for example due to vehicle mode switching. |
| NUTS | No-U-Turn Sampler. An adaptive Markov Chain Monte Carlo algorithm used for Bayesian posterior sampling. |
| OBD-II PID | On-Board Diagnostics II Parameter ID. A standardized identifier used to request vehicle diagnostic or sensor values. |
| PC | Peter-Clark Algorithm. A constraint-based causal discovery algorithm using conditional independence tests. |
| PHEV | Plug-in Hybrid Electric Vehicle. A vehicle combining an internal combustion engine with a rechargeable electric drivetrain. |
| Posterior Predictive Distribution | A probability distribution representing predicted values and uncertainty after observing data in a Bayesian model. |
| Quantitative Finance | A field applying mathematical, statistical, and computational methods to financial markets, risk modelling, and asset pricing. |
| R² | Coefficient of Determination. A metric indicating the proportion of variance explained by a model. |
| Rauch-Tung-Striebel Smoother | A smoothing algorithm used with Kalman filtering to estimate latent states using the full observed sequence. |
| Regime Switching | A situation in which a system alternates between different operating states, such as electric and combustion modes in a hybrid vehicle. |
| RMSE | Root Mean Squared Error. The square root of the average squared prediction error. |
| SCR | Solvency Capital Requirement. A regulatory capital requirement under Solvency II for insurance companies. |
| Sequence-based Imputation | An imputation approach that uses windows of consecutive timesteps to reconstruct missing values by exploiting temporal context. |
| SHD | Structural Hamming Distance. A graph error metric counting edge additions, deletions, or reversals. |
| Sliding Window | A fixed-length sequence of consecutive observations used as input for sequence-based models. |
| State-Space Model | A mathematical model representing observed data as generated from hidden states that evolve over time. |
| Tick-data Synchronisation | The process of aligning asynchronously observed financial market transactions onto a common time grid. |
| Time Series | A sequence of observations recorded over time, where temporal order is central to analysis. |
| Time-Series Imputation | The process of estimating and filling missing values in a time series while preserving temporal structure and inter-variable relationships. |
| UBI | Usage-Based Insurance. An insurance approach based on observed driving behaviour or vehicle usage. |
| UKF | Unscented Kalman Filter. A nonlinear Kalman filter variant using deterministic sampling to approximate nonlinear transformations. |
| VaR | Value-at-Risk. A financial risk metric estimating potential loss at a given confidence level. |
| Vehicular Telematics | Vehicle-generated data collected from sensors and communication systems, including speed, acceleration, mileage, battery voltage, and energy consumption. |
| WMAPE | Weighted Mean Absolute Percentage Error. A relative error metric that is more stable than MAPE for near-zero-valued features. |
| Yield Curve Reconstruction | The process of estimating interest rates at unobserved maturities using available financial data. |
| Zero-inflated Feature | A variable containing many zero values, such as acceleration or distance during stationary vehicle periods. |
| ZLB | Zero Lower Bound. A financial condition where interest rates are close to zero. |


## 2. LLM, Telematics, Privacy, and Causal Graph Glossary

| Term/Abbreviation | Description |
|---|---|
| ACC | Acceleration. Abbreviation used in a ground-truth adjacency matrix for the feature acceleration_kmh2. |
| Acceleration_kmh2 | A vehicle telematics variable representing acceleration in km/h², used to analyse driving behaviour and energy demand. |
| Adjacency Matrix | A matrix representation of a directed graph where each entry indicates whether a relationship exists from one feature to another. |
| AI | Artificial Intelligence. A field of computing concerned with systems that perform tasks requiring human-like intelligence. |
| AIoT | Artificial Intelligence of Things. The combination of AI techniques with IoT systems, mentioned in relation to predictive maintenance and connected systems. |
| Analytical Utility | The usefulness of an LLM output for the intended analytical task, such as recovering correct causal or directed graph relationships. |
| API | Application Programming Interface. A software interface that allows applications or systems to communicate; used in the theses for local model calls through Ollama. |
| Batteryvoltage | A telematics feature representing the electrical voltage of the vehicle battery. |
| BEV | Battery Electric Vehicle. A vehicle powered entirely by an electric battery and motor system. |
| BV | Battery Voltage. Abbreviation used in the ground-truth adjacency matrix for batteryvoltage. |
| Caruso Platform | A vehicle data platform used as a source for telematics data in one of the thesis documents. |
| Causal Discovery | The process of identifying directed cause-and-effect relationships among variables. In the uploaded theses, LLMs are tested as tools for generating candidate causal structures from telematics data. |
| Causal Graph | A directed graph showing assumed or expert-defined causal relationships among variables. |
| Causal Relationship Extraction | The process of extracting directed causal statements from an LLM output before graph construction and evaluation. |
| CNN | Convolutional Neural Network. A neural network architecture referenced in related work on fault diagnosis. |
| Confusion Counts | Counts used in graph evaluation, including true positives, false positives, false negatives, and true negatives. |
| Consensus Graph | A graph produced by aggregating edges predicted across multiple model and prompt configurations. It shows recurring model beliefs but does not guarantee correctness. |
| CSV | Comma-Separated Values. A tabular data file format used for datasets and result artifacts. |
| CWD | Current Working Directory. The active filesystem directory used during notebook execution. |
| DAG | Directed Acyclic Graph. A directed graph with no cycles, used to represent causal structures. |
| Data Fingerprint | A compact dataset summary containing descriptive statistics and correlations, used as LLM input instead of the full dataset. |
| Data Leakage | The unintended exposure of sensitive values, behavioural patterns, or private information in model outputs. |
| Directed Edge | A directed relationship from one variable to another, for example `speed_kmh -> energyconsumptionaverage`. |
| Directed Graph | A graph composed of nodes and arrows, where arrows indicate the direction of influence or relationship. |
| Distance_m | A Tesla EV telematics feature representing travelled distance in meters. |
| DL | Deep Learning. A machine learning approach based on multi-layer neural networks. |
| ECA | Energy Consumption Average. Abbreviation used in the ground-truth adjacency matrix for energyconsumptionaverage. |
| Edge Count | The number of directed relationships predicted or extracted from an LLM output. |
| Edge-Level Analysis | Evaluation of individual predicted relationships to identify correct, false, missing, or reversed edges. |
| Edge Parser | A component that extracts structured directed relationships from raw LLM outputs. |
| Edge Probability Matrix | A matrix that stores how frequently each edge is predicted across repeated runs. |
| Electricenergyremaining | A Tesla EV feature representing remaining usable electric energy. |
| Electricremaining | A telematics feature representing remaining electric range or remaining electric energy proxy. |
| Energyconsumptionaverage | A telematics feature representing average energy consumption over time or distance. |
| ER | Electric Remaining. Abbreviation used in the ground-truth adjacency matrix for electricremaining. |
| EV | Electric Vehicle. A vehicle powered by an electric motor and battery system. |
| Expert-Defined Ground Truth | A manually defined reference graph based on domain knowledge, vehicle physics, or literature. |
| F1 | F1 Score. The harmonic mean of precision and recall. |
| FDR | False Discovery Rate. The proportion of predicted edges that are incorrect. |
| Fleet Monitoring | The use of vehicle data to monitor operations, sustainability, diagnostics, maintenance, or performance. |
| FN | False Negative. A ground-truth edge that the model failed to predict. |
| FP | False Positive. A predicted edge that does not exist in the ground-truth graph. |
| Frobenius Norm | A matrix-level error metric representing the magnitude of the difference between predicted and ground-truth matrices. |
| GDPR | General Data Protection Regulation. The European Union regulation governing personal data protection, relevant to vehicle location and behavioural data. |
| GPU | Graphics Processing Unit. Hardware used to accelerate model inference or computation. |
| Graph Recovery | The task of reconstructing a directed graph from model-generated edges and comparing it with a reference graph. |
| Ground Truth | The reference graph or structure used to evaluate model-generated outputs. |
| Hamming Distance | A metric measuring the proportion of differing entries between the predicted adjacency matrix and the ground-truth adjacency matrix. |
| HEV | Hybrid Electric Vehicle. A vehicle that combines an internal combustion engine with an electric drivetrain. |
| Hybrid Vehicle | A vehicle combining an internal combustion engine with an electric drivetrain. |
| In-Context Learning | The ability of a model to perform a task using information provided directly in the prompt, without changing model parameters. |
| Inference-Time Privacy | Privacy risk that occurs during model use when sensitive prompt content is exposed or inferred in the output. |
| JSON | JavaScript Object Notation. A structured data format used for storing model outputs, parsed edges, and experiment metadata. |
| JSON-LD | JavaScript Object Notation for Linked Data. A structured graph-oriented data format used for knowledge-graph-style exports. |
| KG | Knowledge Graph. A graph-based representation of entities and their relationships. |
| Knowledge Graph | A structured representation of entities and relationships, which can be created from parsed model-generated edges. |
| LLM | Large Language Model. A neural language model capable of processing and generating natural language or structured text. |
| Local Inference | Running an LLM on local hardware rather than sending sensitive data to an external API or cloud system. |
| MHA | Multi-Head Attention. An attention mechanism that allows a model to attend to multiple representation subspaces. |
| Mileage | A telematics variable representing total distance travelled by the vehicle. |
| MIL | Mileage. Abbreviation used in the ground-truth adjacency matrix for the mileage feature. |
| ML | Machine Learning. A field of AI in which models learn patterns from data. |
| NLP | Natural Language Processing. A field of AI focused on understanding and generating human language. |
| Normalization | A preprocessing step that rescales numerical features into a common range, often [0, 1]. |
| NPY | NumPy binary file format. A file format used to store arrays such as predicted adjacency matrices. |
| N_RUNS | Number of repeated experiment runs. In the notebook, this controls how often each model-strategy cell is repeated. |
| OBD | On-Board Diagnostics. A vehicle diagnostic system used to retrieve operational and sensor data. |
| Ollama | A local LLM deployment framework used to run open-weight models on consumer or local hardware. |
| Output Parsing | The process of converting raw LLM-generated text into structured machine-readable outputs such as directed edges. |
| Pearson Correlation | A metric measuring the linear similarity between flattened predicted and ground-truth adjacency matrices. |
| PdM | Predictive Maintenance. Maintenance based on predicting faults, failures, or degradation before they occur. |
| PHM | Prognostics and Health Management. A field focused on system health monitoring, failure prediction, and maintenance decision support. |
| PID | Parameter ID. An identifier used in vehicle diagnostics to request specific sensor values. |
| Precision | The proportion of predicted edges that are correct according to the ground-truth graph. |
| Prompt Engineering | The design of prompts, examples, roles, constraints, and reasoning instructions to influence LLM behaviour. |
| Prompt Scope | The breadth of the requested model output. A narrow prompt scope can reduce sensitivity leakage by restricting what the model is allowed to generate. |
| Prompt Sensitivity | The tendency of LLM outputs to change when prompt wording, structure, or framing changes. |
| RAG | Retrieval-Augmented Generation. A method combining language generation with external information retrieval. |
| Recall | The proportion of ground-truth edges correctly recovered by the model. |
| REST API | Representational State Transfer Application Programming Interface. A web API style used by Ollama for local model calls. |
| RLHF | Reinforcement Learning from Human Feedback. A model-alignment technique using human preference feedback to improve model behaviour. |
| RMSE | Root Mean Square Error. An error metric used to measure the difference between predicted and actual values. |
| RQ | Research Question. A formal question that guides a thesis or research study. |
| RUL | Remaining Useful Life. A predictive-maintenance concept referring to the estimated time before a component or system reaches failure or end of useful operation. |
| Sensitivity Leakage | The exposure of sensitive values, behavioural patterns, location-related inferences, or private information from input data in the model output. |
| SFT | Supervised Fine-Tuning. A training method using labelled instruction-response examples. |
| SHD | Structural Hamming Distance. A graph error metric counting edge additions, deletions, or reversals needed to match the ground truth. |
| SLR | Sensitivity Leakage Rate. A binary metric indicating whether sensitivity leakage is detected in an LLM output. |
| SoC | State of Charge. A battery measure indicating available charge, commonly expressed as a percentage. |
| SOCH | State of Charge High Level. Abbreviation used in the ground-truth adjacency matrix for sochighlevel. |
| Sochighlevel | A telematics feature representing a high-level state-of-charge indicator. |
| SPD | Speed. Abbreviation used in the ground-truth adjacency matrix for speed_kmh. |
| Speed_kmh | A vehicle speed variable measured in kilometers per hour. |
| Structural Evaluation | Evaluation of predicted graph structure by comparing edges, directions, and adjacency matrices against a ground truth. |
| Telematics | The collection and analysis of vehicle-generated data such as speed, acceleration, battery state, mileage, energy consumption, and operational behaviour. |
| Tesla EV Dataset | A Tesla electric-vehicle dataset used in graph-recovery experiments involving features such as remaining electric energy, speed, acceleration, mileage, and distance. |
| Time Series Data | Data recorded sequentially over time. Vehicle telematics data is treated as time series because readings are collected at repeated time intervals. |
| TN | True Negative. A non-edge correctly not predicted by the model. |
| TP | True Positive. A predicted edge that exists in the ground-truth graph. |
| UBI | Usage-Based Insurance. An insurance model using driving behaviour or telematics data for risk assessment or pricing. |


## 3. Prompting Strategy Registry from the Notebook

| Term/Abbreviation | Description |
|---|---|
| Strategy 1 Zero Shot Prompting | Baseline discovery strategy using the common base prompt without additional examples, roles, constraints, or decomposition. |
| Strategy 2 Few Shot Prompting | Provides illustrative example causal edges before the actual task to guide the model toward the expected output pattern. |
| Strategy 3 Role Prompting | Assigns the model the role of an expert automotive causal AI analyst before asking it to generate causal edges. |
| Strategy 4 Chain of Thought Prompting | Instructs the model to think step by step internally about variable pairs before outputting only the final causal edges. |
| Strategy 5 Self Consistency Prompting | Runs multiple internal generations and aggregates the predicted edge set by voting or consistency logic. |
| Strategy 6 Tree of Thought Prompting | Asks the model to consider multiple possible causal pathways for each pair and evaluate the strongest causal direction. |
| Strategy 7 Instruction Prompting | Adds explicit instructions to identify causal links and format the result strictly as `feature_a -> feature_b`. |
| Strategy 8 Emotion Prompting | Adds motivational or risk-based framing, emphasizing that wrong causal links may cause downstream system failure. |
| Strategy 9 Style Prompting | Instructs the model to respond like a scientific causal-discovery engine using minimal formal arrow notation. |
| Strategy 10 Contextual Prompting | Adds context that the dataset comes from EV/HEV telematics for predictive maintenance and that causality must reflect physical vehicle dynamics. |
| Strategy 11 Step Back Prompting | Asks the model to first consider general physical laws governing battery, drivetrain, and vehicle dynamics, then apply them to the dataset. |
| Strategy 12 Decomposition Prompting | Divides the analysis into battery/energy-consumption features, driving-behaviour features, and wear/odometer features before integrating results. |
| Strategy 13 Contrastive Prompting | Asks the model to distinguish strong causal links from mere correlations and exclude correlation-only relationships. |
| Strategy 14 ReAct Prompting | Combines reasoning about vehicle dynamics with an action step that outputs the final causal edges only. |
| Strategy 15 Meta Prompting | Instructs the model to internally choose the most suitable reasoning strategy for the task and then output final causal edges. |
| Strategy 16 Constraint Prompting | Adds constraints such as direct causality only, no bidirectional edges unless physically valid, and no correlation-only links. |
| Strategy 17 Structured Output Prompting | Forces the model to return strict JSON containing the causal-discovery edge list. |
| Strategy 18 Inference Sign | Extends causal edge output by asking for the qualitative sign of each relationship, such as positive, negative, or non-monotonic. |
| Strategy 19 Inference DoOperator | Uses a do-operator thought experiment to keep only edges where intervening on the cause changes the effect. |
| Strategy 20 Inference Counterfactual | Uses counterfactual reasoning to keep only edges where the effect would not occur if the cause were absent. |
| Strategy 21 Rephrase and Respond | Silently rephrases the task for clarity and specificity before answering with only the final causal edges. |
| Strategy 22 Plan and Solve | Uses an internal two-phase plan-and-execute process before producing only the final causal edges. |
| Strategy 23 No Instruction Control | Neutral baseline with no additional methodological framing beyond the base graph-recovery task. |
| Strategy 24 Policy First Structured | Places a numbered causal-discovery policy before the task, requiring direct edges, no transitive links, no correlation-only links, and strict arrow output. |
| Strategy 25 Least to Most | Decomposes the task from simple physical edges to more difficult accumulated-state edges, then filters out weak or mediated relationships. |
| Strategy 26 Skeleton of Thought | Uses a silent internal skeleton covering energy-state edges, driving-behaviour edges, cross-group edges, and an integrity gate before outputting final edges. |


## 4. Ollama LLM Model Tested in the Silicon M1 Max 32GB Machine

| Model | Family | Utilization | Description |
|---|---|---|---|
| deepseek-r1:14b | DeepSeek | Reasoning / CoT-trained / mid | A DeepSeek-R1 14B reasoning model used for structured reasoning, causal graph recovery, and prompt evaluation. Approximate model size: 9.0 GB. |
| gemma3:12b | Gemma | General / mid-small | A Gemma 3 12B model used as a mid-small model for improved quality compared with 7B-class baselines. Approximate model size: 7.8 GB. |
| gemma3:27b | Gemma | General / large quality | A Gemma 3 27B model used as a higher-quality large model candidate within the local hardware constraint. Approximate model size: 16.4 GB. |
| gpt-oss:20b | OpenAI | Reasoning / agentic / MoE | An OpenAI open-weight 20B model using a mixture-of-experts style design, noted as approximately 3.6B active parameters in the experiment list. Approximate model size: 13.0 GB. |
| llama3.1:8b | Llama | General / small baseline | A Meta Llama 3.1 8B model used as a small general-purpose baseline for local graph-recovery and prompting experiments. Approximate model size: 4.9 GB. |
| mistral:7b | Mistral | General / small baseline | A compact 7B Mistral model used as a small baseline for local LLM evaluation on the Apple Silicon M1 Max 32GB machine. Approximate model size: 4.4 GB. |
| mistral-small:24b | Mistral | General / large workhorse | A larger Mistral model used as a workhorse option for higher-quality local inference on the M1 Max 32GB machine. Approximate model size: 14.3 GB. |
| phi4:14b | Phi | Reasoning / mid | A Microsoft Phi 4 14B model used as a mid-sized reasoning-oriented model. Approximate model size: 9.1 GB. |
| qwen2.5:14b | Qwen | General / mid | A Qwen 2.5 14B model used as a mid-sized general-purpose model. Approximate model size: 9.0 GB. |
| qwen2.5:7b | Qwen | General / small baseline | A Qwen 2.5 7B model used as a compact multilingual and general-purpose baseline. Approximate model size: 4.7 GB. |
| qwen3:14b | Qwen | Hybrid-thinking / mid | A Qwen 3 14B model used as a mid-sized hybrid-thinking model in the v3.8 experimental setup. Approximate model size: 9.3 GB. |
---
## 5. Ollama Model Reference List
| Model | Family | Utilization | Description |
|---|---|---|---|
| aya | Cohere | Multilingual | Multilingual model family supporting many languages. |
| bge-m3 | BAAI | Embedding | Multifunctional, multilingual, and multi-granularity embedding model. |
| codeqwen | Qwen | Coder | CodeQwen model pretrained on code data. |
| codellama | Llama | Coder | Code-focused Llama model family for generating and discussing code. |
| codestral | Mistral | Coder | Mistral AI code model designed for code generation tasks. |
| cogito | Cogito | Hybrid reasoning | Hybrid reasoning model family by Deep Cogito. |
| command-r | Cohere | Conversational / long context | Command R model optimized for conversational interaction and long-context tasks. |
| deepseek-coder | DeepSeek | Coder | DeepSeek coding model trained on code and natural language data. |
| deepseek-llm | DeepSeek | General / bilingual | DeepSeek language model trained on bilingual data. |
| deepseek-r1 | DeepSeek | Reasoning / thinking | Open reasoning model family with sizes from small distilled variants to very large models. |
| deepseek-v2 | DeepSeek | MoE / efficient general | Economical Mixture-of-Experts language model. |
| deepseek-v3 | DeepSeek | MoE / general | Large Mixture-of-Experts DeepSeek model with activated sparse parameters. |
| deepseek-v3.2 | DeepSeek | Reasoning / agentic | DeepSeek model combining computational efficiency with reasoning and agent performance. |
| deepseek-v4-flash | DeepSeek | MoE / reasoning | DeepSeek-V4 preview MoE model for efficient reasoning across long context. |
| deepseek-v4-pro | DeepSeek | MoE / reasoning | DeepSeek-V4 Pro frontier MoE model with multiple reasoning modes. |
| deepscaler | DeepSeek-derived | Math / reasoning | Fine-tuned DeepSeek-R1-distilled model for math reasoning. |
| dolphin-llama3 | Dolphin / Llama | General / coding | Dolphin model based on Llama 3 with instruction, conversational, and coding skills. |
| dolphin-mistral | Dolphin / Mistral | General / coding | Dolphin model based on Mistral, commonly used for coding and general tasks. |
| embeddinggemma | Gemma | Embedding | Google embedding model based on Gemma. |
| falcon | TII | General | Falcon large language model family for summarization, generation, and chat. |
| functiongemma | Gemma | Function calling | Gemma-based model fine-tuned for function calling. |
| gemini-3-flash-preview | Gemini | Cloud / vision / thinking | Gemini Flash preview model exposed in the Ollama library as a cloud model. |
| gemma | Gemma | Lightweight / general | Lightweight open model family from Google DeepMind. |
| gemma2 | Gemma | General | Google Gemma 2 model family available in 2B, 9B, and 27B sizes. |
| gemma3 | Gemma | General / vision | Gemma 3 model family designed to run efficiently on a single GPU, with multiple sizes. |
| gemma3n | Gemma | On-device / efficient | Gemma 3n family designed for efficient execution on everyday devices. |
| gemma4 | Gemma | Multimodal / reasoning / coding | Gemma 4 family designed for reasoning, agentic workflows, coding, and multimodal understanding. |
| glm-4.6 | GLM / Z.ai | Agentic / reasoning / coding | GLM model with agentic, reasoning, and coding capabilities. |
| glm-4.7 | GLM / Z.ai | Coding / reasoning | GLM model focused on advancing coding capability. |
| glm-4.7-flash | GLM / Z.ai | Reasoning / tools | GLM model balancing performance and efficiency in the 30B class. |
| glm-5 | GLM / Z.ai | Agentic / reasoning | Large reasoning and agentic model for complex systems engineering. |
| glm-5.1 | GLM / Z.ai | Agentic engineering / coding | Next-generation GLM model focused on agentic engineering and stronger coding. |
| glm4 | GLM / Z.ai | General / multilingual | Multilingual general language model. |
| glm-ocr | GLM / Z.ai | OCR / vision | Multimodal OCR model for complex document understanding. |
| gpt-oss | OpenAI | Reasoning / agentic / developer | OpenAI open-weight model family designed for reasoning, agentic tasks, and developer use cases. |
| gpt-oss-safeguard | OpenAI | Safety / reasoning | Safety reasoning model family built on gpt-oss. |
| granite-code | IBM Granite | Coder | IBM Granite open foundation models for code intelligence. |
| granite-embedding | IBM Granite | Embedding | IBM Granite dense bi-encoder embedding model family. |
| granite3.2 | IBM Granite | Long context / thinking | IBM Granite long-context model family fine-tuned for thinking capabilities. |
| granite3.3 | IBM Granite | Tools / reasoning | IBM Granite model family with long-context and improved reasoning. |
| granite4 | IBM Granite | Enterprise / tools | IBM Granite 4 model family with improved instruction following and tool calling. |
| granite4.1 | IBM Granite | Enterprise / RAG / tools | Enterprise-ready Granite model supporting multilingual capability, coding, RAG, tool use, and structured JSON. |
| hermes3 | Nous Research | General / tools | Hermes 3 model family for general instruction and tool-oriented tasks. |
| kimi-k2.6 | Kimi / Moonshot | Multimodal / agentic / coding | Multimodal agentic model for long-horizon coding and autonomous execution. |
| kimi-k2-thinking | Kimi / Moonshot | Thinking / reasoning | Moonshot AI open-source thinking model. |
| laguna-xs.2 | Laguna | Agentic coding | Mixture-of-Experts model designed for agentic coding and local long-horizon work. |
| lfm2 | LFM | Hybrid / on-device | Hybrid model family designed for efficient on-device deployment. |
| lfm2.5-thinking | LFM | Hybrid / on-device | Hybrid thinking model family designed for on-device deployment. |
| llama2 | Llama | General | Llama 2 foundation language model family. |
| llama2-chinese | Llama | Chinese chat | Llama 2-based model fine-tuned for Chinese dialogue. |
| llama3 | Llama | General | Meta Llama 3 family available in 8B and 70B sizes. |
| llama3.1 | Llama | General / tools | Meta Llama 3.1 model family available in 8B, 70B, and 405B sizes. |
| llama3.2 | Llama | General / tools / small | Meta Llama 3.2 small model family, including 1B and 3B variants. |
| llama3.2-vision | Llama | Vision-language | Llama 3.2 vision model family for image reasoning and multimodal generation. |
| llava | LLaVA | Vision-language | Multimodal model combining a vision encoder with a language model for image and text understanding. |
| magistral | Mistral | Reasoning | Small efficient Mistral reasoning model family. |
| medgemma | Gemma | Medical / vision-language | Gemma 3 variants trained for medical text and image comprehension. |
| medgemma1.5 | Gemma | Medical / vision-language | Updated MedGemma model for medical text and image comprehension. |
| minicpm-v | MiniCPM | Vision-language | Multimodal LLM family designed for vision-language understanding. |
| minimax-m2 | MiniMax | Coding / agentic | High-efficiency model for coding and agentic workflows. |
| minimax-m2.1 | MiniMax | Multilingual / coding | MiniMax model with multilingual and code engineering capability. |
| minimax-m2.5 | MiniMax | Coding / productivity / reasoning | MiniMax model for real-world productivity and coding tasks. |
| minimax-m2.7 | MiniMax | Coding / agentic | MiniMax M2-series model for coding, agentic workflows, and productivity. |
| ministral-3 | Mistral | Edge / tools / vision | Ministral 3 family designed for edge deployment. |
| mistral | Mistral | General / tools | Mistral 7B model family for compact general-purpose local inference. |
| mistral-large | Mistral | Large / reasoning / coding | Mistral flagship model family for code, math, reasoning, and multilingual tasks. |
| mistral-medium-3.5 | Mistral | Reasoning / coding / multimodal | Mistral flagship model combining instruction following, reasoning, and coding. |
| mistral-nemo | Mistral | General / long context | Mistral-Nemo 12B model with long-context capability. |
| mistral-small3.2 | Mistral | General / tools / vision | Mistral Small update improving function calling, instruction following, and repetition handling. |
| moondream | Moondream | Vision-language / edge | Small vision-language model designed for efficient edge use. |
| mxbai-embed-large | Mixedbread | Embedding | Large embedding model from mixedbread.ai. |
| nemotron-3-nano | NVIDIA | Agentic / reasoning / efficient | Efficient Nemotron model for open, intelligent, agentic workflows. |
| nemotron-3-super | NVIDIA | MoE / reasoning / agentic | NVIDIA Nemotron 3 Super MoE model for complex multi-agent applications. |
| nemotron3 | NVIDIA | Multimodal / enterprise | NVIDIA Nemotron model family for video, audio, image, text, Q&A, summarization, and document intelligence. |
| neural-chat | Intel / Mistral-based | Chat | Mistral-based fine-tuned model for chat and general domains. |
| nomic-embed-text | Nomic | Embedding | High-performing text embedding model with a large context window. |
| nous-hermes | Nous Research | General | General-use models based on Llama and Llama 2. |
| nous-hermes2 | Nous Research | General / coding | Nous Hermes 2 model family for scientific discussion and coding tasks. |
| olmo2 | OLMo | General / open research | Open language model family trained for competitive academic performance. |
| olmo-3 | OLMo | Open research / general | Open language model family designed to support language-model science. |
| openchat | OpenChat | General chat | Open-source chat model family trained on varied data. |
| openhermes | OpenHermes | General | OpenHermes model fine-tuned on open datasets. |
| openthinker | OpenThinker | Reasoning | Open-source reasoning model family distilled from DeepSeek-R1-style data. |
| phi3 | Phi | Lightweight / reasoning | Microsoft Phi-3 family of lightweight open models. |
| phi4 | Phi | Reasoning / general | Microsoft Phi-4 14B open model for reasoning and general tasks. |
| phi4-mini | Phi | Lightweight / reasoning / tools | Small Phi-4 model with multilingual support, reasoning, mathematics, and function calling. |
| phi4-reasoning | Phi | Reasoning | Microsoft Phi-4 reasoning model family for complex reasoning tasks. |
| qwen | Qwen | General / multilingual | Alibaba Cloud transformer-based model family spanning several parameter sizes. |
| qwen2 | Qwen | General / tools | Qwen 2 model family from Alibaba. |
| qwen2.5 | Qwen | General / tools / multilingual | Qwen 2.5 model family supporting long context and multilingual use cases. |
| qwen2.5-coder | Qwen | Coder | Code-specific Qwen model family for code generation, code reasoning, and code fixing. |
| qwen2.5vl | Qwen | Vision-language | Qwen 2.5 vision-language model family. |
| qwen2-math | Qwen | Math | Qwen2 specialized math model family. |
| qwen3 | Qwen | General / thinking / MoE | Qwen 3 model family including dense and mixture-of-experts models. |
| qwen3.5 | Qwen | Multimodal / thinking / tools | Open-source multimodal Qwen family with utility across text, tools, reasoning, and vision. |
| qwen3.6 | Qwen | Agentic coding / thinking / vision | Qwen3.6 family with upgrades for coding, thinking preservation, and multimodal use. |
| qwen3-coder | Qwen | Coder / agentic | Long-context Qwen model family for agentic and coding tasks. |
| qwen3-coder-next | Qwen | Coder / agentic | Qwen coding-focused model optimized for agentic local development workflows. |
| qwen3-embedding | Qwen | Embedding | Qwen3-based text embedding model family. |
| qwen3-vl | Qwen | Vision-language / thinking | Vision-language Qwen model family for multimodal reasoning. |
| r1-1776 | Perplexity / DeepSeek-derived | Reasoning / factuality | Post-trained DeepSeek-R1 variant focused on unbiased and factual information. |
| rnj-1 | Essential AI | Code / STEM | Dense open-weight model optimized for code and STEM tasks. |
| smollm | SmolLM | Small / general | Family of small models trained on high-quality datasets. |
| smollm2 | SmolLM | Small / general | Compact model family with 135M, 360M, and 1.7B variants. |
| sqlcoder | SQLCoder | SQL / coder | Model fine-tuned for SQL generation tasks. |
| stable-code | Stability AI | Coder | Compact coding model for code completion and instruction use. |
| stablelm2 | Stability AI | General / multilingual | Stable LM 2 multilingual language model family. |
| starcoder | BigCode | Coder | Code generation model trained on many programming languages. |
| tinyllama | TinyLlama | Small / general | Compact 1.1B Llama-style model trained on large-scale text. |
| translategemma | Gemma | Translation | Gemma-based translation model collection supporting many languages. |
| tulu3 | Allen AI | Instruction following | Open-source instruction-following model family. |
| vicuna | Vicuna | Chat | General chat model based on Llama and Llama 2. |
| wizardcoder | WizardCoder | Coder | Code generation model family. |
| wizardlm2 | WizardLM | General / multilingual / reasoning | Microsoft AI model family for complex chat, multilingual reasoning, and agent use cases. |
| wizard-vicuna-uncensored | Wizard / Vicuna | General chat | Vicuna-based uncensored model family. |
| yi | Yi | Bilingual / general | Bilingual language model family. |
| yi-coder | Yi | Coder | Code language model family with fewer than 10B parameters. |
| zephyr | Hugging Face / Mistral | Assistant / chat | Fine-tuned assistant model family based on Mistral and Mixtral. |
