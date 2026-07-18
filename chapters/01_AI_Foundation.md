# Chapter 1 — AI Foundations for Product Builders

## Chapter purpose

Artificial intelligence is often introduced through spectacular demonstrations: a system writes an essay, creates an image, answers a technical question, or produces working code. Demonstrations are useful because they make an unfamiliar technology visible. They are also incomplete. A successful demonstration does not tell us whether the same system will perform reliably for different users, under different conditions, with private data, at acceptable cost, or in a setting where a wrong answer can cause harm.

For a product builder, the central question is therefore not simply, “What can AI generate?” The more important question is, “What kind of system are we building, for whom, under which conditions, and how will we know that it works?” This chapter develops the conceptual foundation needed to answer that question. It treats AI as a component within a larger human and technical system rather than as an independent source of intelligence.

The discussion is designed for readers without a programming background. Mathematical notation is used sparingly and only where it clarifies an important mechanism. The objective is not to train a machine-learning researcher. It is to help a product builder reason accurately about capabilities, evidence, failure, responsibility, and design.

## Learning objectives

After completing this chapter, you should be able to:

1. distinguish artificial intelligence, machine learning, deep learning, and generative AI;
2. describe how data, models, instructions, tools, interfaces, and human decisions form an AI system;
3. explain, at a conceptual level, how a modern language model is trained and how it generates text;
4. distinguish model fluency from factual accuracy and task reliability;
5. identify common sources of error, bias, privacy risk, and security risk;
6. classify a proposed use case by consequence and determine an appropriate level of human oversight;
7. formulate an AI product opportunity as a measurable problem rather than as a feature idea; and
8. design a basic evaluation plan that includes quality, safety, cost, and user outcomes.

## Key terms

**Artificial intelligence (AI):** a broad category of machine-based systems that infer how to produce outputs—such as predictions, content, recommendations, or decisions—from inputs and objectives.

**Algorithm:** a defined procedure for transforming an input into an output.

**Machine learning (ML):** a family of methods in which a model’s behavior is learned from data rather than specified entirely through hand-written rules.

**Model:** a computational representation that maps inputs to outputs using parameters, rules, or both.

**Parameter:** an internal numerical value adjusted during model training.

**Training:** the process of adjusting a model so that its outputs better match an objective on training data.

**Inference:** the use of a trained model to produce an output for a new input.

**Generative AI:** AI designed to produce new content, such as text, images, audio, video, or code.

**Foundation model:** a model trained on broad data at scale that can be adapted to many downstream tasks.

**Large language model (LLM):** a language model with substantial capacity, commonly trained on large text collections to predict and generate token sequences.

**Token:** a unit of text processed by a language model; it may be a word, part of a word, punctuation, or another symbol.

**Prompt:** the input and instructions supplied to a generative model at inference time.

**Context window:** the amount of information a model can consider in a single interaction, measured in tokens.

**Grounding:** connecting a model’s response to designated sources, data, or tool results.

**Evaluation:** the systematic measurement of whether a system meets defined requirements.

**Human oversight:** meaningful human review, intervention, or decision authority appropriate to the consequences of system behavior.

## 1.1 What counts as artificial intelligence?

There is no single definition of AI that resolves every scientific, commercial, and legal question. The boundary changes as techniques become common. Optical character recognition, for example, was once presented as a striking form of AI; today it is often treated as an ordinary software capability. This changing boundary is sometimes called the **AI effect**: once a capability becomes familiar, people are less likely to describe it as intelligence.

For practical product work, it is more useful to define an **AI system** than to debate whether a machine is genuinely intelligent. The Organisation for Economic Co-operation and Development (OECD) defines an AI system in terms of a machine-based system that infers, from inputs and objectives, how to produce outputs that can influence physical or virtual environments. The outputs may include predictions, content, recommendations, or decisions, and systems vary in autonomy and adaptability [1].

This definition emphasizes four properties:

1. **The system receives inputs.** Inputs may include text, images, sensor readings, database records, or user behavior.
2. **The system operates with objectives.** An objective may be explicit, such as predicting equipment failure, or implicit in training and product design, such as encouraging engagement.
3. **The system infers an output.** It does not merely retrieve a fixed response from a table; it applies learned or encoded relationships.
4. **The output affects an environment.** It may change what a person sees, influence a decision, generate content, or activate a machine.

This systems view prevents a common conceptual error: equating AI with a chat interface. A chatbot is one possible interface. The complete system may also include a model provider, a document store, retrieval software, safety filters, user authentication, analytics, human reviewers, organizational policies, and downstream actions. Product quality depends on all of these elements.

### AI and conventional software

Conventional software and AI overlap. Many useful products combine both.

In conventional rule-based software, a developer attempts to specify the relevant behavior directly. A tax calculator might contain explicit rules for tax brackets. Given the same valid inputs and software version, the calculation should be reproducible. If a rule changes, a developer updates it.

In machine learning, developers specify an objective and a learning procedure, then use data to estimate a model. A spam filter may learn statistical patterns that distinguish unwanted messages from legitimate ones. The developer does not write a complete list of every phrase that could occur in spam. Instead, the model estimates relationships from examples.

The distinction is not “old software versus new software,” nor “simple versus intelligent.” It concerns where behavior is specified. Rule-based systems place more behavior in explicit logic. Learned systems place more behavior in parameters estimated from data. A mature product often uses explicit rules for stable requirements and learned models for ambiguous patterns.

Consider an invoice-processing product:

- conventional software verifies that required fields exist and totals are mathematically consistent;
- optical character recognition extracts text from scanned pages;
- a machine-learning classifier identifies document type;
- a language model converts irregular descriptions into structured categories;
- a rules engine blocks payments above an authorization threshold; and
- a human approves exceptions.

No single component defines the product. Reliability emerges from how the components divide responsibility.

## 1.2 A brief intellectual history

The desire to create artifacts that imitate reasoning predates electronic computing. Modern AI, however, developed through several overlapping research traditions.

### Symbolic AI

