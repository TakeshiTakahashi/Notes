This file contains the summary of academic papers in cybersecurity domain.


# Usenix Security 2018 summary

## Security Impacting the Physical World

### Fear the Reaper: Characterization and Fast Detection of Card Skimmers

University of Floridaの研究成果。
NYPD (New York Police Department)の持つ過去のデータから、スキミングの手口を分析し、対策手法を検討・実装したもの。ハードウェアレイヤのお話で、機械学習も特には利用されていない。


### BlackIoT: IoT Botnet of High Wattage Devices Can Disrupt the Power Grid
Princeton Universityの研究成果
IoT機器を利用して停電を引き起こせる可能性のある攻撃を提案し、評価。
機械学習は関係なし。


### Skill Squatting Attacks on Amazon Alexa

University of Illinois Urbana-Champaignの成果。
音声認識の間違いがsystematicに生じる現状を検証し、それを利用してmalicious applicationを起動させるような攻撃を考えている模様。
機械学習は関係なし。


### CommanderSong: A Systematic Approach for Practical Adversarial Voice Recognition

Chinese Academy of ScienceとFlorida Institute of Technology、University of Illinois、Boston University、Indiana Universityの成果。

Automatic Speech Recognition (ASR)を標的としたcommander songを実証し、その対策についても振れた論文とのこと。背景音の中に隠れたコマンドが既存のASRには実行されてしまうことを示しているとのこと。
DNNベースのASRを対象として考えており、いいかえればDNNベースのASRの脆弱性を突いた攻撃についての論文であり、対策として挙げられているものは特に機械学習を考えてはいない。




## Memory Defenses

### ACES: Automatic Compartments for Embedded Systems

inter-component isolationを実現するコンパイラACESを提案。詳細は読まなければ分からないが、おそらく私の研究範囲外。機械学習とも関係なさそう。


### INIX: In-Process Memory Isolation EXtension

Technische Universtaet Darmstadt (Germany)の成果。x86 CPU用に、in-process memoryのisolationを実現する拡張を提案している。機械学習とも関係なさそう。おそらく私の研究範囲外。


### HEAPHOPPER: Bringing Bounded Model Checking to Help Implementation Security

University of California, Santa Barbaraの成果。
Heap Metadata Attackに対抗する手法を構築したとのこと。機械学習とも関係なさそう。私の研究範囲外。


### GUARDER: A Tunable Secure Allocator

University of TexasとOhio State Universityの成果。
Heap vulnerability対策に関する研究。機械学習と関係なく、また、私の研究範囲外。

## Censorship and Web Privacy

### FP-Scanner: The Privacy Implications of Browser Fingerprint Inconsistencies

Browser Fingerprint対策技術が生じるinconsistencyを検知する技術について書かれている模様。機械学習とは関係なく、私の研究範囲外。

### Who Left Open the Cookie Jar? A Comprehensive Evaluation of Third-Party Cookie Policies

KU Leuven(ベルギー)の成果。

Third Party Cookiesを適切に扱うための各種提案が、どれぐらい有効なのかを評価するフレームワークを提案しているらしい。機械学習とは関係なく、私の研究範囲外。


### Effective Detection of Multimedia Protocol Tunneling using Machine Learning

Universidade de Lisboaの成果。
何故Censorship and Web Privacyに分類されているかはわからないが、Skype等のマルチメディア通信の中にcovert channelが作成された際に、それを検知する手法を提案している。
色々と前提条件はあるものの、decision tree系の機械学習アルゴリズム(Decision Trees, Random Forrests, そしてXG Boost)を用いることで、検知が可能であるとのこと。



### Quack: Scalable Remote Measurement of Application-Layer Censoreship

アプリケーションレイヤでの検閲がなされていることを検知する技術に関する論文。面白そうだが機械学習は関係なく、専門分野でもないため、今度読む。



## Understanding How Humans Authenticate

### Better management than memorized? Studying the Impact of Managers on Password Strength and Reuse

Saarland University (ドイツ)の成果。
パスワードマネージャを使うことのメリットについての初の評価とのこと。機械学習利用なし。詳細は今回はパス。


### Forgetting of Passwords: Ecological Theory and Data


### The Rewards and Costs of Stronger Passwords in a University: Linking Password Lifetime to Strength

### Rethinking Access Control and Authentication for the Home Internet of Things (IoT)





## Vulnerability Discovery

### ATtention Spanned: Comprehensive Vulnerability Analysis of AT Commands Within the Android Ecosystem

