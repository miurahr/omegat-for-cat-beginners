# CATビギナーのためのOmegaT入門

[![hackmd-github-sync-badge](https://hackmd.io/xL4ee8XjRrmuvRYzBhl08Q/badge)](https://hackmd.io/xL4ee8XjRrmuvRYzBhl08Q)

![cover](https://raw.githubusercontent.com/miurahr/omegat-for-cat-beginners/master/images/title.png)

by Susan Welsh & Marc Prior  \
Translation and modification by Hiroshi Miura

---

# Copyright

Copyright (c) 2014 Susan Welsh & Mark Prior
Copyright (c) 2020 Hiroshi Miura

Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.2 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts. A copy of the license is included in the section entitled "GNU Free Document License."

Cover illustration is from www.freeclipartnow.com, in the public domain.

Last update and translated: August 2020  \
Original written: March 2014  \
Refer to OmegaT version: 5.3.0

Screenshots from OmegaT version 5.3.0 (ja translation)
Please note that owing to the pace at which OmegaT is being developed, the appearance of the screenshots and possibly some other information may have changed slightly.

# 著作権表示


Copyright (c) 2014 Susan Welsh & Mark Prior
Copyright (c) 2020 Hiroshi Miura

Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.2 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts. A copy of the license is included in the section entitled "GNU Free Document License."

カバーのイラストは、www.freeclipartnow.com 由来で、パブリックドメイン のものです。

最終更新：2020年8月
オリジナル更新日：2014年3月
参照しているOmegaTバーション: 5.3.0

OmegaT 5.3.0のスクリーンショットを利用  \
開発の進展に伴って、画面や、その他の情報が本書から変わる場合があります。


# はじめに

## 想定読者

CAT(コンピュータ支援翻訳：Computer Assisted Translation)ツールの経験の少ない翻訳者を対象として、本書ではその基礎だけを説明しています。
他の有用な情報源を得るには、[OmegaT Web site/Documentation](https://www.omegat.org/en/documentation.php) へアクセスしてください。

## CATツールとは何か、何故有用なのか？
    
CATツールとは、一般に翻訳者が使用するソフトウェアのことで、特に翻訳されたドキュメントの「翻訳メモリ」(TM)を作成するプログラムのことを指しています。最初のものと非常によく似ている将来の文書の翻訳を容易にすることができます。反復的な作業の場合に、この点が特に有用です。

- 用語集機能を使用すれば、ユーザは原語と訳語を登録しておき、翻訳中に参照できるようになります。

- 検索機能は、以前に翻訳された文書(現在のプロジェクトのドキュメント、または以前のプロジェクトの翻訳メモリ)をスキャンして、ユーザが単語またはフレーズが、以前にどのように翻訳されたかを確認できるようになります。

- セグメンテーション機能は、一度に1つのソーステキストの「セグメント」を表示します(通常は文です)。原文のすぐ下の画面に訳文を入力することで、翻訳がすすんでいきます。これは 1)文章の翻訳忘れを防止; 2) 作業結果の確認; 3) 原文と訳文に自分が作業しやすいフォントを選べる、 というメリットがあります。

CATツールにより、1人の翻訳者が仕事をしている場合を凌ぐ、翻訳の一貫性の向上をもたらします。最後に、CATツールはソース文書のフォーマットを再現します。CATツールの価格は、無料(OmegaT)から25万円以上までかなりの幅があります。OmegaTは、価格が適正で、比較的学習しやすく、MACとLinuxとWindowsで動作するため、出発点としては最適です。

OmegaTは、現在のMicrosoft Officeファイル形式(.docx、.xlsx、.pptx)をサポートしています。古いMicrosoft Officeファイル形式(.doc、.xls、.ppt)はサポートされていません。これらのファイル形式は、最新のMicrosoft Officeファイル形式などに変換する必要があります。

様々なツールの紹介をふくめ、CATツールの詳細については、次のwikipedia記事を参照してください。

http://en.wikipedia.org/wiki/Computer-assisted_translation


# OmegaTのダウンロード

まず、OmegaTをダウンロードしてください(OmegaTのサイトには様々なオプションが記載されています。(「ベータ」バージョンは安定していますが、1つか2つのバグがある場合があり、最新のドキュメントはありません)。

 www.omegat.org

画面の表示されているダウンロードの手順には、すこし説明が必要です。ここでは、Java(JRE)を含むバージョンを選択して、ダウンロードすることをお勧めします。
このチュートリアルでは、Windowsオペレーティングシステムを使用することを前提としています。別のシステムを使用していて問題が発生した場合は、OmegaTユーザーグループのメーリングリストがお手伝いします(ステップ8を参照)。


# OmegaTのインストール

zipファイルをダウンロードしたら、Windowsの場合はC:\Program Filesなどの適切なフォルダに保存します。zipアーカイブを展開(解凍、unzip)します。
OmegaT(Windowsバージョン)をダウンロードしたら、.exeファイルを起動し、画面に表示される説明に従って操作します。

# OmegaTユーザーインターフェイス

OmegaTを起動すると、OmegaTのメインウィンドウが開き、編集ペイン、ファジーマッチペイン、用語集ペインの3つのメインペインと、機会翻訳、複数訳文、 メモ、コメント、辞書の5つのオプションペインが表示されます。オプションのペインについては、『ユーザーズマニュアル』を参照してください。
すべてのメインペインが表示されない場合は、下図のように配置されるまで、ペイン間の境界をドラッグします。
[編集]ペインに「クイックスタート」チュートリアルがOSの言語で表示されます。ユーザーズマニュアルは、「Help」メニュー項目またはF1で呼び出すことができます。
[編集]ウィンドウが空の場合は、インストールされているWindowsの言語が英語ではない可能性があります。またOmegaTに、使用している言語でのインスタントチュートリアルのサポートが無いようです。

この場合は、[Help]>[User's Manual]を選択するか、[F1]を押してOmegaTのマニュアルを呼び出します。

OmegaTが開発されているペースが速いため、ドキュメントが少し時代遅れになっている可能性があることに注意してください。言語によっては、マニュアルがとても古い可能性があります。最新のドキュメントを翻訳してくれるボランティアを歓迎します。ユーザー・グループのメーリングリストへ連絡してください。


# スペルチェック辞書をインストールする

訳文言語のスペルチェック用の辞書を保存する場所が必要です(二言語辞典の場所ではありません)。たとえば、プログラムファイルに「dictionaries」フォルダを作成します([スタート]>[マイコンピュータ]>[ローカルディスク(C:)]>[Program Files]>右クリック>[新規フォルダ]「dictionaries」という名前を付けます)。[OmegaT]メニューから、[設定>[艦橋設定]>[スペルチェッカー]をクリックします。「参照」をクリックし、「dictionaries」フォルダに移動します(スクリーンショット
(下記a、参照)。
「新しい辞書を組み込み」をクリックすると、リストが表示されます。(何も起こらない場合は、別のリポジトリを選択します。 [OmegaT howto Spelling](https://www.omegat.org/en/howtos/spelling.html)を参照。 必要なリポジトリをクリックして、もう一度「辞書を組み込み」をクリックして、ボックスを閉じます。
辞書を選択して「インストール」を選択すると、a)で指定したフォルダに、該当する辞書がインターネットからダウンロードされます。
もちろん、この機能が動作するためにはインターネット接続が必要です。

辞書または「スペルチェッカーの設定」ダイアログウィンドウに辞書の一覧が表示されます。ここで、辞書の言語種別と、ターゲット言語が一致していることを確認してください。辞書やスペルチェッカーは、言語種別が一致しない場合には、動作しません。(例：米国英語と英国英語)


# 新規プロジェクトの作成

ほとんどのCATツールでは、翻訳に関連付けられたフォルダとファイルの集まりを「プロジェクト」と呼びます。「プロジェクト」は通常、翻訳作業を意味しています。

OmegaTでプロジェクトを作成するには、[プロジェクト]を選択し、[新規作成]をクリックします。[新規プロジェクト]ダイアログが表示されます(ここには表示されていません)。
プロジェクトを作成する適切なフォルダ(メインフォルダなど)にナビゲートします。

翻訳に使用するフォルダ、または一時的に簡単にアクセスでき、後でマイドキュメントなどに移動できます。

顧客の名前や発注件名など、プロジェクトに適した名前を入力して、[保存]をクリックします。このチュートリアルでは、これをマイプロジェクト-1と呼ぶことにします。

[新規プロジェクトの作成]ダイアログが表示されます。

これらのフィールドの右側の矢印をクリックして、計画している原文言語と訳文言語を選択します。

[文節化規則]をクリックして、[文節化規則設定]ダイアログを呼び出します。OmegaTには、非常に基本的な文節化のパターンがいくつか用意されています。原文の言語(例:イタリア語、"IT.*")と選択し、"上へ移動"ボタンをつかってリストの先頭に移動します。原文の言語が一覧にない場合は「言語名]フィールドをダブルクリックして言語の省略形に変換します。言語で同じことを行う

[パターン]フィールド今後、OmegaTを長期間使用するようになると、文節化規則をカスタマイズしたくなるかもしれません。
この段階でセグメンテーション規則を微調整する必要はありません。提供されている基本的な規則は、その文の句読点の規則が広く似ている(つまり、イタリア語から翻訳する場合は日本語のセグメンテーション規則を使用しない)場合には、別の(ソース)言語であっても、デモ用に十分に機能するはずです。


セグメント化規則を確認し、「OK」をクリックしてプロジェクトを作成します。このチュートリアルでは、他の設定は変更しないでください。また、「参照」や他の既定のプロジェクトフォルダ(ディレクトリ)を変更しないでください。これで空のプロジェクトが作成されました。

[プロジェクトファイル]ウィンドウが表示されます。このウィンドウは、ファイルがまだ含まれていないプロジェクトのため空です。(「ソースファイルのインポート」機能は使用しないでください。後で自分で試すことができます)。
このウィンドウを閉じます。

ファイルマネージャでプロジェクトを検索します。プロジェクトフォルダには、***/dictionary、/glossary、/omegat、/source、/target、/tm***、および***/glossary*** があることがわかります。すべて空です。翻訳対象の文書は、***/source*** フォルダに配置します。***/target*** フォルダには、翻訳された文書が出力されます。***/omegat*** フォルダはここでは関係ありません。***/tm*** および ***/glossary*** ファイルには、自身でtmxファイルや用語集を造っている場合以外は関係ありません。***/dictionary*** フォルダには、必要に応じて適切なフォーマット(ユーザーズ・マニュアルを参照)の辞書をコピーします。


# 翻訳作業

ここでは、自己トレーニングのための2つのプロジェクトを提供します。
1つ目は、原文に単純なMS Wordファイルを使用する方法です。これはOmegaTの完全な能力を示すものではないのですがが、「初心者」が基本的な手順を把握できるようにしています。2番目のプロジェクトは、インターネットからダウンロードしたHTMLファイルや、複数のHTMLファイルおを使って、OmegaTの複雑なレイアウトと複雑なファイル構造を再現できる、グラフィック処理能力をデモンストレーションします。ここでは
翻訳メモリ、用語集、検索機能の動作をまなびますこれらの機能は、ファイルの種類(.docx、.xlsx、.odt、.txt、.htmlなど)によらず利用できます。下記***6.B.1-6.B.4***参照。トレーニングが目的なので、プロジェクト1ではこれらを無視します。プロジェクト1の完了後、プロジェクト2に進んでください。 

重要:このOmegaT入門の目的は翻訳メモリソフトウェアの基本概念を学ぶことです。OmegaTのより高度で不明瞭な機能が意図的に省略するか、最小限の説明にとどめています。
これらの記述があると確実に、新しいユーザにとって、木を見て森を見ることができない状態になってしまいます。詳細はユーザーマニュアルを参照してください。


## プロジェクト1: 単純なMS Wordファイル

LibreOffice Writerを起動し、新しいテキストドキュメントを作成します。次に ファイル>開く で、原文言語の任意の小さなMS Word文書(.docx形式)を選択します。少なくとも以下のようなフォーマットを含む必要があります。
タイトル、小見出し、フォントの変更。(このチュートリアルの目的のために、この手順で.docxファイルを利用しますが、実際的には、Open Office Writerの仲介は必要ありません。ある程度理解したら『ユーザーズマニュアル』を参照してください。)
ファイル > 名前を付けて保存  を選択し、ファイルに名前を付けて.odt形式で保存します。新たに作成した.odtファイルをクリックして選択し、ドラッグして、ステップ5で作成したProject1のフォルダの/source フォルダへコピーします。

OmegaTを起動し、「プロジェクト」>「開く」をクリックします。「My Project-1」に移動します(横にOmegaTアイコンが表示されています)。ファイルをダブルクリックします。プロジェクトファイル ダイアログにソースドキュメントが表示されます。ダイアログボックスを閉じます。翻訳ファイルが編集ペインに表示され、翻訳を開始できます。(注意： このスクリーンショットは、一番上の青いバーがある OmegaT 5.3.0を参照しています。OmegaTの開発ペースの速さからスクリーンショットの外観やその他の情報がすこし違うかもしれません)

基本的には、テキストは一度に1セグメントずつ表示されます。通常、セグメントは1つの文に対応します。表示されたフィールドをクリックし、訳文を入力して、Enterキーを押して確定します。OmegaTは「インライン」翻訳メモリアプリケーションです。つまり、テキスト部分のコピーだけが見えます。
すでに翻訳されているセグメントはそのまま表示されます。そうでなければ、翻訳されていない原文が表示されます。「アクティブ」な強調表示されているセグメントは、原文と訳文の両方が表示されます。

既定では、原文が訳文セグメントに貼り付けられています。タグ間のテキストを置き換えるだけでタグは損傷しないため、大量にタグ付けされた(書式設定された)テキストでとても便利です。
訳文フィールドの内容を削除し翻訳文を入力するか、空白のままにすることで、デフォルト動作をOmegaTに指示できます。(詳細はユーザーズマニュアルを参照)


### タグの処理

タグの処理には、ある程度の練習が必要です。一般的な原則は、タグ間のテキストを翻訳し、タグはそのままにします。たとえば、この英語のテキストの場合：

> Look at ***that***!

は、OmegaTでは、このようにみえます:

> Look at <a0>that</a0>!

OmegaTで日本語に翻訳してください

> <a0>あれを</a0>みてごらん!

最終的には次のように表示されます。

> ***あれ***をみてごらん!

この場合、それぞれ<a0>および</a0>は太字テキストの開始タグと終了タグです。「<a0>」および「</a0>」は必ずしも太字の開始と終了を示す記号ではありません。もし、「that」という語が原文でイタリック体であった場合
おなじタグが、太字ではなく、イタリック体であることを示すタグになります。ソーステキストで見ることでのみ、特定ケースでのタグの実際の機能を確認できます。

現在のマイクロソフト Officeのファイルフォーマット (.docx, .xlsx, .pptx)は、大量の不要なタグが生成されてしまうため、翻訳が煩雑になります。一つの解決方法は、 Codezapper (http://asap-traduction.com/CodeZapper) を利用することで、必要なタグを保持したまま、これらの不要タグの削除ができます。OmegaTの「全てのタグを削除」機能を利用することで全てのタグを削除することもできます。ユーザーマニュアル(F1)参照。

タグの処理に慣れるまでは、すべてのタグを保持し
できるだけ同じ順序にしてください。OmegaTは、タグを削除し、その順序を変更します。ただし、特定のルールが慎重に適用されている場合に限ります。そうしないと、最終的なドキュメントが開かないようになってしまいます。タグ処理ルールの詳細については、ユーザーズ・マニュアルを参照してください。


### 翻訳の確認

さて、翻訳するファイルの最終行まで作業がおわりました。
プロジェクトに変換用のファイルが複数ある場合は、最初のファイルの最終セグメントを確認すると、2番目のファイルの最初のセグメントに移動します。

すべての翻訳メモリアプリケーションに共通する利点は、チェックが簡単になることです。
最初の翻訳ドラフトが完成したら、原文バージョンと訳文バージョンを並行して表示して、ウオークスルーレビューをおこないます。OmegaTの場合は、有効化されたセグメントについて、原文が訳文の上に表示されているので、比較が簡単です：

### タグの検証、ターゲットドキュメントの作成

翻訳をチェックして保存すると、OmegaTは自動的にタグが破損していないことを確認します。[ツール]>[検証]を選択して、手動でプロセスを実行することもできます。注:次のようなXMLファイル形式のタグが破損または欠落しています。
OpenOffice.orgでは、出力ファイルを開くことができなくなる可能性があります。

プロジェクトドキュメントを作成するには、「プロジェクト」>「訳文を生成する」を選択して、訳文ファイルを作成します。翻訳されたドキュメントは/targetフォルダ内に元のフォーマットで生成されます。プロジェクトが複数の原文ファイルや、場合によっては複数のサブフォルダ、および付随するグラフィックファイルで構成されている場合は、
2番目のHTMLプロジェクトの例のように、/source内のファイルの構造は/target内に複製されます。

#### 最終確認・修正・納品

翻訳を紙で確認する場合は、目的の文書を印刷します。<f0>ただし、Open Office WriterまたはMS Wordファイルを修正しないでください。</f0>(後述の手順<f1>6.B.4</f1>で説明するテキスト検索機能を使用して)OmegaTで該当するセグメントを検索し、そこでセグメントを作成します。
テキストを修正して修正したら、翻訳済みドキュメントを再度作成し、プロジェクトを閉じます。
これで、ジョブを実行する準備ができました。クライアントでMS Office形式が必要な場合は、目的のファイルをOpenOffice.orgの該当するMS形式(.docなど)で保存します。


## プロジェクト2: HTML文書翻訳

### 補助資材をダウンロードする


| 言語組み合わせ | 主題 | 資材 |
---------------------|----------|---------- 
英中 | 投資 | [W:Share](en.wikipedia.org/wiki/Share_%28finance%29) |
| English to Chinese | stocks | en.wikipedia.org/wiki/Share_%28finance%29  en.wikipedia.org/wiki/Shareholder |
| English to Czech | biocoenosis | en.wikipedia.org/wiki/Biocoenosis en.wikipedia.org/wiki/Phytosociology |
| English to Dutch | stocks | en.wikipedia.org/wiki/Share_%28finance%29 en.wikipedia.org/wiki/Shareholder |
| English to Dutch | russian-miscellaneous | en.wikipedia.org/wiki/Russian en.wikipedia.org/wiki/Russian_American en.wikipedia.org/wiki/Russian_Canadian en.wikipedia.org/wiki/Russky_Island |
| English to French | swimming | en.wikipedia.org/wiki/Individual_medley en.wikipedia.org/wiki/World_records_in_swimming |
| English to French | dorset | en.wikipedia.org/wiki/Jurassic_Coast en.wikipedia.org/wiki/Old_Harry_Rocks en.wikipedia.org/wiki/Durdle_Door |
| English to French | medicine | en.wikipedia.org/wiki/Hippocrates |
| English to German | hilton | en.wikipedia.org/wiki/Hilton_Hotels en.wikipedia.org/wiki/Great_Western_Hotel,_London en.wikipedia.org/wiki/Waldorf_Hilton en.wikipedia.org/wiki/The_London_Hilton_on_Park_Lane |
| English to German | construction | en.wikipedia.org/wiki/Wall en.wikipedia.org/wiki/Panelling |
| English to Italian | russian-miscellaneous | en.wikipedia.org/wiki/Russian en.wikipedia.org/wiki/Russian_American en.wikipedia.org/wiki/Russian_Canadian en.wikipedia.org/wiki/Russky_Island |
| English to Italian | yoga | en.wikipedia.org/wiki/Karma_yoga en.wikipedia.org/wiki/Jnana_yoga |
| English to Italian | civil-engineering | en.wikipedia.org/wiki/Blind_Jack |
| English to Polish | construction | en.wikipedia.org/wiki/Wall en.wikipedia.org/wiki/Panelling |
| English to Polish | poland | en.wikipedia.org/wiki/Lubusz_Voivodship en.wikipedia.org/wiki/Podlasie_Voivodship |
| English to Polish | medicine | en.wikipedia.org/wiki/Hippocrates |
| English to Polish | swimming | en.wikipedia.org/wiki/Individual_medley en.wikipedia.org/wiki/World_records_in_swimming |
| English to Portuguese | russian-miscellaneous | en.wikipedia.org/wiki/Russian en.wikipedia.org/wiki/Russian_American en.wikipedia.org/wiki/Russian_Canadian en.wikipedia.org/wiki/Russky_Island |
| English to Russian | biocoenosis | en.wikipedia.org/wiki/Biocoenosis en.wikipedia.org/wiki/Phytosociology |
| English to Russian | stocks | en.wikipedia.org/wiki/Share_%28finance%29 en.wikipedia.org/wiki/Shareholder |
| English to Spanish | dorset | en.wikipedia.org/wiki/Jurassic_Coast en.wikipedia.org/wiki/Old_Harry_Rocks en.wikipedia.org/wiki/Durdle_Door |
| English to Spanish | appliances | en.wikipedia.org/wiki/Small_appliance en.wikipedia.org/wiki/Kitchen_appliance en.wikipedia.org/wiki/Major_appliance |
| English to Spanish | cereal | en.wikipedia.org/wiki/Rye en.wikipedia.org/wiki/Sorghum |
| English to Spanish | skye | en.wikipedia.org/wiki/Skye |
| English to Spanish | hilton | en.wikipedia.org/wiki/Hilton_Hotels en.wikipedia.org/wiki/Great_Western_Hotel,_London en.wikipedia.org/wiki/Waldorf_Hilton en.wikipedia.org/wiki/The_London_Hilton_on_Park_Lane |
| English to Turkish | hilton | en.wikipedia.org/wiki/Hilton_Hotels en.wikipedia.org/wiki/Great_Western_Hotel,_London en.wikipedia.org/wiki/Waldorf_Hilton en.wikipedia.org/wiki/The_London_Hilton_on_Park_Lane |
| French to English | seine-et-marne | fr.wikipedia.org/wiki/Démographie_de_Seine-et-Marne fr.wikipedia.org/wiki/Seine-et-Marne |
| French to English | esoteric | fr.wikipedia.org/wiki/Augure fr.wikipedia.org/wiki/Divination fr.wikipedia.org/wiki/Effet_Barnum |
| French to English | dancing | fr.wikipedia.org/wiki/Danse |
| French to English | cardiology | fr.wikipedia.org/wiki/Cardiologie fr.wikipedia.org/wiki/Tilt-test |
| French to English | linguistics | fr.wikipedia.org/wiki/Romanche fr.wikipedia.org/wiki/Dalmate |
| French to English | ornithology | fr.wikipedia.org/wiki/Moineau fr.wikipedia.org/wiki/Moineau_domestique |
| French to English | wine | fr.wikipedia.org/wiki/Vin_blanc fr.wikipedia.org/wiki/Vin_rouge |
| French to English | rugby | fr.wikipedia.org/wiki/Rugby fr.wikipedia.org/wiki/William_Webb_Ellis |
| German to English | canterbury | de.wikipedia.org/wiki/Canterbury de.wikipedia.org/wiki/Canterbury_(Begriffserkl%C3%A4rung) |
| German to English | domestication | de.wikipedia.org/wiki/Domestizierung |
| German to English | equestrianism | de.wikipedia.org/wiki/Dressurreiten de.wikipedia.org/wiki/Hohe_Schule_(Reitsport) |
| German to English | railways | de.wikipedia.org/wiki/Neigetechnik |
| German to English | music | de.wikipedia.org/wiki/Oberton |
| German to English | psychiatry | de.wikipedia.org/wiki/Psychiatrie |
| German to English | humour | de.wikipedia.org/wiki/Fawlty_Towers |
| German to English | teaching | de.wikipedia.org/wiki/Lehrer |
| Italian to English | librarianship | it.wikipedia.org/wiki/Biblioteca |
| Italian to English | politics | it.wikipedia.org/wiki/Gianni_De_Michelis it.wikipedia.org/wiki/Mariano_Rumor |
| Portuguese to English | chagas | pt.wikipedia.org/wiki/Doen%C3%A7a_de_Chagas |
| Russian to English | law | ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%B0%D0%B2%D0%BE |
| Spanish to English | montevideo | es.wikipedia.org/wiki/Montevideo es.wikipedia.org/wiki/Bruno_Mauricio_de_Zabala |
| Spanish to English | unicef | es.wikipedia.org/wiki/Fondo_de_Naciones_Unidas_para_la_Infancia es.wikipedia.org/wiki/Niño es.wikipedia.org/wiki/Derechos_del_niño |
| Spanish to English | climbing | es.wikipedia.org/wiki/Escalada_en_hielo |



テーマを決めたら、インターネットからファイルをダウンロードし、**プロジェクト-2** の **/source** フォルダに直接移動します。グラフィックを含むWebページ全体をダウンロードしてください。(Various browsers have slightly different methods for doing this. たとえば、Internet Explorer7.xの場合は、[ファイル]>[名前を付けて保存]>[Webページ]の[完了]を選択します。Firefox5の場合は、[ファイル]>[名前を付けて保存]>[Webページ]の[完了]を選択します)。

**/source** フォルダには、1つまたは複数のHTMLファイルと、グラフィックスファイルなどの関連ファイルが含まれます。フォルダとサブフォルダの構造は保持する必要があります。ブラウザでHTMLファイルを開き、インターネット上に表示されているのとほぼ同じ状態で表示できるはずです。
次に、このチュートリアルで使用するために作成した「レガシーパッケージ」をダウンロードします。

www.omegat.org/training/materials/legacy.zip


legacy.zipアーカイブを適切な一時的な場所(マイドキュメントやデスクトップなど)に展開します。このファイルには、多くの翻訳メモリファイル(拡張子.tmx)とOmegaT用語集ファイル(拡張子.txt)が含まれています。使用する言語の組み合わせに対応する.tmxファイルと用語集(.txt)ファイルを指定します。tmxファイルをOmegaTのプロジェクトフォルダの/tmフォルダに、.txtファイルを/glossaryフォルダにコピーします。


### 翻訳用のHTMLファイルについて、さらに注意すべき点

- これらのファイルをPCのブラウザで表示するとインターネットのページみえかたと、わずかに異って見えますOmegaTにも、ブラウザにも出来ることはありません。Wikipediaでは、ページのテンプレート情報はいずれもダウンロードを許可していないことに起因しています。

- ウィキペディアは絶え間ない変化にさらされている。ここにリストされているページは、適切な例として選択されたものです。(「レガシー」ファイルはこれらに対応するために作成されます)。しかし、変更がはいることで、表示されなくなったり、他の場所に移動することもありえます


- HTMLから翻訳しているときには、特に各ファイルの先頭にあるコードは、翻訳する必要がありません。多くの場合、webリンクなどの文節("文")セグメントの全体は、そのままにします。それらの文節をクリックしたら、訳文は変えないことを確認して、[Enter]を押して次へすすみます。



- HTMLは通常、タグの破損や欠落に対して非常に寛容です。予期しないまたは望ましくないフォーマットの結果のファイルを開くことができる可能性が高いです。タグの処理に関する手順6.A.1を確認します。

- 多数のタグ付けされたHTMLテキストでは、ソーステキストを同時に開き、[Alt]+[Tab])を押して、二つのテキストの実際の内容をすばやく確認しながら、どの文章が翻訳されたのかを確認すると便利です。このチュートリアルでは、ブラウザに何かが表示されている場合は、それを翻訳することにします。

上のスクリーンショットでは、OmegaTと(ブラウザ上の)原文を同時に見えるよう、ウインドウのサイズを小さくしています。


- 作業がおわって、確認する準備ができたら ブラウザで、/target フォルダに生成された訳文をブラウザでひらいて、読み通したり、チェック用に印刷してみましょう。作業完了した訳文をスクリーン(つまりブラウザ)で読み通したいときは、ブラウザとOmegaTを切り変えながら見るといいでしょう。ブラウザウィンドウのテキストにエラーがある場合は、OmegaT内の対応する変更を修正します。



### 翻訳メモリ(ファジーマッチ機能)

最終的には、ファジーマッチに遭遇します。通常、有用なファジーマッチを目撃するまでにそれなりの作業時間が必要です。このチュートリアルでは、少しでも体験できるように、「レガシー」翻訳メモリファイルを提供しています。

「ファジーマッチ」は、ある程度の類似性を持つ過去に翻訳した文節です。これらは現在のプロジェクト内にある場合があります(
現在翻訳中、またはプロジェクトが複数ある場合
ソーステキスト、同じプロジェクト内の別のテキスト)
/tmフォルダに配置したlegacy.tmxファイル。

 /tmフォルダーの legacy .tmxは、以前の翻訳作業の成果なので、みなさんの場合は、 OmegaTでいくつかの作業をこなすまでは、有用なLegacy .tmxファイルをもっていないでしょう。

ここで、現在の文節は、既に翻訳されているプロジェクトのどこかの文節とのファジーマッチを表示したものです。

 ファジーマッチを見て役に立つと判断した場合は
任意の点でアクティブセグメントに([Ctrl]+[I])、またはアクティブセグメントを置換(上書き)するには
完全にセグメント化([Ctrl]+[R])してから修正するか、コピーして貼り付けます。
の一部をアクティブセグメントにコピーして貼り付けます(Ctrl+CおよびCtrl+V)。

このチュートリアルで提供されている従来の資料は、OmegaTの機能を示すための目的で提供しています。いかなる場合でも、提供された翻訳メモリ内の翻訳結果を信頼しないでください。
多くのタグがついた文では、OmegaTはタグのみが同一で、文章が異なるファジーマッチを表示することがあり、あまり便利ではありません。


### 用語集機能

翻訳を開始する前に、用語集ファイルを/glossaryフォルダに配置しました。
用語集ファイルは、2列または3列のタブで区切られた用語が配置されたシンプルなプレーンテキストファイルです。(用語集の設定方法については、ユーザーズマニュアルを参照してください)。

<f0>OmegaTでは、プロジェクトを最初に作成するときに、プロジェクト用の空の既定の用語集ファイルが作成されます。独自の用語集ファイルをさらに追加することもできます。プロジェクトの目的に応じて、各言語のくみあわせ毎に、用語集(.txt)ファイルがつくられます。このファイルは、翻訳時の実用的な支援には限りがありますが、用語集の用語がOmegaTで表示されたときに、OmegaTの用語集ペーンにすぐに表示されることを示します。用語とその翻訳は、それらを含むセグメントに到達すると表示されます。

ワイルドカード文字は使用できません。名詞の前に記事を置かないでください。名詞の性別を示す場合は、用語集の最初のタブのあとに、翻訳を置く列に記事を置きます。したがって、原文が「 ein Mensch」という用語を含み、用語集に原文として「 der Mensch」があったときは見つけられません。「Mensch」を用語集の原文として登録します。新しい用語の追加など、用語集の詳細についてはユーザーズマニュアルを参照してください。

上級者向けには、OmegaT-tokenizer(OmegaTバージョン2.1.1以降で使用)と呼ばれるプラグインがあり、OmegaTは単語の屈折した形を認識できる。興味のある方は、ユーザーマニュアルとYahooのユーザーグループを参照してください。OmegaTの最近のバージョンでは、単語の屈折した形をシステムが認識できるようにする「トークナイザー」機能が自動的に組み込まれています。


### テキスト検索(検索)機能

[Ctrl]+[F]を押すと、任意の用語を検索できる検索ダイアログボックスが表示されます。プロジェクト全体を通して検索できます。つまり原文ファイルとレガシー翻訳メモリファイルを含んだ原文文節と訳文文節、および用語集ファイルです。

用語集の機能と同様に、コピーと貼りつけのキーボードショートカットを使用して、[テキスト検索]ウィンドウの内容をアクティブな翻訳文節に貼り付けることが出来ます。[テキスト検索]ウィンドウに表示されている現在のプロジェクト内のセグメント内のテキストを変更する場合は、そのセグメントをダブルクリックすると、[OmegaT]で該当するセグメントに移動します。

[テキスト検索]ウィンドウには、非常に強力な検索機能があります。詳細については、ユーザーズ・マニュアルを参照してください。
ここで、メインプログラムの外部で「スクリプト」プラグインとして使用できる、自動「グローバル置換」機能はありません。『ユーザーズ・マニュアル』で説明されています。しかし、「対処方法」はあります。


# OmegaTユーザー・グループ

OmegaTには親切で役に立つユーザーグループがある。参加すると、次のことができます。
OmegaTに関する質問をそこに投稿する。

グループはxxにある。
The group is hosted by Yahoo!OmTのメンバーシップはモデレートされています。
まずメンバーの承認が必要です。これは、グループへアクセスしようとするスパム送信者を防ぐためです。参加するには、電子メールを使用して「サインイン」するだけです。モデレータが、真のユーザーであり、スパム送信者ではないことを確認できるように、短いメッセージを送信する必要があります。