Early AI research often represented knowledge through symbols and explicit rules. A system might encode statements such as “all approved suppliers have a supplier ID” and apply logical operations to reach conclusions. Symbolic methods can be interpretable because a developer can inspect rules and reasoning paths. They work well when the domain can be expressed clearly and when exceptions are manageable.

Their limitation is the difficulty of representing the complexity and ambiguity of real environments. Everyday language, visual perception, and social situations contain vast numbers of exceptions. Knowledge acquisition becomes expensive, and hand-written rules may become brittle.

### Statistical machine learning

Statistical approaches learn patterns from examples. Instead of defining every visual feature of a cat, developers provide labeled images and optimize a model to distinguish cats from other classes. Instead of specifying every suspicious phrase in a message, a model estimates which patterns are associated with spam.

This transition changed the product builder’s work. Data selection, measurement, and evaluation became as important as code. A system could perform well on average while failing for particular populations or uncommon conditions. The quality of a learned model depended not only on the algorithm but also on how the problem was framed and how examples were collected.

### Neural networks and deep learning

A neural network is a computational structure composed of layers of numerical transformations. The term is inspired loosely by biological neurons, but an artificial neural network should not be mistaken for a simulation of a human brain. Its units perform mathematical operations; its capabilities arise from optimized parameters and architecture.

**Deep learning** refers to neural networks with multiple learned layers. As data, specialized computing hardware, and training methods improved, deep learning produced major advances in speech recognition, computer vision, translation, and language modeling. The key practical advantage was representation learning: instead of relying entirely on human-designed features, a network could learn useful internal representations from data.

### Foundation models and generative AI

A foundation model is trained broadly and then adapted or instructed for many tasks. This differs from a narrow model designed for a single fixed prediction. A language foundation model may support summarization, classification, translation, extraction, question answering, and drafting through changes in instructions, examples, external knowledge, or additional training.

The phrase “foundation model” is important because it shifts attention from a single application to a reusable base. The base model is not the finished product. It is a foundation on which different systems can be built. Each downstream system inherits capabilities and risks from the model while adding new behavior through prompts, data, tools, and interface design.

Generative AI became widely visible because its outputs are directly perceptible. A prediction score is abstract; a paragraph or image can be judged immediately. Yet visibility should not be confused with understanding. Generative systems produce plausible artifacts through learned statistical structure. They do not automatically possess verified knowledge, intention, or accountability.

## 1.3 The anatomy of an AI product

An AI product is best understood as a layered sociotechnical system. **Sociotechnical** means that performance depends on both technical components and human or organizational conditions.

### Layer 1: user need and task

Every product begins with a situation in which someone is trying to achieve an outcome. “Use AI” is not an outcome. “Reduce the time required to turn an approved meeting transcript into a reviewable action list” is closer to a product problem because it identifies a user, an input, a transformation, and a result.

A task definition should answer:

- Who performs the task?
- What starts the task?
- What output is required?
- What makes the output acceptable?
- What happens if the output is wrong?
- Who is responsible for the final decision?

### Layer 2: experience and interface

The interface determines how users express intent, inspect results, correct errors, and understand system status. A technically capable model can produce a poor product if users cannot tell what data it used or cannot revise an output. Conversely, a carefully constrained interface can make a modest model useful.

Important interface elements include input guidance, examples, progress indicators, citations, confidence cues, editable output, undo or recovery, and a clear route to human help. The interface should reveal consequential uncertainty instead of hiding it behind fluent language.

### Layer 3: application logic

Application logic coordinates the workflow. It validates inputs, chooses prompts, calls models or tools, applies business rules, stores state, handles errors, and determines what the user can do next. This layer is where a prototype often becomes a product.

For example, an AI-assisted customer-support tool may:

1. retrieve the customer’s authorized account information;
2. search an approved knowledge base;
3. ask a language model to draft a response grounded in retrieved sources;
4. scan the draft for prohibited disclosures;
5. present the draft and sources to an employee; and
6. record whether the employee accepted or corrected it.

The language model performs only one step.

### Layer 4: model

The model transforms input into output. Model selection involves trade-offs among quality, latency, cost, privacy, context capacity, modality, availability, and controllability. A larger or newer model is not automatically the correct choice. If a smaller model meets requirements with lower cost and faster response, it may be the better product decision.

### Layer 5: data and knowledge

AI behavior depends on data at several stages:

- **training data** influences the base model;
- **adaptation data** may be used for fine-tuning or configuration;
- **retrieved knowledge** supplies information at inference time;
- **user input** provides task-specific context; and
- **evaluation data** tests system behavior.

These data sources have different ownership, quality, retention, and consent requirements. Treating them as one undifferentiated pool creates privacy and governance risk.

### Layer 6: tools and actions

A model may be connected to search, calculators, databases, email, calendars, code execution, or business systems. Tool access expands usefulness because the system can obtain current facts and perform actions. It also expands risk. A model that drafts an email is different from one that sends it; a model that recommends a refund is different from one authorized to issue it.

Product builders should separate **generation authority** from **action authority**. The ability to propose an action does not imply permission to execute it.

### Layer 7: governance and operations

Governance includes policies, ownership, monitoring, incident handling, access control, documentation, and review. Operations include availability, vendor management, cost control, logging, and support. These layers are not administrative decorations. They determine whether a useful prototype remains safe and reliable after deployment.

## 1.4 How machine learning learns from data

The mechanics of machine learning can be described through a simple supervised-learning example. Suppose a business wants to predict whether a support ticket requires urgent attention.

### Examples, labels, and features

Historical tickets provide **examples**. Each example contains input information and a target **label**, such as urgent or non-urgent. A **feature** is a measurable property used by the model. In traditional machine learning, people may design features explicitly, such as message length, presence of particular terms, customer tier, or number of previous incidents. In deep learning, the model may learn useful representations from raw text.

The dataset is commonly divided into:

- a **training set**, used to adjust the model;
- a **validation set**, used to compare designs and tune settings; and
- a **test set**, reserved for a final estimate of performance on unseen examples.

