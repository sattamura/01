# 06 Web戦略リサーチ：横浜元町ショッピングストリート公式サイト リニューアル提案

作成日：2026-11-17　担当：リサーチャー（Web戦略）
提案者：ディシーワークス／CMJ（ウェブ制作・取材）

---

## 0. 調査方法と制約（必読）

- **公式URL**：協同組合元町エスエス会（元町SS会）の公式サイトは **https://www.motomachi.or.jp/**（WordPress。`/wp-content/uploads/` 配下のPDFあり）。英語版は `https://www.motomachi.or.jp/en/` 配下にある。
- **実地取得の制約**：本セッションのネットワーク設定で `www.motomachi.or.jp` と `www.ginza.jp` へのアクセスが拒否された（プロキシ403、WebFetchはENOTFOUND）。このため、HTMLソース・表示速度・meta description・ナビ構成は**直接は確認できていない**。診断は**検索エンジンにインデックスされたページ（URL・タイトル・抜粋）からの外形診断**であり、【要実機確認】と付けた項目は提案前にブラウザ、PageSpeed Insights、Search Consoleで確かめる必要がある。
- **検索回数の上限**：WebSearchは約20回実行したところでセッション全体の上限に達した。神楽坂、二子玉川、代官山、GA4、Core Web Vitals、LLMO（AI検索）の個別調査は実行できなかった。これらの項目は、2026年時点の一般的な業界知識をもとに【一般知識・出典未検証】と明記して書いている。追加調査が必要なら、ドメインの許可設定と検索回数上限の引き上げを行ったうえで再実行する。

---

## 1. 現行サイトの実地診断（外形診断）

### 1-1. 把握できた事実

