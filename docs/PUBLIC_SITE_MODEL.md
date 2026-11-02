# 個人用サイトをモデルにした公開版

個人側のトップとツールをモデルに、てる側の公開サイトを統一しました。

- モデル: `yuuki0928git/yuuki0928git.github.io` の `ca2587f9d2aab6a5d7fa46aba33005fe756917d0`
- 公開側: `teruluce/teruluce.github.io`
- 個人側はこの作業では変更していません。

## URLの対応

| 個人側 | 公開側 |
| --- | --- |
| / | / |
| /tools/ | /tools/ |
| /duckmail/ | /tools/duckmail/ |
| /roulette/ | /tools/roulette/ |
| /split/ | /tools/split/ |
| /timer/ | /tools/timer/ |
| /qr/ | /tools/qr/ |
| /url-cleaner/ | /tools/url-cleaner/ |
| /constellation/ | /tools/constellation/ |
| /rally/ | /tools/rally/ |

## 公開用の調整

- トップは円のモチーフ・書体・行リンクをモデルにし、teru_luceの名前・制作サイト・SNS・About Meへ案内します。個人側の氏名・メール・LINE等は移植していません。
- ツールは生成りとグリーンの配色にそろえ、共通CSSを `tools/site.css` に置きます。ことば星座は元の夜空の表現を保ちます。
- Duckアドレス生成は公開版の入力検証・Gmail・標準メールアプリの機能と詳しい説明を保ちました。
- 全8ツールをトップ・一覧・ツール内ナビから選べます。個人側では一覧に出ていなかった星座とラリーも掲載しています。
- タイトル・description・canonical・OGP・Twitterカード・robots・サイトマップを公開側のURLに設定しています。トップのGoogle所有権確認と既存のDisney・About Meサイトマップも保持しています。
- 各ページに使い方・公開用注意事項を設けています。星座の言葉は共有URLと履歴等に残ること、ラリーの最高得点はlocalStorageへ保存することを明記しています。

## 次回の更新

自動同期は導入していません。個人側の変更を採用する際は、URLの配置、公開側の既存機能、外部リンク、説明、canonicalとサイトマップを確認して反映してください。モデルのHTMLをそのまま上書きすると、公開用の案内が消える可能性があります。

## 検証

- Chromiumでトップ・一覧・8ツールを375/768/1440px幅で確認。横はみ出しなし、h1とcanonicalとrobotsを確認。
- QR生成・SVG出力、Duck宛先生成とメールアプリリンク、割り勘計算、タイマーの開始・リセット、グループ分け、URL削除とコピー、星座の生成と共有URL、ラリーの起動・操作を確認。
- URLクリーナーの処理テスト6件成功。XMLサイトマップ3件を解析確認。
- iPhone/iPad実機、全アプリの共有先、バックグラウンドの通知音、検索エンジンのインデックスは未検証。

