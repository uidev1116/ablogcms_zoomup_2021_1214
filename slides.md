---
theme: penguin
background: https://source.unsplash.com/collection/94734566/1920x1080
highlighter: prism
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
eventLogo:
  https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png
eventUrl: https://ablogcms-zoomup.doorkeeper.jp/events/129702
twitter: '@poorman_ui'
twitterUrl: https://twitter.com/poorman_ui
layout: intro
title: ふむふむと聞くだけで明日から使える！ a-blog cmsの小技集
---

# ふむふむと聞くだけで明日から使える！ a-blog cmsの小技集

<p class="text-right mr-[24px]">有限会社アップルップル 宇井 陸登</p>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: presenter
presenterImage: '/profile.jpg'
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# とりあえず自己紹介

- 2021年4月からアップルップルで働く、新米フロントエンドエンジニア
- a-blog cmsを使用した受託制作を担当している
- JavaScriptやフロントエンドの周辺ツールについて勉強中
- 2021年9月には「assign-holiday」というJSライブラリをリリース
- 好きな食べ物はすりおろしたりんご🍎

---
layout: text-image
media: '/undraw_schedule_re_2vro.svg'
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# お品書き

- 自己紹介
- a-blog cms の小技を1つ1分以内くらいのテンポで紹介
  - 自分で考えた編
  - slackで募集した編
- 最後に

---
layout: text-window
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---
# サイトのロゴマークをトップページだけh1タグで表示する

Webサイトのロゴマークをトップページだけh1タグで表示して、その他のページではpタグで表示したいです。

::window::

```html
<!-- BEGIN_IF [%{BID}/eq/1/and/%{VIEW}/eq/top] --><h1 class="p-header-title"><!-- ELSE --><p class="p-header-title"><!-- END_IF -->
  <a href="%{HOME_URL}">
    <img
      src="%{MEDIA_ARCHIVES_DIR}{site_logo@path}"
      alt="{site_name}"
      width="307"
      height="48"
      role="img"
      class="p-header-title__logo acms-img-responsive"
    >
  </a>
<!-- BEGIN_IF [%{BID}/eq/1/and/%{VIEW}/eq/top] --></h1><!-- ELSE --></p><!-- END_IF -->
```

---
layout: text-image
media: '/server-env-checklist.png'
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---
# サイト公開前にはサーバー環境情報を確認

管理画面チェックリスト及び、サーバーにinfo.phpを設置して確認します。

特に `max_input_vars` は99999 など多めに設定するのがおすすめです。

