## RUN
```
ANSIBLE_NOCOWS=1 ansible-playbook -i hosts ./run_first.yml --private-key=~/.ssh/XXX.pem
```

## やること
- インストール(install.yml)
- 情報収集(collect_basic_info.yml)
- バックアップ
  - /etc以下を /etc.bakに
  - /home/isucon を/home/isucon/home.tar.gzに
  - データベースをすべて~/database_backup.sqlに
    - `mysql -u root データベースの名前 < ~/database_backup.sql`で読み込み
- MySQL
  - バージョン確認
- Nginx
  - バージョン確認
  - kataribeを~/kataribeにダウンロードして解凍
- Python
  - バージョン確認
  - which python (pyenv使ってるかどうかの確認)
- その他セットアップ
  - reload.shを~/に配置
  - .vimrcを配置
  - zshをセットアップ(prezto使用)
    - aliasいくつか追加(zshrcに記載)
  - git aliases追加
    - graph, co, ci, s
  - pecoインストール（履歴の検索用）