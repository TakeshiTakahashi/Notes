This file contains the summary of academic papers in cybersecurity domain.

# Twitter関連論文

キーワードを"Twitter Account"としてIEEExplorerを検索した結果を中心に調査


## doi: 10.1109/UBMK.2017.8093483


M. Kantepe and M. C. Ganiz, "Preprocessing framework for Twitter bot detection," 2017 International Conference on Computer Science and Engineering (UBMK), Antalya, 2017, pp. 630-634.

TwitterのSybilアカウントの特定を、教師あり機械学習問題として解いている。その際のラベル情報は、停止されたTwitterアカウントをbotアカウントとみなすことで付与されている。


## doi: 10.1109/TDSC.2012.75

Z. Chu, S. Gianvecchio, H. Wang and S. Jajodia, "Detecting Automation of Twitter Accounts: Are You a Human, Bot, or Cyborg?," in IEEE Transactions on Dependable and Secure Computing, vol. 9, no. 6, pp. 811-824, Nov.-Dec. 2012.

アカウントを、Human, Bot, Cyborgの3種類に分類する。Cyborgとは、Botを適宜使うHumanのことを指している。分類するために、投稿間隔から自動化されているか否かを検知し、Tweetのコンテンツのテキストパターンがspamに類似しているかを検査し、account propertyが通常の人間のアカウントと異なっていないかを検査する。そのうえで最終判定を下す。



## doi: 10.1109/BigData.2016.7840895

D. Xie, J. Xu and T. Lu, "Automated classification of extremist Twitter accounts using content-based and network-based features," 2016 IEEE International Conference on Big Data (Big Data), Washington, DC, 2016, pp. 2545-2549.

ISISのアカウントを特定することをmotivationとして実施されている研究。手法は深く読まないと不明だが、コンテンツ及びネットワーク情報から特徴を抽出し、ISISプロパガンダアカウントを特定しているとのこと。地理的情報を用いている気配があるが、詳細はよく読まないと不明。



## doi: 10.1109/INM.2015.7140327

I. Bara, C. J. Fung and T. Dinh, "Enhancing Twitter spam accounts discovery using cross-account pattern mining," 2015 IFIP/IEEE International Symposium on Integrated Network Management (IM), Ottawa, ON, 2015, pp. 491-496.

Twitterのspamアカウント検知手法に関する研究。まだアブストのみしか見ていないが、従来のように積極的にアクティビティを実施するspamではなく、検知を回避するために消極的にしか活動しないspam accountを検知する手法について検討しているとのこと。我々の研究に関連しそうなので、是非読むべき。



## doi: 10.1109/ICMLA.2014.81

M. Alsaleh, A. Alarifi, A. M. Al-Salman, M. Alfayez and A. Almuhaysin, "TSD: Detecting Sybil Accounts in Twitter," 2014 13th International Conference on Machine Learning and Applications, Detroit, MI, 2014, pp. 463-469.

従来の検知手法は、Sybil Accountはlegitimateなaccountとのつながりが持てないということを前提にしていたが、その前提が崩れてきているため、Sybil accountの分析を実施し、corpusを作成したとのこと。また、brower pluginを作成し、ユーザにSybil accountについて警告を出せるようにしたとのこと。我々の研究に関連しそうなので、是非読むべき。


## doi: 10.1109/ACCESS.2017.2762418

C. Yin, Y. Zhu, J. Fei and X. He, "A Deep Learning Approach for Intrusion Detection Using Recurrent Neural Networks," in IEEE Access, vol. 5, pp. 21954-21961, 2017.

とある文献によると、下記のように紹介されている。

侵入検知について、RNNを使う方式を提案し、評価している。
最初anomalousかlegitimateを2値分類し、その後、5つのタイプに分類している。









# Twitter関連以外の論文


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