### Charm: Facilitating Dynamic Analysis of Device Drivers of Mobile Systems

### Inception: System-Wide Security Testing of Real-World Embedded Systems Software


### Acquisitional Rule-based Engine for Discovering Internet-of-Thing Devices

IoTデバイスを自動的に発見し、アノテーション付与する技術を提案。
NLPとrule miningを用いたもの。詳細は読んでいないが、面白そう。
かなり我々の研究に関連する。


## Web Applications

### A Sense of Time for JavaScript and Node.js: First-Class Timeouts as a Cure for Event Handler Poisoning

### Freezing the Web: A Study of ReDoS Vulnerabilities in JavaScript-based Web Servers

### NAVEX:Precise and Scalable Exploit Generation for Dynamic Web Applications

### Rampart: Protecting Web Applications from CPU-Exhaustion Denial-fo-Service Attacks


## Anonymity

### How Do Tor Users Interact With Onion Services?

### Towards Predicting Efficient and Anonymous Tor Circuits

TORのpath selectionに機械学習、具体的にはRandom Forestを用いることにより、Torのパフォーマンスを向上する論文。面白そうではあるが、セキュリティ論文ではないので今回はスキップ。

### BurnBox: Self-Revocable Encryption in a World Of Compelled Access

### An Empirical Analysis of Anonymity in Zcash


## Privacy in a Digital World

### Unveiling and Quantifying Facebook Exploitation of Sensitive Personal Data for Advertising Purposes

### Analysis of Privacy Protections in Fitness Tracking Social Networks - or - You can run, but can you hide?

### AttriGuard: A Practical Defense Against Attribute Inference Attacks via Adversarial Machine Learning


### Polisis: Automated Analysis and Presentation of Privacy Policies Using Deep Learning


## Attacks on Crypto & Crypto Libraries

### Efail: Breaking S/MIME and OpenPGP Email Encryption using Exfiltration Channels

### The Dangers of Key Reuse: Practical Attacks on IPsec IKE

### One&Done: A Single-Decryption EM-Based Attack on OpenSSL's Constant-Time Blinded RSA

### DATA - Differential Address Trace Analysius: Finding Address-based Side-Channels in Binaries


## Enterprise Security

### The Battle for New York: A Case Study of Applied Digital Treat Modeling at the Enterprise Level

### SAQL: A Stream-based Query System for Real-Time Abnormal System Behavior Detection


## Zero-Knowledge

### Practical Accountability of Secret Processes

### DIZK: A Distributed Zero Knowledge Proof System

## Network Defenses

### NetHide: Secure and Practical Network Topology Obfuscation

### Towards a Secure Zero-rating Framework with Three Parties


## Fuzzing and Exploit Generation

### MoonShine: Optimizing OS Fuzzer Seed Selection with Trace Distillation

### QSYM: A Practical Concolic Execution Engine Tailored for Hybrid Fuzzing


### Automatic Heap Layout Manipulation for Exploitation


### FUZE: Towards Facilitating Exploit Generation for Kernel Use-After-Free Vulnerabilities


## TLS and PKI


### The Secure Socket API: TLS as an Operating System Service

### Return of Bleichenhacker's Oracle Threat (ROBOT)

### Bamboozling Certificate Authorities with BGP

### The Broken Shield: Measuring Revocation Effectiveness in the WIndows Code-Signing PKI

## Vulnerability Mitigations

### Debloating Software through Piece-Wise Compilation and Loading

### Precise and Accurate Patch Precise Test for Binaries

### From Patching Delays to Infection Symptoms: Using Risk Profiles for an Early Discovery of Vulnerabilities Exploited in the Wild

### Understanding the Reproducibility of Crowd-reported Security Vulnerabilities


## Side Channels

### Malicious Manamgnet Unit: Why Stopping Cache Attacks in Software is Harder Than You Think

### Translation Leak-aside Buffer: Defeating Cache Side-channel Protetions with TLB Attacks

### Meltdown: Reading Kernel Memory from User Space

### Foreshadow: Extracting the Keys to the Intel SGX Kingdom with Transient Out-of-Order Execution


## Cybercrime

### Plug and Prey? Measuring the Commodization of Cybercrime via Online Anonymous Markets

### Reading Thieves' Cant: Automatically Identifying and Understanding Dark Jargons from Cybercrime Marketplace

### Shroedinger's RAT: Profiling the stakeholders in the Remote Access Trojan Ecosystem

### The aftermath of a crypto-ransomware attack at a large academic institution



## Web and Network Measurement

