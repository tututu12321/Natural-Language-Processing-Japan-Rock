
### 邦ロック歌詞分析

このプロジェクトは、日本語の歌詞を分析するために、以下の手法を使用します。

## 使用手法
- **Word2Vecによるベクトル化**: 歌詞の単語をベクトル空間に変換し、単語の意味的な関連性を捉えます。
- **コサイン類似度計算**: 単語間の類似度を計算し、類似した単語やフレーズを特定します。
- **感情分析**: 各行に対してポジティブまたはネガティブな感情を判定します。感情ラベルは以下のように分類されます。
  - 0: 悲しみ
  - 1: 喜び
  - 2: 怒り
  - 3: 驚き
  - 4: 恐れ
  - 5: 嫌悪
  - 6: 期待
  - 7: 信頼
- **K-meansクラスタリング**: 歌詞をテーマやスタイルに基づいてグループ化します。
- **階層的クラスター分析**: 歌詞を階層的にクラスタリングし、類似性を視覚化します。
- **ワードクラウド生成**: 歌詞の中で頻出する単語を可視化し、テーマを理解します。
- **t-SNEによる次元削減**: 高次元データを2次元に可視化し、データの構造を分析します。

## セットアップ

1. Google Colabで新しいノートブックを作成します。
2. 必要なライブラリをインストールします。

```python
# 必要なライブラリのインストール
!pip install gensim
!pip install sklearn
!pip install wordcloud
!pip install matplotlib
!pip install janome
!pip install nltk
```

3. 分析対象のデータをColabにアップロードします。

## 分析ステップ

### 1. Word2Vecでベクトル化し、コサイン類似度を計算
- Word2Vecを用いて日本語の歌詞をベクトル化し、各行の歌詞間でコサイン類似度を計算します。

### 2. 日本語歌詞のトークン化
- 形態素解析モデル（Janomeなど）を使用して、日本語の歌詞を単語に分割（トークン化）します。

### 3. コサイン類似度の計算
- ベクトル化された歌詞のコサイン類似度を計算し、歌詞間の類似性を測定します。

### 4. 感情分析
- 歌詞の各行に対して感情分析を行い、ポジティブかネガティブかを判定します。

### 5. 感情分析モデルの準備
- 感情分析用にスクリプトでモデルを準備し、日本語の歌詞に適した分析を行います。

### 6. 日本語の形態素解析モデルのロード
- Janomeなどの日本語形態素解析モデルを使用して、歌詞の内容を分析します。

### 7. 歌詞のクラスタリング
- 歌詞の内容に基づき、ジャンルやアーティストごとにクラスタリングを行います。

### 8. ワードクラウドの生成
- 歌詞テキストからワードクラウドを生成し、頻出単語の可視化を行います。

### 9. t-SNEによる次元削減
- 調整されたパープレキシティを用い、2次元空間に次元削減を行い、歌詞間の関係を視覚化します。

## Google Colabでの実行

各セルにコードを記述し、順番に実行していきます。適宜、データやグラフの表示などを確認しながら進めることが推奨されます。
```

この内容をREADME.mdにそのままコピーして、必要に応じてプロジェクトの進捗や詳細を追加して完成させてください。
