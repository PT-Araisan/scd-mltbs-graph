# シングルケースデザイン（SCD）における多層ベースライン法の可能性と課題

SCDは必要なサンプルサイズが小さいため、現場の理学療法士にとっては実現可能性（Feasible）が高い介入研究の手法と言えます。さらに、介入時期をずらしながらAB法を数名に実施する多層ベースライン法は、通常の臨床業務の自然な流れに比較的近く、倫理面（Ethical）でも実施しやすいと考えられます。この２つの理由から、個人的にこの手法に大きな可能性を感じています。

しかし、現状では多層ベースライン法はグラフを作成するためのツールに乏しいのが課題です。そこで、Pythonのseabornライブラリを使用して、多層ベースライン法によるグラフを作成するコードを書きました。

以下に、実際に作成されるグラフやその作成手順を記載していますので、良かったら使ってください。何かこうすればもっといいみたいな意見があれば嬉しいです。

## 出来上がるグラフ

例えばこのようなグラフを作ることができます。

- ↓サンプルグラフ⓵

![サンプルグラフ](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/assets/deta.png)

日本語にも対応。被験者４名だとこんな感じです。

- ↓サンプルグラフ⓶

![サンプルグラフ](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/assets/deta_ja.png)

## 使い方手順

1. **データの準備**: グラフで使用するCSVファイルを用意してください。CSVファイルは、エクセルで作成した表データの保存時にCSV形式を選ぶだけでも可能です。
行や列ついては、以下のファイルの形式に沿って入力してください。

- [サンプルグラフ⓵のCSVファイル](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/detaset/deta.csv)

- [サンプルグラフ⓶のCSVファイル](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/detaset/deta_ja.csv)

注）それぞれのグラフに必要な被験者の時系列データ数は等しくなるようにしてください。

サンプルグラフのCSVファイルは赤丸の場所からダウンロードできます。

![画像１](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/assets/demo1.png)



- 次に、後で使うので、↓こちらのファイルを押してから
- [Pythonコードのファイル](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/main.ipynb)

- この赤丸の場所を押してmain.ipynbというファイルをダウンロードしておいてください。
![画像３](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/assets/demo5.png)

2. **Google colaboratoryの利用**: 次にこちらのツールを使います。今回の作業は無料で可能。

- [Google colabのサイトへ行きます）](https://colab.research.google.com/?hl=ja)
Googleアカウントが必要です。

- そして↓アップロードを押す。
![画像４](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/assets/demo2.png)
もしくはファイルのタブから『ノートブックをアップロード』を押す。

- さっきダウンロードしたmain.ipynbをアップロードしてください。

すると、↓このような画面になります。そこで

- ⓵を押すと⓶が出てきます。少し時間がかかることがあります。５秒くらい。

- ⓶を押して、グラフを作りたいCSVファイルをアップロードしてください。

![画像４](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/assets/demo6.png)


- 最後に、↓の画像の'hoge.csv'のところを、自分がアップロードしたファイルの名前に変更して、上の赤丸の△ボタンを押します。Ctrl + Enterでもいいです。
![画像５](https://github.com/PT-Araisan/scd-mltbs-graph/blob/main/assets/demo7.png)

3. **グラフが表示されたら、右クリックで画像を保存してください**


## 補足事項

- 多層ベースライン法の検定や効果量の計算は、[『Rではじめるシングルケースデザイン』（藤巻 峻・山田 剛史　著）](https://ratik.org/9955/907438227/)を参考にすることをお勧めします。そちらでは解析パッケージをダウンロードすることができ、RStudioを活用して簡単にランダマイゼーション検定やTau-Uなども算出できます。

## お問い合わせ

何か質問や要望があれば、[Twitter の DM](https://x.com/Pt96442837Pt) からお気軽にお知らせください。