### We Still Don't Have Secure Cross-Domain Requests: an Empirical Study of CORS

### End-to-End Measurements of Email Spoofing Attacks

### Who Is Answering My Queries: Understanding and Characterizing Interception of the DNS Resolution Path

### End-User Get Maneuvered: Empirical Analysis of Redirection Hijacking in Content Delivery Networks


## Malware

### SAD THUG: Structural Anomaly Detection for Transmissions of High-value Information Using Graphs

### FANCI: Feature-based Automated NXDomain Classification and Intelligence

### An Empirical Study of Web Resource Manipulation in Real-world Mobile Applications

### Fast and Service-preserving Recovery from Malware Infections Using CRIU

## Subverting Hardware Protections

### The Guard's Dilemma: Efficient Code-Reuse Attacks Against Intel SGX

### A Bad Dream: Subverting Trusted Platform Module While You Are Sleeping

## More Malware 

### Tackling runtime-based obfuscation in Android with TIRO

### Discovering Flaws in Security-Focused Static Analysis Tools for Android using Systematic Mutation

## Attacks on Systems That Learn

### With Great Training Comes Great Vulnerability: Practical Attacks against Transfer Learning

### When Does Machine Learning FAIL? Generalized Transferability for Evasion and Poisoning Attacks



## Smart Contracts

### TEETHER: Gnawing at Ethereum to Automatically Exploit Smart Contracts

### Enter the Hydra: Towards Principled Bug Bounties and Exploit-Resisitant Smart Contracts

### Arbitrum: Scalable, private smart contracts

### Erays: Reverse Engineering Ethereum's Opaque Smart Contracts


## Executing in Untrusted Environments

### DELEGATEE: Brokered Delegation Using Trusted Execution Environments

### Simple Password-Hardened Encryption Services

### Security Namespace: Making Linux Security Frameworks Available to Containers

### Shielding Software From Privileged Side-Channel Attacks


## Web Authentication

### Vetting Single Sign-on SDK Implementations via Symbolic Reasoning

### O Single Sign-Off, Where Art Thou? An Empirical Analysis of Signel Sign-On Account Hijacking and Session Management on the Web

### WPSE: Fortifying Web Protocols via Browser-Side Security Monitoring

### Man-in-the-Machine: Exploiting III-Secured Communication Inside the Computer


## Wireless Attacks

### All Your GPS Are Belong To Us: Towards Stealthy Manipulation of Road Navigation Systems

### Injected and Delivered: Fabricating Implicit Control over Actuation Systems by Spoofing Inertial Sensors

### Modeling and Analysis of a Hierarchy of Distance Bounding Attacks

### Off-Path TCP Exploit: How Wireless Routers Can Jeopardize Your Secrets


## Neural Networks

### Formal Security Analysis of Neural Networks using Symbolic Intervals

### Turning Your Weakness Into a Strength: Watermarking Deep Neural Networks by Backdooring

### A4NT: Author Attribute Anonymity by Adversarial Training of Neural Machine Translation

### GAZELLE: A Low Latency Framework for Secure Neural Network Interface


## Information Tracking

### FlowCog: Context-aware Semantics Extraction and Analysis of Information Flow Leaks in Android Apps

### Sensitive Information Tracking in Commodity IoT

### Enabling Refinable Cross-Host Attack Investigation with Efficient Data Flow Tagging and Tracking 

### Dependence-Preserving Data Compaction for Scalable Forensic Analisis




# Twitter関連論文

キーワードを"Twitter Account"としてIEEExplorerを検索した結果を中心に調査

## Twitter Accountを分類する論文

### doi: 10.1109/UBMK.2017.8093483


M. Kantepe and M. C. Ganiz, "Preprocessing framework for Twitter bot detection," 2017 International Conference on Computer Science and Engineering (UBMK), Antalya, 2017, pp. 630-634.

TwitterのSybilアカウントの特定を、教師あり機械学習問題として解いている。特徴量は、投稿されたツイート、プロファイル情報、そして時間軸の挙動情報から生成しているとのこと。その際のラベル情報は、停止されたTwitterアカウントをbotアカウントとみなすことで付与されている。


### doi: 10.1145/2818717

Emilio Ferrara, Onur Varol, Clayton Davis, Filippo Menczer, and Alessandro Flammini. 2016. The rise of social bots. Commun. ACM 59, 7 (June 2016), 96-104.

Botというものは1950年代にChatbotが議論されていたころから存在しており、現在ではsocial mediaにも存在している。その特定手法についてのtaxonomyなども記載されているが、詳細はよく読まないと分からない。基本的には読み物で、具体的な技術を詳しく書いたものではないように感じる。