This separation matters. Measuring a model only on examples it has already seen is like allowing a student to take an examination with the answer sheet. Memorization may look like learning.

### Objective and loss

Training requires an objective. A **loss function** measures how far the model’s prediction is from the desired result. In simplified notation, training seeks parameters \(\theta\) that minimize average loss across examples:

\[
\theta^* = \arg\min_{\theta} \frac{1}{n}\sum_{i=1}^{n} L(f_{\theta}(x_i), y_i)
\]

Here, \(x_i\) is an input, \(y_i\) is the correct label, \(f_{\theta}\) is the model, and \(L\) is the loss function. You do not need to calculate this equation to build an AI product. You should understand its implication: a model is optimized for a measurable proxy, not for every human value associated with the task.

If the label “urgent” reflects inconsistent historical decisions, the model learns those inconsistencies. If the training objective rewards overall accuracy, the model may neglect a small but important category. If missing an urgent ticket is more harmful than incorrectly escalating a routine ticket, product evaluation must reflect that asymmetry.

### Generalization and overfitting

**Generalization** is the ability to perform well on relevant examples not encountered during training. **Overfitting** occurs when a model fits training data so closely that it performs poorly on new data.

A product builder should therefore ask whether evaluation examples represent actual use. A model tested on clean, short, English-language tickets may fail when deployed on long messages, mixed languages, screenshots, sarcasm, or newly introduced products. The issue is not simply model quality. It is a mismatch between evaluation conditions and operational reality.

### Correlation is not causation

Machine-learning models often exploit correlation. If urgent tickets historically contain the word “manager,” a model may use that pattern. The relationship does not prove that mentioning a manager causes urgency. When the surrounding process changes, the correlation may disappear.

This distinction matters when AI supports decisions. A predictive model may identify people who are statistically associated with an outcome without explaining why the outcome occurs or what intervention will improve it. Product claims should match the evidence. Prediction, explanation, and causal intervention are different tasks.

## 1.5 How large language models generate text

Large language models are central to many contemporary AI products. Their apparent conversational ability can make their operation seem mysterious. At a conceptual level, however, text generation can be explained as repeated probabilistic prediction.

### Tokenization

Before text enters a language model, it is converted into tokens. A token may represent a common word, part of a word, punctuation, whitespace pattern, or symbol. The sentence “AI helps builders” is therefore processed as a sequence of numerical token identifiers, not as an indivisible thought.

Tokenization has practical consequences. Context limits and usage costs may be calculated in tokens rather than words. Uncommon names, code, or some languages may require more tokens than familiar English text. A product that accepts documents must manage token limits instead of assuming every page has equal computational size.

### Pretraining through prediction

A common language-model objective is to predict the next token given preceding tokens. If a training sequence contains “The capital of Thailand is Bangkok,” the model is optimized to assign a higher probability to the token representing “Bangkok” after the preceding context.

In simplified form:

\[
P(t_1, t_2, \ldots, t_m) = \prod_{k=1}^{m} P(t_k \mid t_1, \ldots, t_{k-1})
\]

This equation states that the probability of a sequence can be represented as a product of conditional next-token probabilities. Training across enormous and diverse collections allows a model to learn regularities involving grammar, style, facts, code patterns, argument structure, and associations among concepts.

The objective remains prediction. The model is not given a separate internal database in which every sentence is stored as a verified proposition. Some knowledge is encoded diffusely in parameters. Consequently, generation can reproduce accurate patterns, combine patterns productively, or produce a fluent but unsupported continuation.

### The Transformer and attention

The Transformer architecture, introduced in the paper “Attention Is All You Need,” replaced recurrent processing in the original design with attention-based mechanisms that supported greater parallelization during training [2]. Modern language models have evolved substantially, but the Transformer remains a foundational concept.

**Attention** allows the model to compute how strongly different token representations should relate to one another for a particular transformation. In the sentence “The designer placed the laptop in the bag because it was protective,” the model can use contextual relationships to interpret what “it” most likely refers to. Attention does not create human awareness. It is a learned numerical mechanism for combining information across positions.

A Transformer contains repeated blocks that typically include attention and feed-forward transformations. Through training, layers develop representations useful for predicting subsequent tokens. Earlier and later layers may capture different patterns, but these representations are not a human-readable chain of propositions.

### From a base model to an assistant

A model trained only for next-token prediction may not reliably follow user instructions or avoid unsafe content. Providers therefore apply additional stages, which can include supervised instruction training, preference-based optimization, safety training, system instructions, and runtime filters.

The final assistant behavior is thus produced by several influences:

- the architecture;
- pretraining data and objective;
- post-training examples and feedback;
- system-level instructions;
- the user’s prompt and conversation context;
- retrieved information and tool outputs; and
- generation settings and safety controls.

This explains why two products using the same base model can behave differently, and why a model update can change an application even when the application code remains unchanged.

### Sampling and variability

At generation time, the model assigns probabilities to possible next tokens. A decoding procedure selects one token, appends it to the sequence, and repeats the process.

If the system always selects the highest-probability token, output may be more repeatable but can become rigid. Sampling from several likely tokens can produce diverse output. A setting commonly called **temperature** changes the shape of the probability distribution: higher values generally increase variation; lower values generally concentrate probability on more likely tokens.

Temperature is not a truth control. Reducing it may make output more consistent, but it does not verify facts. Likewise, increasing it may support creative variation but does not create genuine creativity in the human sense. It changes selection behavior within the model’s learned distribution.

### Context is not permanent memory

Information in the context window can influence the current response. This is different from permanent learning. If you paste a policy into a conversation, the model may use that policy for the interaction; the base model’s parameters have not necessarily been retrained.

Products use several mechanisms that are often loosely described as “memory”:

- conversation history included in the current prompt;
- saved user preferences inserted into later prompts;
- records stored in an application database;
- retrieved documents supplied for a particular question; and
- updated model parameters produced through training.

These mechanisms have different privacy and reliability properties. A product specification should state which one is intended.

## 1.6 What generative AI does well

