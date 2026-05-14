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


## 5. Ollama Model Reference List

| Model | Parameter Size | Family | Utilization | Ollama Pull Model | Description |
|---|---:|---|---|---|---|
| alfred | 40B | Alfred | Chat / instruct | `ollama pull alfred` | Robust conversational model designed for both chat and instruction-following use cases. |
| all-minilm | 22M, 33M | MiniLM | Embedding | `ollama pull all-minilm` | Embedding models trained on very large sentence-level datasets. |
| athene-v2 | 72B | Athene | Coding / math / log extraction | `ollama pull athene-v2` | Model focused on code completion, mathematics, and log extraction tasks. |
| aya | 8B, 35B | Cohere | Multilingual | `ollama pull aya` | Multilingual model family supporting many languages. |
| aya-expanse | 8B, 32B | Cohere | Multilingual / tools | `ollama pull aya-expanse` | Cohere For AI language models trained to perform well across 23 languages. |
| bakllava | 7B | LLaVA / Mistral | Vision-language | `ollama pull bakllava` | Multimodal model consisting of a Mistral 7B base model augmented with LLaVA architecture. |
| bespoke-minicheck | 7B | Bespoke Labs | Fact-checking | `ollama pull bespoke-minicheck` | Fact-checking model developed for verification-oriented tasks. |
| bge-large | 335M | BAAI | Embedding | `ollama pull bge-large` | BAAI embedding model that maps text into vectors. |
| bge-m3 | 567M | BAAI | Embedding / multilingual | `ollama pull bge-m3` | Multifunctional, multilingual, and multi-granularity embedding model. |
| codebooga | 34B | CodeBooga | Coder | `ollama pull codebooga` | Code-instruction model created by merging existing code models. |
| codegemma | 2B, 7B | Gemma | Coder / general | `ollama pull codegemma` | Lightweight coding model family for code completion, generation, mathematical reasoning, and instruction following. |
| codegeex4 | 9B | CodeGeeX | Coder | `ollama pull codegeex4` | Model for AI software development scenarios, including code completion. |
| codellama | 7B, 13B, 34B, 70B | Llama | Coder | `ollama pull codellama` | Code-focused Llama model family for generating and discussing code. |
| codeqwen | 7B | Qwen | Coder | `ollama pull codeqwen` | CodeQwen model pretrained on code data. |
| codestral | 22B | Mistral | Coder | `ollama pull codestral` | Mistral AI code model designed for code generation tasks. |
| codeup | 13B | Llama | Coder | `ollama pull codeup` | Code generation model based on Llama 2. |
| cogito | 3B, 8B, 14B, 32B, 70B | Cogito | Hybrid reasoning / tools | `ollama pull cogito` | Hybrid reasoning model family by Deep Cogito. |
| cogito-2.1 | 671B | Cogito | General / cloud | `ollama pull cogito-2.1` | Instruction-tuned generative model family released under MIT license. |
| command-a | 111B | Cohere | Enterprise / tools | `ollama pull command-a` | Enterprise-oriented model optimized for fast, secure, and high-quality AI tool use. |
| command-r | 35B | Cohere | Conversational / long context / tools | `ollama pull command-r` | Model optimized for conversational interaction and long-context tasks. |
| command-r-plus | 104B | Cohere | Enterprise / tools | `ollama pull command-r-plus` | Scalable enterprise model designed for real-world enterprise use cases. |
| command-r7b | 7B | Cohere | Lightweight / tools | `ollama pull command-r7b` | Small Command R model designed for speed and efficiency on commodity GPUs and edge devices. |
| command-r7b-arabic | 7B | Cohere | Arabic / enterprise / tools | `ollama pull command-r7b-arabic` | Command R7B variant optimized for Arabic-language enterprise use cases. |
| dbrx | 132B | Databricks | General | `ollama pull dbrx` | Open general-purpose LLM created by Databricks. |
| deepcoder | 1.5B, 14B | DeepCoder | Coder / reasoning | `ollama pull deepcoder` | Open-source coder model family with strong code-reasoning capability. |
| deepscaler | 1.5B | DeepSeek-derived | Math / reasoning | `ollama pull deepscaler` | Fine-tuned DeepSeek-R1-distilled model for math reasoning. |
| deepseek-coder | 1.3B, 6.7B, 33B | DeepSeek | Coder | `ollama pull deepseek-coder` | Coding model trained on code and natural language data. |
| deepseek-coder-v2 | 16B, 236B | DeepSeek | Coder / MoE | `ollama pull deepseek-coder-v2` | Mixture-of-Experts code model for code-specific tasks. |
| deepseek-llm | 7B, 67B | DeepSeek | General / bilingual | `ollama pull deepseek-llm` | Bilingual language model trained on large-scale English and Chinese data. |
| deepseek-ocr | 3B | DeepSeek | OCR / vision | `ollama pull deepseek-ocr` | Vision-language model for token-efficient OCR. |
| deepseek-r1 | 1.5B, 7B, 8B, 14B, 32B, 70B, 671B | DeepSeek | Reasoning / thinking | `ollama pull deepseek-r1:14b` | Open reasoning model family with performance approaching leading reasoning models. |
| deepseek-v2 | 16B, 236B | DeepSeek | MoE / efficient general | `ollama pull deepseek-v2` | Economical and efficient Mixture-of-Experts language model. |
| deepseek-v2.5 | 236B | DeepSeek | General / coding | `ollama pull deepseek-v2.5` | Upgraded DeepSeek-V2 model integrating general and coding abilities. |
| deepseek-v3 | 671B | DeepSeek | MoE / general | `ollama pull deepseek-v3` | Large Mixture-of-Experts model with sparse activated parameters. |
| deepseek-v3.1 | 671B | DeepSeek | Hybrid thinking / tools | `ollama pull deepseek-v3.1` | Hybrid DeepSeek model supporting thinking and non-thinking modes. |
| deepseek-v3.2 | Not specified | DeepSeek | Reasoning / agentic / tools | `ollama pull deepseek-v3.2` | Model combining computational efficiency with reasoning and agent performance. |
| deepseek-v4-flash | 284B total, 13B active | DeepSeek | MoE / reasoning / cloud | `ollama pull deepseek-v4-flash` | Preview model for efficient reasoning across long context. |
| deepseek-v4-pro | Not specified | DeepSeek | MoE / reasoning / cloud | `ollama pull deepseek-v4-pro` | Frontier DeepSeek-V4 model with multiple reasoning modes. |
| devstral | 24B | Mistral | Coding agent / tools | `ollama pull devstral` | Open-source model for coding agents. |
| devstral-2 | 123B | Mistral | Coding agent / tools / cloud | `ollama pull devstral-2` | Large coding-agent model for exploring codebases and editing multiple files. |
| devstral-small-2 | 24B | Mistral | Coding agent / tools / vision | `ollama pull devstral-small-2` | Smaller Devstral model for software engineering agent workflows. |
| dolphin-llama3 | 8B, 70B | Dolphin / Llama | General / coding | `ollama pull dolphin-llama3` | Dolphin model based on Llama 3 for instruction, conversation, and coding. |
| dolphin-mistral | 7B | Dolphin / Mistral | General / coding | `ollama pull dolphin-mistral` | Dolphin model based on Mistral, commonly used for coding and general tasks. |
| dolphin-mixtral | 8x7B, 8x22B | Dolphin / Mixtral | Coding / MoE | `ollama pull dolphin-mixtral` | Dolphin fine-tuned model based on Mixtral MoE models. |
| dolphin-phi | 2.7B | Dolphin / Phi | General chat | `ollama pull dolphin-phi` | Dolphin model based on Microsoft Phi. |
| dolphincoder | 7B, 15B | Dolphin / StarCoder2 | Coder | `ollama pull dolphincoder` | Dolphin coding model based on StarCoder2. |
| duckdb-nsql | 7B | DuckDB / Numbers Station | SQL / text-to-SQL | `ollama pull duckdb-nsql` | Text-to-SQL model made by MotherDuck and Numbers Station. |
| embeddinggemma | 300M | Gemma | Embedding | `ollama pull embeddinggemma` | Google embedding model based on Gemma. |
| everythinglm | 13B | Llama | General chat | `ollama pull everythinglm` | Llama 2-based model with support for a 16K context window. |
| exaone-deep | 2.4B, 7.8B, 32B | EXAONE | Reasoning / math / coding | `ollama pull exaone-deep` | LG AI Research model family for reasoning tasks including math and coding. |
| exaone3.5 | 2.4B, 7.8B, 32B | EXAONE | Bilingual / instruction | `ollama pull exaone3.5` | Instruction-tuned bilingual English-Korean generative model family. |
| falcon | 7B, 40B, 180B | TII | General | `ollama pull falcon` | Falcon model family for summarization, text generation, and chatbots. |
| falcon2 | 11B | TII | General | `ollama pull falcon2` | Causal decoder-only model trained on large-scale tokens. |
| falcon3 | 1B, 3B, 7B, 10B | TII | Science / math / coding | `ollama pull falcon3` | Efficient model family under 10B parameters for science, math, and coding. |
| firefunction-v2 | 70B | Fireworks / Llama | Function calling / tools | `ollama pull firefunction-v2` | Function-calling model based on Llama 3. |
| functiongemma | 270M | Gemma | Function calling / tools | `ollama pull functiongemma` | Gemma-based model fine-tuned for function calling. |
| gemini-3-flash-preview | Not specified | Gemini | Cloud / vision / thinking / tools | `ollama pull gemini-3-flash-preview` | Gemini Flash preview model exposed through Ollama’s library interface. |
| gemma | 2B, 7B | Gemma | Lightweight / general | `ollama pull gemma:7b` | Lightweight open model family from Google DeepMind. |
| gemma2 | 2B, 9B, 27B | Gemma | General | `ollama pull gemma2:9b` | Google Gemma 2 model family for efficient general use. |
| gemma3 | 270M, 1B, 4B, 12B, 27B | Gemma | General / vision / cloud | `ollama pull gemma3:12b` | Current Gemma model family designed to run efficiently on a single GPU. |
| gemma3n | E2B, E4B | Gemma | On-device / efficient | `ollama pull gemma3n` | Gemma 3n model family designed for everyday devices. |
| gemma4 | E2B, E4B, 26B, 31B | Gemma | Multimodal / reasoning / coding / tools | `ollama pull gemma4` | Gemma 4 family for reasoning, agentic workflows, coding, and multimodal understanding. |
| glm-4.6 | Not specified | GLM / Z.ai | Agentic / reasoning / coding | `ollama pull glm-4.6` | GLM model with agentic, reasoning, and coding capabilities. |
| glm-4.7 | Not specified | GLM / Z.ai | Coding / reasoning / tools | `ollama pull glm-4.7` | GLM model focused on advancing coding capability. |
| glm-4.7-flash | Not specified | GLM / Z.ai | Reasoning / lightweight / tools | `ollama pull glm-4.7-flash` | Lightweight GLM model balancing performance and efficiency. |
| glm-5 | 744B total, 40B active | GLM / Z.ai | Agentic / reasoning / cloud | `ollama pull glm-5` | Large reasoning and agentic model for complex systems engineering. |
| glm-5.1 | Not specified | GLM / Z.ai | Agentic engineering / coding / cloud | `ollama pull glm-5.1` | Next-generation GLM model focused on stronger coding and agentic engineering. |
| glm4 | 9B | GLM / Z.ai | General / multilingual | `ollama pull glm4` | Multilingual general language model competitive with Llama 3. |
| glm-ocr | Not specified | GLM / Z.ai | OCR / vision / tools | `ollama pull glm-ocr` | Multimodal OCR model for complex document understanding. |
| goliath | Not specified | Llama | General | `ollama pull goliath` | Model created by combining two fine-tuned Llama 2 70B models. |
| gpt-oss | 20B, 120B | OpenAI | Reasoning / agentic / developer / tools | `ollama pull gpt-oss:20b` | OpenAI open-weight model family for reasoning, agentic tasks, and developer use cases. |
| gpt-oss-safeguard | 20B, 120B | OpenAI | Safety / reasoning / tools | `ollama pull gpt-oss-safeguard` | Safety reasoning model family built on gpt-oss. |
| granite-code | 3B, 8B, 20B, 34B | IBM Granite | Coder | `ollama pull granite-code` | IBM Granite open foundation models for code intelligence. |
| granite-embedding | 30M, 278M | IBM Granite | Embedding | `ollama pull granite-embedding` | IBM Granite dense bi-encoder embedding model family. |
| granite3-dense | 2B, 8B | IBM Granite | Tools / RAG / coding | `ollama pull granite3-dense` | IBM Granite dense models for tool use, RAG, code generation, translation, and bug fixing. |
| granite3-moe | 1B, 3B | IBM Granite | MoE / low latency / tools | `ollama pull granite3-moe` | IBM Granite MoE models designed for low-latency usage. |
| granite3.1-dense | 2B, 8B | IBM Granite | Tools / dense | `ollama pull granite3.1-dense` | IBM Granite dense text-only LLMs trained on large-scale data. |
| granite3.1-moe | 1B, 3B | IBM Granite | MoE / long context / tools | `ollama pull granite3.1-moe` | Long-context Mixture-of-Experts Granite models designed for low latency. |
| granite3.2 | 2B, 8B | IBM Granite | Long context / thinking / tools | `ollama pull granite3.2` | IBM Granite long-context model family fine-tuned for thinking capabilities. |
| granite3.2-vision | 2B | IBM Granite | Vision-language / document understanding / tools | `ollama pull granite3.2-vision` | Compact vision-language model for visual document understanding. |
| granite3.3 | 2B, 8B | IBM Granite | Tools / reasoning | `ollama pull granite3.3` | IBM Granite models with long context and improved reasoning. |
| granite3-guardian | 2B, 8B | IBM Granite | Safety / guardrail | `ollama pull granite3-guardian` | Granite Guardian models for detecting risks in prompts and responses. |
| granite4 | 350M, 1B, 3B | IBM Granite | Enterprise / tools | `ollama pull granite4` | IBM Granite 4 models with improved instruction following and tool calling. |
| granite4.1 | 3B, 8B, 30B | IBM Granite | Enterprise / RAG / tools | `ollama pull granite4.1` | Enterprise-ready Granite models for multilingual, coding, RAG, tool use, and structured JSON. |
| hermes3 | 3B, 8B, 70B, 405B | Nous Research | General / tools | `ollama pull hermes3` | Hermes 3 model family for general instruction and tool-oriented tasks. |
| internlm2 | 1M, 1.8B, 7B, 20B | InternLM | Reasoning / general | `ollama pull internlm2` | InternLM2.5 family for practical scenarios with strong reasoning. |
| kimi-k2 | Not specified | Kimi / Moonshot | MoE / coding agent / cloud | `ollama pull kimi-k2` | Mixture-of-Experts model with improvements on coding-agent tasks. |
| kimi-k2.5 | Not specified | Kimi / Moonshot | Multimodal / agentic / thinking | `ollama pull kimi-k2.5` | Multimodal agentic model integrating vision, language, and agentic capability. |
| kimi-k2.6 | Not specified | Kimi / Moonshot | Multimodal / agentic / coding | `ollama pull kimi-k2.6` | Multimodal agentic model for long-horizon coding and autonomous execution. |
| kimi-k2-thinking | Not specified | Kimi / Moonshot | Thinking / reasoning / cloud | `ollama pull kimi-k2-thinking` | Moonshot AI open-source thinking model. |
| laguna-xs.2 | 33B total, 3B active | Laguna | Agentic coding / MoE | `ollama pull laguna-xs.2` | Mixture-of-Experts model for agentic coding and local long-horizon work. |
| lfm2 | 24B | LFM | Hybrid / on-device / tools | `ollama pull lfm2` | Hybrid model family designed for efficient on-device deployment. |
| lfm2.5-thinking | 1.2B | LFM | Hybrid thinking / on-device / tools | `ollama pull lfm2.5-thinking` | Hybrid thinking model designed for on-device deployment. |
| llama-guard3 | 1B, 8B | Llama | Safety classification | `ollama pull llama-guard3` | Llama Guard 3 models for safety classification of LLM inputs and responses. |
| llama-pro | Not specified | Llama | General / programming / math | `ollama pull llama-pro` | Llama 2 expansion specializing in general language, domain knowledge, programming, and mathematics. |
| llama2 | 7B, 13B, 70B | Llama | General | `ollama pull llama2:7b` | Llama 2 foundation language model family. |
| llama2-chinese | 7B, 13B | Llama | Chinese chat | `ollama pull llama2-chinese` | Llama 2-based model fine-tuned for Chinese dialogue. |
| llama2-uncensored | 7B, 70B | Llama | General chat | `ollama pull llama2-uncensored` | Uncensored Llama 2 model variant. |
| llama3 | 8B, 70B | Llama | General | `ollama pull llama3:8b` | Meta Llama 3 model family. |
| llama3-chatqa | 8B, 70B | Llama / NVIDIA | QA / RAG | `ollama pull llama3-chatqa` | NVIDIA model based on Llama 3 for conversational QA and RAG. |
| llama3-gradient | 8B, 70B | Llama | Long context | `ollama pull llama3-gradient` | Llama 3 variant extending context length to over 1M tokens. |
| llama3-groq-tool-use | 8B, 70B | Llama / Groq | Tool use / function calling | `ollama pull llama3-groq-tool-use` | Groq model family focused on tool use and function calling. |
| llama3.1 | 8B, 70B, 405B | Llama | General / tools | `ollama pull llama3.1:8b` | Meta Llama 3.1 model family. |
| llama3.2 | 1B, 3B | Llama | General / small / tools | `ollama pull llama3.2` | Small Llama 3.2 model family. |
| llama3.2-vision | 11B, 90B | Llama | Vision-language | `ollama pull llama3.2-vision` | Llama 3.2 vision model family for image reasoning and multimodal generation. |
| llama3.3 | 70B | Llama | General / tools | `ollama pull llama3.3` | Llama 3.3 70B model with strong general performance. |
| llama4 | 16x17B, 128x17B | Llama | Multimodal / tools / vision | `ollama pull llama4` | Meta multimodal model family. |
| llava | 7B, 13B, 34B | LLaVA | Vision-language | `ollama pull llava` | Multimodal model combining a vision encoder with a language model. |
| llava-llama3 | 8B | LLaVA / Llama | Vision-language | `ollama pull llava-llama3` | LLaVA model fine-tuned from Llama 3 Instruct. |
| llava-phi3 | 3.8B | LLaVA / Phi | Vision-language | `ollama pull llava-phi3` | Small LLaVA model fine-tuned from Phi-3 Mini. |
| magistral | 24B | Mistral | Reasoning / thinking / tools | `ollama pull magistral` | Small efficient Mistral reasoning model. |
| magicoder | 7B | Magicoder | Coder | `ollama pull magicoder` | Code model trained on synthetic instruction data. |
| marco-o1 | 7B | Alibaba AIDC | Reasoning | `ollama pull marco-o1` | Open reasoning model for real-world solutions. |
| mathstral | 7B | Mistral | Math / scientific reasoning | `ollama pull mathstral` | Mistral model designed for math reasoning and scientific discovery. |
| medgemma | 4B, 27B | Gemma | Medical / vision-language | `ollama pull medgemma` | Gemma variants trained for medical text and image comprehension. |
| medgemma1.5 | 4B | Gemma | Medical / vision-language | `ollama pull medgemma1.5` | Updated MedGemma model for medical text and image comprehension. |
| meditron | 7B, 70B | Llama | Medical | `ollama pull meditron` | Medical LLM adapted from Llama 2 to the medical domain. |
| medllama2 | 7B | Llama | Medical QA | `ollama pull medllama2` | Fine-tuned Llama 2 model for answering medical questions. |
| megadolphin | 120B | Dolphin | General | `ollama pull megadolphin` | Large Dolphin-derived model created by interleaving model weights. |
| minicpm-v | 8B | MiniCPM | Vision-language | `ollama pull minicpm-v` | Multimodal LLM family for vision-language understanding. |
| minimax-m2 | Not specified | MiniMax | Coding / agentic / thinking | `ollama pull minimax-m2` | Efficient model for coding and agentic workflows. |
| minimax-m2.1 | Not specified | MiniMax | Multilingual / coding / tools | `ollama pull minimax-m2.1` | MiniMax model with multilingual and code-engineering capabilities. |
| minimax-m2.5 | Not specified | MiniMax | Productivity / coding / reasoning | `ollama pull minimax-m2.5` | Model for productivity and coding tasks. |
| minimax-m2.7 | Not specified | MiniMax | Coding / agentic / productivity | `ollama pull minimax-m2.7` | MiniMax M2-series model for coding and professional productivity. |
| ministral-3 | 3B, 8B, 14B | Mistral | Edge / tools / vision | `ollama pull ministral-3` | Ministral model family designed for edge deployment. |
| mistral | 7B | Mistral | General / tools | `ollama pull mistral:7b` | Compact Mistral 7B model for local general-purpose inference. |
| mistral-large | 123B | Mistral | Large / coding / reasoning / tools | `ollama pull mistral-large` | Mistral flagship model for coding, mathematics, reasoning, and multilingual tasks. |
| mistral-large-3 | Not specified | Mistral | Multimodal / enterprise / cloud | `ollama pull mistral-large-3` | General-purpose multimodal MoE model for production-grade tasks. |
| mistral-medium-3.5 | 128B | Mistral | Reasoning / coding / multimodal | `ollama pull mistral-medium-3.5` | Flagship Mistral model combining instruction following, reasoning, and coding. |
| mistral-nemo | 12B | Mistral | General / long context / tools | `ollama pull mistral-nemo` | Mistral-Nemo model with long-context capability. |
| mistral-openorca | 7B | Mistral | General | `ollama pull mistral-openorca` | Mistral 7B fine-tuned on OpenOrca data. |
| mistral-small | 22B, 24B | Mistral | General / tools | `ollama pull mistral-small` | Mistral Small model family below 70B. |
| mistral-small3.1 | 24B | Mistral | Vision / long context / tools | `ollama pull mistral-small3.1` | Mistral Small update with vision understanding and long context. |
| mistral-small3.2 | 24B | Mistral | General / tools / vision | `ollama pull mistral-small3.2` | Mistral Small update improving function calling and instruction following. |
| mistrallite | 7B | Mistral | Long context | `ollama pull mistrallite` | Fine-tuned Mistral model with enhanced long-context capability. |
| mixtral | 8x7B, 8x22B | Mistral | MoE / tools | `ollama pull mixtral` | Open-weight Mixture-of-Experts model family from Mistral AI. |
| moondream | 1.8B | Moondream | Vision-language / edge | `ollama pull moondream` | Small vision-language model designed for efficient edge use. |
| mxbai-embed-large | 335M | Mixedbread | Embedding | `ollama pull mxbai-embed-large` | Large embedding model from mixedbread.ai. |
| nemotron | 70B | NVIDIA | General / tools | `ollama pull nemotron` | NVIDIA-customized Llama 3.1 Nemotron model for helpfulness. |
| nemotron-3-nano | 4B, 30B | NVIDIA | Agentic / reasoning / tools | `ollama pull nemotron-3-nano` | Efficient Nemotron model for open, intelligent, agentic workflows. |
| nemotron-3-super | 120B | NVIDIA | MoE / reasoning / agentic | `ollama pull nemotron-3-super` | NVIDIA MoE model with 12B active parameters for multi-agent applications. |
| nemotron-cascade-2 | 30B total, 3B active | NVIDIA | MoE / reasoning / agentic | `ollama pull nemotron-cascade-2` | NVIDIA MoE model with strong reasoning and agentic capability. |
| nemotron-mini | 4B | NVIDIA | Roleplay / RAG / function calling | `ollama pull nemotron-mini` | Small commercial-friendly NVIDIA model. |
| nemotron3 | 33B | NVIDIA | Multimodal / enterprise / tools | `ollama pull nemotron3` | Multimodal model supporting video, audio, image, text, Q&A, summarization, and document intelligence. |
| neural-chat | 7B | Intel / Mistral | Chat | `ollama pull neural-chat` | Mistral-based fine-tuned model for chat and general domains. |
| nexusraven | 13B | Nexus Raven | Function calling | `ollama pull nexusraven` | Instruction-tuned model for function-calling tasks. |
| nomic-embed-text | Not specified | Nomic | Embedding | `ollama pull nomic-embed-text` | High-performing open embedding model with a large context window. |
| nomic-embed-text-v2-moe | Not specified | Nomic | Embedding / MoE / multilingual | `ollama pull nomic-embed-text-v2-moe` | Multilingual MoE text embedding model for retrieval. |
| notus | 7B | Notus / Zephyr | Chat | `ollama pull notus` | Chat model fine-tuned with high-quality data and based on Zephyr. |
| notux | 8x7B | Notux | MoE / general | `ollama pull notux` | Mixture-of-Experts model fine-tuned with high-quality data. |
| nous-hermes | 7B, 13B | Nous Research | General | `ollama pull nous-hermes` | General-use models based on Llama and Llama 2. |
| nous-hermes2 | 10.7B, 34B | Nous Research | General / coding | `ollama pull nous-hermes2` | Model family for scientific discussion and coding tasks. |
| nous-hermes2-mixtral | 8x7B | Nous Research / Mixtral | MoE / general | `ollama pull nous-hermes2-mixtral` | Nous Hermes 2 model trained over Mixtral. |
| nuextract | 3.8B | NuExtract / Phi | Information extraction | `ollama pull nuextract` | Information-extraction model based on Phi-3. |
| olmo-3 | 7B, 32B | OLMo | Open research / general | `ollama pull olmo-3` | Open language model family designed to support language-model science. |
| olmo-3.1 | 32B | OLMo | Open research / tools | `ollama pull olmo-3.1` | OLMo model family post-trained on open datasets. |
| olmo2 | 7B, 13B | OLMo | General / open research | `ollama pull olmo2` | OLMo 2 model family trained on large-scale tokens. |
| open-orca-platypus2 | 13B | OpenOrca / Platypus | Chat / code | `ollama pull open-orca-platypus2` | Merged model designed for chat and code generation. |
| openchat | 7B | OpenChat | General chat | `ollama pull openchat` | Open-source chat model family trained on varied data. |
| opencoder | 1.5B, 8B | OpenCoder | Coder / bilingual | `ollama pull opencoder` | Reproducible code LLM family supporting English and Chinese chat. |
| openhermes | Not specified | OpenHermes | General | `ollama pull openhermes` | OpenHermes 2.5 model fine-tuned on open datasets. |
| openthinker | 7B, 32B | OpenThinker | Reasoning | `ollama pull openthinker` | Open-source reasoning model family distilled from DeepSeek-R1-style data. |
| orca-mini | 3B, 7B, 13B, 70B | Orca | General / entry-level hardware | `ollama pull orca-mini:7b` | General-purpose model family suitable for entry-level hardware. |
| orca2 | 7B, 13B | Orca / Llama | Reasoning | `ollama pull orca2` | Microsoft research model fine-tuned from Llama 2 for reasoning. |
| paraphrase-multilingual | 278M | Sentence Transformers | Embedding / semantic search | `ollama pull paraphrase-multilingual` | Sentence-transformer model for clustering and semantic search. |
| phi | 2.7B | Phi | Lightweight / reasoning | `ollama pull phi` | Microsoft Phi-2 model with reasoning and language understanding capabilities. |
| phi3 | 3.8B, 14B | Phi | Lightweight / reasoning | `ollama pull phi3` | Microsoft Phi-3 lightweight open model family. |
| phi3.5 | 3.8B | Phi | Lightweight / reasoning | `ollama pull phi3.5` | Lightweight Phi model with strong performance for its size. |
| phi4 | 14B | Phi | Reasoning / general | `ollama pull phi4` | Microsoft Phi-4 14B open model for reasoning and general tasks. |
| phi4-mini | 3.8B | Phi | Lightweight / reasoning / tools | `ollama pull phi4-mini` | Small Phi-4 model with multilingual support, reasoning, mathematics, and function calling. |
| phi4-mini-reasoning | 3.8B | Phi | Lightweight / reasoning | `ollama pull phi4-mini-reasoning` | Lightweight Phi-4 model balancing efficiency with advanced reasoning. |
| phi4-reasoning | 14B | Phi | Reasoning | `ollama pull phi4-reasoning` | Phi-4 reasoning model family for complex reasoning tasks. |
| phind-codellama | 34B | Phind / CodeLlama | Coder | `ollama pull phind-codellama` | Code generation model based on Code Llama. |
| qwen | 0.5B, 1.8B, 4B, 7B, 14B, 32B, 72B, 110B | Qwen | General / multilingual | `ollama pull qwen:7b` | Alibaba Cloud transformer-based model family. |
| qwen2 | 0.5B, 1.5B, 7B, 72B | Qwen | General / tools | `ollama pull qwen2` | Qwen 2 model family from Alibaba. |
| qwen2-math | 1.5B, 7B, 72B | Qwen | Math | `ollama pull qwen2-math` | Qwen2 specialized math model family. |
| qwen2.5 | 0.5B, 1.5B, 3B, 7B, 14B, 32B, 72B | Qwen | General / multilingual / tools | `ollama pull qwen2.5:7b` | Qwen2.5 model family supporting long context and multilingual use cases. |
| qwen2.5-coder | 0.5B, 1.5B, 3B, 7B, 14B, 32B | Qwen | Coder / tools | `ollama pull qwen2.5-coder` | Code-specific Qwen model family for code generation, code reasoning, and code fixing. |
| qwen2.5vl | 3B, 7B, 32B, 72B | Qwen | Vision-language | `ollama pull qwen2.5vl` | Flagship Qwen vision-language model family. |
| qwen3 | 0.6B, 1.7B, 4B, 8B, 14B, 30B, 32B, 235B | Qwen | General / thinking / MoE / tools | `ollama pull qwen3:14b` | Qwen 3 model family including dense and mixture-of-experts models. |
| qwen3-coder | 30B, 480B | Qwen | Coder / agentic / tools | `ollama pull qwen3-coder` | Long-context Qwen model family for agentic and coding tasks. |
| qwen3-coder-next | Not specified | Qwen | Coder / agentic / tools | `ollama pull qwen3-coder-next` | Coding-focused Qwen model optimized for agentic local development workflows. |
| qwen3-embedding | 0.6B, 4B, 8B | Qwen | Embedding | `ollama pull qwen3-embedding` | Qwen3-based text embedding model family. |
| qwen3-next | 80B | Qwen | Thinking / tools / cloud | `ollama pull qwen3-next` | Qwen3-Next model focused on parameter efficiency and inference speed. |
| qwen3-vl | 2B, 4B, 8B, 30B, 32B, 235B | Qwen | Vision-language / thinking / tools | `ollama pull qwen3-vl` | Vision-language Qwen model family for multimodal reasoning. |
| qwen3.5 | 0.8B, 2B, 4B, 9B, 27B, 35B, 122B | Qwen | Multimodal / thinking / tools | `ollama pull qwen3.5` | Open-source multimodal Qwen family with text, tools, reasoning, and vision support. |
| qwen3.6 | 27B, 35B | Qwen | Agentic coding / thinking / vision | `ollama pull qwen3.6` | Qwen family with upgrades for coding, thinking preservation, and multimodal use. |
| qwq | 32B | Qwen | Reasoning / tools | `ollama pull qwq` | Qwen reasoning model. |
| r1-1776 | 70B, 671B | Perplexity / DeepSeek | Reasoning / factuality | `ollama pull r1-1776` | Post-trained DeepSeek-R1 variant focused on unbiased and factual information. |
| reader-lm | 0.5B, 1.5B | ReaderLM | HTML-to-Markdown | `ollama pull reader-lm` | Model family for converting HTML content to Markdown. |
| reflection | 70B | Reflection | Reasoning correction | `ollama pull reflection` | Model trained with Reflection-tuning to detect and correct reasoning mistakes. |
| rnj-1 | 8B | Essential AI | Code / STEM / tools | `ollama pull rnj-1` | Dense open-weight model optimized for code and STEM tasks. |
| sailor2 | 1B, 8B, 20B | Sailor | Multilingual / Southeast Asia | `ollama pull sailor2` | Multilingual model family for Southeast Asian languages. |
| samantha-mistral | 7B | Samantha / Mistral | Companion assistant | `ollama pull samantha-mistral` | Companion assistant trained in philosophy, psychology, and personal relationships. |
| shieldgemma | 2B, 9B, 27B | Gemma | Safety / guardrail | `ollama pull shieldgemma` | Gemma-based safety evaluation model family. |
| smallthinker | 3B | Qwen-derived | Small reasoning | `ollama pull smallthinker` | Small reasoning model fine-tuned from Qwen 2.5 3B Instruct. |
| smollm | 135M, 360M, 1.7B | SmolLM | Small / general | `ollama pull smollm` | Small model family trained on high-quality datasets. |
| smollm2 | 135M, 360M, 1.7B | SmolLM | Small / general / tools | `ollama pull smollm2` | Compact language model family. |
| snowflake-arctic-embed | 22M, 33M, 110M, 137M, 335M | Snowflake | Embedding | `ollama pull snowflake-arctic-embed` | Snowflake embedding model suite optimized for performance. |
| snowflake-arctic-embed2 | 568M | Snowflake | Embedding / multilingual | `ollama pull snowflake-arctic-embed2` | Multilingual Snowflake embedding model. |
| solar | 10.7B | Upstage Solar | General chat | `ollama pull solar` | Compact single-turn conversation model. |
| solar-pro | 22B | Upstage Solar | General | `ollama pull solar-pro` | Solar Pro preview model designed to fit into a single GPU. |
| sqlcoder | 7B, 15B | SQLCoder | SQL / coder | `ollama pull sqlcoder` | Model fine-tuned for SQL generation. |
| stable-beluga | 7B, 13B, 70B | Stable Beluga / Llama | General chat | `ollama pull stable-beluga` | Llama 2-based model fine-tuned on Orca-style data. |
| stable-code | 3B | Stability AI | Coder | `ollama pull stable-code` | Compact coding model for code completion and instruction use. |
| stablelm-zephyr | 3B | Stability AI / Zephyr | Lightweight chat | `ollama pull stablelm-zephyr` | Lightweight chat model for accurate and responsive output. |
| stablelm2 | 1.6B, 12B | Stability AI | General / multilingual | `ollama pull stablelm2` | Multilingual language model family. |
| starcoder | 1B, 3B, 7B, 15B | BigCode | Coder | `ollama pull starcoder` | Code generation model trained on many programming languages. |
| starcoder2 | 3B, 7B, 15B | BigCode | Coder | `ollama pull starcoder2` | Next-generation openly trained code LLM family. |
| starling-lm | 7B | Starling | Chat / RLHF-style | `ollama pull starling-lm` | Chat model trained by reinforcement learning from AI feedback. |
| tinydolphin | 1.1B | Dolphin / TinyLlama | Small / experimental | `ollama pull tinydolphin` | Experimental Dolphin model based on TinyLlama. |
| tinyllama | 1.1B | TinyLlama | Small / general | `ollama pull tinyllama` | Compact Llama-style model trained on large-scale text. |
| translategemma | 4B, 12B, 27B | Gemma | Translation / vision | `ollama pull translategemma` | Gemma-based translation model collection supporting many languages. |
| tulu3 | 8B, 70B | Allen AI | Instruction following | `ollama pull tulu3` | Open-source instruction-following model family. |
| vicuna | 7B, 13B, 33B | Vicuna | Chat | `ollama pull vicuna` | General chat model based on Llama and Llama 2. |
| wizard-math | 7B, 13B, 70B | Wizard | Math / logic | `ollama pull wizard-math` | Model focused on math and logic problems. |
| wizard-vicuna | 13B | Wizard / Vicuna | Chat | `ollama pull wizard-vicuna` | Vicuna-based model trained by MelodysDreamj. |
| wizard-vicuna-uncensored | 7B, 13B, 30B | Wizard / Vicuna | General chat | `ollama pull wizard-vicuna-uncensored` | Uncensored Vicuna-based model family. |
| wizardcoder | 33B | WizardCoder | Coder | `ollama pull wizardcoder` | Code generation model family. |
| wizardlm | Not specified | WizardLM | General | `ollama pull wizardlm` | General-use model based on Llama 2. |
| wizardlm-uncensored | 13B | WizardLM | General chat | `ollama pull wizardlm-uncensored` | Uncensored WizardLM variant. |
| wizardlm2 | 7B, 8x22B | WizardLM | General / multilingual / reasoning | `ollama pull wizardlm2` | Microsoft AI model family for complex chat, multilingual reasoning, and agent use cases. |
| xwinlm | 7B, 13B | Xwin-LM | Conversational | `ollama pull xwinlm` | Conversational model based on Llama 2. |
| yarn-llama2 | 7B, 13B | Llama | Long context | `ollama pull yarn-llama2` | Llama 2 extension supporting up to 128K context. |
| yarn-mistral | 7B | Mistral | Long context | `ollama pull yarn-mistral` | Mistral extension supporting 64K or 128K context windows. |
| yi | 6B, 9B, 34B | Yi | Bilingual / general | `ollama pull yi` | High-performing bilingual language model family. |
| yi-coder | 1.5B, 9B | Yi | Coder | `ollama pull yi-coder` | Code language model family with fewer than 10B parameters. |
| zephyr | 7B, 141B | Hugging Face / Mistral | Assistant / chat | `ollama pull zephyr` | Fine-tuned assistant model family based on Mistral and Mixtral. |
