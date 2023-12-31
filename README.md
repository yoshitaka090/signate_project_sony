# signate_contest_for_sony
このリポジトリに格納されているコードは、2022年4月頃に開催されたSignateのコンテスト「ソニーグループ合同 データ分析コンペティション」に参加した際に自作したコードである。

▼コンテストのURL<br>
https://signate.jp/competitions/624


▼タスク説明<br>
・世界各都市の大気観測データ（観測日時、位置情報、PM2.5以外の大気物質濃度）、気象情報（天気、湿度、風速等）、及び必要に応じて外部データを用いて、特定の日時・都市における「PM2.5濃度」を予測する。
・学習用データと評価用データにはそれぞれ別の都市のデータが含まれており、評価用データのPM2.5濃度が「未観測」の都市が予測対象となる。

▼ファイルの説明<br>
1. data_preprocessing.ipynb - train.csvおよびtest.csvのデータファイルを整形するコード
2. data_analysis.ipynb - 整形したデータを元に予測するコード
3. test.csv - 評価用ファイル
4. test_seikei.csv - データ整形した評価用ファイル
5. submit_sample.csv - 提出する形式のサンプルファイル
6. submit_result.csv - 予測したデータを入れた提出ファイル

▼コードの概要<br>
data_preprocessing.ibpynファイルでは、データの中で、外れ値や、0などノイズのデータを平均値に置き換えている。
data_analysis.ipynbファイルでは、整形したデータをLightGBMを使用して分析し、予測している。

▼備考<br>
学習用データファイルであるtrain.csv、学習用データを整形したtrain_seikei.csvファイルは25MB以上のためアップロードできませんでした。
