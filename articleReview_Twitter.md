# Twitter関連論文のSurvey

キーワードを"Twitter Account"としてIEEExplorerを検索した結果を中心に調査

## 1. Twitter Accountを分類

### 1.1. Sybilアカウント/Botアカウントの特定

#### doi: 10.1109/UBMK.2017.8093483

M. Kantepe and M. C. Ganiz, "Preprocessing framework for Twitter bot detection," 2017 International Conference on Computer Science and Engineering (UBMK), Antalya, 2017, pp. 630-634.

TwitterのSybilアカウントの特定を、教師あり機械学習問題として解いている。特徴量は、投稿されたツイート、プロファイル情報、そして時間軸の挙動情報から生成しているとのこと。その際のラベル情報は、停止されたTwitterアカウントをbotアカウントとみなすことで付与されている。


#### doi: 10.1145/2818717

Emilio Ferrara, Onur Varol, Clayton Davis, Filippo Menczer, and Alessandro Flammini. 2016. The rise of social bots. Commun. ACM 59, 7 (June 2016), 96-104.

Botというものは1950年代にChatbotが議論されていたころから存在しており、現在ではsocial mediaにも存在している。その特定手法についてのtaxonomyなども記載されている模様。基本的には読み物で、具体的な技術を詳しく書いたものではないように感じる。




#### doi: 10.1109/TDSC.2012.75

Z. Chu, S. Gianvecchio, H. Wang and S. Jajodia, "Detecting Automation of Twitter Accounts: Are You a Human, Bot, or Cyborg?," in IEEE Transactions on Dependable and Secure Computing, vol. 9, no. 6, pp. 811-824, Nov.-Dec. 2012.

アカウントを、Human, Bot, Cyborgの3種類に分類する。Cyborgとは、Botを適宜使うHumanのことを指している。分類するために、投稿間隔から自動化されているか否かを検知し、Tweetのコンテンツのテキストパターンがspamに類似しているかを検査し、account propertyが通常の人間のアカウントと異なっていないかを検査する。そのうえで最終判定を下す。



#### doi: 10.1109/MC.2016.183

V. S. Subrahmanian et al., "The DARPA Twitter Bot Challenge," in Computer, vol. 49, no. 6, pp. 38-46, June 2016.

TwitterやFacebookにおける影響力の高いボットを特定する必要性を記載している模様。
本記事は、DARPAが2015年に開催した影響力の高いTwitterボットを特定するcompetitionについて、記載している。




#### doi: 10.1109/INM.2015.7140327

I. Bara, C. J. Fung and T. Dinh, "Enhancing Twitter spam accounts discovery using cross-account pattern mining," 2015 IFIP/IEEE International Symposium on Integrated Network Management (IM), Ottawa, ON, 2015, pp. 491-496.

Twitterのspamアカウント検知手法に関する研究。従来のように積極的にアクティビティを実施するspamではなく、検知を回避するために消極的にしか活動しないspam accountを検知する手法について検討しているとのこと。



#### doi: 10.1109/ICMLA.2014.81

M. Alsaleh, A. Alarifi, A. M. Al-Salman, M. Alfayez and A. Almuhaysin, "TSD: Detecting Sybil Accounts in Twitter," 2014 13th International Conference on Machine Learning and Applications, Detroit, MI, 2014, pp. 463-469.

従来の検知手法は、Sybil Accountはlegitimateなaccountとのつながりが持てないということを前提にしていたが、その前提が崩れてきているため、Sybil accountの分析を実施し、corpusを作成したとのこと。また、brower pluginを作成し、ユーザにSybil accountについて警告を出せるようにしたとのこと。


#### doi: 10.1109/ICDM.2016.0096

N. Chavoshi, H. Hamooni and A. Mueen, "DeBot: Twitter Bot Detection via Warped Correlation," 2016 IEEE 16th International Conference on Data Mining (ICDM), Barcelona, 2016, pp. 817-822.


長期にわたりほぼ同期して動作するアカウントはボットであるとの前提の下、ボットを特定する技術を提案。
教師なし学習を用いているところ、および単体のユーザではなくユーザ間の関係を見ているところを新規性として主張している。
94%の検知率を誇り、Twitterがアカウントを停止するより前にアカウントを特定することに成功しているとのこと。




### 1.2. Twitterの中のcriminal networkを発見

#### doi: 10.1109/BigData.2016.7840895

D. Xie, J. Xu and T. Lu, "Automated classification of extremist Twitter accounts using content-based and network-based features," 2016 IEEE International Conference on Big Data (Big Data), Washington, DC, 2016, pp. 2545-2549.

ISISのアカウントを特定することをmotivationとして実施されている研究。手法は深く読まないと不明だが、コンテンツ及びネットワーク情報から特徴を抽出し、ISISプロパガンダアカウントを特定しているとのこと。地理的情報を用いている可能性あり。要確認。


#### doi: 10.1109/MCI.2013.2291689

R. Y. K. Lau, Y. Xia and Y. Ye, "A Probabilistic Generative Model for Mining Cybercriminal Networks from Online Social Media," in IEEE Computational Intelligence Magazine, vol. 9, no. 1, pp. 31-43, Feb. 2014.

Twitterに限らずではあるが、social mediaの中のcriminal networkを特定するためにminingを実施し、forensicsに活かすという論文。


### 1.3. トピック別のグルーピングを実施

#### doi: 10.1145/2531602.2531636

Parantapa Bhattacharya, Saptarshi Ghosh, Juhi Kulshrestha, Mainack Mondal, Muhammad Bilal Zafar, Niloy Ganguly, and Krishna P. Gummadi. 2014. Deep Twitter diving: exploring topical groups in microblogs at scale. In Proceedings of the 17th ACM conference on Computer supported cooperative work & social computing (CSCW '14). ACM, New York, NY, USA, 197-210

大量のTwitterのユーザの中から、共通のトピックを持つグループを見つけ出す手法を提案。これらのグループは規模も小さく、これまで研究業界では着目されておらず、そこに着目したとのこと。まずは特定の話題毎に専門家を見つけ、次にそのフォロワーを探すという方法により、グループを生成していくとのこと。




## 2. Tweetの信頼性を追求

#### doi: 10.1109/TDSC.2016.2602338

M. Alrubaian, M. Al-Qurishi, M. M. Hassan and A. Alamri, "A Credibility Analysis System for Assessing Information on Twitter," in IEEE Transactions on Dependable and Secure Computing, vol. 15, no. 4, pp. 661-674, 1 July-Aug. 2018.

Twitter accountを評価するのが目的ではなく、Tweet自体の信頼性を評価する。とはいえ、Twitter userの評価も内部で実施している。reputationシステムが幹の論文のように見える。牛込君のレポートに詳しい記載有。



## 3. Twitterをセキュリティアラート生成に活かす論文

#### doi: 10.1109/ASONAM.2016.7752338

S. Mittal, P. K. Das, V. Mulwad, A. Joshi and T. Finin, "CyberTwitter: Using Twitter to generate alerts for cybersecurity threats and vulnerabilities," 2016 IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining (ASONAM), San Francisco, CA, 2016, pp. 860-867.

TwitterをOSINT sourceとして用いようというもの。
構造化されていないTwitterの内容を、SVCEと呼ばれるシステム(修士論文が参照されている)を用いて分析し、RDF形式にて記録する。
SWRLを用いて演繹計算などするようである。
セキュリティについては、情報が正確とは限らないため、人をプロセスの中に介在させるべきである、と言っているのみであり、本論文のfocusにはなっていない。



