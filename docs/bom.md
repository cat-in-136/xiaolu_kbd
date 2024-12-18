パーツリスト
============

## PCB

Xiaolu Keyboard PCBはKicad 6で設計され、51mm x 76mmの寸法を持つ2層設計になっています。PCBには、16個のダイオード（1N4148）と2個の4.7kΩ抵抗（4.7kΩ 0402 Resister）のSMT部品が含まれています。

.kicad_pcb、.kicad_schなどのPCB設計ファイルは、「pcb」フォルダーにあります。

このPCBは、一般的なPCBメーカーである[JLCPCB](https://jlcpcb.com/)で製造することを前提に設計されています。PCBをJLCPCB PCB+SMT製造サービスに発注するには、KiCadのプラグインで製造用のガーバーファイルなどのファブリケーションファイルを生成できる[JLCPCB fabrication toolkit](https://github.com/bennymeg/JLC-Plugin-for-KiCad)を利用することができます。このツールキットを使うと、JLCPCBに発注するのに必要なファブリケーションファイルであるgerber.zip、bom.csv、position.csvを生成できます。


SMT 部品表

|部品名             |数量|LCSC Part #                                                                                                                     |
|-------------------|----|--------------------------------------------------------------------------------------------------------------------------------|
|1N4148 Diode       |16  |[C2128](https://www.lcsc.com/product-detail/Switching-Diode_Jiangsu-Changjing-Electronics-Technology-Co-Ltd-1N4148WS_C2128.html)|
|4.7kΩ 0402 Resistor|2   |[C25900](https://www.lcsc.com/product-detail/Chip-Resistor-Surface-Mount_UNI-ROYAL-Uniroyal-Elec-0402WGF4701TCE_C25900.html)    |

## 電子部品

|部品名                                |数量|秋月通販コード                                        |備考                     |
|--------------------------------------|----|------------------------------------------------------|-------------------------|
|Seeed XIAO RP2040                     |1   |[117044](https://akizukidenshi.com/catalog/g/g117044/)|必須                     |
|Switronic TS-AGGNH-G プッシュボタン   |16  |[103654](https://akizukidenshi.com/catalog/g/g103654/)|必須                     |
|USB Type C ケーブル                   |1   |                                                      |必須。適当なもので良い   |
|GroveコネクタL型スルーホール          |1   |[112634](https://akizukidenshi.com/catalog/g/g112634/)|Grove拡張用オプション部品|
|TRRS ジャック PJ-320A(または MJ-4PP-9)|1   |[106070](https://akizukidenshi.com/catalog/g/g106070/)|TRRS拡張用オプション部品 |

## ケース

ケースセットアップの例をいくつか記載します。

### 最も安価なケースセットアップ〜市販品の利用〜

Xiaolu Keyboard PCBは、ケースの組み立てを容易にするために、四隅にM3ホールが配置されています。このM3ホールは、秋月電子のC基板との互換となる配置と直径になっています。これにより、秋月電子C基板用のケースやアクリルパネルに、Xiaolu Keyboard を簡単に組み込むことができます。

以下は、最も安価なケースセットアップの一例です。より高さを低くするにはより短いスペーサーを使用してください。

|部品名                                     |数量|秋月通販コード                                        |備考                                    |
|-------------------------------------------|----|------------------------------------------------------|----------------------------------------|
|C基板用アクリルパネル                      |1   |[109853](https://akizukidenshi.com/catalog/g/g109853/)|                                        |
|3mmプラネジ(7mm)+六角スペーサー(14mm)セット|1   |[101861](https://akizukidenshi.com/catalog/g/g101861/)|8 x M3プラネジと4 x M3スペーサーのセット|

### サンドイッチマウントケース

カードケース（名刺ケース）に入るよう設計されたサンドイッチマウントケースです。

![](xiaolu_sandwitch_in_cardcase.jpg)

アクリル板のデザインは [case/lasercut/acrylic_plate.pdf](../case/lasercut/acrylic_plate.pdf) にあります。
お手持ちのレーザー加工機もしくはレーザー加工サービスの入稿条件に従って編集しボトムプレートとトッププレートを製造してください。

|部品名                            |数量|通販                                                                                   |備考                                              |
|----------------------------------|----|---------------------------------------------------------------------------------------|--------------------------------------------------|
|ボトムプレート (76mm x 51mm x 2mm)|1   |                                                                                       |※レーザー加工によって製造                         |
|トッププレート (76mm x 51mm x 2mm)|1   |                                                                                       |※レーザー加工によって製造                         |
|なべ小ねじ M3 x 4mm               |4   |[千石電商: EEHD-6DKV](https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-6DKV)|                                                  |
|なべ小ねじ M3 x 8mm               |4   |[千石電商: EEHD-6DKY](https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-6DKY)|                                                  |
|六角ナット M3 x 2.4mm             |4   |[千石電商: EEHD-6EBP](https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-6EBP)|スペーサの代わりに使用。JIS B1181 規格の六角ナット|
|六角スペーサ 両メネジ M3 x 5mm    |4   |[千石電商: EEHD-0DLK](https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-0DLK)|                                                  |

## 工具

Xiaolu Keyboard PCBはハンダ付けが必要なため、ハンダ付けやその他の電子工作のための一般的な工具が必要です。

* ハンダごて - 温度調節機能付きのものでも、ベーシックなものでもよいのですが、温度調節機能付きのものを強くお勧めします。
* ハンダ - この組み立てには、はんだが必要です。
* ドライバーセット - ケースの組み立てには、ドライバーセットが必要です。

工具を扱うときは、常に適切な安全対策に従ってください。