[公式ドキュメント](https://developer.a-blogcms.jp/document/trouble-shooting/entry-2898.html)

---
layout: new-section
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# モジュールIDや、コンフィグセット、ルールはインポート・エクスポートできます😚

最初は、インポート・エクスポートできること知らなくて、ローカル環境で設定したモジュールIDやコンフィグセットを本番環境でもう一度設定し直すという非効率なことをしていました…🤔

---
layout: text-window
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# メディアのカスタムフィールドでwidthとheightを設定する

メディアのカスタムフィールドには悲しいことに、画像のカスタムフィールドのように幅と高さを出力してくれる変数がありません。😂

320×240 のように幅と高さをまとめて出力してくれる変数はあるので、`split` 校正オプションを活用しています。😎

::window::

```html
<img
  src="%{MEDIA_ARCHIVES_DIR}{sample_img@path}"
  width="{sample_img@imageSize}[split(' x ', 0)]"
  height="{sample_img@imageSize}[split(' x ', 1)]"
  alt="{sample_img@alt}"
  class="acms-img-responsive"
>
```
---
layout: new-section
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# 管理ボックスはカスタマイズできます☺️

[コンテンツ専用の「エントリー作成」ボタンで、よりわかりやすく。](https://developer.a-blogcms.jp/document/practice/specialized_button.html)

上記の公式ドキュメントがわかりやすいです。

---
layout: new-section
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---
# エントリーコードが空の場合はエントリーのタイトルをタイトルタグに出力しない

<div class="grid grid-cols-2 gap-4">
  <div class="text-left">

  [一道さんの記事](https://kazumich.com/entry-5044.html)で言及されている通り、a-blog cmsでエントリーを作成する際にはエントリーコードを空にして作成することができます。

  エントリーコードを空にしてエントリーを作成すると、そのエントリーのOGPモジュールによって出力されるタイトルタグが エントリータイトル | カテゴリー名 | ブログ名 となってしまいますが、OGPモジュールの設定をすることで カテゴリー名 | ブログ名 として出力させることが可能です。

  </div>
  <div>

  ![空のエントリーコードの場合はタイトルを含めない](/empty-entry-code.png)

  </div>

</div>

---
layout: new-section
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# PDFのサムネイル画像に任意のページを選択する

<div class="grid grid-cols-2 gap-4">
  <div class="text-left">

  メディア機能で登録されたPDFのサムネイル画像はPDFファイルが複数ページある場合、任意のページをサムネイル表示することができます。☺️

  </div>
  <div>

  ![PDFのサムネイル画像に任意のページを選択できます](/select-pdf-thumbnail.png)

  </div>

</div>


---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# Entry_Summary系のモジュールでecdを表示する

<div class="grid grid-cols-2 gap-4">
  <div class="text-left">

  Entry_Summary系のモジュール（Entry_ListやEntry_Headline）ではエントリーコードを表示することができませんが、Entry_Fieldモジュールとエスケープ、ctx の機能を組み合わせることで新しくモジュールIDを作成することなく表示できます。

  右のコードでは組み込みJSのscrollToのアンカーリンク先を設定するために実装しています😯

  </div>
  <div>

  ```html
  <!-- BEGIN_MODULE Entry_List id="{{module_id}}"-->
  <div class="c-local-nav">
    @include("/admin/module/setting.html")
    <ul class="c-local-nav__list">
      <!-- BEGIN entry:loop -->
      <li><a <!-- BEGIN_MODULE\ Entry_Field ctx="bid/%{BID}/cid/%{CID}/eid/{eid}" --> href="#\{code\}[trim4ext('.html')]" class="c-local-nav__item scrollTo -\{code\}[trim4ext('.html')]<!-- END_MODULE\ Entry_Field -->">
        <p class="c-local-nav__title">{title}<span class="text-word-break">について</span></p>
        <i class="fas fa-angle-down c-local-nav__ico"></i>
      </a></li>
      <!-- END entry:loop -->
    </ul>
  </div>
  <!-- END_MODULE Entry_List -->
  ```

  </div>

</div>

---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# ページャーの総エントリー数が色々便利な件 🥳

Entry_Summary や Entry_Body などのページャーが使用できるモジュールで表示できる `{itemsAmount}` という変数が便利

- カテゴリーで絞り込んだときの件数表示に役立つ！
- エントリーの件数が〇〇件だった場合〇〇したいといった場合に最適 🤩

<br>
<br>
<br>
<br>

ページャーという機能名からは想像がつきにくい使い方ができます 😇

---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# 管理画面ではSelect2というJavaScriptが使用できる

<div class="grid grid-cols-2 gap-4 mt-16">
  <div class="text-left">

  選択肢の多いセレクトボックスのカスタムフィールドを実装するときに便利 🤓

  ```html
  <select name="prefs" class="acms-admin-form-width-mini js-select2">
    <option value="" selected>都道府県</option>
    <option value="北海道" {prefs:selected#北海道}>北海道</option>
    <option value="青森県" {prefs:selected#青森県}>青森県</option>
    <option value="岩手県" {prefs:selected#岩手県}>岩手県</option>
    ...省略
  </select>
  <input type="hidden" name="field[]" value="prefs" />
  ```

  </div>
  <div>

  ![select2を使用したセレクトボックス](/select2-demo.png)

  </div>

</div>

---

<style>

  h1 {
    font-size: 28px!important;
  }

  p {
    margin: 0!important;
  }

  pre {
    max-height: 400px!important;
  }

</style>

# select2を使って複数の値を選択できるselectボックスを作る

<div class="grid grid-cols-2 gap-4">
  <div>

  <span>HTML</span>

  ```html
  <select name="prefs[]" class="js-select2" style="width: 300px;" multiple>
    <option value="" selected>都道府県</option>
    <option value="北海道" {prefs:selected#北海道}>北海道</option>
    <option value="青森県" {prefs:selected#青森県}>青森県</option>
    <option value="岩手県" {prefs:selected#岩手県}>岩手県</option>
    ...省略
  </select>
  <input type="hidden" name="field[]" value="prefs" />
  ```

  <div class="mt-[40px]">

  ![複数選択できるセレクトボックス](/multiple-select2.png)

  </div>

  </div>

  <div>

  <span>CSS</span>

  ```css
  .select2-container .select2-selection--multiple.acms-admin-selectbox {
    min-height: auto;
    padding: 0;
    background-color: #fbfbfb;
    border: 1px solid rgba(0, 0, 0, 0.2) !important;
  }

  .select2-container .select2-selection--multiple.acms-admin-selectbox[aria-expanded='true'] {
    background-color: #fff;
    border-color: rgba(0, 0, 0, 0.2);
  }

  .select2-container .select2-selection--multiple.acms-admin-selectbox .select2-selection__rendered li {
    padding: 2px 5px;
  }

  .select2-container .select2-selection--multiple.acms-admin-selectbox .select2-search__field {
    min-height: auto;
    line-height: 1;
  }

  .select2-container .select2-selection--multiple.acms-admin-selectbox .select2-search__field:focus {
    background: none;
    border: none;
    box-shadow: none;
  }
  ```

  </div>

</div>

---
class: text-center
---

# ここで少し一休み 🍵

<div v-click class="text-left text-xl font-bold font-serif absolute bottom-[24px]">

次は、a-blog cms公式slackチャンネルでa-blog cmsユーザーの方々が投稿してくださった技を紹介します。！

</div>

---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# グローバル変数の値も表示されます！ベンチマークモード 😎

<img src="/benchimark-mode.png" alt="ベンチマークモードに全グローバル変数の出力内容が表示されている画像" class="m-auto" >

---
layout: new-section
---

# IFブロックが意図通り動かない時あるある

😱

<style>

    p {
      font-size: 64px;
    }

</style>

---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# IFブロックの値に改行が入るとIFブロックが動かない

<div class="grid grid-cols-2 gap-4" >

  <div>

  たとえば右のような記述は `{hoge}` に改行（コード）が含まれているとIFブロックが正常に動作せず、全部表示されてしまいます 😭

  </div>

  <div>

  ```html
  <!-- BEGIN_IF [{hoge}/lk/あいうえお] -->
  <p>あいうえおが含まれます</p>
  <!-- ELSE -->
  <p>あいうえおが含まれていません</p>
  <!-- END_IF -->
  ```

  </div>

</div>


---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# IFブロックの値に演算子が入るとIFブロックが動かない

- また、先程のコードで `{hoge}` にIFブロックで使用するオプション（演算子）が入っている場合も動作しません
- 例えば、値として `/category/field/fuga/lk/あいうえお` が入力された場合、"あいうえおが含まれていません" というテキストが表示されてしまいます。


---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# …その結果

<div class="grid grid-cols-2 gap-4" >

  <div class="flex flex-col gap-y-8">

  - 変数に改行が入力される可能性がある場合は、 `[delnl]` の校正オプション
  - 変数にオプション（演算子）が入植される可能性がある場合は、 `[convert('A')]` の校正オプション

  ```html
  <!-- BEGIN_IF [{hoge}[convert('A')|delnl]/lk/あいうえお] -->
  <p>あいうえおが含まれます</p>
  <!-- ELSE -->
  <p>あいうえおが含まれていません</p>
  <!-- END_IF -->
  ```

  </div>

  <div class="text-center flex justify-center items-center">

  <span class="text-[120px]"> 🙂 </span>

  </div>

</div>


---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# 〇〇_Fieldと〇〇Fieldの違い

〇〇_Fieldという名前がつけられているフィールドモジュールとEntry_SumamryやEntry_Body といった一部のモジュールの中に存在する〇〇Field（フィールドブロック）は名前が似ていることもあり、とってもややこしいことでしょう 🤔

細かい違いはいくつかありますが、実装時にどちらを使用するかの選定基準としては以下になると思います 🧐

フィールドモジュールはモジュールなのでエスケープして使用することができます。逆にフィールドブロックはブロックなので実行順序を操作する事ができません。


---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# クエリストリングの値（バリュー）をグローバル変数で取得する

たとえば、`https://developer.a-blogcms.jp/document/search.html?keyword=テスト&start=1` というURLのページで↓のHTMLを記述すると

```html
<p>クエリストリングを取得：%{start}</p>
```

出力結果は「クエリストリングを取得：1」 となります。

僕が、最もよく利用するのは、[Custom Search API との連携
](https://developer.a-blogcms.jp/document/externalservice/custom-search-api.html) して、サイト内検索を実装するときでしょうか 🤔

---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# Field_Searchモジュールでカスタムフィールド検索の値を保持する

- [Field_Searchモジュール](https://developer.a-blogcms.jp/document/customfield/entry-1707.html#entry-1) を使用することで、カスタムフィールドで検索したとき、検索結果のテンプレートで検索したカスタムフィールドの値を表示できます。
- `<option value="red" {color:selected#red}>赤色</option>` の `{color:selected#red}` の記述を動かすことができます。
- また、検索後のURLが https://example.com/field/color/red/ となっているときに↓のようにField_Searchモジュールを使うと red のように `{color}` の値が表示できます。

```html
<!-- BEGIN_MODULE Field_Search -->
<p>{color}</p>
<!-- END_MODULE Field_Search -->
```


---
eventLogo: 'https://dzpp79ucibp5a.cloudfront.net/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekI3QVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b58ed7b62454fe7eb5a6d291314ef342bb897970/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RTNKbGMybDZaVjloYm1SZmNHRmtXd2RwQWNocEFjZz0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--e0e57e8ab7f02a9e57804bb53ef80c2bdc861848/logo_community.png'
eventUrl: 'https://ablogcms-zoomup.doorkeeper.jp/events/129702'
twitter: '@poorman_ui'
twitterUrl: 'https://twitter.com/poorman_ui'
---

# 最後に

- slackでの募集に回答していただいた皆様！ありがとうございました 🙇
- 発表を聞いてくださった参加者の皆様もありがとうございました 🙇
- Twitterもよろしければフォローお願いします 🐦
  - [@poorman_ui](https://twitter.com/poorman_ui)