| 観点 | 把握できた内容 | 出典 |
|---|---|---|
| CMS | WordPress（`/wp-content/uploads/2024/02/…pdf` などPDF資料をアップロード） | [motomachi.or.jp PDF](https://www.motomachi.or.jp/wp-content/uploads/2024/02/2dbd992ce2e4a922f48db708223e4f80.pdf), [2021プレスリリースPDF](https://motomachi.or.jp/wp-content/uploads/2021/02/Release_Motomachi.ChinaTown210212.pdf) |
| 構成 | `/news/`、`/event/{slug}/`、`/charming_sale/`、`/en/`（`s_type_cat`＝業種別、`s_name_cat`＝頭文字別のショップ分類）、`/en/contact` | 検索インデックス（下記URL） |
| イベント情報 | チャーミングセール2026春（2/21〜3/1）・2026秋（9/19〜9/27）、クリスマスイルミネーション2026（11/4〜12/25、点灯式11/8）、スーパー耐久マシンお披露目（2026年3月）、元町ハマフェスセール（2025年5月）、元町ハマフェスワンダーストリート（2026年5月、市観光サイトに掲載） | [news](https://www.motomachi.or.jp/news/), [秋セール](https://www.motomachi.or.jp/event/yokohamamotomachi-charmingsale2026autumn/), [Xmas2026](https://www.motomachi.or.jp/event/christmasillumination2026/), [春セール](https://www.motomachi.or.jp/event/yokohamamotomachi_charmingsale2026spring/), [supra_z](https://www.motomachi.or.jp/event/supra_z/), [横浜市観光](https://www.welcome.city.yokohama.jp/eventinfo/ev_detail.php?bid=yw12357) |
| 店舗検索 | 英語版で業種別（food / accessories 等）と頭文字別（a〜z）の一覧。キーワード検索、営業時間での絞り込み、地図連動はインデックス上で確認できない【要実機確認】 | [EN food](https://www.motomachi.or.jp/en/s_type_cat/food), [EN accessories](https://www.motomachi.or.jp/en/s_type_cat/accessories), [EN y](https://www.motomachi.or.jp/en/s_name_cat/y) |
| 多言語 | 英語版あり。中国語（簡体字・繁体字）と韓国語のページはインデックスで見つからない | [EN contact](https://www.motomachi.or.jp/en/contact) |
| SNS | 2021年時点でX（旧Twitter）「【公式】横浜元町shopping st.」@yokohamamtmc、Instagramハッシュタグ #yokohamamotomachi の運用実績あり。英語版contactページにFacebookリンクあり。現在のInstagram公式アカウント名は確認できなかった | [ASCII 2021](https://weekly.ascii.jp/elem/000/004/052/4052850/), [横浜市観光 T03742](https://www.welcome.city.yokohama.jp/topics/tp_detail.php?tpid=T03742) |
| 店舗数表記 | 「200以上」「230超」「約250」「211」と、出典ごとに数字がばらばら | [gltjp](https://www.gltjp.com/en/directory/item/14295/), [横浜市 空き店舗DB](https://translate-en.city.yokohama.lg.jp/business/kigyoshien/syogyo/akitenseido/datebase/touroku29020.html), [Tokyo Weekender](https://www.tokyoweekender.com/japan-life/european-charm-and-great-shopping-in-yokohamas-motomachi-area/) |

### 1-2. 評価（10観点）

| 観点 | 評価 | 所見 |
|---|---|---|
| ①構成 | △ | ニュース、イベント、セール、ショップの基本は揃っている。ただし「街の魅力を伝える読み物」「モデルコース」「アクセス・駐車場」など来街の判断材料になるコンテンツはインデックス上で目立たない。 |
| ②店舗検索 | △ | 業種別・頭文字別のみ。「今営業中」「ギフト」「老舗」「英語対応可」「免税」「キャッシュレス」など目的別の切り口がない。地図連動、Googleマップへのリンク、多言語の店舗詳細も確認できない【要実機確認】。 |
| ③イベント情報 | ○〜△ | 大型イベントはきちんと更新されている。ただしslugの命名規則がばらばら（`-charmingsale2026autumn`／`_charmingsale2026spring`／日本語をエンコードしたslug）。カレンダー表示やEvent構造化データの有無は【要実機確認】。終了したイベントは「本イベントは終了しました」と表示して残しているので、アーカイブとしては使える。 |
| ④多言語 | × | 英語のみ。2025年の訪日客は過去最高の4,268万人で、消費額は中国・台湾・米国・韓国・香港の順に多い（[JNTO](https://www.jnto.go.jp/news/press/20260121_monthly.html), [観光庁PDF](https://www.mlit.go.jp/kankocho/content/001992584.pdf)）。簡体字・繁体字・韓国語がないことは機会損失が大きい。 |
| ⑤スマホ対応 | 【要実機確認】 | WordPressなのでレスポンシブの可能性は高い。ただし店舗一覧が頭文字別でページが分かれる作りは、スマホでは回遊しにくい。 |
| ⑥更新頻度 | △ | イベント更新は年に数回の大型企画が中心（春秋のセール、ハマフェス、クリスマス、単発イベント）。店舗の新着や季節の読み物を日常的に更新している形跡は少ない。 |
| ⑦SNS連携 | △ | アカウントが外部の記事から見つけにくい（2021年の記事頼み）。サイトからSNSへの導線、Instagram投稿の埋め込み、UGC（#yokohamamotomachi）の活用が弱いとみられる。 |
| ⑧デザイン印象 | 【要実機確認】 | 実画面を取得できなかったため評価を保留。「ハマトラ発祥」「港町の洋館」という街のブランド資産をビジュアルで表現できているかが焦点になる。 |
| ⑨表示速度 | 【推測】△ | WordPressで画像やPDFの多いイベント告知中心の構成なので、LCP（最大の要素の表示時間）が遅くなりやすい傾向がある。PageSpeed InsightsでLCP、INP、CLSを実測する。 |
| ⑩SEO（title/description） | × | **検索結果では `/news/` も各 `/event/…/` も、titleがすべて「横浜元町ショッピングストリート」で同じ**。英語ショップ一覧も「SHOP INFORMATION」で同じ。ページごとに固有のtitleがなく、検索やAI検索で個別ページが評価されにくい。meta descriptionは【要実機確認】。 |

### 1-3. 現行サイトの課題リスト（優先度順）

1. **ページ固有のtitle・descriptionがない**（全ページ共通タイトル）→ SEOとAI検索での評価が低くなる。
2. **中国語（簡体字・繁体字）と韓国語に未対応**。結果として、多言語情報は第三者サイト（gltjp、japan.travel、tsunagujapan等）が担っている。
3. **店舗データベースが弱い**：業種と頭文字だけで探す作り。地図、営業時間、対応言語、決済、免税などの属性がなく、Googleビジネスプロフィール（GBP）とも連携していない。
4. **公式な店舗数がひとつに定まっていない**（200〜250で表記が揺れている）→ データの正本（シングルソース）がない状態。
5. **読み物（ストーリー）が不足**：老舗の歴史、店主の人柄、ハマトラ文化などの資産がサイト上で編集されていない。
6. **SNSと公式アカウントの導線が見えない**。
7. **URL命名と情報設計がばらばら**（slugの揺れ、PDF告知への依存）→ 運用ルールとCMSの型が必要。
8. **計測とKPIの設計が不明**（GA4のキーイベント設定などは【要実機確認】）。

---

## 2. ベンチマーク（国内・海外）

| サイト | 運営 | 良い点（元町に取り入れたい要素） | 出典 |
|---|---|---|---|
| **GINZA OFFICIAL（ginza.jp）** | 一般社団法人銀座インフォメーションマネジメント（GIM、全銀座会の出資） | ①運営を専門法人に集約し、継続的に運用できる体制。②「Shop & Restaurant」は**審査制の会員掲載**で、掲載の質を保っている。③日英の店舗ページに住所、営業時間、電話を揃えて掲載。 | [ginza.jp/?p=176](https://www.ginza.jp/?p=176), [ginza.jp/en/aboutus](https://www.ginza.jp/en/aboutus), [en/shop](https://ginza.jp/en/shop/page/18) |
| **自由が丘オフィシャルウェブサイト（jiyugaoka-abc.com）** | 自由が丘商店街振興組合（制作協力：ジェイ・スピリット） | ①組合の紙媒体（自由が丘新聞・かべ新聞）をウェブで継続公開し、地域メディアとして機能。②**公式LINEアカウント**で地元の生活者とつながる。③元町と同じWordPress基盤で、組合の運営規模に合っている。 | [自由が丘新聞466号PDF](https://www.jiyugaoka-abc.com/wp-content/uploads/2026/04/466.pdf), [かべ新聞PDF](https://jiyugaoka-abc.com/wp-content/uploads/2024/08/kabe169.pdf), [MEGURO+](https://www.city.meguro.tokyo.jp/meguroplus/special_20240315.html) |
| **Regent Street（regentstreetonline.com）** | The Crown Estate | ①「What's on」でポップアップ、展示、上映などを**定期更新**。②クリスマスライト点灯など、**看板イベントを街のブランドにする**運営。③会員限定オファー（Events & Offers）を**週次で更新**し、再訪の動機をつくる。 | [regentstreetonline.com](https://www.regentstreetonline.com), [about](https://www.regentstreetonline.com/about), [Crown Estate Events & Offers](https://www.thecrownestate.co.uk/our-business/property-and-places/retail-and-leisure/property-management/property-management-events-&-offers) |
| **Marylebone Village（marylebonevillage.com）** | Howard de Walden Estate | ①**店舗ディレクトリ**（store-directory）と「街の歴史」ページの二本柱。②紙の「Marylebone Journal」と連動した**編集型コンテンツ**で、Villageというブランドを育てている。③Food & Drink / Fashion & Beautyなど、来街者の目的に沿った分類。 | [About](https://marylebonevillage.com/about-us), [Our history](https://marylebonevillage.com/about-and-visit/our-history), [HDWE retail](https://www.hdwe.co.uk/our-properties/retail-and-leisure), [Diplomat Magazine](https://diplomatmagazine.com/the-exciting-hum-of-marylebone-village-retail-destination/) |
| **日本橋高島屋（多言語の参考）** | 高島屋 | 日本語・英語・中国語（繁体字・簡体字）・韓国語の**4言語5表記を切り替えるメニュー**。商業施設の多言語化の標準形。 | [takashimaya.co.jp](https://www.takashimaya.co.jp/nihombashi/departmentstore/topics/campaign.html?page=1) |
| 参考：原宿表参道欅会 | 商店街振興組合 | Visaと組んだ訪日客向けショッピングキャンペーン（2019）。決済事業者との協業の例。 | [TCVB PDF](https://tcvb.or.jp/jp/forum/TSW2019_press%20release.pdf) |

※ 表参道（omotesando.or.jp）、日本橋（nihonbashi-tokyo.jp）、神楽坂、二子玉川、代官山の公式サイトは、検索で一次情報を確認できなかった（または検索上限に達した）。本書では比較対象から外している。

**ベンチマークから得られる共通原則**
1. 運営主体を明確にし、編集体制を持つ（銀座GIM、Crown Estate、Howard de Walden）。
2. 「店舗DB」と「読み物」を両輪にする（Marylebone）。
3. 看板イベントと、定期的に更新する小ネタを組み合わせる（Regent Street）。
4. 紙・LINE・ウェブを連動させ、地元の生活者とつながる（自由が丘）。

---

## 3. 2026年時点のベストプラクティス

### 3-1. 店舗データベース＋Googleビジネスプロフィール（GBP）連携
- 店舗の正本（名称、住所、電話、営業時間、業種、対応言語、決済手段、免税、バリアフリー、創業年）を**サイトのDBに一元化**する。GBPとの差異は組合事務局がチェックする。
- GBPは「統制は本部（組合）、写真と現場の情報は店舗」という役割分担が実務の定石。全店に同じ投稿文を流すと重複として評価が下がるので注意する（[0120.co.jp](https://0120.co.jp/blog/shobai-ai-90/), [sungrove](https://www.sungrove.co.jp/businessprofile-manager/), [ASPIC](https://www.aspicjapan.org/asu/article/9523)）。
- サイトの店舗ページには「Googleマップで開く」「電話」「公式SNS」ボタンを置き、GA4で計測する。

### 3-2. 多言語（英・中簡・中繁・韓）
- 2025年の訪日客は4,268万人で過去最高。消費額は中国2.0兆円、台湾1.2兆円、米国1.1兆円、韓国0.99兆円、香港0.56兆円の順（[JNTO](https://www.jnto.go.jp/news/press/20260121_monthly.html), [観光庁](https://www.mlit.go.jp/kankocho/content/001992584.pdf), [honichi](https://honichi.com/news/2026/01/21/inbound202512/)）。**繁体字（台湾・香港）の優先度は簡体字と同等以上**と考える。
- 方針：店舗DBの定型項目は機械翻訳＋用語集で自動生成し、街紹介、アクセス、モデルコース、看板イベントは人が翻訳・監修する。言語ごとにURLを分け（`/en/` `/zh-hans/` `/zh-hant/` `/ko/`）、hreflangを設定する。

### 3-3. AI検索（AIO/LLMO）対策と構造化データ
- JSON-LDで `ShoppingCenter`（または `Place`）を街全体に、`LocalBusiness`（Store/Restaurant等）を各店舗に、`Event` を各イベントに、`Article`（著者付き）を読み物に、`BreadcrumbList` をパンくずに付ける。NAP（名称・住所・電話）、営業時間、areaServedを正確に記載する（[mapatlas](https://mapatlas.eu/ja/blog/google-ai-overviews-local-business), [BrightLocal](https://www.brightlocal.com/learn/ai-google-business-profile-homepage/), [SE Ranking](https://seranking.com/blog/ai-overviews/)）。
- 注意：構造化データがAI Overviewsへの掲載を直接左右するという公式の確認は今回の調査では得られなかった。Googleは「AI機能向けの特別な最適化は不要。通常のSEOの基本が有効」という立場をとっている【一般知識・出典未検証：Google Search Central「AI features and your website」】。LLMO対策の本質は**一次情報（店主の言葉、歴史、正確な営業データ）を、固有のtitleと見出しで構造化して公開すること**であり、llms.txtなどは補助策にとどめる。
- 「元町 ハマトラ とは」「元町 ランチ 老舗」「Motomachi Yokohama what to buy」など、**質問の形をしたFAQページ**を多言語で用意する。

### 3-4. 読み物（店主インタビュー）コンテンツ
- CMJの取材力を活かし、月2本程度の「元町の人」連載（老舗3代目、新店オーナー、職人など）を掲載する。各記事から店舗DBへリンクし、`Article`＋`author` の構造化データを付ける。Marylebone Journal型の編集ブランドを目指す。
- 年1回、ベスト記事を紙の冊子（多言語版を含む）にまとめ、ホテルや観光案内所で配布する。

### 3-5. デジタルマップ
- Google Maps Platform（またはMapbox）で、通り（1〜5丁目）と裏通りの店舗をピン表示し、業種・言語・免税で絞り込めるようにする。現在地を表示し、モデルコースをルートとして描く。駐車場、トイレ、授乳室、AED、コインロッカーなど、来街の不安を解消する情報も載せる。

### 3-6. イベントカレンダー
- 月表示とリスト表示を用意し、`Event` 構造化データ、ICS／Googleカレンダー追加、多言語表示に対応する。チャーミングセール（2月・9月）、ハマフェス（5月）、クリスマス（11〜12月）を「年間の看板」として固定のLPにし、毎年同じURLで更新する（例：`/charming-sale/`）。年度ごとの個別URLはやめる。

### 3-7. 会員店舗が自分で更新できるCMS
- WordPressを継続（もしくはヘッドレス化）し、**店舗アカウント権限**を持たせる。店舗は自店の営業時間、お知らせ、写真、クーポンだけを編集でき、公開前に事務局が承認する。フォームは定型化し、文字数制限と写真比率のガイドを設ける。
- 店舗向けに半日の操作講習を実施し、スマホから投稿できるようにする（LINE連携の投稿フォームも検討）。

### 3-8. アクセシビリティ
- 2024年4月施行の改正障害者差別解消法で、民間事業者にも**合理的配慮の提供が義務化**された。ウェブアクセシビリティの確保（環境の整備）は努力義務の位置づけ（[issoh](https://www.issoh.co.jp/column/details/17566/), [Web担当者Forum](https://webtan.impress.co.jp/e/2024/04/09/46700)）。
- 目標：JIS X 8341-3:2016 適合レベルAA（WCAG 2.xのAA相当）に準拠する。代替テキスト、コントラスト、キーボード操作、動画字幕、PDF告知のHTML化を行う。アクセシビリティ方針ページも公開する。

### 3-9. 表示速度（Core Web Vitals）
- 【一般知識・出典未検証】2024年3月にINPがFIDに代わって指標になった。目標値はLCP 2.5秒以下、INP 200ミリ秒以下、CLS 0.1以下。画像はWebP/AVIFで遅延読み込みし、CDNを使う。

### 3-10. KPI設計（GA4）

| 層 | KPI | GA4での計測方法 |
|---|---|---|
| 最終成果（来街・売上） | 来街者数（人流データ／カウンター）、セール期間の売上（加盟店アンケート） | GA4の外で計測。サイトの指標と月次で突き合わせる |
| 行動（来店につながる行為） | 「地図で開く」「経路」「電話タップ」「店舗公式サイト・SNSへ遷移」の数 | キーイベント：`click_map` `click_tel` `click_outbound_shop` |
| 関心 | 店舗詳細ページの閲覧数、店舗検索の利用数、イベントページの閲覧数、カレンダー追加数 | `view_shop` `search`（推奨イベント） `add_to_calendar` |
| 集客 | 自然検索の流入とクリック数（Search Console連携）、言語別セッション、SNSからの流入、AI検索からの参照（chatgpt.com、perplexity.ai などのreferrer） | 参照元レポート、言語ディメンション |
| 運用 | 店舗による自己更新の件数／月、情報鮮度（90日以上更新のない店舗の割合）、記事の公開本数 | CMSログ |

初年度の目標案（暫定）：自然検索流入 前年比+50%、多言語セッション比率15%以上、来店行動キーイベント 月3,000件、店舗の自己更新率60%以上。

---

## 4. 新サイト構成案（サイトマップ）

```
/ （トップ：今週の元町／看板イベント／読み物／店舗検索窓／マップ）
├─ /shops/                店舗検索（業種・目的・言語・免税・営業中で絞り込み＋地図）
│   └─ /shops/{shop-slug}/  店舗詳細（LocalBusiness構造化データ、GBPリンク、店主記事へのリンク）
├─ /map/                  デジタルマップ（丁目別、モデルコース、施設情報）
├─ /events/               イベントカレンダー（月／リスト）
│   ├─ /charming-sale/    チャーミングセール（固定URLで毎年更新）
│   ├─ /hamafes/          元町ハマフェス
│   ├─ /christmas/        クリスマスイルミネーション
│   └─ /events/{slug}/    単発イベント
├─ /stories/              読み物（店主インタビュー、老舗の系譜、ハマトラ、季節特集）
├─ /guide/                来街ガイド（アクセス、駐車場、モデルコース、FAQ、バリアフリー）
├─ /about/                元町について（歴史、街づくり協定、元町SS会、プレス）
├─ /news/                 お知らせ／プレスリリース
├─ /members/              加盟店向け（ログイン、入会案内、マニュアル、出店相談）
├─ /en/ /zh-hans/ /zh-hant/ /ko/   多言語（shops / map / events / guide / stories の主要部分）
└─ /accessibility/ /privacy/ /contact/
```

---

## 5. 段階的ロードマップ

| フェーズ | 期間 | 内容 | 成果物 |
|---|---|---|---|
| **0. 診断** | 1か月 | アクセス解析、Search Console、PageSpeedの実測。店舗データの棚卸し（店舗数の正本化）。加盟店ヒアリング | 現状レポート、KPIの基準値 |
| **1. 応急改善（クイックウィン）** | 1〜2か月 | 全ページ固有のtitle・description、構造化データ（Organization/Event）、GA4キーイベント設定、SNS導線、PDF告知のHTML化 | 既存サイトの改善 |
| **2. 基盤リニューアル** | 4〜6か月 | 新しい情報設計とデザイン、店舗DB＋店舗による自己更新CMS、デジタルマップ、イベントカレンダー、英語版の刷新、アクセシビリティAA | 新サイト公開（チャーミングセール秋に合わせる案） |
| **3. 多言語・コンテンツ拡充** | 6〜12か月 | 簡体字・繁体字・韓国語の公開、「元町の人」連載（月2本）、FAQ、モデルコース | 多言語版、記事24本／年 |
| **4. 運用高度化** | 2年目〜 | GBP一括運用支援、会員オファーやデジタルクーポン、LINE連携、AI検索の引用状況のモニタリング、年次冊子 | 月次レポート、四半期改善 |

体制案：ディシーワークスが設計・開発・保守を担当、CMJが取材・編集・翻訳ディレクションを担当、組合事務局が承認・店舗窓口を担当。月1回の定例でKPIをレビューする。

---

## 6. 出典一覧

**元町（現行サイト・周辺）**
- https://www.motomachi.or.jp/news/
- https://www.motomachi.or.jp/event/yokohamamotomachi-charmingsale2026autumn/
- https://www.motomachi.or.jp/event/yokohamamotomachi_charmingsale2026spring/
- https://www.motomachi.or.jp/event/christmasillumination2026/
- https://www.motomachi.or.jp/event/supra_z/
- https://www.motomachi.or.jp/charming_sale/
- https://www.motomachi.or.jp/en/s_type_cat/food
- https://www.motomachi.or.jp/en/s_type_cat/accessories
- https://www.motomachi.or.jp/en/s_name_cat/y
- https://www.motomachi.or.jp/en/contact
- https://www.motomachi.or.jp/wp-content/uploads/2024/02/2dbd992ce2e4a922f48db708223e4f80.pdf
- https://motomachi.or.jp/wp-content/uploads/2021/02/Release_Motomachi.ChinaTown210212.pdf
- https://www.welcome.city.yokohama.jp/spot/details.php?bbid=814
- https://www.welcome.city.yokohama.jp/eventinfo/ev_detail.php?bid=yw12357
- https://www.welcome.city.yokohama.jp/topics/tp_detail.php?tpid=T03742
- https://weekly.ascii.jp/elem/000/004/052/4052850/
- https://www.gltjp.com/en/directory/item/14295/
- https://kanagawa-kankou.or.jp/spot/1117
- https://news.allabout.co.jp/articles/o/101419/
- https://www.tokyoweekender.com/japan-life/european-charm-and-great-shopping-in-yokohamas-motomachi-area/

**ベンチマーク**
- https://www.ginza.jp/?p=176 ／ https://www.ginza.jp/en/aboutus ／ https://ginza.jp/en/shop/page/18
- https://www.jiyugaoka-abc.com/wp-content/uploads/2026/04/466.pdf ／ https://www.city.meguro.tokyo.jp/meguroplus/special_20240315.html
- https://www.regentstreetonline.com ／ https://www.regentstreetonline.com/about ／ https://www.thecrownestate.co.uk/our-business/property-and-places/retail-and-leisure/property-management/property-management-events-&-offers
- https://marylebonevillage.com/about-us ／ https://marylebonevillage.com/about-and-visit/our-history ／ https://www.hdwe.co.uk/our-properties/retail-and-leisure ／ https://diplomatmagazine.com/the-exciting-hum-of-marylebone-village-retail-destination/
- https://www.takashimaya.co.jp/nihombashi/departmentstore/topics/campaign.html?page=1
- https://tcvb.or.jp/jp/forum/TSW2019_press%20release.pdf

**ベストプラクティス・統計**
- https://www.jnto.go.jp/news/press/20260121_monthly.html ／ https://www.mlit.go.jp/kankocho/content/001992584.pdf ／ https://honichi.com/news/2026/01/21/inbound202512/
- https://mapatlas.eu/ja/blog/google-ai-overviews-local-business ／ https://www.brightlocal.com/learn/ai-google-business-profile-homepage/ ／ https://seranking.com/blog/ai-overviews/
- https://www.issoh.co.jp/column/details/17566/ ／ https://webtan.impress.co.jp/e/2024/04/09/46700
- https://0120.co.jp/blog/shobai-ai-90/ ／ https://www.sungrove.co.jp/businessprofile-manager/ ／ https://www.aspicjapan.org/asu/article/9523
