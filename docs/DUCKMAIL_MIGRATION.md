# Duckアドレス生成ツールの集約

## 正式な保管場所

- リポジトリ: teruluce/teruluce.github.io
- フォルダ: tools/duckmail/
- 公開URL: https://teruluce.github.io/tools/duckmail/
- 一覧: https://teruluce.github.io/tools/

## 2026-11-02 — ChatGPTの移転作業記録

ユーザーの依頼により、別リポジトリ duck-address-generator を公開用 /tools/ に集約します。
移転元と移動先に同一の生成・検証・メールアプリ連携スクリプトが既存配置されていたため、移動先の動作コードは変更せず、編集先をこのフォルダに統一しました。移転元のMIT Licenseも配置しています。

| 旧URL | 移動先 |
| --- | --- |
| /duck-address-generator/ および /duck-address-generator/index.html | /tools/ |
| /duck-address-generator/duckmail/ および /duck-address-generator/duckmail/index.html | /tools/duckmail/ |

旧HTMLは自動転送と手動リンクに置き換えます。固定の移動先を使い、旧URLのクエリ・フラグメントは渡しません。canonicalも新URLを指します。旧リポジトリは履歴と転送用に保持します。

GitHub PagesではHTTPステータスによる301/308転送を設定できないため、location.replaceとmeta refreshを使います。検索エンジンの移転認識やインデックス更新時期は保証しません。移転先のcanonicalとサイトマップはすでに新URLを指しています。

## 検証範囲

- 移転元・移動先の動作スクリプトが同一。
- Chromiumで旧トップ・旧ツールのディレクトリURLとindex.htmlからそれぞれの移動先へ到達。
- JavaScriptが無効でもmeta refreshで到達。
- 戻る操作で旧URLの転送ループが起きない。
- 移動先でアドレス生成、入力不正時のエラー、Gmail/標準メールアプリリンク、コピーを確認。
- iPhone実機でのメールアプリ起動と検索インデックスの移転完了は未検証。

## 他の変更との関係

サイト全体のデザイン統一PR #9とは独立した移転です。PR #9はこの正式配置を保つため、移転のためにマージする必要はありません。