Capabilities should be described in relation to tasks and conditions, not as universal traits. A language model may perform strongly at summarizing a clearly written document and poorly at summarizing a corrupted scan. It may classify familiar requests accurately and fail on a new product category.

### Transformation

Generative models are often useful when an input must be transformed while preserving meaning. Examples include rewriting text for a different audience, converting notes into a structured draft, translating language, extracting fields, or changing content format.

Transformation tasks can be easier to evaluate than open-ended creation because the source provides a reference. A reviewer can ask whether the output preserved required facts and omitted unsupported additions.

### Classification and extraction

Although language models generate text, they can also assign categories or extract structured information. A model might classify feedback by topic or convert a product description into fields such as audience, problem, and constraints.

These tasks benefit from precise category definitions and examples. If categories overlap, the model will reflect that ambiguity. Structured output validation should be handled by application logic rather than assumed from a prompt alone.

### Drafting and variation

Models can produce candidate text quickly. The correct product interpretation is often “first-draft acceleration,” not “automatic authorship.” A draft can reduce the cost of starting, offer alternatives, or reveal missing requirements. Human review remains necessary when accuracy, voice, legal rights, or social consequences matter.

### Synthesis across supplied material

When provided with relevant sources, a model can compare themes, identify contradictions, and organize information. Grounding improves the relationship between an answer and designated evidence, but it does not guarantee faithful interpretation. Source quality, retrieval quality, and citation verification remain necessary.

### Interaction with tools

Language can serve as a flexible control layer for calculators, search, databases, and software. A model can translate an ordinary-language request into a proposed tool call. The tool, rather than the model, should perform operations that require exactness, such as arithmetic, data retrieval, or transaction execution.

This division of labor is powerful: the model interprets ambiguous intent, while deterministic systems execute constrained actions. It is safe only when permissions, input validation, confirmation, and error handling are designed explicitly.

## 1.7 What generative AI does not guarantee

### Fluency does not imply truth

Language models are optimized to produce probable continuations, and post-training encourages useful responses. Neither mechanism independently verifies every claim. A response can be grammatical, detailed, and false. This phenomenon is often called a **hallucination**, although terms such as fabrication, confabulation, or ungrounded generation may be more precise in a product specification.

Hallucination is not limited to obscure questions. A model may invent a citation, misstate a date, combine two people, or describe a nonexistent product feature. The risk increases when the prompt demands an answer despite insufficient evidence.

Controls include:

- providing authoritative sources;
- requiring citations that can be inspected;
- allowing the system to state that evidence is insufficient;
- using tools for current or exact information;
- applying deterministic validation where possible; and
- requiring human approval for consequential claims.

No single control eliminates the risk.

### Reasoning traces are not proof

A model may produce a step-by-step explanation that appears logical. The explanation is itself generated text. It may contain an error or may not faithfully represent the internal process that produced the answer. Product evaluation should focus on verifiable outputs, intermediate artifacts that can be checked, and external evidence—not on eloquence alone.

### Confidence language is not calibrated probability

Phrases such as “I am certain” or “this is definitely correct” should not be interpreted as measured confidence unless the system has been specifically designed and validated to provide calibrated probabilities. Conversational confidence is a style feature. A careful product avoids presenting it as evidence.

### Current knowledge is not automatic

A model’s parameters reflect training and update processes that occurred before use. Even when a product offers web search or database access, the model must retrieve the right source, interpret it correctly, and distinguish publication date from event date. Current information requires current retrieval and verification.

### Context capacity is not perfect recall

A large context window does not guarantee that every detail will be used correctly. Relevant information can be overlooked, confused, or outweighed by conflicting instructions. Long documents may require segmentation, retrieval, summarization, and targeted evaluation.

### General capability is not domain authority

A model can discuss medicine, law, finance, engineering, and education because it has learned linguistic patterns from broad data. This does not make it a licensed professional, a responsible decision maker, or an authoritative source. High-stakes uses require domain-specific controls, qualified human oversight, and compliance with applicable law and policy.

## 1.8 Sources of system failure

Failure analysis should move beyond the statement “the AI made a mistake.” That statement is too broad to guide improvement.

### Problem-framing failure

The product may solve the wrong problem. Automating a slow approval step will not help if the actual delay is caused by missing information upstream. A chatbot will not solve customer frustration if the underlying policy is unclear.

### Data failure

Training or evaluation data may be incomplete, outdated, mislabeled, duplicated, unlawfully obtained, or unrepresentative. Retrieved documents may be obsolete or contradictory. User input may omit essential context.

### Model failure

The selected model may lack required capability, produce unstable output, fail in a language, or perform poorly on unusual cases. A provider update may cause behavioral drift.

### Instruction failure

Prompts may contain ambiguous goals, conflicting constraints, missing examples, or no definition of success. The system may also be exposed to **prompt injection**, in which untrusted content attempts to override instructions or manipulate tool use.

### Tool failure

A search service may return irrelevant results. An API may be unavailable. A calculator may receive malformed data. A database query may use the wrong identifier. Tool output should be treated as data requiring validation, not as unquestionable truth.

### Interface failure

Users may not understand what information is required, may over-trust a polished response, or may approve an action accidentally. An interface that hides sources or makes correction difficult can turn a minor model error into a consequential product failure.

### Governance failure

No one may own the system after launch. Logs may be absent, incidents may not be reported, and evaluation may stop while the world changes. A system that was acceptable during a pilot can become risky when user volume, data, or intended use changes.

The practical lesson is that reliability must be engineered across the complete workflow. Replacing a model may help, but it is only one possible intervention.

## 1.9 Bias, fairness, and representation

AI systems learn from human-produced and institutionally produced data. Such data reflect unequal access, historical decisions, cultural assumptions, measurement practices, and gaps in representation. A model can therefore reproduce or amplify undesirable patterns without any developer explicitly programming discrimination.

### Bias has multiple meanings

In statistics, bias may refer to systematic estimation error. In social analysis, bias may refer to patterns that disadvantage a group or embed a partial perspective. Product teams should specify which meaning they are discussing.

Potential sources include:

