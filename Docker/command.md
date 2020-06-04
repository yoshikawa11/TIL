### Dockerとは
- 仮想化技術のひとつ
- 従来(サーバー仮想)よりもDockerのコンテナ仮想のほうが軽量でプロセッサやメモリの消費が少なくストレージの使用もわずか
- 開発環境や実行環境の構築が主
- Docker image:コンテナを作るために必要なもの。配布や携帯ができる。Docker imageはimage layerから構成される。
               layerごとに更新・追加されることでコンテナ間で共有・省エネとなる
- Docker file:Docker imageの設計書、textファイル
- コンテナを実行すると自動的にroot権限になる
- 指定しない限りコンテナからホストOSにアクセスできない
- コンテナ名はランダムに設定される、オプションで指定可能

### コマンド
- $docker login :ログイン
- $docker pull {イメージ名:タグ名} :ローカルのimageを探し、ない場合Docker Hubのレポジトリから落とす対象を指定
- $docker images :イメージ一覧
- $docker run {イメージ名:タグ名} :イメージからコンテナを作成※作成後exitする
- $docker run it {イメージ名:タグ名} bash :イメージからコンテナを作成後コンテナの中に入る
- $docker ps -a :アクティブなコンテナを表示
- $exit :コンテナを停止する。ステータスはExited
- $docker run --name {コンテナ名} -it {IMAGE名:TAG名} bash :コンテナ作成時に名前を指定
- $docker restart {コンテナ名} :コンテナの再起動
- $ctrl + p + q :depatchしてコンテナから抜ける(コンテナは起動したまま)※detachすると，そのプロセスは残る．detach後に再度$docker execでコンテナに入って                      exitしても，前にdetachしたプロセスは残り続ける．なのでExitedにならない．detachした時のそのプロセスに戻るには$docker attach ｛コンテナ                      名/ID｝を実行し、そこでexitするとStatusがExitedになる。
                 execは新規プロセスを利用する。
- $docker exec -it {コンテナ名} bash :動いているコンテナに入る