### doi: 10.1109/TDSC.2012.75

Z. Chu, S. Gianvecchio, H. Wang and S. Jajodia, "Detecting Automation of Twitter Accounts: Are You a Human, Bot, or Cyborg?," in IEEE Transactions on Dependable and Secure Computing, vol. 9, no. 6, pp. 811-824, Nov.-Dec. 2012.

アカウントを、Human, Bot, Cyborgの3種類に分類する。Cyborgとは、Botを適宜使うHumanのことを指している。分類するために、投稿間隔から自動化されているか否かを検知し、Tweetのコンテンツのテキストパターンがspamに類似しているかを検査し、account propertyが通常の人間のアカウントと異なっていないかを検査する。そのうえで最終判定を下す。



### doi: 10.1109/MC.2016.183

V. S. Subrahmanian et al., "The DARPA Twitter Bot Challenge," in Computer, vol. 49, no. 6, pp. 38-46, June 2016.

TwitterやFacebookにおける影響力の高いボットを特定する必要性を記載している模様。
本記事は、DARPAが2015年に開催した影響力の高いTwitterボットを特定するcompetitionについて、記載している。詳細は後日読む。




### doi: 10.1109/BigData.2016.7840895

D. Xie, J. Xu and T. Lu, "Automated classification of extremist Twitter accounts using content-based and network-based features," 2016 IEEE International Conference on Big Data (Big Data), Washington, DC, 2016, pp. 2545-2549.

ISISのアカウントを特定することをmotivationとして実施されている研究。手法は深く読まないと不明だが、コンテンツ及びネットワーク情報から特徴を抽出し、ISISプロパガンダアカウントを特定しているとのこと。地理的情報を用いている気配があるが、詳細はよく読まないと不明。



### doi: 10.1109/INM.2015.7140327

I. Bara, C. J. Fung and T. Dinh, "Enhancing Twitter spam accounts discovery using cross-account pattern mining," 2015 IFIP/IEEE International Symposium on Integrated Network Management (IM), Ottawa, ON, 2015, pp. 491-496.

Twitterのspamアカウント検知手法に関する研究。まだアブストのみしか見ていないが、従来のように積極的にアクティビティを実施するspamではなく、検知を回避するために消極的にしか活動しないspam accountを検知する手法について検討しているとのこと。我々の研究に関連しそうなので、是非読むべき。



### doi: 10.1109/ICMLA.2014.81

M. Alsaleh, A. Alarifi, A. M. Al-Salman, M. Alfayez and A. Almuhaysin, "TSD: Detecting Sybil Accounts in Twitter," 2014 13th International Conference on Machine Learning and Applications, Detroit, MI, 2014, pp. 463-469.

従来の検知手法は、Sybil Accountはlegitimateなaccountとのつながりが持てないということを前提にしていたが、その前提が崩れてきているため、Sybil accountの分析を実施し、corpusを作成したとのこと。また、brower pluginを作成し、ユーザにSybil accountについて警告を出せるようにしたとのこと。我々の研究に関連しそうなので、是非読むべき。


### doi: 10.1109/ICDM.2016.0096

N. Chavoshi, H. Hamooni and A. Mueen, "DeBot: Twitter Bot Detection via Warped Correlation," 2016 IEEE 16th International Conference on Data Mining (ICDM), Barcelona, 2016, pp. 817-822.


長期にわたりほぼ同期して動作するアカウントはボットであるとの前提のした、ボットを特定する技術を提案。
教師なし学習を用いているところ、および単体のユーザではなくユーザ間の関係を見ているところを新規指定として主張している。
94%の検知率を誇り、Twitterがアカウントを停止するより前にアカウントを特定することに成功しているとのこと。


## doi: 10.1145/2531602.2531636