- **historical bias:** past outcomes reflect inequity;
- **sampling bias:** collected examples do not represent the intended population;
- **measurement bias:** a convenient variable poorly represents the concept of interest;
- **label bias:** human judgments used as labels are inconsistent or prejudiced;
- **aggregation bias:** one model is applied to groups with meaningfully different patterns;
- **evaluation bias:** benchmarks omit important users or conditions; and
- **deployment bias:** the system is used for a purpose different from the one evaluated.

### Fairness is a design decision

There is no universal numerical definition of fairness that fits every setting. Different fairness criteria can conflict. Equal error rates, equal access, equal treatment, and correction of historical disadvantage are distinct objectives. Choosing among them requires domain knowledge, stakeholder participation, and ethical or legal judgment.

For a low-consequence writing assistant, inclusive language tests may be appropriate. For employment, credit, health, education, policing, or essential services, the required analysis is substantially more rigorous. A product builder should not treat a prompt such as “be unbiased” as a fairness program.

### Representation in generative output

Generated text and images can reproduce stereotypes or systematically underrepresent people, languages, and cultures. Evaluation should therefore include varied identities, dialects, names, regions, and accessibility needs relevant to the target users. Testing should examine not only offensive output but also differences in helpfulness, refusal, accuracy, and tone.

## 1.10 Privacy, security, and intellectual property

### Data minimization

The safest sensitive data is often data the system never receives. **Data minimization** means collecting and processing only what is necessary for a defined purpose. Before sending content to an AI service, determine whether names, account numbers, health information, confidential business material, or other identifiers can be removed.

Privacy analysis should address:

- what data enters the system;
- why each field is necessary;
- where data is transmitted and stored;
- how long it is retained;
- who can access logs and outputs;
- whether data may be used to improve a service;
- how deletion and correction requests are handled; and
- which laws, contracts, or organizational policies apply.

Do not infer privacy guarantees from a product’s conversational tone. Verify the applicable terms, settings, and contracts.

### Security boundaries

Language models process instructions and data in the same general medium. A retrieved web page, uploaded document, or email can contain text that looks like an instruction. If the application allows untrusted content to influence tool use, attackers may attempt prompt injection, data exfiltration, or unauthorized actions.

Security controls can include least-privilege access, separation of trusted instructions from untrusted data, allow-listed tools, schema validation, confirmation before consequential actions, output encoding, secret isolation, rate limits, logging, and independent authorization checks.

The model should never be the sole security boundary. If a user lacks permission to open a payroll record, the database must enforce that permission even if the model requests the record.

### Intellectual property and provenance

AI products can raise questions about rights in training data, user inputs, generated outputs, brands, and third-party materials. Legal rules and service terms vary by jurisdiction and provider. Product teams should document source provenance, licenses, permitted uses, attribution requirements, and review procedures.

A generated artifact should not be assumed original merely because it was produced in response to a unique prompt. For publication or commercial use, apply an appropriate rights review, especially when output imitates identifiable creators, incorporates protected characters, or resembles existing material.

## 1.11 Responsible AI as product practice

Responsible AI is not a statement placed on a website after development. It is a set of decisions across the system lifecycle. UNESCO’s Recommendation on the Ethics of Artificial Intelligence frames AI ethics around human dignity, human rights, well-being, inclusion, environmental concerns, transparency, fairness, and human oversight [3]. The United States National Institute of Standards and Technology (NIST) AI Risk Management Framework provides a voluntary structure organized around four functions: **Govern, Map, Measure, and Manage** [4].

These frameworks operate at different levels, but they support a common conclusion: responsibility requires ongoing evidence and institutional practice.

### Govern

Establish ownership, policies, roles, documentation, escalation routes, and acceptable-use boundaries. Governance answers questions such as:

- Who is accountable for the product?
- Who can approve a change?
- Which uses are prohibited?
- How are incidents reported?
- When must deployment be paused?

### Map

Describe the context in which the system will operate. Identify users, affected non-users, intended benefits, foreseeable misuse, data flows, dependencies, and consequences of failure. Mapping prevents a narrow technical test from being mistaken for complete product evidence.

### Measure

Evaluate quality and risk with defined methods. Measurement may include task success, error severity, subgroup performance, privacy checks, security testing, accessibility review, latency, cost, and user understanding.

### Manage

Prioritize risks, implement controls, monitor operation, respond to incidents, and decide whether remaining risk is acceptable. Management is iterative because models, users, data, and environments change.

### Trustworthiness is contextual

NIST describes characteristics associated with trustworthy AI, including validity and reliability, safety, security and resilience, accountability and transparency, explainability and interpretability, privacy enhancement, and fairness with harmful bias managed [5]. These characteristics may involve trade-offs. Maximum transparency can conflict with privacy or security; maximum automation can conflict with meaningful oversight.

The goal is not to attach the word “trustworthy” to a system. It is to produce evidence that justifies an appropriate level of trust for a defined context.

## 1.12 Consequence-based design

Not every use of AI requires the same control. Asking a model to suggest fictional character names has different consequences from using it to prioritize patients.

### Low-consequence use

Errors are easy to detect and reverse, and they cause little harm. Examples include brainstorming internal event themes or producing placeholder copy. Controls may include basic review, privacy rules, and routine quality testing.

### Moderate-consequence use

Errors can waste time, damage reputation, expose confidential information, or affect a meaningful workflow. Examples include customer-facing drafts, internal policy summaries, or code changes. Controls may include grounding, structured review, access controls, regression tests, and monitoring.

### High-consequence use

Outputs can materially affect rights, safety, health, employment, credit, legal status, education, or access to essential services. These uses require specialized expertise, formal risk analysis, strong evidence, meaningful human authority, security and privacy controls, legal review, auditability, and often regulatory compliance. Some uses should not be automated.

Consequence is determined by actual use, not by the model’s marketing category. A general-purpose model becomes part of a high-consequence system when its output influences a high-consequence decision.

### Human in, on, or out of the loop

The phrase **human in the loop** is often used without precision. Human involvement can take several forms:

