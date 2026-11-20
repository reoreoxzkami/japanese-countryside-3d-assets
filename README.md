# SEO個別ページサイト（静的HTML 12ページ）— 2026-11-20制作

## 目的と背景
宣伝サイト https://pjqipl.readdy.co は Readdy のSPAで、実質1ページ構成のため sitemap が1URLしかなく、Googleで「クロール済み - インデックス未登録」が続いている。
対策として、パックごとに実HTMLの個別ページを持つ静的サイトを別途用意した。Readdy側はそのまま残す（既存のSearch Console所有権タグやIndexNow鍵は触らない）。

## 構成（全12ページ・検証済み）
- `/` ホーム（全パックグリッド＋コレクション導線）
- `/packs/<slug>/` ×10（kominka / shinto-shrine / rice-terraces / roadside-props / river-waterfall / unmanned-station / abandoned-school / showa-shopping-street / forest-floor-rocks / fishing-harbor）
- `/collection/` コレクション専用ページ（$24.99 / 単品合計$80.90 / BF $12.49）
- `sitemap.xml`（12 URL・XML妥当性確認済み）、`robots.txt`
- 各ページ: title重複なし、H1は1つ、meta description、canonical、OG、パックページは Product JSON-LD、内部リンク切れなし（全ページ自動チェック済み）
- 画像は実シーンのレンダー（images/scene-v7.jpg, 450KB）

## 公開先（決定：GitHub Pages）
- 2026-11-20 ユーザー選択により GitHub Pages で公開。BASE は `https://reoreoxzkami.github.io/japanese-countryside-3d-assets` に差し替えて再生成済み。
- 画像はバイナリをリポジトリに置かず、itch CDN（img.itch.zone）の実カバー画像URLをページごとに参照する（パック別カバー＋コレクションカバー、いずれもReaddy宣伝サイトで使用中の実URL）。
- リポジトリ: reoreoxzkami/japanese-countryside-3d-assets

## 公開後にやること
- Search Consoleに新プロパティ（または既存プロパティ配下なら sitemap.xml を追加送信）
- IndexNowで12 URLを一括送信（既存の鍵が使えるのは pjqipl ドメインのみ。新ドメインなら鍵を再設置）
- dev.to記事（11/24）・itch各パックページ・SNSプロフィールからリンクを張る
- Black Friday終了後（12/1）にセール表記を通常価格へ戻す（Readdy側バナー撤去と同時）
