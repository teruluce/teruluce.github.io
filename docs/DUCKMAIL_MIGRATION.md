# ツールの正式配置（2026-11-02）

ユーザーの最終指定により、ツールの正式な保管先は **teruluce/teru-tools**、公開トップは **https://teruluce.github.io/teru-tools/** です。
Duckmailは duckmail/index.html にあります。全8ツールは専用トップから選べます。

teruluce.github.io の / はディズニー系の入口、About Meは既存の /aboutme/ を維持します。
このリポジトリの旧 /tools/ と公開済み3ツールのURLは、新しい /teru-tools/ の対応ページへ転送します。転送は固定URLのみを使い、旧クエリやフラグメントは引き継ぎません。

旧duck-address-generatorは公開HTMLを削除して終了し、リポジトリ自体も削除対象です。削除APIが連携にないため、リポジトリ本体の削除はGitHub Settingsからユーザー操作が必要です。MIT Licenseは移転先のduckmail/LICENSEに保存しています。

## てる側の4リポジトリ

1. teruluce/teruluce.github.io — ディズニー系入口・About Me
2. teruluce/disney-bgs — BGS Chronicles
3. teruluce/disney-discovery — Disney Discovery
4. teruluce/teru-tools — ツール専用サイト

個人用のyuuki0928gitリポジトリは別枠です。

## 過去の変更との関係

当初は /tools/ への集約と旧サイトの転送を行いましたが、ユーザーの指定で上記の別リポジトリ運用に変更しました。PR #9のデザイン・機能はteru-toolsのPR #1へ引き継ぎ、#9はマージせず閉じています。
