### Dockerとは
- 仮想化技術のひとつ
- 従来(サーバー仮想)よりもDockerのコンテナ仮想のほうが軽量でプロセッサやメモリの消費が少なくストレージの使用もわずか
- 開発環境や実行環境の構築が主
- Docker image:コンテナを作るために必要なもの。配布や携帯ができる
- Docker file:Docker imageの設計書、textファイル

### コマンド
- $docker login :ログイン
- $docker pull {イメージ名:タグ名} :Docker Hubから落とす対象を指定
- $docker images :イメージ一覧
- $docker run {イメージ名:タグ名} :イメージからコンテナを作成※作成後exitする
- $docker run it {イメージ名:タグ名} bash :イメージからコンテナを作成後コンテナの中に入る
- $docker ps -a :アクティブなコンテナを表示