- a human supplies input;
- a human reviews an output;
- a human approves an action;
- a human monitors aggregate performance;
- a human handles exceptions; or
- a human can stop the system.

Meaningful oversight requires time, information, authority, and competence. A reviewer who sees hundreds of outputs per hour, cannot inspect evidence, or is penalized for rejecting the model is not an effective safeguard.

## 1.13 From an AI idea to a product problem

Product work should begin with an observed need, not with a model capability.

### The weak formulation

> We want an AI assistant for our business.

This statement does not identify a user, outcome, constraint, or measure. Almost any feature could satisfy it, which means the team cannot determine whether it has succeeded.

### The stronger formulation

> Customer-support coordinators spend a median of 18 minutes turning resolved case notes into a standardized handoff. We want to reduce preparation time while preserving all required fields, preventing disclosure of restricted data, and keeping the coordinator responsible for approval.

This formulation contains a baseline, task, user, desired improvement, quality constraint, safety constraint, and decision owner.

### The AI opportunity statement

Use the following structure:

> For **[specific user]** who needs to **[complete a task]**, the current process causes **[measured problem]**. We will test whether **[AI-supported intervention]** can improve **[primary outcome]** while maintaining **[quality and safety constraints]**. A human will remain responsible for **[decision or action]**.

The phrase “we will test whether” is deliberate. At the beginning, the benefit is a hypothesis, not a fact.

### Should AI be used at all?

AI is a poor choice when:

- a stable deterministic rule solves the problem more reliably;
- there is insufficient lawful, relevant data;
- errors cannot be detected before harm occurs;
- the task requires accountability that cannot be delegated;
- users do not have a meaningful way to contest outcomes;
- operating cost exceeds the value created; or
- automation would preserve a broken process.

Choosing not to use AI can be a sophisticated product decision.

## 1.14 The AI product lifecycle

### Stage 1: discover

Observe the current workflow. Interview users. Measure the baseline. Identify exceptions, workarounds, and downstream effects. Separate the stated request from the underlying need.

Output: a problem statement, user definition, baseline measure, and initial consequence classification.

### Stage 2: define

Specify the task boundary, inputs, outputs, acceptance criteria, prohibited behavior, human responsibility, and data constraints. Decide which parts should use deterministic software, AI, or human judgment.

Output: a testable product specification.

### Stage 3: prototype

Build the smallest workflow capable of testing the central assumption. A prototype may use manual steps behind the interface. The purpose is learning, not scale.

Output: an instrumented workflow and a small evaluation set.

### Stage 4: evaluate

Run representative cases, including difficult and adversarial cases. Compare results with the baseline. Record errors by type and severity. Test whether users understand limitations and can correct output.

Output: evaluation evidence and a decision to revise, proceed, or stop.

### Stage 5: deploy carefully

Begin with limited users, limited permissions, monitoring, and a rollback path. Communicate scope and constraints. Avoid expanding autonomy before evidence supports it.

Output: a controlled release with operational ownership.

### Stage 6: monitor and improve

Track performance, incidents, cost, user behavior, and changing conditions. Re-evaluate after model updates or workflow changes. Retire the system when it no longer meets requirements.

Output: an auditable record of performance and decisions across time.

This lifecycle is cyclical. Evaluation may reveal that the problem must be redefined. Monitoring may reveal a new user population. A responsible team treats revision as normal rather than as evidence of failure.

## 1.15 Evaluation: replacing impressions with evidence

A compelling demo answers, “Can the system produce a good result once?” Evaluation asks, “How often does it meet requirements across relevant conditions, and what happens when it does not?”

### Build an evaluation set

An evaluation set is a collection of representative test cases with expected properties. It should include:

- common cases;
- uncommon but plausible cases;
- difficult edge cases;
- incomplete or ambiguous inputs;
- multilingual or accessibility-relevant cases where applicable;
- unsafe or prohibited requests;
- adversarial inputs; and
- cases drawn from real operation with appropriate privacy protection.

Avoid designing the entire set from examples that the team used while writing prompts. That creates an evaluation version of teaching to the test.

### Define a rubric

A rubric converts vague judgments into repeatable criteria. For a meeting action-item extractor, a rubric might assess:

1. **Completeness:** Were all explicit action items captured?
2. **Faithfulness:** Does every item follow from the transcript?
3. **Ownership:** Is the responsible person preserved when stated?
4. **Due date:** Is the date preserved without invention?
5. **Structure:** Does output match the required schema?
6. **Privacy:** Is restricted information excluded?

Each criterion can use a scale, such as pass/fail or 0–3, with concrete examples of each score.

### Use multiple metrics

No single metric represents product value. A useful evaluation may include:

- task accuracy or rubric score;
- severe-error rate;
- time saved;
- correction rate;
- user completion rate;
- latency;
- cost per successful task;
- accessibility findings;
- privacy or security findings; and
- user trust calibration.

Trust calibration means users rely on the system when warranted and remain appropriately skeptical when evidence is weak. High reported trust is not automatically positive.

### Compare with a baseline

The baseline may be the current manual process, a simple template, a search function, a rules-based system, or a smaller model. Without a baseline, a team can demonstrate capability but cannot establish improvement.

### Analyze errors, not only averages

An average score can hide serious failure. Suppose a system is correct in 95 of 100 cases. If the five failures expose confidential data, the average is unacceptable. Categorize errors by severity, affected users, detectability, and reversibility.

A practical severity scale is:

- **S0 — cosmetic:** no effect on meaning or action;
- **S1 — minor:** causes small correction or delay;
- **S2 — material:** meaningfully impairs the task or user outcome;
- **S3 — critical:** creates significant safety, rights, financial, legal, privacy, or security harm.

Release criteria should set separate limits for critical errors rather than relying solely on an overall quality score.

## 1.16 Guided practice: create an AI Opportunity Brief

This exercise turns an appealing idea into a testable product hypothesis. You can complete it without writing code.

### Scenario

A small training company receives course feedback through online forms. An operations manager reads every response, groups comments by theme, and prepares a monthly report. The manager believes AI could help.

