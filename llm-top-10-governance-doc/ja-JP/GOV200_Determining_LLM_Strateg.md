## 第二章　LLM戦略の決定

大規模言語モデル（Large Language Model：LLM）アプリケーションの急速な拡大により、業務で使用されるすべてのAI/MLシステム（Generative AI（ジェネレーティブAI）および古くから確立されているPredictive AI/MLシステムの両方を含む）への注目と検討が高まっています。このような注目の高まりは、これまで見過ごされていたシステムを標的とする攻撃者や、法的、プライバシー、責任、保証の観点から軽視されていたガバナンスや法的課題などの潜在的なリスクを露呈しています。AI/MLシステムを業務に活用するあらゆる組織にとって、包括的なポリシー、ガバナンス、セキュリティ・プロトコル、プライバシー対策、アカウンタビリティ基準を評価・確立し、これらのテクノロジーが安全かつ倫理的にビジネス・プロセスと整合していることを確認することが重要です。

攻撃者（敵対者）は、企業、国民、政府機関にとって最も直接的で有害な脅威です。彼らの目的は、金銭的な利益からスパイ活動まで多岐にわたり、重要な情報を盗み、業務を妨害し、信用を傷つけることにあります。さらに、AIや機械学習などの新技術を活用する彼らの能力は、攻撃のスピードと洗練度を高め、防御が攻撃に先んじることを困難にしています。

多くの組織にとって最も差し迫った逆らえないLLMの脅威は、「シャドーAI」によるものです。従業員が未承認のオンラインAIツール、安全でないブラウザのプラグイン、標準的なソフトウェアの承認プロセスを回避してアップデートやアップグレードによってLLM機能を導入するサードパーティのアプリケーションを使用している場合です。

>||center|16|16 LLM Deployment Steps

>dodgerblue|white|left|14|20 Step 1: Resilience First Strategy

    >fidlightblue|black|justified|12|16 ▶ Identify immediate threads by Threat Modeling abuse cases
    >fidlightblue|black|justified|12|16 ▶ Review internal or external exploitation cases for threat model scenarios and verify security controls
    >fidlightblue|black|justified|12|16 ▶ Scan and monitor the environment for any instances of roge applications

>dodgerblue|white|left|14|20 Step 2: Update existing policy

    >fidlightblue|black|justified|12|16 ▶ Review contracts, NDA, governance, and security to incorporate LLM or GenAI use or threat

>dodgerblue|white|left|14|20 Step 3: Training / Education

    >fidlightblue|black|justified|12|16 ▶ Update security awareness training, developer, legal, or other training to include LLM or GenAI use or threats

>dodgerblue|white|left|14|20 Step 4: Engage with leaders

    >fidlightblue|black|justified|12|16 ▶ Work with executives, business leaders, and other stakeholders to identify an LLM or GenAI solutions strategy
    >fidlightblue|black|justified|12|16 ▶ Implement mitigation / risk strategy

>dodgerblue|white|left|14|20 Step 5: Update Third Party Risk Management Program

    >fidlightblue|black|justified|12|16 ▶ Third-party and vendor AI solutions will require augmented questionnaires and reviews

>dodgerblue|white|left|14|20 Step 6: Choose a development strategy

##### 図 2.1　展開戦略の選択肢

### 展開戦略

その範囲は、一般消費者向けのアプリケーションを活用するものから、個人データで独自のモデルをトレーニングするものまで多岐にわたります。使用ケースの感度、必要な機能、利用可能なリソースなどの要因が、利便性と制御の適切なバランスを決定するのに役立ちます。しかし、これらの5つのモデルタイプを理解することは、オプションを評価するためのフレームワークを提供します。

>||center|16|16 展開

>forestgreen|white|left|14|20 タイプ 1: 直接、アクセスする

    >honeydew|black|left|12|16 ▶ 自社製の大規模言語モデルのインターフェースを使う
    >honeydew|black|left|12|16 ▶ 会社の方針を決め、従業員のトレーニングを行って、リスクを軽減する
    >honeydew|black|left|12|16 ▶ 利点：柔軟に、早く実験を進めることができる
    >honeydew|black|left|12|16 ▶ 例：Perplexity, ChatGPT, big-AGI

>forestgreen|white|left|14|20 タイプ 2: モデルAPIを経由してアクセスする

    >honeydew|black|left|12|16 ▶ ベンダー提供の大規模言語モデルのAPIを使いアクセスする
    >honeydew|black|left|12|16 ▶ 会社の方針を決め、従業員のトレーニングを行って、リスクを軽減する
    >honeydew|black|left|12|16 ▶ 利点：使用するAPIを
    >honeydew|black|left|12|16 ▶ 例：Perplexity, ChatGPT, big-AGI


>forestgreen|white|left|14|20 Type 3: Pre-Trained Models

    >honeydew|black|left|12|16 ▶ Start with a general foundation model, then customize by fine-tuning on your data
    >honeydew|black|left|12|16 ▶ Accelerates timelines versus building fully custom.  Examples: Falcon, Llama, and Amazon Bedrock

>forestgreen|white|left|14|20 Type 4: Fine-Tuned Models

    >honeydew|black|left|12|16 ▶ Start with proven models and tine-tune further with proprietary data to adapt them to your domain
    >honeydew|black|left|12|16 ▶ Enables customization beyond pre-trained, Amazon SageMaker, Amazon Bedrock, Llama2, LegalAI

>forestgreen|white|left|14|20 Type 5: Custom Models

    >honeydew|black|left|12|16 ▶ Build tailored architectures from scratch for your specific use case
    >honeydew|black|left|12|16 ▶ Requires large investment but maximizes customization

##### 図 2.2　展開タイプ
##### 作成: sdunn
