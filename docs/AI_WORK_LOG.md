# AI Work Log

このログは、サイト運営に関するAI作業の引き継ぎ記録です。作業担当・変更内容・検証範囲・公開状態を区別して記録します。未確認の事項は確認済みと記載しません。

## 2026-10-21 — ChatGPT：About Meページを落ち着いたカフェ風に調整

- **作業AI:** ChatGPT
- **対象サイト:** https://teruluce.github.io/aboutme/
- **リポジトリ:** https://github.com/teruluce/teruluce.github.io
- **対象ファイル:** `aboutme/index.html`
- **依頼:** 以前の木目調背景が不自然に感じられるため、木目を廃止し、落ち着いたカフェのような雰囲気に変更する。
- **変更内容:** 木目画像を使った背景を無地のグレージュに変更。カードをオフホワイトにし、枠線・影・角丸を控えめに調整。文字色を落ち着いたグレー系に整え、プロフィール写真のセピア調フィルターを解除。本文、プロフィール情報、リンク先は意図的に変更していない。
- **変更理由:** 木目の強い質感を避け、自然で清潔感のある落ち着いたデザインにするため。
- **ブランチ:** `design/aboutme-calm-cafe`
- **PR:** https://github.com/teruluce/teruluce.github.io/pull/4
- **状態:** ユーザーがPRをマージしたと報告。マージコミットSHAはこの記録作成時には未確認。
- **検証結果:** GitHub上の `aboutme/index.html` の更新内容を確認。実ブラウザでのPC／スマートフォン表示、公開ページへの反映、画像の実表示はこの作業記録作成時点では未確認。
- **Claudeとの連携:** この変更をClaudeが確認・レビューしたかは未確認。共通ログへの記録を追加したが、Claude側への自動通知・自動同期を保証するものではない。
- **次の作業:** 公開ページの表示を確認。必要に応じてClaudeに本ログとPR差分を確認してもらい、レビュー結果を追記する。

## 2026-10-21 — ChatGPT：Tools Personalのデザインを統一

- **作業AI:** ChatGPT
- **対象サイト:** Tools Personal（ツール一覧・Duckmail・ルーレット）
- **リポジトリ:** https://github.com/teruluce/teruluce.github.io
- **対象ファイル:** `tools/index.html`、`tools/duckmail/index.html`、`tools/roulette/index.html`、`tools/favicon.svg`
- **依頼:** 3ページのデザインを統一する。
- **変更内容:** 淡い水色・白・ネイビーを基調に共通の配色、見出し、余白、カード、ボタン、入力欄、注意書き、フッターのスタイルを追加。ファビコンを水色系に変更し、ルーレットにも設定。DuckmailのOGPサイト名をTools Personalに統一。一覧ページの入れ子になっていたfooter構造を修正。ツールのJavaScript機能、本文説明、canonical URL、サイトマップURLは意図的に変更していない。
- **変更理由:** ページごとの見た目の違いを減らし、統一感と安心感のあるツールサイトにするため。
- **ブランチ:** `design/unify-tools-personal`
- **PR:** https://github.com/teruluce/teruluce.github.io/pull/6
- **状態:** PR作成済み・未マージ。公開サイトへの反映は未確認。
- **検証結果:** GitHub上の変更後ファイルを再取得し、3ページすべてに共通デザインCSSがあること、CSS閉じタグ、ルーレットのファビコン設定、一覧ページのfooter構造を確認。実ブラウザのPC／スマートフォン表示、実機での操作、公開環境への反映は未確認。
- **Claudeとの連携:** Claudeによるレビューは未実施・未確認。PR #6の差分をレビュー対象にできる。
- **次の作業:** PR #6の差分を確認し、問題がなければマージ。マージ後に公開ページをPC／スマートフォンで確認し、必要なら見た目を微調整する。

## 2026-11-02 — ChatGPT：公開用URLクリーナーを追加

- **作業AI:** ChatGPT
- **対象サイト:** https://teruluce.github.io/tools/url-cleaner/
- **対象ファイル:** `tools/index.html`、`tools/sitemap.xml`、`tools/url-cleaner/{index.html,cleaner.mjs,app.mjs,cleaner.test.mjs,README.md}`、本ログ。
- **依頼:** yuuki側と同じURLクリーナーを、てる側の公開用ツールとして追加し、SEOも整備する。
- **変更内容:** 既知の追跡パラメータをブラウザ内で自動削除し、コピー・共有・削除項目と件数を表示。未知のクエリ、生のエンコード・順序・重複、パス・フラグメント、既知の署名付きURLを保持。既存の水色・白・ネイビーのデザインに統合し一覧に追加。
- **SEO:** 日本語タイトル・description・canonical・OGP・Twitterカード・index/follow・使い方と説明本文・toolsサイトマップを追加。既存robots.txtのAllowとルートサイトマップからtoolsサイトマップへの参照を確認済み。検索エンジンへの登録・順位を保証するものではない。
- **プライバシー:** URL送信・履歴保存・短縮URLの展開なし。Web Share TargetはiOS/iPadOSの受信対応とブラウザ内処理の要件を考慮して未実装。
- **ブランチ:** `codex/add-url-cleaner`
- **公開状態:** PR作成用の変更。未マージ・未公開。
- **検証結果:** Node.jsの処理テスト6件成功。Chromiumで375/768/1440px幅、横はみ出しなし、自動処理、コピー、共有API呼び出し（モック）、不正URL、クリア、一覧からの導線、JSエラーなしを確認。SEOメタ情報、canonical、h1が1個、サイトマップを確認。
- **未検証・制約:** iPhone/iPad実機のネイティブ共有とLINE送信、公開後のクロール・インデックスは未確認。未知の署名方式やすべてのサイトの動作は保証できない。Claudeレビューは未実施。

## 2026-11-02 — ChatGPT：トップページにツールへの導線を追加

- **依頼:** トップページからいろいろなツールに進めるようにする。
- **変更:** `index.html` にTools Personal一覧、URLクリーナー、Duckアドレス生成、ルーレットへのカードを追加。descriptionとキーボードフォーカス表示を調整。
- **検証:** Chromiumで375/768/1440px幅の表示、カード4件、横はみ出しなしを確認。各リンク先のHTTP 200を確認済み。
- **公開:** 公開用PRとして反映予定。公開後の状態はGitHubのマージ・Pagesデプロイ状況を参照。
