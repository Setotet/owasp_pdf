## Determining LLM Strategy

The rapid expansion of Large Language Model (LLM) applications has heightened the attention and examination of all AI/ML systems used in business operations, encompassing both Generative AI and long-established Predictive AI/ML systems. This increased focus exposes potential risks, such as attackers targeting systems that were previously overlooked and governance or legal challenges that may have been disregarded in terms of legal, privacy, liability, or warranty issues. For any organization leveraging AI/ML systems in its operations, it's critical to assess and establish comprehensive policies, governance, security protocols, privacy measures, and accountability standards to ensure these technologies align with business processes securely and ethically.

Attackers, or adversaries, provide the most immediate and harmful threat to enterprises, people, and government agencies. Their goals, which range from financial gain to espionage, push them to steal critical information, disrupt operations, and damage confidence. Furthermore, their ability to harness new technologies such as AI and machine learning increases the speed and sophistication of attacks, making it difficult for defenses to stay ahead of attacks.

The most pressing non-adversary LLM threat for many organizations stem from "Shadow AI": employees using unapproved online AI tools, unsafe browser plugins, and third-party applications that introduce LLM features via updates or upgrades, circumventing standard software approval processes.

>||center|16|16 Deployment Steps

>cornflower|white|left|14|18 Step 1: Resilience First Strategy

    >fidlightblue|black|justified|12|16 ▶ Identify immediate threats by Threat Modeling abuse cases
    >fidlightblue|black|justified|12|16 ▶ Review internal or external exploitation cases for threat model scenarios and verify security controls
    >fidlightblue|black|justified|12|16 ▶ Scan and monitor the environment for any instances of rogue applications

>dodgerblue|white|left|14|18 Ste 2: Update Existing Policy

    >fidlightblue|black|justified|12|16 ▶ Review contracts, NDA, governance, and security to incorporate LLM or GenAI use or threat

>fidblue|white|left|14|18 Step 3: Training / Education

    >fidlightblue|black|justified|12|16 ▶ Update security awareness training, developer, legal, or other training to include LLM or GenAI use or threat

>darkblue|white|left|14|18 Step 4: Engage with Leaders

    >fidlightblue|black|justified|12|16 ▶ Work with executives, business leaders, and other stakeholders to identify an LLM or GenAI solutions strategy
    >fidlightblue|black|justified|12|16 ▶ Implement mitigation / risk strategy

>cornflower|white|left|14|18 Step 5: Update Third Party Risk Management Program

    >fidlightblue|black|justified|12|16 ▶ Third-party and vendor AI solutions will require augmented questionnaires and reviews

>dodgerblue|white|left|14|18 Step 6: Choose a Deployment Strategy

##### Figure 2.1  Options for Deployment Strategy
##### credit sdunn


### Deployment Strategy

The scopes range from leveraging public consumer applications to training proprietary models on private data. Factors like use case sensitivity, capabilities needed, and resources available help determine the right balance of convenience vs. control. However, understanding these five model types provides a framework for evaluating options.

>||center|16|16 Deployment Types

>cornflower|white|left|14|18 Type 1: Direct Access

    >fidlightblue|black|left|12|16 ▶ Use large language models from their interface
    >fidlightblue|black|left|12|16 ▶ Mitigate risk with corporate policy and employee training
    >fidlightblue|black|left|12|16 ▶ Pros: Flexible and rapid experimentation
    >fidlightblue|black|left|12|16 ▶ Examples: Perplexity, ChatGPT, big-AGI

>dodgerblue|white|left|14|18 Type 2: Access Through Model API

    >fidlightblue|black|left|12|16 ▶ Use large language models directly from vendors through their API
    >fidlightblue|black|left|12|16 ▶ Mitigate risk with corporate policy and employee training
    >fidlightblue|black|left|12|16 ▶ Pros: Enables quick experimentation with some central control through the API
    >fidlightblue|black|left|12|16 ▶ Examples: Claude, ChatGPT, Gemini

>fidblue|white|left|14|18 Type 3: Licensed Model

    >fidlightblue|black|left|12|16 ▶ Use a licensed large language model in enterprise tenant
    >fidlightblue|black|left|12|16 ▶ Mitigate risk by managing in own tenant.  Reduce risk with corporate policy and employee training
    >fidlightblue|black|left|12|16 ▶ Pros: Provides more control and integration with internal tools and workflow
    >fidlightblue|black|left|12|16 ▶ Examples: Microsoft Enterprise CoPilot, Amazon Codewhisperer, SalesForce Einstein GPT

>darkblue|white|left|14|18 Type 4: Pre-Trained Model

    >fidlightblue|black|left|12|16 ▶ Use a general foundation model, then customize by fine-tuning with enterprise or custom data
    >fidlightblue|black|left|12|16 ▶ Mitigate risk with increased visibility, enhance performance, reduce hallucinations.  Reduce risk with corporate policy and employee training
    >fidlightblue|black|left|12|16 ▶ Pros: enhance performance and reduce hallucinations
    >fidlightblue|black|left|12|16 ▶ Examples: QwenLM/Qwen 1.5, DBRX, Starling 7B

>cornflower|white|left|14|18 Type 5: Fine-Tune Proven Model

    >fidlightblue|black|left|12|16 ▶ Use a proen(specialized) models and fine-tune further with proprietary data to adapt them to your enterprise
    >fidlightblue|black|left|12|16 ▶ Mitigate risk with increased visibility, enhance performance, reduce hallucinations.  Reduce risk with corporate policy and employee training
    >fidlightblue|black|left|12|16 ▶ Pros: Enables customization beyond pre-trained
    >fidlightblue|black|left|12|16 ▶ Examples: Google MedPalm, Amazon Bedrock, Llama2, LegalAI

>dodgerblue|white|left|14|18 Type 6: Custom Models

    >fidlightblue|black|left|12|16 ▶ Build a tailored AI/ML Model architecture for enterprise specific use case
    >fidlightblue|black|left|12|16 ▶ Mitigate risk with complete visibility and control.  Reduce risk with corporate policy, developer, and employee training
    >fidlightblue|black|left|12|16 ▶ Pros: Requires large investment but maximizes customization

##### Figure 2.2 Options for Deployment Types
##### credit: sdunn
