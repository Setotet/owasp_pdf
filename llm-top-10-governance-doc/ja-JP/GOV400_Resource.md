## 第四章　リソース・リンク

#### OWASP 大規模言語モデル・アプリケーション リスク トップ10

  >dodgerblue|white|left|12|16 LLM01: プロンプト・インジェクション
  >azure|black|justified|10|12 巧妙な入力によって大規模な言語モデル（LLM）を操作し、LLMが意図しない動作を引き起こします。直接注入はシステムのプロンプトを上書きし、間接注入は外部ソースからの入力を操作するものです。

  >dodgerblue|white|left|12|16 LLM02: 安全が確認されていない出力ハンドリング
  >azure|black|justified|10|12 この脆弱性は、LLM の出力が精査されずに受け入れられ、バックエンドシステムを露出させるという場合に起きることです。悪用されると、XSS、CSRF、SSRF、特権の昇格、リモート・コードの実行といった深刻な結果につながる可能性があります。

  >dodgerblue|white|left|12|16 LLM03: 訓練データの汚染
  >azure|black|justified|10|12 LLM の訓練データが改ざんされ、セキュリティ、有効性、倫理的行動を損なう脆弱性やバイアスなどが入った状態です。情報源としては、Common Crawl、WebText、OpenWebText、書籍などがあります。

  >dodgerblue|white|left|12|16 LLM04: モデルのDoS
  >azure|black|justified|10|12 攻撃者はLLM上でリソースを大量に消費する操作を引き起こすことで、サービスの低下や高コストをもたらします。LLMはリソースを大量に消費し、ユーザーの入力が予測できないため、脆弱性は拡大します。

  >dodgerblue|white|left|12|16 LLM05: サプライチェーンの脆弱性
  >azure|black|justified|10|12 LLMアプリケーションのライフサイクルは、脆弱なコンポーネントやサービスによって侵害される可能性があり、セキュリティ攻撃につながります。サードパーティのデータセット、事前に訓練されたモデル、およびプラグインを使用することで、脆弱性が増える可能性があります。

  >dodgerblue|white|left|12|16 LLM06: 機微情報の漏えい
  >azure|black|justified|10|12 LLMは、その応答の中で不注意に機密データを暴露する可能性があり、不正なデータアクセス、プライバシー侵害、セキュリティ侵害につながります。これを軽減するためには、データのサニタイズと厳格なユーザー・ポリシーを導入することが極めて重要です。

  >dodgerblue|white|left|12|16 LLM07: 安全が確認されていないプラグイン設計
  >azure|black|justified|10|12 LLMプラグインにおいて、入力の安全性が確認されておらず、あるいはアクセスコントロールが不十分である場合、このようなアプリケーションにおけるコントロールの欠如は、悪用が容易であり、リモート・コード実行のような結果をもたらす可能性があります。

  >dodgerblue|white|left|12|16 LLM08: 過剰な代理行為
  >azure|black|justified|10|12 LLMベースのシステムは、意図しない結果を招く動作をすることがあります。この問題は、LLMベースのシステムに与えられた過剰な機能、権限、または自律性に起因します。

  >dodgerblue|white|left|12|16 LLM09: 過度の信頼
  >azure|black|justified|10|12 十分監督されていないLLMに過度に依存したシステムや人々は、LLMが生成したコンテンツが不正確または不適切なものである場合、誤った情報、誤ったコミュニケーション、法的問題、セキュリティの脆弱性に直面する可能性があります。

  >dodgerblue|white|left|12|16 LLM10: モデルの盗難
  >azure|black|justified|10|12 これには、独自のLLMモデルへの不正アクセス、コピー、または流出が含まれます。その影響には、経済的損失、競争上の優位性の低下、機密情報へのアクセスの可能性などが含まれます。

