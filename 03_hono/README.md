# 遺伝子発現DB・解析ツールの紹介　担当: <a href="https://sites.google.com/dbcls.rois.ac.jp/hono/" rel="nofollow">小野 浩雅</a>

<p>目次</p>
<div class="contents">
<a id="contents_1"></a>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="#q2fedcc8"> 講習に際しての注意とお願い </a></li>
<li><a href="#eb068d9f"> 【参考】統合TV </a></li>
<li><a href="#z1254cb8"> いざ講習、その前に </a></li>
<li><a href="#ac44a051"> 個々の遺伝子の発現プロファイルを調べる </a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="#s29e8caa"> RefEx?（Reference Expression dataset） </a>
<ul class="list3" style="padding-left:16px;margin-left:16px"><li><a href="#d71c8bae"> 【実習1】RefExを使って、組織特異的遺伝子を検索する </a></li></ul></li>
<li><a href="#bb55f671"> BioGPS </a>
<ul class="list3" style="padding-left:16px;margin-left:16px"><li><a href="#b7dd172e"> 【実習2】BioGPSを使ってある遺伝子の発現プロファイルを調べる </a></li></ul></li></ul></li>
<li><a href="#cb46fe2b"> 数十～数千の遺伝子群の生物学的解釈 </a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="#x426b06b"> DAVID: The Database for Annotation, Visualization and Integrated Discovery </a>
<ul class="list3" style="padding-left:16px;margin-left:16px"><li><a href="#wd2c65be"> マイクロアレイデータの準備 </a></li>
<li><a href="#t120060f"> 【実習3】DAVIDを用いて、発現データの結果を生物学的に解釈する </a></li></ul></li>
<li><a href="#e6714e0c"> PANTHER </a>
<ul class="list3" style="padding-left:16px;margin-left:16px"><li><a href="#t120060f"> 【実習3-2】PANTHERを用いて、発現データの結果を生物学的に解釈する </a></li></ul></li></ul></li>
<li><a href="#n6fd3a54"> NCBI GEOを用いたマイクロアレイデータ解析 (データの検索・生データの取得・統計解析・可視化) </a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="#z337008a"> NCBI Gene Expression Omnibus (GEO) </a>
<ul class="list3" style="padding-left:16px;margin-left:16px"><li><a href="#lca52056"> GEOのエントリについて </a></li>
<li><a href="#p112cdc5"> 【参考】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する </a></li>
<li><a href="#r4b74645"> 【参考】GEO2Rを利用して、GEOに登録されているマイクロアレイデータを解析する </a></li>
<li><a href="#a83d5bfe"> 【参考】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる </a></li>
<li><a href="#ze44dc22"> 【参考】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&amp;生データをダウンロードする </a></li></ul></li>
<li><a href="#b6353d6e"> 【参考】遺伝子発現バンク(GEO)目次、通称「GEO目次」 </a></li></ul></li></ul>
</div>

<h3 id="content_1_0"><a id="q2fedcc8" href="" title="q2fedcc8"><span class="sanchor">_</span></a> 講習に際しての注意とお願い  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>みんなで同時にアクセスするとサイトにつながりにくくなることが予想されます。
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>資料を見ながら自力で進められそうな方はどんどん先に、そうでない方は講師と一緒にすすめていきましょう。</li>
<li>サイトの反応が悪い時はタイミングをずらして実行してみてください。</li>
<li>反応が無いからと言って何度もクリックするとますます遅くなるだけです。おおらかな気持ちで臨みましょう。</li></ul></li>
<li>わからないことがあったら挙手にてスタッフに質問してください。
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>遠慮は無用です(そのための講習会です!)。おいてけぼりは楽しくありません。</li></ul></li></ul>

<h3 id="content_1_1"><a id="eb068d9f" href="" title="eb068d9f"><span class="sanchor">_</span></a> 【参考】統合TV  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/ja/" rel="nofollow">http://togotv.dbcls.jp/ja/</a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>YouTube版もあります　<a href="http://www.youtube.com/user/togotv/videos" rel="nofollow">http://www.youtube.com/user/togotv/videos</a></li></ul></li>
<li>生命科学分野の有用なデータベースやツールの使い方を動画で紹介するウェブサイト
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/ja/contents/category/expression#%E9%81%BA%E4%BC%9D%E5%AD%90%E3%83%BB%E3%82%BF%E3%83%B3%E3%83%91%E3%82%AF%E8%B3%AA%E7%99%BA%E7%8F%BE%E3%82%92%E7%B6%B2%E7%BE%85%E7%9A%84%E3%81%AB%E8%AA%BF%E3%81%B9%E3%81%9F%E3%81%84" rel="nofollow">統合TV の発現制御解析 カテゴリー</a>から探す</li>
<li><a href="http://togotv.dbcls.jp/index.rb?category=%E7%99%BA%E7%8F%BE%E6%83%85%E5%A0%B1" rel="nofollow">旧 統合TVの「発現情報」タグ </a>をクリック！</li></ul></li>
<li>本講習のほぼすべての内容は統合TVに収録されており、いつでもどこでも繰り返し復習できるようになっています。</li></ul>

<h3 id="content_1_2"><a id="z1254cb8" href="" title="z1254cb8"><span class="sanchor">_</span></a> いざ講習、その前に  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>講習内容をスムーズに理解するために押さえておくとよい基礎知識として、<a href="http://motdb.dbcls.jp/?AJACS33%2Fmeso#e3b0f070" rel="nofollow">「遺伝子のDB・ウェブツールの基礎」(過去の講習会ページ)</a>の内容をご参照ください。</li></ul>

<h3 id="content_1_3"><a id="ac44a051" href="" title="ac44a051"><span class="sanchor">_</span></a> 個々の遺伝子の発現プロファイルを調べる  </h3>