Parantapa Bhattacharya, Saptarshi Ghosh, Juhi Kulshrestha, Mainack Mondal, Muhammad Bilal Zafar, Niloy Ganguly, and Krishna P. Gummadi. 2014. Deep Twitter diving: exploring topical groups in microblogs at scale. In Proceedings of the 17th ACM conference on Computer supported cooperative work & social computing (CSCW '14). ACM, New York, NY, USA, 197-210

大量のTwitterのユーザの中から、共通のトピックを持つグループを見つけ出す手法を提案。これらのグループは規模も小さく、これまで研究業界では着目されておらず、そこに着目したとのこと。まずは特定の話題毎に専門家を見つけ、次にそのフォロワーを探すという方法により、グループを生成していくとのこと。


## Tweetの信頼性を追求する論文

### doi: 10.1109/TDSC.2016.2602338

M. Alrubaian, M. Al-Qurishi, M. M. Hassan and A. Alamri, "A Credibility Analysis System for Assessing Information on Twitter," in IEEE Transactions on Dependable and Secure Computing, vol. 15, no. 4, pp. 661-674, 1 July-Aug. 2018.

Twitter accountを評価するのが目的ではなく、Tweet自体の信頼性を評価する。とはいえ、Twitter userの評価も内部で実施している。reputationシステムが幹の論文のように見えるが、詳細は読み込む必要有。牛込君のレポートに詳しい記載有。



## Twitterの中のcriminal networkを発見する論文


### doi: 10.1109/MCI.2013.2291689

R. Y. K. Lau, Y. Xia and Y. Ye, "A Probabilistic Generative Model for Mining Cybercriminal Networks from Online Social Media," in IEEE Computational Intelligence Magazine, vol. 9, no. 1, pp. 31-43, Feb. 2014.

Twitterに限らずではあるが、social mediaの中のcriminal networkを特定するためにminingを実施し、forensicsに活かすという論文。
詳細は後日読む。




## Twitterをセキュリティアラート生成に活かす論文

### doi: 10.1109/ASONAM.2016.7752338

S. Mittal, P. K. Das, V. Mulwad, A. Joshi and T. Finin, "CyberTwitter: Using Twitter to generate alerts for cybersecurity threats and vulnerabilities," 2016 IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining (ASONAM), San Francisco, CA, 2016, pp. 860-867.

TwitterをOSINT sourceとして用いようというもの。
構造化されていないTwitterの内容を、SVCEと呼ばれるシステム(修士論文が参照されている)を用いて分析し、RDF形式にて記録する。
SWRLを用いて演繹計算などするようであるが、詳細は不明。
セキュリティについては、情報が正確とは限らないため、人をプロセスの中に介在させるべきである、と言っているのみであり、本論文のfocusにはなっていない。



# Twitter関連以外の論文


## Usenix_2014_Viswanath

Towards Detecting Anomalous User Behavior in Online Social Networks
Authors: 
Bimal Viswanath and M. Ahmad Bashir, Max Planck Institute for Software Systems (MPI-SWS); Mark Crovella, Boston University; Saikat Guha, Microsoft Research; Krishna P. Gummadi, Max Planck Institute for Software Systems (MPI-SWS); Balachander Krishnamurthy, AT&T Labs–Research; Alan Mislove, Northeastern University

TwitterというよりはFacebookを対象とし、異常な挙動を検知する。結果的に怪しいアカウントを特定する方式である。PCAを利用することで、その異常な挙動を特定することを試みている。詳細は読む必要有。牛込君のレポートに詳しい記載有。



## doi: 10.1109/ACCESS.2017.2762418

C. Yin, Y. Zhu, J. Fei and X. He, "A Deep Learning Approach for Intrusion Detection Using Recurrent Neural Networks," in IEEE Access, vol. 5, pp. 21954-21961, 2017.

とある文献によると、下記のように紹介されている。

侵入検知について、RNNを使う方式を提案し、評価している。
最初anomalousかlegitimateを2値分類し、その後、5つのタイプに分類している。


## 2017_SMARTCOMP_Yuan

X. Yuan, C. Li and X. Li, "DeepDefense: Identifying DDoS Attack via Deep Learning," 2017 IEEE International Conference on Smart Computing (SMARTCOMP), Hong Kong, 2017, pp. 1-8.
doi: 10.1109/SMARTCOMP.2017.7946998

とある文献によると、下記のように紹介されている。

bidirectional RNNを活用したDDoS検知を提案している。
DeepDefenseという名前のモデルを提唱し、RNNを使った手法とrandom forest、およびLSTMと比較評価を実施し、RNNを利用するのが最も良いとしている。

## 2013_コンピュータソフトウェア_藤井

「ビッグデータ時代における情報の巨大集積化・並列分散処理に関する研究開発動向」
本論文はサーベイ論文である。
まず、データベースの基本的な考え方整理のフレームワークであるCAP定理、ACID特性のお話を紹介した後に、各種のデータベースの紹介をしている。
特に、NoSQLを強く意識した記述になっている。
また、ファイルシステム別、もしくはクラウドの3要素であるVolume, Variety, Velocity別から、これらの紹介されたデータベースを分類している。



