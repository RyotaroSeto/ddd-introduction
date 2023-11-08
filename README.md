# ddd-introduction
「実践ドメイン駆動設計」から学ぶDDDの実践入門

## 第1章　「DDDへの誘い」〜ドメイン駆動設計のメリットとはじめ方〜

### DDDを導入するメリット
- 顧客と開発者が1つのチームになり、設計と実装を1つのソフトウェアとして構築できる
- 顧客がソフトウェア開発がビジネス的事業価値を高めること。という認識になるため、開発費用を「コスト」から「事業投資」という認識になる
- 「ドメインモデル」を使用することでシステム開発の複雑さに対応できる(将来的に複雑になるシステムはDDDで開発した方がよい)

### ユビキタス言語とは
- ドメインエキスパートや開発者を含めたチーム全体で作り上げる共通言語のこと。(日本語)

### ユビキタス言語の見つけ方
- ドメインに登場する用語について名称とアクションを記載する
- 「用語集」を作成する。用語の候補と採用/却下理由を記載する
- 用語集作成が困難な場合、すでに存在するドキュメントを集めて、重要な用語やフレーズを取り出す

### DDD導入への説得材料
- ビジネス的価値
  - 組織としてコアドメインに注力し、有益なモデル(コード)を作成できる
  - 事業と業務を正しく理解し定義できる
  - ドメインエキスパートがソフトウェアを設計できる
  - よりよいユーザー体験を提供できる
- 技術的価値
  - モデル感の境界を明確に定められる
  - エンタープライズアーキテクチャを整理できる
  - アジャイルでイテレーティブなモデリングを継続的に行える
  - 新しいツール(戦略:ユビキタス言語、戦術:エンティティ)を使える

### DDD導入を阻害するもの
- 増える作業量
  - 対策: 価値を生み出すためには、新たな検討時間が増えることは必須と割り切る
- 多忙なドメインエキスパート
  - 対策:お菓子や飲み物のプレゼントや趣味の雑談をきっかけにし、彼らが興味をもつユビキタス言語で関心を誘う
- 開発者の抵抗
  - 対策:技術的視点から業務的視点に関心を移す。それをオブジェクト指向設計で実装できるメリットを理解してもらう
 
### ドメインモデルを構築する優先順位
1. ドメインで一番重要な「コアドメイン」にエースエンジニアを投入し、戦術的設計を行う
2. コアドメイン以外で重要な「汎用サブドメイン」においても戦術的設計の検討をおこなう
3. 重要ではない「支援サブドメイン」では状況に応じて判断する

コアドメインに注力し、それ以外はDDDを採用するか状況に応じて検討する


## 第2章 「ドメイン」「サブドメイン」「境界づけられたコンテキスト」

### 「境界づけられたコンテキスト」とは
- ドメインの部分を解決する部分のこと

**「アカウント」という言葉の場合(業種によって意味が異なる)**

|業種|「アカウント」という用語の意味|
|--|--|
|会計システム|勘定科目|
|営業管理システム|顧客|
|コンピューターシステム|ログイン権限|

**ECサイトのタイミングに応じた「商品」の呼び名の変化**
|順番|「商品」の取り扱い状態|「商品の呼び名」|
|--|--|--|
|1|予約中|入荷待ち|
|2|入荷時|出荷中|
|3|販売中|在庫品|
|4|販売後|出庫品|
|5|トラブル発生時|不良品|

このように「アカウント」や「商品」という言語が、2つ以上の意味を持たないように「境界づけられたコンテキスト」を適切に分割し、プログラムの複雑化を防ぐ


### ドメイン(問題領域)の評価ポイント
1. 戦略的コアドメインの名前、ビジョン、検討すべき概念が正しいか
2. 必要な支援サブドメインと汎用サブドメインの抜け漏れがないか
3. 各ドメインの担当者を招集可能か

### 境界づけられたコンテキスト(解決領域)の評価ポイント
1. 既存ソフトウェア資産の把握
2. 新規ソフトウェア資産の検討
3. 既存ソフトウェアと新規ソフトウェアの統合方法検討
4. 依存する関連プロジェクトのリスク検討
5. ユビキタス言語の抜け漏れの確認
6. 境界づけられたコンテキスト間における「重複または共有しているユビキタス言語」の調査とマッピング方法/変換方法検討
7. コアドメインの概念が境界づけられたコンテキストに適切にふくまれているか確認