<h3 id="content_1_4"><a id="s29e8caa" href="" title="s29e8caa">_</a> <a href="http://refex.dbcls.jp/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px"><span class="noexists">RefEx?</span>（Reference Expression dataset）</span></a>  </h3>
<p><span style="color:green">ヒト、マウス、ラットの4つの異なる実験手法によって得られた40種類の正常組織における遺伝子発現リファレンスデータセット</span></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://refex.dbcls.jp/" rel="nofollow">http://refex.dbcls.jp/</a></li>
<li>正常組織・臓器の遺伝子発現状況を ひと目で
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>4つの異なる実験手法によって得られた40種類の正常組織・臓器における遺伝子発現データを並列に表現することで、手法間の比較とともに各遺伝子の発現量を直感的に比較することができます。</li>
<li>論文を読んでいて見かけた馴染みのない遺伝子がどの組織・臓器で発現しているのか、どんな特徴があるのかを論文の記述ではなく、バイアスの少ない実際の測定データから研究者自身の目で簡単に確認することができます。</li></ul></li>
<li>調べたい遺伝子を より探しやすく より分かりやすく
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>もっとも基本的なキーワード・遺伝子名検索では逐次的に検索語候補が提示されるので、遺伝子名をすべて正確に入力する必要はありません。</li>
<li>『転写因子』や『Gタンパク質共役受容体』などのようなあるカテゴリーに属した遺伝子群についてまとめて検索できるよう整理されています。</li>
<li>さまざまな実験において比較対照などによく用いられる『組織特異的遺伝子』を一覧することができます。</li></ul></li>
<li>直感的な可視化で 新たな知識発見・仮説構築を
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>組織間の比較と測定手法間の比較を両立させた相対発現量のバーチャートを表示するとともに人体の3Dモデルに発現量を反映させたヒートマップを表示しています。</li>
<li>リスト機能を用いて任意で選んだ最大3つの遺伝子について、発現データを含む全ての詳細データを並列に比較することができ、遺伝子発現解析などで見出された不詳な遺伝子群の関係性を知るためのツールとしても有用です。</li></ul></li>
<li>再利用可能で有用なパブリックデータの活用例
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>RefExで使用しているデータは公的データベースの中から、正常組織・臓器における遺伝子発現データのリファレンスとするにふさわしいデータセットを、測定サンプルの広範さなどを基準に選び出し、クオリティチェックを行い、互いに比較できるように整理しなおしたものです。さらに、RefExが提供するすべてのデータもまた、クリエイティブ・コモンズ (CC) ライセンス ( &#65533; DBCLS Licensed under CC 表示 2.1 日本 )のもとで、自由にダウンロードおよび再利用することができます。</li></ul></li></ul>

<h4 id="content_1_5"><a id="d71c8bae" href="" title="d71c8bae">_</a> 【実習1】RefExを使って、組織特異的遺伝子を検索する  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20140222.html#p01" rel="nofollow">【復習用】RefExの使い方</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://refex.dbcls.jp/testsite" rel="nofollow">http://refex.dbcls.jp/</a> を開きます。</li>
<li>2. 画面中央の「組織特異的に発現する遺伝子を見る」の臓器アイコンにカーソルを合わせると、更に詳細な部位のアイコンが出るので、調べたい臓器（例は<a href="http://MotDB.DBCLS.jp/?%5B%5Bhttp%3A%2F%2Frefex.dbcls.jp%2Fgenelist.php%3Flang%3Dja%26db%3Dhuman%26gc40%5B%5D%3Dv31%26order_key%3Dscore%5D%5D" title="http://refex.dbcls.jp/genelist.php?lang=ja&amp;db=human&amp;gc40[]=v31&amp;order_key=score" rel="nofollow">肝臓</a>）をクリックします。</li>
<li>3. 検索結果一覧では、「ソート項目の切り替え」や「絞り込み検索」、「リストへの追加」ができます。</li>
<li>4. ソート項目を切り替えて、どのように結果が変わるでしょうか。</li>
<li>5. 絞り込み検索は左のバーから行えます。
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>遺伝子名に「liver」を含むデータは何件あるでしょうか。</li>
<li>「遺伝子名」の下の「条件なし」をクリックして表示されるウインドウに「liver」と入力し、「Include」をクリックし、「この条件で絞り込み」を押します。</li>
<li>また「遺伝子名」の項目で「Exclude」に「solute」を加えると、検索結果はどう変わるでしょうか。</li>
<li>さらに「必ず含むデータセット」の「ALL」にチェックを入れると、検索結果はどう変わるでしょうか。</li>
<li>右上の「ダウンロード」をクリックすると検索結果のタブ区切りテキストがダウンロードできます。</li></ul></li>
<li>6. 各遺伝子の青字の部分（例 <a href="http://refex.dbcls.jp/gene_info.php?lang=ja&amp;db=human&amp;geneID=2243&amp;refseq=NM_000508&amp;unigene=Hs.351593&amp;probe=205649_s_at" rel="nofollow">fibrinogen alpha chain</a>）をクリックすると詳細情報を閲覧できます。</li>
<li>7. 「ヒートマップ on Bodyparts3D」では、表示する部位の切り替え（全身・体幹部・頭部）ができます。「皮膚・骨格筋を表示」もしくは「アニメーション表示」にチェックを入れるとどのように表示されるでしょうか。</li>
<li>8. 「組織40分類別データ」では、バーの上にマウスオーバーすると測定部位と発現値が表示されます。</li>
<li>9. 「Download」をクリックすると、表示中の遺伝子の組織40分類別の発現データがタブ区切り形式でダウンロードできます。</li>
<li>10. 「Probe set ID」のリンク先をクリックすると、どういう情報が参照できるでしょうか。</li>
<li>11. オーソログ対応遺伝子について、ヒトとマウスで比較してみましょう。どのような違いがあるでしょうか。</li>
<li>12. 個々の遺伝子の詳細情報は、リストに追加することで並列に比較することができます。
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="http://bit.ly/16WrPJU" rel="nofollow">肝臓特異的遺伝子の検索結果一覧</a>に移動して、3つの遺伝子を「リストに追加」してみましょう。</li>
<li>追加した件数は「リストを見る」の横に表示されます。</li>
<li>「リストを見る」をクリックするとリストに移動します。</li>
<li>『並べて表示する』にチェックを入れて、「遺伝子を並べて表示」をクリックします。</li>
<li>並列に比較することで見えてくる「違い」はなんでしょうか。</li></ul></li>
<li>13. 自分の研究テーマに関連する、また興味のある遺伝子について検索してみましょう。</li></ul>

<h3 id="content_1_6"><a id="bb55f671" href="" title="bb55f671">_</a> <a href="http://biogps.org/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">BioGPS</span></a>  </h3>
<p><span style="color:green">ヒト、マウス、ラットのさまざまな組織や細胞(株)における遺伝子発現プロファイルのデータベース</span></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://biogps.org/" rel="nofollow">BioGPS</a>はAffymetrix社製のマイクロアレイであるGeneChipを用いたさまざまな組織や細胞(株)遺伝子発現プロファイルのデータベース。
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>検索した遺伝子に対して、種々の外部データベースを横断検索することができるだけでなく、それらの設定を保存したり、表示方法を自由にカスタマイズすることができる「Gene annotation portal」。</li>
<li>外部データベースには、Wikipedia(Gene Wiki)、著名な試薬会社の検索窓へのリンク集、pathway、Nature系DB、モデル生物DB、文献DBなど多種多様</li>
<li>マウスのエキソンアレイのデータから遺伝子のスプライシングバリアント(Splicing variant)の発現状況も調べることが可能。最近ではCircadian関係のデータも。</li></ul></li>
<li>さらに最近のアップデートで、NCBI Gene Expression Omnibus (GEO)中から選抜されたデータセットに切り替えて発現状況を調べることが可能に。</li></ul>

<h4 id="content_1_7"><a id="b7dd172e" href="" title="b7dd172e">_</a> 【実習2】BioGPSを使ってある遺伝子の発現プロファイルを調べる  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120911.html#p01" rel="nofollow">【復習用】遺伝子発現プロファイルデータベースBioGPSを使い倒す2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li><a href="http://togotv.dbcls.jp/20100829.html#p01" rel="nofollow">【以前の講習会動画】遺伝子発現データベースの活用法</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://biogps.org/" rel="nofollow">http://biogps.org/</a>を開きます。</li>
<li>2.骨格筋の分化決定遺伝子であるMyogenic differentiation 1(MyoD)の発現プロファイルを調べてみましょう。中央の検索窓に「myod」と入力し、「search」を押します。</li>
<li>3. 表示された検索結果の中から「ID 4654」をクリックします。</li>
<li>4. 最初はヒトのマイクロアレイデータが表示されます。</li>
<li>5. 画面左側の&quot;Current Gene List&quot;は右上の&lt;&lt;アイコンをクリックすると非表示にできます。非表示にすることで画面を広く使うことができます。</li>
<li>6. ページ内のウインドウは通常のウインドウと同じようにドラッグによる移動やサイズの変更などを行うことができます。 歯車マークのメニューから&quot;Open in browser&quot; を選択すると、新しいタブで表示できます。</li>
<li>7. &quot;Search&quot; と書かれた窓に単語(組織名など)を入力すると、その単語の含まれた部分が赤くハイライト表示されます。今回は &quot;Muscle&quot; と入力してみます。</li>
<li>8. &quot;Zoom&quot; のバーを用いることで、グラフの表示範囲を調整することが出来ます。</li>
<li>9. 発現量を示すバーをクリックすると発現強度の値が表示されます。</li>
<li>10. マイクロアレイデータ右上の&quot;Species: Hs&quot;をクリックするとマウスやラットを選択できるので、&quot;M. musculus (Mouse)&quot;をクリックしてマウスのデータを表示できます。</li>
<li>11. MyoDはどの組織、細胞で強く発現しているでしょうか？</li>
<li>12. 場合によっては&quot;Probeset&quot;のプルダウンメニューから複数の項目を選択できる場合があります。これはどのようなケースが考えられるでしょうか？</li>
<li>13. &quot;Static Image&quot; をクリックすると、ズームや検索機能などのついていない、画像だけのグラフで表示されます。低スペックなマシンでは、こちらの方が軽快に動作するでしょう。</li>
<li>14. &quot;Correlation&quot;タブをクリックして検索すると、発現パターンが似ている他の遺伝子を検索できますが、どのような遺伝子が出てくるでしょうか？</li>
<li>15. &quot;Downloads&quot; をクリックすると現在表示している遺伝子の発現データを CSV 形式でダウンロードできます。</li>
<li>16. &quot;Dataset&quot;の右にある'change&quot;をクリックすると、デフォルトで用意されているデータセットやNCBI GEO中のデータセットを検索でき、それらのデータに表示を切り替えることができます。&quot;Species: Hs&quot;に切り替えてから、&quot;change&quot;をクリックしたあと、&quot;Default Datasets&quot;から&quot;Barcode on normal tissues (262 samples)&quot;を選択します。どのようにデータが変わったでしょうか。</li>
<li>17. さらに&quot;Search&quot;からキーワード検索で、GEOのデータを検索してみましょう。&quot;C2C12&quot;と検索するとどのようなデータが選択できるでしょうか。</li>
<li>18. 右上の「default rayout」をクリックすると、検索した遺伝子に関して種々の外部データベースを横断検索できますが、どのようなデータが閲覧できるのか調べてみましょう。</li>
<li>19. 左上の「Search」タグをクリックして検索画面にもどり、自分の興味ある遺伝子について同様に検索してみましょう。
すぐに自分の興味ある遺伝子が浮かばない場合は、著名な<a href="http://ja.wikipedia.org/wiki/%E4%BA%BA%E5%B7%A5%E5%A4%9A%E8%83%BD%E6%80%A7%E5%B9%B9%E7%B4%B0%E8%83%9E" rel="nofollow">iPS細胞</a>を作るために必要な4因子（Oct3/4・Sox2・Klf4・c-Myc）がどの組織で発現しているか、またデータを切り替えて検索してみましょう。</li></ul>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>【余談】
<a href="http://biogps.org/iphone/" rel="nofollow">BioGPSのiPhoneアプリ</a>が無料で公開されていますので、「あの遺伝子はどの組織で発現してるのかな？」とふと調べたいときにお手持ちのiPhoneで遺伝子発現を調べられます。</li></ul>

<h3 id="content_1_8"><a id="cb46fe2b" href="" title="cb46fe2b"><span class="sanchor">_</span></a> 数十～数千の遺伝子群の生物学的解釈  </h3>

<h3 id="content_1_9"><a id="x426b06b" href="" title="x426b06b">_</a> <a href="http://david.abcc.ncifcrf.gov/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">DAVID: The Database for Annotation, Visualization and Integrated Discovery</span></a>  </h3>
<p><span style="color:green">マイクロアレイデータの生物学的な解釈</span></p>
<blockquote><p class="quotation"><a href="http://david.abcc.ncifcrf.gov/" rel="nofollow">http://david.abcc.ncifcrf.gov/</a></p></blockquote>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>マイクロアレイ実験の一般的な目的は、実験条件によって得られた数十～数千の遺伝子群の発現が生物学的にどういう意味を持つかを考えることです。
<div class="img_margin" style="text-align:left"><img src="microarray.analysis.005.png" alt="microarray.analysis.005.png" title="microarray.analysis.005.png" width="410" height="242" /></a></div>
</li>
<li>今回は、その方法の一つとして、マイクロアレイの結果に<a href="http://www.google.co.jp/url?sa=t&amp;source=web&amp;cd=4&amp;ved=0CEEQFjAD&amp;url=http%3A%2F%2Fja.wikipedia.org%2Fwiki%2F%25E9%2581%25BA%25E4%25BC%259D%25E5%25AD%2590%25E3%2582%25AA%25E3%2583%25B3%25E3%2583%2588%25E3%2583%25AD%25E3%2582%25B8%25E3%2583%25BC&amp;ei=ve9QTd6XMtG6cbeW1KUH&amp;usg=AFQjCNF8U-O4ktlMGoR9DNC0wKltmbjtmw" rel="nofollow">Gene Ontology</a>の用語を付与することで、生物学的な解釈を行います。</li></ul>

<h4 id="content_1_10"><a id="wd2c65be" href="" title="wd2c65be">_</a> マイクロアレイデータの準備  </h4>
<p>サンプルデータとして、<a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">NCBI GEO</a>より取得した公共の遺伝子発現データを用います。このデータは、ある実験の前後の2群間で有意に発現減少した遺伝子群のリストです。
<br class="spacer" />
→ <a href="http://motdb.dbcls.jp/?plugin=attach&amp;refer=AJACS24%2Fhono&amp;openfile=110208_IDlist.txt" rel="nofollow">マル秘遺伝子リスト</a>
<br class="spacer" />
（右クリックして「新しいタブで開く」もしくは「名前を付けてリンク先を保存」してください。）
<br class="spacer" />
このデータは、どのような実験から得られたデータなのか、どのように解釈できるのかをDAVIDを使って考察してみましょう！</p>

<h4 id="content_1_11"><a id="t120060f" href="" title="t120060f">_</a> 【実習3】DAVIDを用いて、発現データの結果を生物学的に解釈する  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120927.html#p01" rel="nofollow">【復習用】DAVIDを使ってマイクロアレイデータを解析する 2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li><a href="http://togotv.dbcls.jp/20130528.html#p01" rel="nofollow">【復習用】DAVIDの使い方 実践編</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. 上部メニューの「Start Analysis」をクリックします。</li>
<li>2. 画面左側バーで、probe IDリストをコピペ or ファイルを指定します。</li>
<li>3. リストのIDの種類タイプを選択します。 … 今回は、「AFFY_ID」と「Gene List」</li>
<li>4. Submit List をクリックするとリストが読み込まれます。</li>
<li>5. アップロードしたリストは、左側バーの「List Manager」で「Uploaded List_1」として保存されています。削除やrenameもできます。</li>
<li>6. 解析を続けます。真ん中の「Functional Annotation Tool」をクリックします。</li>
<li>7. 「Gene Ontology」をクリックすると、Gene Ontologyを用いた解析の細かいメニューが表示されます。</li>
<li>8. 今回は、GOTERM_BP_FAT (BP=Biological Process)に注目します。その右の「Chart」をクリックすると結果がポップアップされます。</li>
<li>9. P-value を2回クリックしてp-valueが小さい（統計的に有意である）順にしてみましょう … p-value小さい順は、一度やればしばらく覚えているので、次からはしばらくは必要ないです

<a name="plugin_fold_anchor1"></a>
<div class="plugin_fold_title_plus" onclick="return plugin_fold_onclick(this,event,'plugin_fold_anchor1')"><p>結果</p>
</div>
<div class="plugin_fold_body"><div class="img_margin" style="text-align:left"><img src="david_go_bp.png" alt="david_go_bp.png" title="david_go_bp.png" width="989" height="833" /></a></div>

</div></li>
<li>[応用編] Pathways &gt; KEGG_PATHWAY や Tissue Expression &gt; UP_TISSUE なども見てみましょう。生物学的にどういうことが言えるでしょうか。
<a name="plugin_fold_anchor2"></a>
<div class="plugin_fold_title_plus" onclick="return plugin_fold_onclick(this,event,'plugin_fold_anchor2')"><p>サンプルデータの答え</p>
</div>
<div class="plugin_fold_body"><p>Arabidopsis thaliana (シロイヌナズナ)の植物細胞と細胞壁分解酵素を用いて取り除いた植物細胞（<a href="http://ja.wikipedia.org/wiki/%E3%83%97%E3%83%AD%E3%83%88%E3%83%97%E3%83%A9%E3%82%B9%E3%83%88" rel="nofollow">プロトプラスト</a>）との比較（＝植物細胞の<a href="http://ja.wikipedia.org/wiki/%E3%82%AB%E3%83%AB%E3%82%B9_%28%E6%A4%8D%E7%89%A9%29" rel="nofollow">脱分化</a>前・後）</p>
</div></li></ul>
<p><br class="spacer" /></p>

<h3 id="content_1_12"><a id="e6714e0c" href="" title="e6714e0c">_</a> <a href="http://pantherdb.org/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">PANTHER</span></a>  </h3>
<p><span style="color:green">DAVIDに似たマイクロアレイデータの解析ツール</span></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>DAVIDでの解析結果が芳しくなかった場合に、セカンドオピニオン(?)として、PANTHERを使ってみるのも手です。</li>
<li>先ほどと同じデータを使って、解析結果にどのような違いがあるか調べてみましょう。
<br class="spacer" /></li></ul>
<p><br class="spacer" /></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>しかし、<a href="http://pantherdb.org/" rel="nofollow">PANTHER</a>では、<a href="http://pantherdb.org/tips/tips_batchIdSearch_supportedId.jsp" rel="nofollow">サポートされているID</a>が少なく、先ほどのデータのIDはそのまま使えません。</li>
<li>そこで、まずはIDの変換をします。ID変換ツールとして<a href="http://www.biomart.org/" rel="nofollow">BioMart</a><a id="notetext_1" href="#notefoot_1" class="note_super" title="参考統合TV">*1</a>などが有名ですが、今回はDAVIDのID変換機能を紹介します。
<br class="spacer" /></li></ul>
<p><br class="spacer" /></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>ID変換は、「<a href="http://david.abcc.ncifcrf.gov/tools.jsp" rel="nofollow">Start Analysis</a>」をクリックした先の「Analysis Wizard」の下部にある<a href="http://david.abcc.ncifcrf.gov/conversion.jsp" rel="nofollow">Gene ID Conversion Tool</a> から行います。</li>
<li>ID変換したいリストが既にアップロードしてある場合には、そのまま「Option 1: Convert the gene list being selected in left panel to」の項目を、変換したいIDに変え(今回はENTREZ_GENE_ID)、「Submit to Conversion tool」をクリックします。</li>
<li>ID変換の対応表が出力されます。右上の「Download File」から対応表をダウンロードできます。
<br class="spacer" /></li>
<li><a href="http://togotv.dbcls.jp/20130528.html#p01" rel="nofollow">【復習用】DAVIDの使い方 実践編 </a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a> 後半にID変換の話が出てきます。</li></ul>
<p><br class="spacer" /></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>その後、Entrez Gene ID行のみに整形したテキストファイルをPANTHERにSubmitします。
<br class="spacer" />
→ <a href="http://motdb.dbcls.jp/?plugin=attach&amp;pcmd=open&amp;file=affy_to_geneid.txt&amp;refer=AJACS35%2Fhono" rel="nofollow">変換済みマル秘遺伝子リスト</a>
<br class="spacer" /></li></ul>

<h4 id="content_1_13"><a id="t120060f" href="" title="t120060f">_</a> 【実習3-2】PANTHERを用いて、発現データの結果を生物学的に解釈する  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20130430.html#p01" rel="nofollow">【復習用】PANTHERを使ってマイクロアレイデータを機能解析する</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. トップページのGene List Analysisから遺伝子リストのアップロードをします。</li>
<li>2. 「Enter IDs:」にコピペするか、「Upload IDs:」から遺伝子リストのファイルをアップロードします。</li>
<li>3. 「Select List Type:	」でアップロードするリストの種類を選択します。今回は、「ID List」を選択します。</li>
<li>4. 続いて、「2.Select organism.」 で生物種を選択します。今回は、「Arabidopsis thaliana」を選択します。</li>
<li>5. 「3.Select Analysis.」で「Statistical overrepresentation test」を選択し、Submit します。</li>
<li>6. 「Select lists to analyze」で、解析するリストを確定します。続けてアップロードするリストがある場合には、ここで追加します。リストが選択されていることを確認したら、「Finished selecting lists」をクリックします。</li>
<li>7. 次にSelect Reference Listを選択します。(デフォルトではSelect List(s)で選んだ生物種のwhole-genome listが選択されるので、他の生物種と比較を行いたい場合は適宜選び直してください。)</li>
<li>8. 最後に、Search optionsを指定します。今回はデフォルトのまま GO Biological Process にチェックを入れておきます。</li>
<li>9. Launch Analysisをクリックして分析結果を表示します。</li>
<li>7. まず、P-valueの昇順でリストが表示されます。どのようなGO termが上位に来ているでしょうか。またそれらをDAVIDと比較してみましょう。</li>
<li>8. [応用編] Viewを切り替えて、さまざまなグラフ形式で解析結果を見てみましょう。生物学的にどういうことが言えるでしょうか。</li>
<li>9. その他のデータではどのような結果が表示されるでしょうか。<a href="http://motdb.dbcls.jp/?plugin=attach&amp;pcmd=open&amp;file=gse1657_adipo_up500_geneid.txt&amp;refer=AJACS38%2Fhono2" rel="nofollow">参考動画で使われているヒトの脂肪細胞の分化過程(GSE1657)で発現増加した上位500個の遺伝子群のEntrez Gene IDリスト</a></li></ul>
<hr class="full_hr" />

<h3 id="content_1_14"><a id="n6fd3a54" href="" title="n6fd3a54"><span class="sanchor">_</span></a> NCBI GEOを用いたマイクロアレイデータ解析 (データの検索・生データの取得・統計解析・可視化)  </h3>

<h3 id="content_1_15"><a id="z337008a" href="" title="z337008a">_</a> <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">NCBI Gene Expression Omnibus (GEO)</span></a>  </h3>
<p><span style="color:green">世界最大の遺伝子発現（<a href="http://ja.wikipedia.org/wiki/DNA%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%82%A2%E3%83%AC%E3%82%A4" rel="nofollow">マイクロアレイ</a>）データベース（レポジトリ）</span></p>
<blockquote><p class="quotation"><a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a></p></blockquote>

<h4 id="content_1_16"><a id="lca52056" href="" title="lca52056">_</a> <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">GEO</a>のエントリについて  </h4>
<pre>    GEO ID 番号の最初の3文字が
    GPL:  プラットフォーム（マイクロアレイ等の型番）
    GSM: サンプル（1枚のマイクロアレイから出たデータ）
    GSE:  シリーズ（1つの実験で出たデータを集めたもの。通常複数の GSM からなる）
    GDS:  データセット（NCBIで比較可能なデータを集めて再編成したもの。GEO上で簡単な解析が可能）</pre>
<p><br class="spacer" /><br class="spacer" /></p>

<h4 id="content_1_17"><a id="p112cdc5" href="" title="p112cdc5">_</a> 【参考】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120128.html#p01" rel="nofollow">【復習用1】NCBI GEOの使い方3～データセットブラウザの使い方1～ 2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li><a href="http://togotv.dbcls.jp/20120227.html#p01" rel="nofollow">【復習用2】NCBI GEOの使い方4～データセットブラウザの使い方2～ 2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2.「Gene profiles」に自分の検索したい遺伝子名を入力します。</li>
<li>3. 今回は例として「<a href="http://www.google.co.jp/search?hl=ja&amp;q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90" rel="nofollow">nanog</a>」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。</li>
<li>4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験におけるnanog遺伝子の発現データが表示されます。</li>
<li>5. 検索結果の<a href="http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294" rel="nofollow">アクセッション番号（今回は GDS2294）</a>をクリックすると、解析用の「データセットブラウザ」が開きます。</li>
<li>6. 「<a href="http://MotDB.DBCLS.jp/?%5B%5Bhttp%3A%2F%2Fwww.ncbi.nlm.nih.gov%2Fgeoprofiles%3Fterm%3DGDS2294%5BACCN%5D%5D" title="http://www.ncbi.nlm.nih.gov/geoprofiles?term=GDS2294[ACCN" rel="nofollow">Expression profiles</a>」をクリックすると、<a href="http://MotDB.DBCLS.jp/?%5B%5Bhttp%3A%2F%2Fwww.ncbi.nlm.nih.gov%2Fsites%2Fentrez%3Fdb%3Dgeo%26cmd%3Dsearch%26term%3DGDS2294%5BACCN%5D%5D" title="http://www.ncbi.nlm.nih.gov/sites/entrez?db=geo&amp;cmd=search&amp;term=GDS2294[ACCN" rel="nofollow">この実験データセットにおける個々の遺伝子発現状況を検索できるページ</a>に飛びます。</li>
<li>7. 検索窓に表示されているアクセッション番号の後に続けて遺伝子名を追加（今回は例として <a href="http://www.google.co.jp/search?q=Oct4" rel="nofollow">Oct4</a> ）すると、この実験データセット内におけるその遺伝子の発現データが検索できます。</li>
<li>8. 「データセットブラウザ」の「<a href="http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294#details" rel="nofollow">Data Analysis Tools</a>」では詳細なデータ解析が可能です。</li>
<li>9. 「Find gene name or symbol:」のところに自分の興味ある遺伝子名を入れてみましょう。</li>
<li>10. 「Find genes that are up/down for this condition(s):」の「GO」をクリックするとどのような遺伝子がヒットするでしょうか。</li>
<li>11. 「Compare 2 sets of samples」では2群間で発現に差のある遺伝子を（統計学的に）検索できます。step1で発現量の違いを検出する方法を設定します。step.2で比較する2群の設定をします。step.3の「Query Group A vs. B」をクリックすると、検索が始まります。</li>
<li>12. 「Cluster heatmaps」では、マイクロアレイデータ解析でよく用いられる<a href="http://MotDB.DBCLS.jp/?%5B%5Bhttp%3A%2F%2Fimages.google.co.jp%2Fimages%3Fq%3D%A5%D2%A1%BC%A5%C8%A5%DE%A5%C3%A5%D7%5D%5D" title="http://images.google.co.jp/images?q=ヒートマップ" rel="nofollow">ヒートマップ</a>でのデータ表示が行なえます。分類方法としてHierarchical、Partitional (K-means/K-medians)、By location on chromosomeの3種類が選べますが、それぞれどのようにデータが分類されるか試してみましょう。</li>
<li>13. ヒートマップ上をクリックすると領域選択が開始されます。リサイズや移動で範囲を決定した後、Stack up をクリックすると選択した範囲が拡大されます。</li>
<li>14. サンプルの内容とIDの対応は、元のページに戻って、Sample Subsets から確認できます。</li>
<li>15. さらに範囲選択して、Plot values をクリックすると、各遺伝子のサンプルごとの発現の様子がプロットで確認できます。</li>
<li>16. 範囲選択して、View in Entrez をクリックすると、選択範囲内のデータを棒グラフで見られます。</li>
<li>17. 範囲選択して、Download をクリックすると、選択範囲内のデータがテキスト形式でダウンロードできます。</li>
<li>18.  「Experiment design and value distribution」では実験データにおける発現の分布を参照できます。これにより、各サンプルのデータが互いに比較可能か（実験上のミスがないか）チェックすることができます。</li></ul>

<h4 id="content_1_18"><a id="r4b74645" href="" title="r4b74645">_</a> 【参考】GEO2Rを利用して、GEOに登録されているマイクロアレイデータを解析する  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120524.html#p01" rel="nofollow">【復習用】NCBI GEOの使い方5～GEO2Rを使う～</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2. 画面中央下の「<a href="http://www.ncbi.nlm.nih.gov/geo/browse/?view=series" rel="nofollow">Series</a>」をクリックします。</li>
<li>3. 検索機能を使って興味のある実験データセットを探すことができます。</li>
<li>4. 今回は喫煙による遺伝子発現の変化に関するデータについて調べたいというモチベーションを例にするので、「cigarette smoke」と入力し、検索します。</li>
<li>5. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE17913" rel="nofollow">GSE17913 - Effects of Cigarette Smoke on the Human Oral Mucosal Transcriptome</a> という喫煙による口腔粘膜の遺伝子発現を調べたデータセットが見つかったので、「<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE17913" rel="nofollow">GSE17913</a>」をクリックします。</li>
<li>6. 今回のテーマであるGEO2Rへのリンクはページ下部にあるので、リンクをクリックし<a href="http://www.ncbi.nlm.nih.gov/geo/geo2r/?acc=GSE17913" rel="nofollow">GEO2Rのページに移動</a>します。</li>
<li>7. このデータセットに含まれるサンプルの一覧が表示されます。列見出しをクリックすると各項目でソートできます。「Title」をクリックすると、今回のデータセットが、喫煙者・非喫煙者のそれぞれ男性・女性の頬粘膜(buccal mucosa)から得られたサンプルであることがわかります。</li>
<li>8. 比較したいグループをそれぞれ設定します。「Define groups」をクリックして、それぞれのグループ名を入力します。今回は、非喫煙者の女性(never_smoker_F)と、喫煙者の女性(smoker_F)のサンプルをそれぞれグループ化します。</li></ul>
<p><span style="color:red">（※GEO2Rの各ジョブの実行は時間がかかるので要注意。講習では<a href="http://togotv.dbcls.jp/20120524.html#p01" rel="nofollow">復習用統合TV</a>の実行結果を見ながら進めるので、実行しないでください。）</span></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>9. グループに入れたいサンプルをクリックやドラッグで選択してからグループ名をクリックすると、サンプルがグループに登録されます。</li>
<li>10. 次に、「Samples」をクリックした後、「Value distribution」タブをクリックし、「View」をクリックすると各サンプルの発現分布を調べることができます。</li>
<li>11. 発現分布が箱ひげ図で示されます。データセットブラウザと異なり、GEO2R では投稿された生のデータを用いて解析されます。</li>
<li>12. &quot;Export&quot; をクリックすると、箱ひげ図で与えられている値をまとめたタブ区切りテキストが表示され、これらを保存できます。</li>
<li>13. GEO2R タブに戻り、&quot;Top 250&quot; をクリックすると、選択したグループ間で各遺伝子の発現量に差があるかどうかの t 検定の結果、P 値が小さい順に 250 件表示されます。&quot;P.Value&quot; は元の P 値、&quot;adj.P.Val&quot; は多重検定の補正をかけた後の P 値です。有意性の評価は adj.P.Val に基づいています。
&quot;t&quot; は普通の t の標準偏差を全遺伝子の標準偏差を用いて調整したもの (moderated-t) です。普通の t より精度が上がっていますが、普通の t 分布に従うものとして扱えます。 &quot;B&quot; は2つのグループで発現量が異なっている対数オッズ値です。exp(B)/(1+exp(B)) の値が、発現量が異なっている確率で
す。&quot;logFC&quot; は、発現量の差が何倍であるかを2底の対数にしたものです。つまり値が 2 なら 4 倍の差を示しています。ここでの解析では発現量が対数で与えられている必要がありますが、元のデータでは対数になっていないことがあります。そのような場合デフォルトでは自動検出し、対数変換して計算してくれます。その上でこのような表示がされます。</li>
<li>14. 行をクリックすると、その行の遺伝子の各サンプルでの発現量グラフが見られます。</li>
<li>15. 今回喫煙者女性・非喫煙者女性間で最も差が大きいとされた遺伝子であるシトクロム P450 (異物代謝に関わる遺伝子)は、喫煙者群で有意に発現増加したことがわかります。</li>
<li>16. &quot;Sample values&quot; をクリックすると、発現量の値が一覧できます。</li>
<li>17. &quot;Select columns&quot; をクリックすると、表示するカラムを変更できます。 &quot;logFC&quot; を消し &quot;GO.Function&quot; を追加してみましょう。</li>
<li>18. &quot;Save all results&quot; をクリックすると、結果をテキストで表示・保存できます。</li>
<li>19. Options タブをクリックすると、いくつかの設定を変更できます。右の項目は多重検定の補正法の選択です。デフォルトでは Benjamini &amp; Hochberg の方法が使われていますが、これを Bonferroni の方法に変更してみます。中央はデータの対数をとるかどうかの選択です。デフォルトでは先程説明したとおり自動検出です。左の項目はプラットフォームの注釈の選択です。&quot;NCBI generated&quot; がある場合はそれの方が信頼できます。</li>
<li>20. Options に変更を加えたら、GEO2R タブに戻って &quot;Recalculate&quot; をクリックします。 変更を反映した計算結果が表示され、多重検定の補正法を変更したため、adj.P.Val が変わっていることがわかります。</li>
<li>21. Profile graph の項目では、プローブ ID を元に、個々の遺伝子の発現状況を調べることができます。</li>
<li>22. 「View data for (platform ID)」をpクリックするとプラットフォームの情報が表示されるので、目的の遺伝子のプローブ ID を、ブラウザの検索機能 (Ctrl+F)を用いて調べます。今回は例としてNFE2L2（酸化ストレスによって活性化する転写因子）を検索してみましょう。</li>
<li>23. 一番左がプローブIDなので、これをコピーし、さきほどの&quot;Enter ID&quot; の窓にプローブ ID をペーストし、&quot;Set&quot; をクリックすると。発現量のグラフが表示されます。（なおこの操作では、何の計算も実行されないので、検定の結果の P 値を調べることはできません。）</li>
<li>24. R script タブをクリックするとこれまでに実際に実行された R のスクリプトを見ることができます。これを参考に、手元の R でパラメータを調整するなどして更なる解析を行うことができます。</li>
<li>R の使い方については、下記の統合TV のコンテンツ「統計解析ソフト「R」の使い方」シリーズをご覧ください。</li>
<li><a href="http://togotv.dbcls.jp/20090618.html#p01" rel="nofollow">統計解析ソフト「R」の使い方 ～導入編～</a></li>
<li><a href="http://togotv.dbcls.jp/20091219.html#p01" rel="nofollow">統計解析ソフト「R」の使い方 ～ヒートマップ編～</a></li>
<li><a href="http://togotv.dbcls.jp/20111107.html#p01" rel="nofollow">統計解析ソフト「R」での立廻り</a></li></ul>

<h4 id="content_1_19"><a id="a83d5bfe" href="" title="a83d5bfe">_</a> 【参考】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20111020.html#p01" rel="nofollow">【復習用】NCBI GEOの使い方2～遺伝子プロファイルの検索・処理済みデータの取得～ 2011</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2.「Gene profiles」に自分の検索したい遺伝子名を入力します。</li>
<li>3. 今回は例として「<a href="http://www.google.co.jp/search?hl=ja&amp;q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90" rel="nofollow">nanog</a>」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。</li>
<li>4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。</li>
<li>5. 検索結果の右端にある画像をクリックすると、<a href="http://www.ncbi.nlm.nih.gov/geo/gds/profileGraph.cgi?&amp;dataset=DEAryz&amp;dataset=yyyzzz$&amp;gmin=5173.000000&amp;gmax=11680.000000&amp;absc=&amp;gds=2294&amp;idref=161072_at&amp;annot=Nanog" rel="nofollow">発現データの詳細をみる</a>ことができます。</li>
<li>6. <a href="http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294" rel="nofollow">このサンプル（GDS2294）</a>では、nanogはどういう細胞のどういう実験条件で発現が増減しているか調べてみましょう。</li>
<li>7. ページ下部の「samples」に列挙された<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365" rel="nofollow">リンク</a>をクリックすると、そのサンプル（一枚のマイクロアレイ）の詳細を閲覧できます。</li>
<li>8. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365" rel="nofollow">リンク先のページ</a>の中ほどにある<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583" rel="nofollow">「series」のリンク</a>をクリックすると、この実験全体の詳細情報が見られます。</li>
<li>9. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583" rel="nofollow">この実験全体の詳細情報ページ</a>の下部にある<a href="ftp://ftp.ncbi.nih.gov/pub/geo/DATA/SeriesMatrix/GSE5583/" rel="nofollow">「Series Matrix File(s)」</a>をクリックすると、この実験の正規化補正済みのマイクロアレイデータをダウンロードすることができます。</li></ul>

<h4 id="content_1_20"><a id="ze44dc22" href="" title="ze44dc22">_</a> 【参考】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&amp;生データをダウンロードする  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20110711.html#p01" rel="nofollow">【復習用】NCBI GEOの使い方1～マイクロアレイデータの検索・取得～ 2011</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2. 画面中央の「Platforms」をクリックします。</li>
<li>3. <a href="http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=imageSummaryByMrk&amp;key=25000&amp;imageType=8" rel="nofollow">Platform(マイクロアレイの種類)の一覧画面が現れる</a>ので、上部の「FIND PLATFORM」をクリックします。</li>
<li>4. <a href="http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=findplatform" rel="nofollow">platformの検索画面</a>が現れるので、「Company name」に「Affymetrix」、「organism」に「Homo sapiens」を選択し、「FIND PLATFORM」をクリックします。</li>
<li>5. <a href="http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=foundplatform" rel="nofollow">Affymetrixのヒトのマイクロアレイの検索結果</a>が表示されるので、中程にある「Affymetrix GeneChip Human Genome U133 Plus 2.0 Array」の左端にある<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570" rel="nofollow">「GPL570」というID</a>をクリックします。</li>
<li>6. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570" rel="nofollow">表示された画面</a>の真ん中あたりにある「series」下の「More...」をクリックすると、登録されているデータセットを閲覧できます。</li>
<li>7. ブラウザの検索ボタンなどを使って「reprogramming」という単語を検索するとどういうデータがヒットするでしょうか？</li>
<li>8. ヒットしたデータの左端にあるIDをクリックすると、<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE9832" rel="nofollow">そのデータセットの詳細情報</a>が閲覧できます</li>
<li>9. ページ下部の「Download family」の中にある「Series Matrix File(s)」をクリックすると正規化済みのデータのダウンロードリンクが表示されます。</li>
<li>10. ページ最下部の「Supplementary file」にあるリンクから生データをダウンロードすることができます。</li>
<li>11. 自分の研究テーマに近い、また興味のあるマイクロアレイデータが利用可能か検索してみましょう。</li></ul>

<h3 id="content_1_21"><a id="b6353d6e" href="" title="b6353d6e">_</a> 【参考】<a href="http://lifesciencedb.jp/geo/" rel="nofollow">遺伝子発現バンク(GEO)目次、通称「GEO目次」</a>  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20080623.html#p01" rel="nofollow">使い方参考動画 遺伝子発現バンク(GEO)目次を使い倒す－その壱</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>NCBI GEO を日本語のインターフェイスで快適に使い、データの全容を俯瞰するための仕組みです。数多く登録されている遺伝子発現データの大まかな傾向をつかむのに役に立つことでしょう。</li>
<li>検索結果のRSS配信機能があるので、これを活用して、遺伝子発現データの新規登録の有無をチェックできます（便利！）。</li></ul>