##### 図 4.1　OWASP 大規模言語モデル・アプリケーション リスク トップ10
#### OWASP 大規模言語モデル・アプリケーション リスクの所在箇所
![OWASP Top10 for LLM Visual](images/GOV1_Fig_4_2.jpg)
##### 図 4.2　OWASP 大規模言語モデル・アプリケーション リスクの所在箇所

OWASP リソース LLM ソリューションを使用すると、組織の攻撃対象領域が拡大し、新たな課題が発生するため、特別な戦術や防御が必要になります。また、既知の問題と類似した問題も発生し、すでに確立されたサイバーセキュリティの手順と緩和策が存在します。LLMサイバーセキュリティを組織の確立されたサイバーセキュリティ管理、プロセス、手順と統合することで、組織は脅威に対する脆弱性を減らすことができます。これらがどのように統合されるかは、OWASP Integration Standards（OWASP統合基準）をご覧ください。

#### OWASP リソース・リンク
  [OWASP SAMM](https://owasp.org/www-project-samm/)
#### 説明
  ソフトウェア保証成熟度モデル
#### お勧めする理由と場所、使用方法
  効果的で組織の安全な開発ライフサイクルを分析し、改善するための測定可能な方法。SAMM は、ソフトウェアライフサイクル全体をサポートします。  SAMM は相互作用的でリスク駆動型であるため、組織はセキュアなソフトウエア開発におけるギャップを特定し、優先順位を付けることができます。

#### OWASP リソース・リンク
  [OWASP AIセキュリティとプライバシーガイド](https://owasp.org/www-project-ai-security-and-privacy-guide/)
#### 説明
  AIセキュリティに関する交流、標準の整合性の促進、コラボレーションの推進を目的として、世界中を結ぶことを目的としているOWASPプロジェクトです。
#### お勧めする理由と場所、使用方法
  OWASP AIセキュリティとプライバシー　ガイドは、AIのセキュリティとプライバシーに関する最も重要な考慮事項の包括的なリストです。開発者、セキュリティ研究者、セキュリティ・コンサルタントがAIシステムのセキュリティとプライバシーを検証するための包括的なリソースとなることを目的としています。

#### OWASP リソース・リンク
  [OWASP AI Exchange](https://owasp.org/www-project-ai-security/)
#### 説明
  OWASP AI ExchangeはOWASP AIセキュリティ・プライバシーガイドのための摂取方法です。
#### お勧めする理由と場所、使用方法
  AIエクスチェンジは OWASP が OWASP AIセキュリティ・プライバシーガイドの方向性を推進するために使用する摂取方法。

#### OWASP リソース・リンク
  [OWASP 機械学習セキュリティ トップ10](https://mltop10.info/)
#### 説明
  機械学習システムのセキュリティ問題トップ10。
#### お勧めする理由と場所、使用方法
  OWASP Machine Learning Security Top 10は、機械学習システムの最も重要なセキュリティ問題を収集し、セキュリティ専門家とデータサイエンティストの両方が理解しやすい形式で提示するコミュニティ主導の取り組みです。このプロジェクトは、ML Top 10 を含み、安全でプライバシーを保護する AI システムの設計、作成、テスト、調達に関する明確で実行可能な洞察を提供する、生きた作業文書です。これは、AIのグローバルな規制とプライバシー情報のための最高のOWASPリソースです。

#### OWASP リソース・リンク
   [OpenCRE](https://www.opencre.org/)
#### 説明
  OpenCRE (共通要件列挙)は、セキュリティ標準とガイドラインを1つの概要にまとめるためのインタラクティブなコンテンツリンクプラットフォームです。
#### お勧めする理由と場所、使用方法
  標準、規格を検索するため。規格名またはコントロールタイプで検索できます。

#### OWASP リソース・リンク
  [OWASP脅威モデリング](https://owasp.org/www-community/Threat_Modeling)
#### 説明
  構造化された正式なアプリケーションの脅威モデリングプロセス
#### お勧めする理由と場所、使用方法
  脅威モデリングについて知ることができます。脅威モデリングとは、アプリケーションのセキュリティに関する情報を体系的にまとめています。

#### OWASP リソース・リンク
  [OWASP CycloneDX](https://owasp.org/www-project-cyclonedx/)
#### 説明
  OWASP CycloneDXは、サイバーリスク低減のための高度なサプライチェーン機能を提供するフルスタックの部品表（BOM）規格です。
#### お勧めする理由と場所、使用方法
  最新のソフトウェアはサードパーティやオープンソースのコンポーネントを使用しています。これらのコンポーネントは、複雑かつ独自の方法で接着され、目的の機能を実現するために元のコードと統合されます。SBOM は、組織がリスクを特定し、透明性を高め、迅速な影響分析を可能にする、すべてのコンポーネントの正確なインベントリを提供します。EO 14028 は、連邦システムの SBOM に関する最低要件を規定。

#### OWASP リソース・リンク
  [OWASP ソフトウェアコンポーネント検証規格（SCVS）](https://scvs.owasp.org/)
#### 説明
  コミュニティ主導アクティビティ、コントロール、ベストプラクティスを特定するためのフレームワークを確立する取り組みは、ソフトウェアサプライチェーンにおけるリスクの特定と削減に役立ちます。
#### お勧めする理由と場所、使用方法
  SCVSを使って共通のソフトウェアサプライチェーンのリスクを低減し、成熟したソフトウェアサプライチェーンへの警戒のベースラインと道筋を特定することができる活動、管理、ベストプラクティスのセットです。

#### OWASP リソース・リンク
  [OWASP API セキュリティ プロジェクト](https://owasp.org/www-project-api-security/)
#### 説明
  アプリケーション・プログラミング・インターフェース（API）のセキュリティに関するユニークな脆弱性とセキュリティリスクを理解し、軽減するための戦略とソリューションについて、説明しています。
#### お勧めする理由と場所、使用方法
  APIは基盤となる要素ユーザと組織を保護するためには、アプリケーションを接続し、誤設定や脆弱性を緩和することが必須です。ビルド環境と本番環境のセキュリティテストとレッドチームに使用してください。

#### OWASP リソース・リンク
  [OWASP アプリケーション セキュリティ 検証基準 ASVS](https://owasp.org/www-project-application-security-verification-standard/)
#### 説明
  アプリケーション・セキュリティ検証標準（ASVS）プロジェクトは、ウェブアプリケーションの技術的なセキュリティ管理をテストするための基礎を提供します。   プロジェクトは、ウェブアプリケーションの技術的なセキュリティ制御をテストするための基礎を提供し、また、開発者に安全な開発のための要求事項のリストを提供します。
#### お勧めする理由と場所、使用方法
  ウェブアプリケーション用クックブックセキュリティ要件、セキュリティテスト、メトリクスセキュリティユーザストーリーとセキュリティユースケースのリリーステストを確立するために使用します。

#### OWASP リソース・リンク
  [OWASP 脅威およびセーフガードマトリックス (TaSM)](https://owasp.org/www-project-threat-and-safeguard-matrix/)
#### 説明
  ビジネスを守り、可能にするために、行動重視の視点を提供します。
#### お勧めする理由と場所、使用方法
  このマトリックスにより、企業は以下のことが可能になります。主要な脅威をNISTサイバーセキュリティフレームワークの機能（特定、保護、検知、対応、回復）に重ね合わせ、強固なセキュリティ計画を構築します。ダッシュボードとして使用して、組織全体のセキュリティを追跡し、報告します。

#### OWASP リソース・リンク
   [欠陥 道場](https://www.defectdojo.com/)
#### 説明
  テンプレート化、レポート作成、数値化、基準となるセルフサービスツールにより、テストプロセスを合理化する、オープンソースの脆弱性管理ツールです。
#### お勧めする理由と場所、使用方法
  「欠陥 道場」を使えば、テンプレートを使い、一般的な脆弱性を検出し、レポート生成、数値化し、脆弱性のログ作成時間を短縮できます。

### MITRE のリソース

LLM の脅威が頻発するようになったことで、組織の攻撃対象領域を防御するためのレジリエン ス第一のアプローチの価値が強調されています。既存の TTPS は、LLM における新たな攻撃対象領域と機能と組み合わされています。MITRE は、実世界での観察に基づき、敵対者の戦術と手順を調整するための、確立され広く受け入れられているメカニズムを維持しています。

組織の LLM セキュリティ戦略を MITRE ATT&CK と MITRE ATLAS に調整しマッピングすることで、LLM セキュリティが API セキュリティ標準などの現在のプロセスでカバーされている部分や、セキュリティホールが存在する部分を特定することができます。

MITRE ATT&CK（Adversarial Tactics, Techniques, and Common Knowledge）は、MITRE Corporationによって作成されたフレームワーク、データマトリックス集、および評価ツールです。これは世界中で使用されている知識リポジトリです。MITRE ATT&CKマトリックスには、敵対者が特定の目標を達成するために使用する戦略のコレクションが含まれています。ATT&CK マトリックスでは、これらの目的は戦術として分類されています。目的は攻撃順に概説されており、偵察から始まり、最終的な目標である殲滅または影響へと進んでいきます。

MITRE ATLASは「Adversarial Threat Landscape for Artificial Intelligence Systems」の略で、悪質な行為者による機械学習（ML）システムへの攻撃の実例に基づいた知識ベースです。ATLASはMITREのATT&CKアーキテクチャに基づいており、その戦術と手順はATT&CKに見られるものを補完しています。

#### MITRE リソース・リンク
  [MITRE ATT&CK](https://attack.mitre.org/)
#### 説明
  実際の観察に基づく敵の戦術とテクニックの知識ベース
#### お勧めする理由と場所、使用方法
  具体的な脅威モデルと方法論の開発の基礎として使用します。組織内の既存の管理策を敵の戦術や技法にマップし、ギャップやテストすべき領域を特定します。

#### MITRE リソース・リンク
  [MITRE AT&CK 作業台](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/attck-workbench/)
#### 説明
  ローカルな知識ベースを使って、ATT&CKの作成または拡張する際に使う作業台です。
#### お勧めする理由と場所、使用方法
  ATT&CK 知識ベースをコピーし、新しい、または更新されたテクニック、戦術、ミティゲーション・グループ、および組織に特化したソフトウェアで拡張することができます。

#### MITRE リソース・リンク
   [MITRE ATLAS](https://atlas.mitre.org/)
#### 説明
  MITRE　ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) is a globally accessible, living knowledge base of adversary tactics and techniques against Al-enabled systems based on real-world attack observations and realistic demonstrations from Al red teams and security groups.
#### お勧めする理由と場所、使用方法
  Use it to map known ML vulnerabilities and map checks and controls for proposed projects or existing systems.

#### MITRE リソース・リンク
  [MITRE ATT&CK Powered Suit](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/attack-powered-suit/)
#### 説明
  ATT&CKパワードスーツはは、MITRE ATT&CKナレッジベースをあなたの手元に置くブラウザ拡張機能です。
#### お勧めする理由と場所、使用方法
  ATT&CKパワードスーツはは、MITRE ATT&CK ナレッジベースをあなたの手元に置くブラウザ拡張機能です

#### MITRE リソース・リンク
  [The Threat Report ATT&CK Mapper (TRAM)](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/threat-report-attck-mapper-tram/)
#### 説明
  CTI レポートのTTP Identificationを自動化する
#### お勧めする理由と場所、使用方法
  CTIレポートに見られるTTPをMITRE ATT&CKに対応させるのは難しく、エラーが発生しやすく、時間がかかります。TRAMはLLMを使用し、最も一般的な50の技術についてこのプロセスを自動化します。Juypterノートブックをサポート

#### MITRE リソース・リンク
   [Attack Flow v2.1.0](https://center-for-threat-informed-defense.github.io/attack-flow/)
#### 説明
  アタックフローはサイバー敵対者が、様々な攻撃技術をどのように組み合わせ、目的を達成するのかを記述するための言語。
#### お勧めする理由と場所、使用方法
  攻撃者がどのようなテクニックを使うかを理解することで、防御者や指導者は敵の動きを理解し、自らの防御態勢を向上させることができます。

#### MITRE リソース・リンク
  [MITRE カルデラ](https://caldera.mitre.org/)
#### 説明
  敵のエミュレーションを自動化し、手動レッドチームを支援し、インシデントレスポンスを自動化するように設計された、サイバーセキュリティ・プラットフォームです。
#### お勧めする理由と場所、使用方法（プラグインへのリンク付）
  [Caldera 用のプラグイン](https://caldera.readthedocs.io/en/latest/Plugin-library.html) 利用可能です。フレームワークのコア機能を拡張し、エージェント、レポート、TTP のコレクションなどの追加機能を提供します。

#### MITRE リソース・リンク
  [CALDERA ラグイン: アーセナル](https://www.mitre.org/news-insights/news-release/microsoft-and-mitre-create-tool-help-security-teams-prepare-attacks)
#### 説明
  AI対応システムの敵対的エミュレーションのために開発されたプラグインです。
#### お勧めする理由と場所、使用方法
  このプラグインは、CALDERA とインターフェースするため、MITRE ATLAS に定義された TTP を提供します。

#### MITRE リソース・リンク
  [アトミック・レッド・チーム](https://github.com/redcanaryco/atomic-red-team)
#### 説明
  MITRE ATT&CKフレームワークで使うテストのライブラリ
#### お勧めする理由と場所、使用方法
  コントロールの検証とテストのために使用することができます。セキュリティチームは、Atomic Red Team を使用することで、自分たちの環境を素早く、ポータブルに、再現性よくテストすることができます。アトミックテストはコマンドラインから直接実行できます。インストレーションする必要はありません。

#### MITRE リソース・リンク
  [MITRE CTI ブループリント](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/cti-blueprints/)
#### 説明
  サイバー脅威情報のレポートを自動化する
#### お勧めする理由と場所、使用方法
  CTIブループリントは、サイバー脅威インテリジェンス（CTI）アナリストが、高品質で実用的なレポートをより一貫して効率的に作成するのを支援します。


### AI脆弱性リポジトリ

#### 名称
  [AI インシデント・データベース](https://incidentdatabase.ai/)
#### 説明
  過去に失敗したAIアプリケーションの事例を蓄積しています。大学の研究グループによって維持され、クラウドソーシングされています。

#### 名称
  [OECD AI インシデント・モニター (AIM)](https://oecd.ai/en/incidents)
#### 説明
  AIに関連する課題を理解するためのわかりやすい出発点を提供します。

### AIモデルの脆弱性を追跡する大手企業3社

1. [Huntrバグバウンティ　：　プロテクトAI](https://huntr.com/)
  AI/ML向けバグ報奨金プラットフォーム

2. [AI脆弱性データベース(AVID) ：　ガラク](https://avidml.gitbook.io/)
  モデルの脆弱性データベース

3. [AIリスクデータベース　：　ロバスト・インテリジェンス](https://airisk.io/)
  モデルの脆弱性データベース

### AI調達ガイダンス

#### 名称
  [世界経済フォーラム：AI責任の導入：民間セクターによるAIソリューション調達のためのガイドライン：インサイトレポート 2023年6月](https://www.weforum.org/publications/adopting-ai-responsibly-guidelines-for-procurement-of-ai-solutions-by-the-private-sector/)
#### 説明
  人工知能システムの調達のための、標準ベンチマークと評価基準は、まだ開発初期段階にあります。この調達ガイドラインは、エンド・ツー・エンドの調達プロセスにおける考慮事項の基準を組織に提供します。このガイダンスを使うと、既存のサードパーティリスクサプライヤーとベンダー調達プロセスを強化することができます。
