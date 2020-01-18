# elephant42 の組み立てかた

自作キーボードキット [elephant42](https://illness072.booth.pm/items/1775017) のビルドガイド(組立説明書)です。

**組み立ての前に、このビルドガイドを先に読んで理解して、材料・工具等を揃え、環境構築をし、最後に実際の組立作業を行ってください。**


## 準備

### キット内容の確認

内容物に不足や破損などがないか確認してください。

| ![基板(PCB)](item_pcb.jpeg) | ![トッププレート](item_top_plate.jpeg) | ![ミドルプレート](item_middle_plate.jpeg) | ![ボトムプレート](item_bottom_plate.jpeg) |
|:--:|:--:|:--:|:--:|
|基板(PCB) ... 1枚|トッププレート ... 2枚<br/>(薄くて穴が小さい方)|ミドルプレート ... 2枚<br/>(厚くて穴が大きい方)|ボトムプレート ... 2枚|
| ![ProMicro 保護プレート](item_promicro_plate.jpeg) | ![ダイオード](item_diode.jpeg) | ![MX 互換スイッチ用 PCB ソケット](item_mx_socket.jpeg) | ![TRRS ジャック](item_trrs_jack.jpeg) |
| ProMicro 保護プレート ... 2枚 | ダイオード ... 44個<br/>(予備2個) | MX 互換スイッチ用<br/>PCB ソケット ... 42個 | TRRS ジャック ... 2個 |
| ![タクトスイッチ](item_tact_switch.jpeg) | ![スペーサー(短)](item_spacer_short.jpeg) | ![スペーサー(長)](item_spacer_long.jpeg) | ![ネジ](item_screw.jpeg) |
| タクトスイッチ ... 2個<br/>※色は異なる場合があります | スペーサー(短) ... 20本 | スペーサー(長) ... 4本 | ネジ ... 40本 |
| ![クッションゴム](item_cushion_rubber.jpeg) ||||
| クッションゴム ... 10個 ||||


### 必要部品の調達

キットに含まれていないが必要なものを購入します。

初心者向けのおすすめ購入先 (国内通販) のリンクも併せて載せておきますので参考にしてください。

#### 必須

- Pro Micro(コンスルー付き) ... 2組
   - おすすめ購入先
     - [Pro Micro （コンスルー付き）| 遊舎工房](https://yushakobo.jp/shop/promicro-spring-pinheader/) ※2つ購入してください
     - TALP KEYBOARD
       - [Pro Micro ATmega32U4 5V/16MHz/MicroUSB2(互換品)](https://talpkeyboard.stores.jp/items/5b24504ba6e6ee7ec60063e3) ※2つ購入してください
       - [MAC8 コンスルー XB-3-2.5-12P (高さ2.5mm/12ピン/1個)](https://talpkeyboard.stores.jp/items/5e056626d790db16e2889233) ※4つ購入してください
- MX 互換スイッチ ... 42個
   - おすすめ購入先
     - [Switches | 遊舎工房](https://yushakobo.jp/product-category/switches/)
     - [TALP KEYBOARD](https://talpkeyboard.stores.jp/?category_id=59cf8860ed05e668db003f5d)
     - [SWITCHES - ゆかりキーボードファクトリー](https://eucalyn.shop/product-category/keyswitches)
   - 「Kailh ロープロファイル (Choc) スイッチ」および「Kailh Mid-Heightスイッチ」は非対応ですのでご注意ください。
- 1Uキーキャップ ... 42個
   - おすすめ購入先
     - [Keycaps | 遊舎工房](https://yushakobo.jp/product-category/keycaps/)
     - [TALP KEYBOARD](https://talpkeyboard.stores.jp/?category_id=59be183f428f2d49120007b1)
     - [KEYCAPS - ゆかりキーボードファクトリー](https://eucalyn.shop/product-category/keycaps)
   - キースイッチと同じく「Kailh ロープロファイル (Choc) スイッチ」用のキーキャップは非対応ですのでご注意ください。
- TRSケーブル ... 1本
    - AUX ケーブル、ステレオミニプラグケーブルなどとも呼ばれています。所謂イヤホンのプラグが両方についてるケーブルです。
      - Amazon などで見た目が良いものが売られています
    - elephant42 が必要とするのは 3 極(黒線が2本入るタイプ)の TRS ケーブルですが、自作キーボードショップなどでよく売られている 4 極(黒線が3本入るタイプ) の TRRS ケーブルでも代用可能です。
      - [TRRSケーブル 1m | 遊舎工房](https://yushakobo.jp/shop/trrs_cable/)
- USB ケーブル (Type-A to Micro-B) ... 1本
    - 所謂 Micro USB ケーブルです。
      - Amazon などで見た目が良いものが売られています
      - [USBケーブル Micro B 1m | 遊舎工房](https://yushakobo.jp/shop/usb_cable_micro_b/)
      - [USB2.0ケーブル（0.6m/USB(A)オス - USB(Micro-B)オス) | TALP KEYBOARD](https://talpkeyboard.stores.jp/items/5df82904a551d528d7360c34)


#### オプション

1. OLEDモジュール（ピンソケット付き） ... 2個
    - [OLEDモジュール | 遊舎工房](https://yushakobo.jp/shop/oled/) ※ピンソケット付きを選択してください
1. YS-SK6812MINI-E ... 54個
    - [YS-SK6812MINI-E（10個入り） | 遊舎工房](https://yushakobo.jp/shop/ys-sk6812mini-e/) ※6パック購入してください(6個余ります)
    - **従来品の「[SK6812MINI](https://yushakobo.jp/shop/sk6812mini-35/)」は互換性がないため使用できません。**
    - **※遊舎工房実店舗で購入する場合、見た目が非常に似通っている「[リバースマウント RGB LED](https://yushakobo.jp/shop/a0800rl-10/)」を誤って購入しないよう注意してください。互換性がないため使用できません。**
