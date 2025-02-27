### 重要なお知らせ

10月7日追記：削除するのでなくアーカイブ化してほしいという[リクエスト](https://github.com/Yuki2718/adblock/issues/67)があったため、今後メンテナンスするものは新レポジトリに移行します。

管理人の環境変化により、来年からこれまでのようにフィルタを提供することが難しくなります。**そのため、Yuki's uBlock Japanese filtersファミリーなどの更新・公開を10月いっぱいを目途に停止する**つもりです。申し訳ありませんが、ユーザーの方はAdGuard Japanese<sup>1</sup>などへの乗り換えをご検討ください。現時点で公開を停止する予定のものは、

- Yuki's uBlock Japanese filters
- Yuki's uBlock Japanese filters - Paranoid
- Yuki's uBlock Japanese filters - Mobile
- Yuki's uBlock Japanese filters - Social
- Yuki's uBlock Japanese filters - Annoyancesとそのサブリスト
- Yuki's uBlock Japanese filters - Annoyances Plus
- Anti Anti-adblock Enhancer for AdGuard (AdGuard Japanese filter Plusに組込み予定)
- Placeholder Hider with no generic hiding （他リストより早く公開停止予定）

です。**AdGuardやuBlock Originのフィルターへの貢献は続けます**が、規模は縮小することになるでしょう。また、AdGuard MV3用にAdGuard Japanese filterの強化パッチを準備中ですが、これの構成を少し変えてuBlock OriginやuBlock Origin Liteでも使えるようにします。したらばの雪フィルタ簡易報告スレッドはアーカイブ化し、メンテナンスを続けるリスト用に新たなスレッドを作る予定です。なお、これらのリストはGPLv3のAnti Anti-adblock Enhancer for AdGuardを除きすべてCC BY-SA 4.0ですので、それぞれのライセンス要件を満たす限り改変、再配布は自由です。これまで貢献いただいた方にはお詫びいたしますとともに、ご理解を願います。質問やご要望等ございましたら、[したらば](https://jbbs.shitaraba.net/bbs/read.cgi/internet/25463/1652115193/)（本来、問題報告用ですがこの件については例外とします）か管理人の[Twitter](https://twitter.com/Yuki27183)にコメントいただければ可能な範囲で対応いたします。

<sub>1: AdGuard Japaneseは単独使用を想定していませんので、内製やEasyListの併用が必要です。</sub>

### Chromium Manifest V3（MV3）について

Chrome, Edge上でuBlock Originをご利用の方は、主に４つの選択肢があります
- ブラウザをBraveかFirefoxに移行し、uBlock Originを使う

  <sup>FirefoxもいずれMV3に移行しますが、それによりuBlock Originが使えなくなることはありません※</sup>

- AdGuard MV3かuBlock Origin Liteが完成するのを待つ

  <sup>現時点ではいずれもベータ版以前の状態です。完成しても性能は今より落ちます。</sup>
 
- AdGuard for Windows/Macに移行

  <sup>uBlock Origin並みのフィルタリング精度を得るにはHTTPSフィルタリングを有効にしてください</sup>

- Braveブラウザに移行する

  <sup>ブラウザ組込みのブロッカーとしては唯一、uBlock Originに[準ずる性能](https://github.com/Yuki2718/adblock/wiki/Japanese-FAQ#q1-3-%E3%83%96%E3%83%A9%E3%82%A6%E3%82%B6%E7%B5%84%E8%BE%BC%E3%81%BF%E3%81%AE%E3%83%96%E3%83%AD%E3%83%83%E3%82%AB%E3%83%BC%E3%81%AF%E3%81%A9%E3%81%86%E3%81%A7%E3%81%99%E3%81%8B)があります</sup>

<details>
<summary>移行先として不適当なもの</summary>

あくまで、uBlock Originからの移行先としては問題があるという意味で、個人的に満足しているなら問題ありません。

- Vivaldiの組込みブロッカー

  <sup>ルール数制限はないものの、フィルタの表現力がMV3対応ブロッカーより大幅に劣ります</sup>

- DNSやhostsなどドメイン単位のブロック

  <sup>Vivaldiよりさらに劣る、きわめて粒度の荒いブロックしかできません</sup>

- Adblock Plus

  <sup>フィルタスタッフが日本語用フィルタを準備中ですが、外国人にどこまでできるか懸念が残ります。また、方針としてアンチ広告ブロックに対応しません</sup>

</details>

 <sup>※ 追記：blocking webRequestを維持するからしばらく大丈夫なのではなく、仮にblocking webRequestを廃止することになっても大丈夫なはずです。[ChromiumのMV3と互換性を維持しながら、ブロッカーの機能への悪影響を抑えたMV3を実装することは十分可能です](https://github.com/uBlockOrigin/uBlock-issues/issues/338#issuecomment-534261690)。本当の問題はChromium MV3がアドオン開発者の声を[十分に聞いて反映するのでなく](https://github.com/uBlockOrigin/uBlock-issues/issues/338#issuecomment-465093102)、あくまでGoogleのペースとロジックで進められており、それでいてプライバシー保護効果への疑問には[ちゃんと答えていない](https://www.eff.org/deeplinks/2019/07/googles-plans-chrome-extensions-wont-really-help-security)ことです。[ビジネスパートナーであり](https://github.com/uBlockOrigin/uBlock-issues/issues/338#issuecomment-496009417)、そもそもMV3の影響をそれほど強く受けないeyeo社のような都合のいい声だけ[聴いても](https://blog.chromium.org/2020/12/manifest-v3-now-available-on-m88-beta.html)意味がありません。Mozillaはアドオン開発者の声をしっかり聴いて調整していくことを[約束して](https://blog.mozilla.org/addons/2022/05/18/manifest-v3-in-firefox-recap-next-steps/)おり、十分な代替がみつかるまではblocking webRequestを維持するとしています。MozillaのMV3を指揮するRob Wu氏はList Authors Chatという広告ブロックの「現場」にも加わっており、広告ブロック界隈とのつながりが以前より強い人です。仮にブロッカーの機能に一定の制約が出ても、それで実際にプライバシー保護につながるのであればuBlock Originの作者が反対するとは考えられず、どこかで妥協点を探すことになるでしょう。</sup>

（[FAQ A1-4](https://github.com/Yuki2718/adblock/wiki/Japanese-FAQ#q1-4-chrome%E6%8B%A1%E5%BC%B5%E6%A9%9F%E8%83%BD%E3%81%AEmanifest-v3mv3%E7%A7%BB%E8%A1%8C%E3%81%A7%E5%BA%83%E5%91%8A%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E6%8B%A1%E5%BC%B5%E3%81%AF%E4%BD%BF%E3%81%88%E3%81%AA%E3%81%8F%E3%81%AA%E3%82%8B%E3%81%A8%E8%81%9E%E3%81%8D%E3%81%BE%E3%81%97%E3%81%9F)も参照）

### お知らせ（2022年7月27日：Youtube広告および不具合について）

※古いお知らせは随時消していきます。

Youtubeで動画が再生できない不具合がこれまで散発的に報告されてきましたが、特定のプレイヤーサイズおよび/あるいは解像度（かつ特定の動画？）で発生することがわかりました。問題となっているルールを無効化してしまうと広告が出るため、これから対応が検討されると思います<sup>1</sup>。ユーザーの方は当面の間、プレイヤーサイズの変更で対応していただくしかありません<sup>2</sup>。この不具合はAdblock Plus, AdGuard, uBlock Originで共通です（おそらくBraveも）。

Chrome, Edgeなどではブラウザの起動直後はYoutube広告を確実にブロックできません。この問題でお悩みのuBlock Originユーザーは、オプションの「フィルターリスト」下にある「フィルターリストをすべて読み込むまで、ネットワークアクティビティを停止する」にチェックを入れることで対応できます。ただし、[別の問題](https://github.com/uBlockOrigin/uBlock-issues/issues/1973)が起こる可能性もあります。

<sub>1. あるパラメータをURLに付与すると回避できるようですが、パラメータの付与は現在のuBlock Originではできません。もしこれが解決に必須であれば、以前から検討されている「信頼済みリスト」が導入される可能性があると思います。これは特定のリスト、おそらくは内製フィルタのみにリスクの高い特権的な操作を認めるものです。仮定の話ですが、そうなった場合はこれまでのようにYuki's uBlock Japanese filtersの単独使用はもはやおすすめできなくなります。</sub>

<sub>2. 広告が出てもよろしければuBlock Originなら`youtube.com#@#+js(set, ytInitialPlayerResponse.adPlacements, undefined)`を追加、AdGuardなら`youtube.com#@%#//scriptlet('set-constant', 'ytInitialPlayerResponse.adPlacements', 'undefined')`を追加してください。</sub>

<details>
<summary>（2022年6月12日：4月20日分の追記）</summary>

Braveは以前よりChromiumのManifest V2（MV2）サポート終了後もMV2のサポートを継続すると[明言](https://github.com/brave/brave-browser/issues/20059)していましたが、本当にできるのかはまだわかりません。実際にuBlock Originが2023年1月以降もBraveで利用可能なのであれば、Yuki's uBLock Japanese filtersファミリーでのBraveのサポートは見送るかもしれません。

</details>

<details>
<summary>（2022年5月10日：Brave Shield不具合簡易報告スレッドの開設）</summary>

[Brave Shield不具合簡易報告スレッド](https://jbbs.shitaraba.net/bbs/read.cgi/internet/25463/1651822005/)を開設いたしました。Yuki's uBLock Japanese filtersファミリーで将来的にBrave組み込みの広告ブロック（Shield）をサポートするための情報収集を兼ねます。改めて強調しますが、**現時点ではサポートしていません**。Brave Shieldはブラウザ組み込みのブロッカーとしてはもっとも高度なものですが、[以前より](https://github.com/brave/brave-browser/issues/9625)uBlock Originでは生じない[固有の問題](https://github.com/brave/adblock-lists/issues/614)が多く（[現在発生中の例](https://github.com/brave/brave-browser/issues/22719)）、uBlock Originの文法解釈も[常に](https://github.com/brave/adblock-lists/pull/775)本家より一歩遅れているため、それによる問題がたびたび発生しています（[最近の例](https://github.com/easylist/easylist/pull/11918)）。現時点でYuki's uBLock Japanese filtersをBraveで利用されても性能を発揮できないばかりか、不具合のもとになります。

3月21日の予告通り、280blocker adblock filter 悪質サイト対策強化パッチは公開停止いたしました。

</details>

## Yuki's uBlock Japanese filters （雪フィルタ）

日本語サイト閲覧者がPCで遭遇する広告・解析のほとんどを除去できる、**最新版uBlock Origin専用**フィルタです。AdBlock, Adblock Plus, AdGuard, uBlock-for-firefox-legacy, またはBrave, Vivaldi, Berry Browser, Yuzu Browserの組み込みブロッカーなどでは**使わないで**ください[^1]！

- **ご利用の場合は、標準で有効のAdGuard Japaneseは無効にする（設定のフィルターリスト > 地域・言語でチェックを外す）ことをおすすめします。**
- 他所では広告ブロックフィルタでブロックしていても、当サイトでは迷惑要素に分類している場合もあります。ブロックに不足を感じられたら、Annoyancesの購読もご検討ください。
- Android版Firefoxでご利用の場合、Yuki's uBlock Japanese filters - Mobileを併用してください。

Yuki's uBlock Japanese filtersファミリーが適しているのは以下のような方です。

- とにかく徹底的にブロックしたい
- オンラインのアクセス解析、行動追跡が気になる
- 専門サイト、あるいは他人に言えないサイトをよく利用する
- ほかの日本用フィルタではアンチ広告ブロックに遭遇してしまう
- uBlock Origin標準のリストを購読している
- ソーシャルボタンやページ内ポップアップなどの迷惑要素もブロックしたいが、既存のソーシャル/迷惑系フィルタでは満足できない/誤爆が多い
- 速度・効率とブロック力を両立させたい
- 広告を目にしないことより、通信量の削減が第一
- ある程度は悪質サイトやコインマイナーもブロックしてほしい

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-filters.txt&title=Yuki's%20uBlock%20Japanese%20filters">購読する（他の日本用リストは無効化推奨、uBlock Origin以外で使わない）</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-filters.txt)

#### 特徴

<details>
<summary><strong>網羅性</strong></summary>

日本語サイト[^2]のPC用公開フィルタリストとして、2022年2月現在メンテナンスされているものの中で最高のブロック性能を持ちます。とくにアクセス解析については他の日本用フィルタではおまけ程度にしか扱われていませんが、当フィルタはできるだけブロックします[^3]。アンチ広告ブロックについても、日本用フィルタのなかで最も先進的な対策を取り入れています。また、当フィルタの管理人は国際的な広告ブロックコミュニティと連携しているため、YoutubeやFacebookなど個人での対応が困難なサイトにもある程度対応できます（これらのサイトの広告は特定条件でしか出なかったり、人によって出方が違ったりするため、コミュニティでの議論や情報を反映させていただいています）。さらにuBlock Originの新機能を常にいち早く取り入れており、逆にこちらで有用・必要と思われる機能は開発陣に提言するという双方向の機能改善を確立しています[^4]。

</details>

<details>
<summary><strong>ブロック優先</strong></summary>

ブロック可能な対象はできる限りブロックします。これは当然ではなく、他のフィルタではブロック可能でも非表示で済ましているケースが多数あります[^5][^6]。ブロックが困難な場合、HTMLフィルタリングによる除去を試みています（これは広告を根こそぎ取り除きますがEdgeやChrome上で使えず、Firefoxでもいつも可能なわけではありません）。ブロックさえできればよいという中級者以上の方は「汎用整形フィルターを無視する」にチェックを入れてください。表示崩れや多少の広告漏れと引き換えに、パフォーマンスを高めることができます。Yuki's uBlock Japanese filtersファミリーは、その場合でもある程度の性能を維持できます[^7]。

<strong>初心者向け補足：</strong>広告ブロックには、ブロックと非表示（要素隠蔽、整形とも）という２種類の方法があります。ブロックはそのままですが、非表示とは広告を見えなくすることです。広告自体は読み込まれているため、通信量やコンピュータのリソースを消費しますし、悪質広告（Malvertising）の防御もできないことがあります。それでも非表示を使う理由はいろいろありますが、どこまで使うかはフィルタによってまちまちです。当フィルタは世界的に見てもブロックに極振りしたフィルタです。

</details>

<details>
<summary><strong>高効率</strong></summary>

ほとんどのルールがuBlock Originに最適化された、現状唯一の日本用フィルタです。uBlock Originはトークン化という仕組みにより高速処理を実現しています[^8]。ブロックルールがトークン化可能なら、全体のルール数は[処理時間に](https://www.wilderssecurity.com/threads/ublock-a-lean-and-fast-blocker.365273/page-155#post-2831026)[影響しません](https://twitter.com/i/web/status/1289255976198123520)。uBlock Originにおける限り、ルールが多いと重くなるという議論は[ナイーブな直感に基づいた完全な誤りです](https://www.wilderssecurity.com/threads/ublock-a-lean-and-fast-blocker.365273/page-204#post-2975580)が[^9]、ユーザーの体感に[一番影響するのはそうした誤った信念](https://www.wilderssecurity.com/threads/ublock-a-lean-and-fast-blocker.365273/page-162#post-2849890)のようです。当フィルタはできるだけトークン化を意識したルールを心がけており[^10]、整形フィルタについても[最小マッチング](https://github.com/gorhill/uBlock/wiki/Procedural-cosmetic-filters#important)の原則を満たしつつ、できるだけ高速で誤爆の少ないフィルタを使うよう心がけているつもりです。さらに、数か月ごとに冗長なルールとデッドドメインのチェックを行い無駄を省いているほか、スクリプトレットフィルタについてはプロパティや関数のチェックをできる限り行い、不要なルールを追加しないようにしています。

</details>

<details>
<summary><strong>併用可</strong></summary>

日本人作者によるフィルタリストとして初、かつ現状唯一、EasyListなど標準フィルタリストとの併用を考慮しています。具体的にはブロック対象に違いがなく、パフォーマンスや誤爆の観点から問題がない場合、[EasyList](https://easylist.to/easylist/easylist.txt), [EasyPrivacy](https://easylist.to/easylist/easyprivacy.txt), [Peter Lowe's Ad and tracking server list](https://pgl.yoyo.org/adservers/serverlist.php), [uBlock₀ 内製フィルター](https://github.com/uBlockOrigin/uAssets), [AdGuard Base](https://filters.adtidy.org/extension/ublock/filters/2_without_easylist.txt), [AdGuard Tracking Protection](https://filters.adtidy.org/extension/ublock/filters/3.txt), [AdGuard URL Tracking Protection](https://filters.adtidy.org/extension/ublock/filters/17.txt), [Fanboy Enhanced Tracking](https://www.fanboy.co.nz/enhancedstats.txt)など、標準リストおよび併用されることが多そうなリストとルールを統一しています[^11]。これにより重複が排除され、[フィルターリスト]ペインでのフィルタ有効数[^12]が正しく表示されるだけでなく、整形フィルタの多重適用も回避できます。つまり単独でもご利用可能ですが、上述の各種リストと併用した場合でも無駄がありません[^13]。逆にAdGurad Japaneseを除く他の日本用リストは標準リストとの併用が考慮されておらず、パフォーマンス上の影響に加え、まれに競合して不具合やアンチ広告ブロックの原因となることもあり[^14]、Braveの日本用フィルタに採用されなかった[一因](https://github.com/brave/adblock-lists/issues/355#issuecomment-609680337)となっています。また、標準リストで発生する不具合が当該リストで修正されない場合、こちらで修正いたします。以下に主要なフィルタリストとYuki's uBlock Japanese filtersファミリーとの互換性をまとめました（同系統、たとえばAdGuard AnnoyancesならYuki's uBlock Japanese filters - Annoyancesを購読した場合です）。

| リスト名 | 互換性 | 説明 |
|:---|:---:|:---:|
| uBlock内製フィルター, EasyList, EasyPrivacy, Peter Lowe’s Ad and tracking server list, AdGuard Base, AdGuard Mobile Ads, AdGuard Social Media, uBlock₀ filters – Annoyances, Block Outsider Intrusion into LAN, 280blocker domain filter | ◎ | 互換性が最大限考慮されており、併用しても無駄はほとんど生じない |
| AdGuard Chinese, RU AdList, AdGuard URL Tracking Protection, Fanboy Enhanced Tracking, AdGuard Annoyances, EasyList Cookie, Fanboy’s Annoyance, Fanboy’s Social, Fanboy's Notifications Blocking List | ○ | 互換性がある程度考慮されており、多少の無駄は生じるがあまり問題ない（Fanboy系は互換性低め） |
| もちフィルタ, もち拡張フィルタ, いちごフィルタ, ことりフィルタ, ねぎフィルタ, AdGuard Japanese | △ | 併用すると大量の無駄が生じるが、問題が生じるかは未確認 |
| 豆腐フィルタ, 280blocker adblock filter | × | 大量の無駄だけでなく、実際に問題が生じるため併用は非推奨 |

</details>

<details>
<summary><strong>柔軟性</strong></summary>

uBlock Originはインストールしたての状態でも広告ブロッカーとして十分に機能しますが、「広告ブロッカーではなく広域ブロッカー」といっているように、多様な使い方ができます。Yuki's uBlock Japanese filtersファミリーでは様々な用途に合わせたリストを提供しているだけでなく、「ミディアムモード」や「汎用整形フィルターを無視する」など、様々なコンフィギュレーションに最大限対応しています。

</details>

#### 対象
- 広告、アフィリエイトリンク
- 一部のプロモーションコンテンツ（ネイティブ広告）[^15]
- 侵襲性の高いセルフプロモーション[^16]
- アクセス解析、行動追跡、ヒートマップ、バグレポート
- サードパーティーまたはスクリプトを伴うアクセスカウンター
- 一部のトラッキングパラメータ
- 主に上記をブロックしたため生じた枠や不要なスペース
- アンチ広告ブロック
- 迷惑・有害なポップアップ、ポップアンダー、リダイレクト
- 一部の詐欺・悪質サイトや知恵袋の偽サイト（セキュリティーソフトの代わりにはなりません）
- コインマイニングなど、ユーザーの同意を得ずにコンピュータのリソースを浪費するもの
- uBlock Origin標準フィルタリストで生じる不具合の修正

#### 対象外
- サイトの内容と強く関連しており（例：具体的な商品のレビュー）、かつ量が過剰でなくユーザーに不利益・不快感を与えない広告[^17]（「ゲームのブログだからゲームの広告」程度では強く関連しているとみなしません。ただしあるテーマのまとめサイトなどで潜在的な有用性がある場合、画像のみブロックしリンクは残すことがあります）
- 運営母体の系列サイトへのリンクバナーで、それほど不快でないもの[^18]
- アフィリエイトリンクの一般非表示（280blockerさんと同様の[理由](https://280blocker.net/advanced-settings/)）
- 広告ブロッカー検知用の罠スクリプト
- ファーストパーティーの単純なCGI/SSIアクセスカウンターで、広範に使われているもの以外
- プッシュ通知（EasyPrivacyは一部ブロックしていますが、こちらでは悪質なもの以外はAnnoyancesで対応します）
- タイマースキップ（uBlock₀ filtersは対応していますが、まれに不具合を起こすため原則としてAnnoyancesで対応します）
- Google Safe Browsingでカバーされている、またはモバイル限定の悪質サイト
- 失効ドメイン

<details open>
<summary><strong>購読例</strong></summary>

1. 基本

![subscription-ex1](https://user-images.githubusercontent.com/82331005/175021459-8ccd5135-a992-465d-bdd9-54c43db0666d.png)

2. 最小

![subscription-ex2](https://user-images.githubusercontent.com/82331005/175021463-5892c56a-aebf-4e34-9b61-cbab99abaeeb.png)

3. ブロック対象拡大、汎用整形無効

![subscription-ex3](https://user-images.githubusercontent.com/82331005/175021464-8678fc84-0d4f-4c9c-99eb-53ee2b3e6eb1.png)

4. 基本（モバイル）

![subscription-ex4](https://user-images.githubusercontent.com/82331005/175021467-481796fb-c01a-45aa-b2bb-aeb4110cd5d9.png)

</details>

## Yuki's uBlock Japanese filters - Mobile （霜フィルタ）

Android版Firefoxでご利用になる場合、Yuki's uBlock Japanese filtersに加えてこちらも**追加購読**してください。PCでは不要です。標準のAdGuard JapaneseからYuki's uBlock Japanese filters + Yuki's uBlock Japanese filters - Mobileに置き換えた場合（AdGuard Japaneseとの併用は無意味）

1. 高い網羅性とブロック優先主義により、通信量をさらに抑えることができます。
2. ほぼすべてのフィルタがuBlock Originに最適化されているため、一部のページでCPU使用率が抑えられます[^19]。
3. uBlock Origin標準リストによる不具合の修正を受けることができます。AdGuard Mobile Adsともルールを統一しており、無駄はほとんど生じません。
4. uBlock Originをモバイルで使う場合に生じる枠や空白の消し残り等が少なくなります[^20]。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-mob.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Mobile">購読する（Yuki's uBlock Japanese filtersの購読が前提）</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-mob.txt)

## Yuki's uBlock Japanese filters - Paranoid （大雪フィルタ）

Yuki's uBlock Japanese filtersに追加できるフィルタで、多少の不具合を覚悟でより強固にブロックします。<strong>自己責任で使用してください</strong>。トラッキングパラメータも除去するほか、一部、トラッキングパラメータを含むリンクからの移動もブロックします。この場合、<strong>「uBlock Origin は以下のページの読み込みを防ぎました」画面で右側の虫眼鏡アイコンをクリックすると、トラッキングパラメータを除いたURLが（場合によってはいくつか）表示され、そのままクリックできます。</strong>ただし、ブロックするとあまりに煩雑になる場合はブロックしません。また、[Block Outsider Intrusion into LAN](https://github.com/uBlockOrigin/uAssets/blob/master/filters/lan-block.txt)フィルタによるLANへの攻撃を防ぐルールも含みます。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-paranoid.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Paranoid">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-paranoid.txt)

## Yuki's uBlock Japanese filters - Social （あられフィルタ）

ソーシャル要素をブロックするフィルタです。[AdGuard Social media filter](https://kb.adguard.com/en/general/adguard-ad-filters#social)との互換性を重視しており、一部、共通のルールがあります。ブロック優先主義のため、非表示にしかできないものは迷惑度が高いものを除き無視します。また、ブロックできても他の要素まで巻き込んでしまう場合はブロックしません。これらも非表示にしたい方や、海外のサイトもご覧になる方はAdGuard Social mediaを併用してください。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-social.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Social">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-social.txt)

#### 対象

- シェアボタン
- FeedlyとTumblrのフォローボタン
- Lineのいいね/友だち追加ボタン
- 有益性の低い一部のソーシャルウィジェット
- ごく一部のソーシャルログイン
- 一部対象外に該当するが、とくに迷惑なもの

#### 対象外

- Feedly, Tumblr以外のフォローボタンやInstagramバッジ
- Facebook/Twitter動画
- Twitterタイムラインウィジェット
- Facebook、Twitter等の更新情報ウィジェット
- Pinterestの写真ウィジェット（しばしば記事の一部）
- 記事に対するソーシャルメディア上の反応が閲覧できるもの、その他潜在的に有用なもの
- 対象に入るが、ブロックすると対象外まで巻き込むもの
- 対象に入るが、非表示にしかできず、かつ一定の基準を満たさないもの


## Yuki's uBlock Japanese filters - Annoyances （みぞれフィルタ）

広告以外の迷惑要素をブロックするフィルタで、Yuki's uBlock Japanese filtersとの併用を前提とします。一部、[Fanboy's Annoyance List](https://easylist.to/easylist/fanboy-annoyance.txt), [AdGuard Annoyances](https://kb.adguard.com/en/general/adguard-ad-filters#annoyances), [uBlock₀ filters – Annoyances](https://github.com/uBlockOrigin/uAssets/blob/master/filters/annoyances.txt), および[Web Annoyances Ultralist](https://github.com/yourduskquibbles/webannoyances)と共通のルールもあります。AdGuard AnnoyancesおよびuBlock₀ filters – Annoyancesとの互換性を意識していますが、Socialの場合ほどではありません（併用可能ですが、多少の無駄が生じます）。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Annoyances">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances.txt)

#### 対象

- サイト内ポップアップ、モダルウィンドウ等
- プッシュ通知を中心とした、有益性の低い通知
- スマホアプリの宣伝バナーで大画像を伴うか、広い面積を占有するもの
- ブログロール、相互RSSの類（そのブログ自身の更新通知は除く[^21]）
- ブラウザチェックとIE用スクリプト
- クッキーやプライバシーポリシーの同意バナー
- ランキングボタンやその他の不要なブログパーツ
- 広告や行動解析を伴う、または不快なレコメンド（追尾型など）
- 一部のセルフプロモーションや、プロモーション広告
- メールマガジン購読やサブスクリプションを促すバナー
- 不要な待ち時間（多くの場合、広告の類を見せるために使われる）
- 楽天の、デフォルトでチェックされているメールマガジン配信チェックボックス（アンチェックします）
- Twitterのおすすめトピック、おすすめユーザー、おすすめツイート、「タイムラインにトピックも表示しましょう」、新しいリストを見つける
- 迷惑度の高いチャットウィジェット（大型ポップアップなど）
- その他多くのユーザーにとって迷惑・不要と思われるもの

#### 対象外

- 上記対象に該当するが潜在的に、または人によっては有用なもの
- ログインサイトで、デフォルトで無効のプッシュ通知（ニコニコなど）
- 右クリック防止やコピープロテクトの類（すべての利用者に著作権を遵守していただけるならよいのですが、その保証がない以上あえてブロックしません）
- 開発者ツールの妨害スクリプト
- ペイウォール（クッキーを参照して「無料で読める記事はあと〇〇」と警告するタイプのものは対応する場合もあります）
- ポップアップやクッキーバナーの内、クリックが必須のもの（セキュリティ上の理由により、uBlock Originではあえて対応するスクリプトを採用していません）
- モバイルブラウザチェック（モバイルも限定的にサポートするため）
- レーティングウィジェット
- ブログ以外のブックマークボタン、クリップ系
- 一般のチャットウィジェット
- コロナウイルス関係で、一般的な通知ブロックで防げないもの（一時的なものなので）

モバイルサイトは限定的に対応します、メインはPCです。モバイルで使用する場合、Android版FirefoxにuBlock Originを入れてご利用ください。迷惑度のとくに高いものはYuki's uBlock Japanese filtersでブロックすることもあります。たとえば忍者レコメンドは当初、Annoyancesに入れていましたが、動画中に画像を挿入するケースなどが散見されたため方針を変えました。なお、AnnoyancesはAdGuardとも許容範囲といえる程度の互換性がありますが、`if`構文で囲ったルールが機能しないなど対応は不完全ですので推奨はしません。基本的にuBlock Origin向けです。一部のサブフィルタのみ、完全な互換性があります。

<details>
<summary><strong>Annoyancesのサブフィルタ</strong></summary>

特定の迷惑要素だけをブロックしたい場合、みぞれフィルタの代わりにサブフィルタ（の組み合わせ）をご利用いただくこともできます[^22]。

### Yuki's Cookie Dialogue filters （旧：Sabre filters 2）

クッキーの同意バナーを除去します。<strong>Yuki's uBlock Japanese filters - Annoyancesに含まれており、これを購読しているなら必要ありません（AdGuard for Androidを除く）</strong>。一方でYuki's uBlock Japanese filters - Annoyancesと異なり、AdGuardとも完全な互換性があります。

<a href="https://subscribe.adblockplus.org/?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/sabre-filters2.txt&title=Sabre%20filters%202">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/sabre-filters2.txt)


### Yuki's Blog parts filters

ランキングボタン等のブログパーツをブロックします。AdGuardとも完全な互換性があります。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blog-parts.txt&title=Yuki's%20Blog%20parts%20filters">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blog-parts.txt)

### Yuki's Blogroll filters

ブログロール、相互RSSの類をブロックします。uBlock Origin専用で、Yuki's uBlock Japanese filtersとの併用を前提としています。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blogroll.txt&title=Yuki's%20Blog%20parts%20filters">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blogroll.txt)

### Yuki's Mobile App filters

モバイルアプリのダウンロードを促すバナーを除去します。AdGuardとも完全な互換性があります。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/mob-app.txt&title=Yuki's%20Mobile%20App%20filters">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/mob-app.txt)

</details>

## Yuki's uBlock Japanese filters - Annoyances Plus （ひょうフィルタ）

人によって要否がわかれる、微妙な迷惑要素をブロックするフィルタです。対象をよく見て、必要な人だけ購読、または必要部分だけマイフィルターにコピーしてください。

#### 対象

- リスト中に日本語でコメントを入れているので、それを見て判断してください。 

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances-plus.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Annoyances%2B">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances-plus.txt)

## Anti Anti-adblock Enhancer for AdGuard （AdGuard アンチ広告ブロック対策強化パッチ）

<strong>「信頼するフィルタ」のチェックが必要です。また、DNSフィルタリングが有効の場合、効果が半減します（リソースリダイレクトの問題）。とはいえDNSフィルタリングにはメリットもあるため、各自の優先項目に応じて総合的に判断してください</strong>

AdGuard for Windows, AdGuard for Android, AdGuard for Mac, AdGuardブラウザ拡張機能専用です。AdGuard for Safari, AdGuard for iOS, AdGuardコンテンツブロッカーではあまり機能しません。AdGuardのアンチ広告ブロック対策機能を汎用フィルタで底上げします。個別対策はしませんので、対応漏れはこちらではなくAdGuard公式に報告してください（表示崩れなどの不具合報告は受けつけます）。一部アダルトサイト、違法コンテンツサイト、短縮リンクなどでよくみられる悪質ポップアップも軽減します。AdGuard標準フィルタリストへの追加を想定しています。uBlock₀ filtersから取られたルールが多いため、ライセンスはGPLv3としています。

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/anti-antiadb.txt&title=Anti%20Anti-adblock%20Enhancer%20for%20AdGuard">購読する</a>
[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/anti-antiadb.txt)

## AdGuard DNS filter Unbreaker for Japanese （AdGuard DNSフィルタ不具合修正パッチ）

<strong>ブロックよりも不具合の低減を優先するユーザー向けです。コンテンツブロック/ブロッカーではなくDNSフィルタに追加購読してください。</strong>

AdGuard DNSフィルタの既知の不具合を独自に修正します。DNSフィルタはブロックするかしないかの二択しかなく、融通が利きません。しかし、AndroidのAdGuard無料版ユーザーやiOSユーザーはこれを使わずにアプリ内広告をブロックする手段があまりなく、他に代替となるリストも多くはないと思われます。また、不具合を報告してもブロック漏れとの兼ね合いがあるため必ずしも対処されませんし、当管理人はDNSフィルタの編集権限を持たないためDNSフィルタの問題はあまり扱いたくないのが本音です。

- 直接こちらに不具合を報告する前に、まずAdGuard公式に報告してください。メンテンナンスは主に、AdGuardに報告された問題の中から任意に行う予定です
- あらゆる不具合に対処する予定はありません。公式より緩い基準とはいえ、ブロック除外により漏れる広告が多い場合は対応しません
- 今後とも、モバイルアプリの問題を積極的にサポートする予定はありません。メンテンナンスコストが高くなった場合、公開停止もあり得ます

[中身を見る](https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/dns-unbreak.txt)

## 不具合、ブロック漏れの報告

GithubのIssueか[掲示板](https://jbbs.shitaraba.net/internet/25463/)を通して受けつけます。報告前に一度、<strong>新しいブラウザプロファイルを作り、uBlock OriginをクリーンインストールしてYuki's uBlock Japanese filters (+ Paranoid/Social/Annoyances）のみを購読した状態で問題が再現できるか</strong>を確認してください。また、ネットワークの別の部分でブロックしていないか（例: AdGuard Home）も確かめてください。報告される方は、<strong>必ず以下の項目をすべて記入してください（Githubではテンプレートを用意してありますのでご利用ください）。</strong>海外サイトの不具合は、AdGuard Japaneseを除くuBlock Origin標準のフィルタ（+ 英語以外の場合、その言語の標準フィルタ）を併用しても再現する場合のみ対応いたします。

1. 問題が起こるサイトの完全なURL: 検索エンジンの場合は検索語もお願いします。
2. 現象の説明: 言葉による説明とスクリーンショットを両方含めてください。
3. 現象の再現方法: そのサイトに行くだけで100%再現できる場合でも、順を追って記述してください。例えばYoutube広告では新しいタブで開いたか、ページ内遷移したかで広告の出方が違います。そのサービスにログインした状態か否かも必ず記述してください。
4. 環境と設定: OS、ブラウザ、uBlock Originの種類とバージョン、また購読しているフィルタの一覧（スクリーンショット可）は必須です。Firefox上でのみ問題が発生する場合、GoogleかCloudflareのDNSで現象が再現できるかも確かめていただけると助かります。

注意： ログインが必要なサイトでの不具合や広告漏れにつきましては、ログや開発者ツールのスクリーンショット等、こちらがログインせずとも現象や解決を確認できる手段の提供をお願いすることがあります。

### ブロックおよびメンテナンス方針

- ルールの追加・削除については問題の検証を必須とします。他のフィルタが採用しているからというだけの理由、またはユーザー様の自己報告だけに基づく追加・削除は原則として行いません。

- 誤爆かどうかの判定が難しいケースもあります。そのような場合、そのサイトを日常的に使う人を想定するため、たまたま訪れた人には判定が甘い（広告漏れ）ように映るかもしれません。できるだけ最大公約数をとるように努力しますが、そもそも万人向けのフィルタなどありません。可能でしたら、適宜`$badfilter`, `$important`や例外などで対応してください。

- 他フィルタとルールを統一する場合を除き、汎用ルールの使用を最小限に抑えています。ルールを汎用化するのは原則、1) 少なくとも3か所以上で使われており、2) 他の場所でも使われる見込みが高く、3)かつ、誤爆する見込みが低い場合のみです。１つでも既知の誤爆がある場合は極力避けています。

- 失効ドメインや不要になったルールは見つけ次第取り除く方針です。失効ドメインでもリクエストは発生するため、ほかのフィルタよりブロックが少なく見えることがあり得ます。

- Yuki's uBlock Japanese filtersファミリーでは日本のサイトと、日本人が訪れる一部の海外サイトを対象としています。後者の詳細は[こちら](https://github.com/Yuki2718/adblock/wiki/Japanese-FAQ#q4-1-%E9%9B%AA%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%81%AE%E4%B8%AD%E3%82%92%E8%A6%8B%E3%82%8B%E3%81%A8%E6%B5%B7%E5%A4%96%E3%82%B5%E3%82%A4%E3%83%88%E7%94%A8%E3%81%AE%E3%83%AB%E3%83%BC%E3%83%AB%E3%81%8C%E7%B5%90%E6%A7%8B%E3%81%82%E3%82%8A%E3%81%BE%E3%81%99%E3%81%A9%E3%81%AE%E3%82%88%E3%81%86%E3%81%AA%E3%82%B5%E3%82%A4%E3%83%88%E3%81%8C%E5%AF%BE%E8%B1%A1%E3%81%AA%E3%81%AE%E3%81%A7%E3%81%97%E3%82%87%E3%81%86%E3%81%8B)をご覧ください。

- ブロッカー検知用の罠スクリプトは意図的にブロックから除外しています。初心者の方にはこれがブロック漏れにみえるようです（[例1](https://github.com/easylist/easylist/issues/6407)、[例2](https://github.com/AdguardTeam/AdguardFilters/issues/67785)）。報告は実際の問題に対して行うか、せめてスクリプトの内容を確認してからにしてください。

- 正直なところ、長期的にメンテナンスできるかはわかりません。元々、当時更新が停滞していた[豆腐フィルタ](http://tofukko.r.ribbon.to/abp.html)のフォークを考えていたのですが、許可が下りなかったためオリジナルフィルタを企画しました（わざわざフィルタを公開するからには、理由は他にもあります）。その間に豆腐さんも更新を再開されたようです。オリジナルとはいえ豆腐フィルタを参考にした部分は多々あり、ここに感謝申し上げます。

- 当フィルタの方針に同意いただけ、かつフィルタを作成する技能のある方の貢献は歓迎いたします。興味がおありの方はプルリクエストやIssueを通じて声をおかけください。それが面倒な方は、CC BY-SA 4.0の範囲において自由に改変、再配布も可能です。識別のために管理人の名前を入れたものの、本来はチームによる共同管理が望ましいと考えています。

## その他

[よくある質問](https://github.com/Yuki2718/adblock/wiki)

### お断り

当サイト（レポジトリ）管理人および貢献者は、当サイトのフィルタやルールによって生じたいかなる損害についても責任を負いません。また、事前の予告なく公開を中止する可能性があります。

### 管理人について

EasyListなどの国際的な広告ブロックコミュニティにボランティアとして二年以上貢献を続けており、uBlock内製フィルタおよびAdGuard公式フィルタの共同管理者でもあります。280blockerさん、もちフィルタさん、豆腐フィルタさんなどにも問題報告をすることがあります。AppleストアにあるYuki - Ad Blocker+ for YouTubeとは何の関係もありません、念のため。

[^1]: AdGuardはuBlock Origin文法と高い互換性を持っているとはいえ、Yuki's uBlock Japanese filtersはAdGuardで機能しない書き方を多数用いています（例：末尾以外の`:upward()`）。また、スクリプトレットなどのリソースの互換性やAdGuard標準リストとの干渉によって不具合やポップアップ、アンチ広告ブロックを惹起するケースが多数ある上、AdGuard for Android/Windowsなどアプリ版ではCSSの優先度やルール処理の優先順位など別の問題もあり、誤爆の危険もあります。AdGuardで標準のリストをご利用の場合、Yuki's uBlock Japanese filtersとの差をいくらか埋め合わせるアンチ広告ブロック対策強化パッチも提供しています。なお、uBlock OriginはVivaldiを[公式にサポートしていません]((https://www.reddit.com/r/uBlockOrigin/comments/l2ik0b/excessive_ads_count_on_youtube_gets_really_heavy/gk8fxt4/))が、Yuki's uBlock Japanese filtersファミリーはVivaldi上のuBlock Originをサポートしており、Vivaldi固有の問題にも対応しています。Vivaldi内臓のブロッカーはサポートしません。
[^2]: いくつかの日本用フィルタと同様、日本語話者がよく利用すると思われる海外サイトにも対応しています（[FAQ A4-1](https://github.com/Yuki2718/adblock/wiki/Japanese-FAQ#q4-1-%E9%9B%AA%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%81%AE%E4%B8%AD%E3%82%92%E8%A6%8B%E3%82%8B%E3%81%A8%E6%B5%B7%E5%A4%96%E3%82%B5%E3%82%A4%E3%83%88%E7%94%A8%E3%81%AE%E3%83%AB%E3%83%BC%E3%83%AB%E3%81%8C%E7%B5%90%E6%A7%8B%E3%81%82%E3%82%8A%E3%81%BE%E3%81%99%E3%81%A9%E3%81%AE%E3%82%88%E3%81%86%E3%81%AA%E3%82%B5%E3%82%A4%E3%83%88%E3%81%8C%E5%AF%BE%E8%B1%A1%E3%81%AA%E3%81%AE%E3%81%A7%E3%81%97%E3%82%87%E3%81%86%E3%81%8B)）。ただし、日本できわめてメジャーなサイトを除き多少の空白、枠残りなどは許容するものとします。
[^3]: 後述のようにEasyListやEasyPrivacyなどから多くのルールを取り入れているものの、誤爆率の高いルールは除外しています。EasyPrivacyではレコメンドウィジェットやプッシュ通知などもブロックしていますが、これには異論もあるためこちらではAnnoyancesに分類しています。また私の知るこれらのフィルタによる誤爆で、未報告または報告済みだが未対処のものにも対応しています。一方、EasyPrivacyなどに含まれていないアクセス解析も（誤爆率の高そうなもの以外）多く盛り込んでいます。
[^4]: これまでに`match-case`, `matches-path`などの新機能を追加してもらっているほか、Issueや内部的なやりとりを通してスクリプトレットやリダイレクトリソースの追加・強化を多数依頼し、ほぼすべて了承されています。
[^5]: 「要素をブロック」機能でマイフィルターを作っている人も同様です。画像についてはブロックしてくれることもありますが、イニシエイターはお手上げです。非表示についても質の低いルールが多いです。同機能は[あくまで補助であり](https://github.com/uBlockOrigin/uBlock-issues/issues/1058#issuecomment-631459847)、過剰に頼るべきではありません。
[^6]: uBlock Originポップアップパネルの目玉アイコンをクリックして×印をつけると、ブロックされていない広告が見えてきます。元に戻すにはもう一度クリックして×印を外してください。
[^7]: 当サイトのフィルタは[specific-generic](https://github.com/gorhill/uBlock/wiki/Static-filter-syntax#specific-generic)を利用したおそらく最初の公開フィルタです。なお、汎用整形フィルタの数はパフォーマンスに[影響しません](https://github.com/uBlockOrigin/uBlock-issues/issues/738#issuecomment-619450820)。細かいことをいうとすべての汎用整形フィルタが同列ではなく、大量の[Highly generic cosmetic filters](https://github.com/uBlockOrigin/uBlock-issues/discussions/1998)は望ましくないでしょう。
[^8]: 簡単に言うと、リクエストとルールそれぞれから抽出したトークンを使ってマッチする見込みがありそうなルールを絞り込んでいます。一般的なリクエストに対して大部分のルールは無いも同然であり、計算量のオーダーはルール数に依存しません。理屈は検索エンジンの転置インデックスと同じです（ウェブサイトの数がいくら増えても検索にかかる時間は変わりません）。</sub>
[^9] 実測するのが早いです（benchmarkDatasetURLを書き換えると測定できます）。[こちら](https://brave.com/improved-ad-blocker-performance/)はBraveがuBlock Originの方式を導入した時の記事ですが、16,000個ルールを追加しても個々のリクエスト処理にかかる時間は1μsも変わらないことがわかります。メモリ消費はルール数に応じて増えますが、PCで問題になる量ではありません。ブロック漏れによる消費のほうが大きいでしょう。逆に、非効率なルールが増えると遅くなるため、対象を絞り込むなどの対策が必要です。Twitterや個人ブログなどでルールを公開する人は多いですが、それらの中には問題のあるものも少なくありません。
[^10]: ABP文法と異なり、[単語境界を意識](https://github.com/gorhill/uBlock/issues/1065)する必要があります。たとえば`/foo`というルールは、（他の部分でトークンマッチが起きない限り）`/foo1`というリクエストをブロックしません。明示的に`*`を追加するとブロックするようになりますが（`/foo*`）、これは`foo`のトークン化を妨げます（細かく言うと、８文字以上だと[話が別になります](https://github.com/gorhill/uBlock/issues/3011#issuecomment-329140908)）。主要な[bad token](https://github.com/gorhill/uBlock/blob/381498daa2a9ce089a69d044760190b1dd14b5ac/src/js/static-net-filtering.js#L2062)（原則、トークン化されない文字列）も覚えた方がよいでしょう。一般に遅いとされる正規表現ルールも条件を満たせばトークン化可能です。
[^11]: 当フィルタはCC BY-SA 4.0のもとに配布しており、これはuBlock内製フィルターと280blocker以外を正しく継承（デュアルライセンス、バージョン違い）しています。uBlock内製フィルターはGPLv3ですが、AdGuardなどと比較して癖のないルールであり、一般的なフィルタ作者が思いつく範囲だと思います（管理人はuBlock内製フィルターのメンテナーでもあるため、自ら追加したルールも多数あります）。280blockerはライセンス指定なしですが、参考にしているのはドメインリストのみであり、これは書き方がほぼ一意に決まってしまうため問題ないと考えます。また一部、[EasyList China](http://abpchina.org/forum/forum.php), [RU AdList](https://forums.lanik.us/viewforum.php?f=102), [Brave Unbreak](https://github.com/brave/adblock-lists)（MITライセンス）からとられたルールがある他、[豆腐フィルタ](http://tofukko.r.ribbon.to/abp.html)を参考にしたルールが少なからずあります（著作権上、そのままの使用はなるべく避けましたが、どうしても同じになってしまったものもあります）。AdGuard URL Tracking Protectionとの併用も可能ですが、同リストはutm系の一括削除などにより一部で不具合が起きるため、あまり初心者向けではないと考えています。Yuki's uBlock Japanese filtersおよびParanoidでは同リストを参考に問題がなさそうなものを個別に追加する一方、一部のルールはuBlock Originに最適化した形で置き換えています。
[^12]: 有効数には優先順位がありませんので、Yuki's uBlock Japanese filtersの内どれだけ使われているか知りたい場合、一度Yuki's uBlock Japanese filtersのチェックを外して他のフィルタを更新し、再度チェックを入れてください。なお、この方法で真の有効数がわかるのはYuki's uBlock Japanese filtersならではであり、ほかのフィルタではわかりません。同じブロック対象を別のルールでターゲットにするケースが多数生じるためで、この場合、優先順位の低いトークン化可能ブロックルールは「死んだルール」（メモリのみ消費）、トークン化不能ブロックルールやProcedural cosmetic filters、スクリプトレットルール等はパフォーマンス上の損失となります。[フィルターリスト]ペインの使用数は実際に使われるフィルタ数ではないということです
[^13]: これらのフィルタによる誤爆をより網羅的に修正していることもあり、既にEasyList等を併用されている方にはもっともおすすめできる日本用フィルタと言ってよいでしょう。ちなみに、日本以外の国や地域ではEasyListに各言語用のフィルタを追加して使うのが普通であり、各言語用フィルタはEasyListの併用を前提としたものとなっています。中国ではEasyList Liteというのを用意しており、中国語サイトを中心にみる場合はEasyListの代わりにこれを使ってもよいとされています。Yuki's uBlock Japanese filtersも、日本のサイトを中心に見るなら10万以上のルール数におよぶ標準リストの代わりに使えるものとして提供していますが、標準リストとの併用も可能としている点が異なります。実は、標準リストの変更に追随していくのが一番大変な作業です。
[^14]: 主に汎用ルールやスクリプトレットの不一致によるもので、海外アダルトサイトなどで顕著です。
[^15]: 有用性などを鑑み、すべてはブロックしません。大まかには、記事リストの間に挿入されるもの、ネイティブ広告としての性質が強いものなどを中心にブロックしています。
[^16]: セルフプロモーションは悩ましい対象です。AdGuardなどにもしばしば広告として報告する方が来られますが、基本的に迷惑要素として対処しています。Yuki's uBlock Japanese filtersの基準はこれより厳しく、記事中に挿入されるバナーなど侵襲性が高いものや、冗長なものなどはブロックすることがあります。とはいえ、ブロックしすぎと思われるものがあればご報告ください。
[^17]: 実際には、1. 一般的なブログにおける商品かサービスについてのレビューに付随するAmazonや楽天へのリンクで、量が過剰でなく、他の関係ない商品やサービスへのリンクを含まないもの、2. そのサイトの管理者による著作物などの紹介、に限定しています。280blockerさんの[おっしゃるように](https://280blocker.net/advanced-settings/)これらを消すと文章が不自然になるケースもありますし、消したい方は「要素をブロック」で簡単に消せるものがほとんどです。他の日本用フィルタでも、もちフィルタさんが`amazon-adsystem.com`のウィジェットをブロックされている以外はせいぜい汎用非表示にとどまっています。そのもちフィルタさんも、`ssl-images-amazon.com`や`ecx.images-amazon.com`はコメントアウトされている（ブロックしていない）ことから苦心の跡がうかがえます。この辺りはすべてのフィルタ作者の悩みの種です。
[^18]: こちらも基本、他の日本用フィルタでもブロックされていません。そもそも広告でなく、画像付きのリンクに過ぎませんが、侵襲性が高いものについては（ときにAnnoyancesで）ブロックする場合もあります。
[^19]: AdGuard Japaneseにおいても、当管理人がコミットする場合はできるだけuBlock Originでも最適となるようフィルタを書いていますが、AdGuardの仕様の違いやフィルターポリシーの違いなどにより、そうできないケースもあります。
[^20]: モバイルでは「汎用整形フィルターを無視する」がデフォルトで有効になります。これによりパフォーマンスが向上しますが、消し残り等も出てくるためuBlock Originチーム内でディスカッションした結果、いくつかの汎用性の高い整形フィルタをspecific-genericとして内製フィルタに追加しました。これらのフィルタの選定はAdGuard社のフィルタ統計を参考にしながら当管理人が行いましたが、国際的なサイトや英語サイトが中心となっています。一方、国際的にはマイナーでも日本のサイトでよく問題になるものもあり、これまで内製フィルタやAdGuard Japaneseで対応してきましたが、AdGuardのフィルタでuBlock Origin固有の問題をどこまで対応すべきなのか、内製フィルタで日本固有の問題をどこまで対応すべきなのか、という問題がありました。Yuki's uBlock Japanese filters - Mobileでは、日本のサイトでよく問題になるものをspecific-genericに追加しています。uBlock Origin開発者によれば、何千もの汎用整形フィルタを挿入するのが問題なのであって、数十程度ならパフォーマンス上の懸念はありません。
[^21]: クリック後に外のサイトを経由するもので、本文中に挿入されているなど迷惑度が高いものはブロックすることがあります。
[^22]: ポップアップ、サブスクリプション、プロモーションについては個別のサブリスト化は困難です。AdGuard Annoyancesでもそうですが、ポップアップという括りは「表示形式がポップアップであるあらゆる迷惑要素」ぐらいの意味しかなく、サブスクリプションやプロモーションにも分類可能なものが含まれているからです。プッシュ通知はサブリスト化可能ですが、Fanboy's Annoyanceのサブリストである[Fanboy's Notifications Blocking List](https://easylist-downloads.adblockplus.org/fanboy-notifications.txt)と大部分重複しており、そちらを購読していただければよいと思います。ターゲットが明確でルールも少ないため、Fanboy系にしては不具合は少ないです（2022年8月12日追記：最近、モバイルアプリのバナー通知も対象とするなど範囲が拡大しており、要注視）。Othersに含めているカウントダウン系もサブリスト化可能ですが、uBlock₀ filtersで標準対応しているため需要が低いと思います。こちらで標準対応しないのは、広告でないことに加えてまれに不具合を起こすためです。