### Step 1: document the current process

Record the process before proposing a solution:

- Inputs: free-text feedback, course identifier, date, and optional rating.
- Current work: read, remove personal details, classify themes, select examples, count recurring issues, and draft report.
- Output: a monthly report reviewed by the program director.
- Baseline: approximately six hours of work per month.
- Known difficulty: comments may contain instructor names, health information, or emotionally charged language.

### Step 2: identify the decision boundary

The report informs changes to courses and instructors. The system may assist with organizing comments, but it should not decide whether an instructor is disciplined. That decision requires broader evidence and accountable human judgment.

Decision boundary:

> AI may propose themes and draft a descriptive report. The operations manager verifies every quoted comment, corrects themes, and approves the final report. Personnel decisions remain outside the system.

### Step 3: define success

Possible success criteria:

- reduce preparation time from six hours to three hours or less;
- capture at least 90 percent of themes identified by two human reviewers;
- include no invented quotations;
- remove designated personal and sensitive information before model processing;
- allow the manager to trace each claim to source comments; and
- keep final approval with the manager.

These thresholds are hypotheses. A pilot will determine whether they are achievable and sufficient.

### Step 4: map data

Create a simple data inventory:

| Data element | Purpose | Sensitivity | Needed by model? | Control |
|---|---|---:|---:|---|
| Feedback text | Identify themes | Variable | Yes, after filtering | Redact and restrict access |
| Course ID | Group results | Low | Yes | Use internal identifier |
| Student name | Follow-up | High | No | Remove before processing |
| Instructor name | Internal analysis | Moderate | Preferably no | Replace with coded identifier |
| Rating | Compare patterns | Low | Yes | Validate numeric range |

The table often reveals that a system needs less data than the existing process contains.

### Step 5: identify failure modes

List failures before building:

- invented quotation;
- incorrect theme assignment;
- minority concern hidden by majority patterns;
- personal information retained in output;
- sarcastic comment interpreted literally;
- multilingual comment ignored;
- report language more negative than the source evidence; and
- user accepts the report without source review.

For each failure, specify prevention, detection, and response. For example, invented quotations can be reduced by requiring quotation identifiers, detected by exact source matching, and handled by blocking report export until mismatches are resolved.

### Step 6: write the opportunity statement

> For the operations manager who prepares the monthly course-feedback report, the current process requires approximately six hours and makes it difficult to trace recurring themes across courses. We will test whether an AI-assisted classification and drafting workflow can reduce preparation time to three hours while preserving traceability, excluding designated personal data, and meeting a human-reviewed theme-recall threshold. The operations manager will approve the report, and the system will not make personnel decisions.

### Step 7: define the smallest pilot

Use one month of appropriately de-identified historical feedback. Ask two reviewers to create a reference theme set. Compare an AI-assisted workflow with the existing process. Do not connect the prototype to automatic email or personnel systems.

### Expected result

A successful exercise produces a one-page brief containing:

- a specific user and task;
- a measured baseline;
- a testable AI intervention;
- quality and safety constraints;
- a human decision owner;
- an initial data inventory;
- named failure modes; and
- a limited pilot design.

If any of these elements is missing, the project is not ready for implementation.

## 1.17 Common misconceptions and corrections

### “AI understands exactly what I mean”

Natural language allows flexible interaction, but the model only receives the information encoded in the prompt, context, tools, and learned parameters. Ambiguous goals remain ambiguous. Product builders must define terms, constraints, and success conditions.

### “A larger model is always better”

Model size may improve some capabilities, but product quality also depends on task fit, data, latency, cost, privacy, reliability, and controls. Comparative evaluation is more useful than prestige.

### “If the answer includes sources, it is correct”

Citations can be fabricated, irrelevant, outdated, or misinterpreted. The application should retrieve authoritative sources, preserve source links, and enable claim-level review.

### “Human review eliminates the risk”

Review can fail through fatigue, automation bias, lack of expertise, time pressure, or poor interface design. Oversight must be supported by evidence, authority, and manageable workload.

### “We can remove bias with one instruction”

Bias can arise from data, labels, objectives, evaluation, interface, and deployment. A general instruction may influence tone but cannot replace representative testing and contextual fairness analysis.

### “The model will learn from every correction”

Corrections may remain only in the conversation or application record. Persistent improvement requires a defined feedback pipeline, evaluation, and possibly prompt, retrieval, software, or model changes.

### “Automation means no people are involved”

People choose objectives, collect data, configure systems, approve budgets, define policies, and experience consequences. Automation redistributes human work and authority; it does not remove them.

## 1.18 Improving an initial product concept

Use the following sequence when an AI idea is too broad.

### Narrow the task

Replace “answer all employee questions” with “answer questions about the approved travel policy using cited policy sections.” Narrow tasks are easier to ground and evaluate.

### Constrain the output

Define required fields, length, tone, source behavior, and allowed actions. Constraints reduce ambiguity and enable validation.

### Add authoritative knowledge

Use approved, current sources. Record version dates and document ownership. Retrieval should return evidence relevant to the question, not merely documents with similar words.

### Separate recommendation from execution

Allow the system to draft or propose before it acts. Add confirmation, permissions, and transaction limits.

### Design for correction

Make output editable. Preserve source links. Capture correction categories. A correction interface is part of the learning system even if the base model is never retrained.

### Add deterministic checks

Use conventional software for schema validation, calculations, identifier matching, authorization, duplicate detection, and prohibited-field checks. Do not ask a probabilistic model to replace every exact operation.

### Evaluate again

Every material change can alter performance. Prompt changes, model versions, new sources, different users, and additional tools require proportionate regression testing.

## 1.19 Safety and privacy checklist

Before an AI prototype uses real data, answer the following questions:

### Purpose and scope

- Is the intended use specific and documented?
- Are prohibited uses documented?
- Is AI necessary, or would a simpler method be more reliable?

### People and consequences

- Who uses the system?
- Who may be affected without directly using it?
- What is the most serious plausible error?
- Can an affected person question or contest the result?

### Data

- Is every collected field necessary?
- Do we have authority to use the data for this purpose?
- Have sensitive fields been removed or protected?
- Are retention and deletion rules defined?

### Model and tools

- Has the model been evaluated on representative cases?
- Can untrusted content influence instructions or actions?
- Are tools limited to minimum permissions?
- Are consequential actions independently authorized?

### Output and interface

- Can users inspect supporting evidence?
- Can they edit, reject, or escalate output?
- Does the interface communicate uncertainty and scope?
- Are accessibility needs addressed?

### Operations

- Is there a named owner?
- Are incidents and corrections logged appropriately?
- Is there a rollback or shutdown procedure?
- Will the system be re-evaluated after changes?

A “no” or “unknown” answer is not automatically a reason to abandon the project. It is a requirement to investigate or add a control before proceeding.

## 1.20 Chapter consolidation

Artificial intelligence is a broad category of machine-based inference systems, not a synonym for a chatbot or a single model. Machine learning estimates behavior from data; deep learning uses multilayer neural networks; generative AI produces new content; and foundation models provide broad capabilities that can be adapted into many products.

Modern language models commonly generate text through repeated next-token prediction. Transformer-based attention helps them represent relationships across a sequence, while instruction training, system instructions, retrieval, tools, and application logic shape assistant behavior. These mechanisms can produce flexible and valuable output, but they do not guarantee truth, current knowledge, fairness, privacy, or responsible action.

For product builders, the appropriate unit of analysis is the complete system: user, task, interface, application logic, model, data, tools, governance, and operating environment. Failure can originate in any layer. A model-centered solution is incomplete if it lacks a measurable problem, representative evaluation, consequence-based controls, and a human accountability structure.

Responsible AI turns values into lifecycle practices. Teams govern ownership, map context and impact, measure behavior, and manage risk continuously. They distinguish low-consequence experimentation from high-consequence decision support. They use human oversight precisely, preserve decision authority where needed, and recognize that oversight without time, evidence, competence, and power is not meaningful.

The product-builder mindset is empirical. Begin with an observed problem, state an AI opportunity as a hypothesis, construct the smallest useful pilot, compare against a baseline, analyze severe errors, and expand only when evidence supports expansion. The objective is not maximum automation. It is a useful, understandable, and responsibly operated product.

## 1.21 Review questions

1. Why is an AI system a more useful unit of analysis than a model alone?
2. How does learned software differ from software whose behavior is specified primarily through rules?
3. What is the difference between training and inference?
4. Why are training, validation, and test data separated?
5. What does next-token prediction explain about both the capability and limitations of a language model?
6. Why does low temperature not guarantee factual accuracy?
7. How does grounding differ from permanent model learning?
8. Name three failure sources outside the model itself.
9. Why can two fairness objectives conflict?
10. What is the difference between generation authority and action authority?
11. What conditions make human oversight meaningful?
12. Why should evaluation include error severity rather than only average accuracy?
13. How does a baseline strengthen a product claim?
14. Under which conditions should a team prefer deterministic software to AI?
15. Explain the relationship among the Govern, Map, Measure, and Manage functions.

## 1.22 Applied exercises

### Exercise 1: classify system components

Choose an AI feature you use or have observed. Draw a seven-layer map containing user need, interface, application logic, model, data, tools, and governance. For each layer, identify one plausible failure. Do not use “the AI is wrong” as a failure description; state the mechanism and consequence.

### Exercise 2: rewrite a feature idea

Rewrite each statement as a testable opportunity statement:

- “Create an AI tutor.”
- “Automate our marketing.”
- “Use AI to read contracts.”

Each rewritten statement must identify a user, task, baseline problem, proposed intervention, success measure, safety constraint, and human decision owner.

### Exercise 3: build an evaluation rubric

Select one transformation task, such as converting notes into a client email. Create four quality criteria and one safety criterion. Define what scores of 0, 1, 2, and 3 mean for each criterion. Test the rubric with three human-written examples before using it on AI output.

### Exercise 4: consequence and oversight

Classify the following uses as low, moderate, or high consequence, then justify the required oversight:

1. suggesting names for fictional planets;
2. drafting a public response to a customer complaint;
3. ranking scholarship applicants;
4. extracting totals from invoices before human approval; and
5. controlling the dosage of a medical device.

There may be reasonable disagreement about categories. Your justification and controls are more important than the label.

### Exercise 5: model versus system intervention

For each failure, propose one intervention that does not require changing the model:

- invented policy citation;
- unauthorized database access;
- missing required output field;
- user over-trust;
- outdated product price; and
- accidental disclosure of a customer identifier.

## References

1. Organisation for Economic Co-operation and Development. “Explanatory Memorandum on the Updated OECD Definition of an AI System.” 2024. <https://oecd.ai/en/ai-publications/explanatory-memorandum-on-the-updated-oecd-definition-of-an-ai-system>
2. Vaswani, Ashish, et al. “Attention Is All You Need.” *Advances in Neural Information Processing Systems*, 2017. <https://arxiv.org/abs/1706.03762>
3. United Nations Educational, Scientific and Cultural Organization. “Recommendation on the Ethics of Artificial Intelligence.” Adopted 23 November 2021. <https://www.unesco.org/en/legal-affairs/recommendation-ethics-artificial-intelligence>
4. National Institute of Standards and Technology. “AI Risk Management Framework.” <https://www.nist.gov/itl/ai-risk-management-framework>
5. National Institute of Standards and Technology. “AI Risk Management Framework FAQs.” <https://www.nist.gov/itl/ai-risk-management-framework/ai-risk-management-framework-faqs>

## Further reading

- Brown, Tom B., et al. “Language Models are Few-Shot Learners.” 2020. <https://arxiv.org/abs/2005.14165>
- Kaplan, Jared, et al. “Scaling Laws for Neural Language Models.” 2020. <https://arxiv.org/abs/2001.08361>
- National Institute of Standards and Technology. *Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile*. NIST AI 600-1, 2024. <https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf>
