---
title: "Ryzen 5900X と RTX 3080でゲーミングPCを組んだ"
date: 2020-12-26T10:30:00+09:00
draft: false
description: "4年ぶりにデスクトップPCを組み立てたので、雑感を書きます。"
images:  [ "buildingpc.jpg"]
tags: ["gadget"]
cover: "/buildingpc.jpg"
---

![building gaming pc](/buildingpc.jpg)

こんにちは、[@punchdrunker](https://twitter.com/punchdrunker)です。4年ぶりにPC組んだら浦島太郎過ぎたので振り返りを書いていきます。

これまではIntelチップでしかPC組んだことなかったのですが、最近はAMDが人気なので勢いで5900X 買ってみました。サムネはRTX 2080ですが、色々あって最後は RTX 3080を使ってます。

# 実際の様子

ためしに組立てるところを撮影して6倍速でまとめてみました。カメラはsonyのa7r2で撮影してみてわかったけど、照明とレンズを揃えないと微妙。明るいレンズが55mmしかなかったのでセッティングが大変でした。モニタもあると安心。

{{< youtube fBbw9u_4Amg >}}

# 買い替える前のマシンスペック

4年前の年末に15万弱で作った気がします。SSD起動のWindowsは今でもそこそこ快適でした。

- CPU: intel core i 7 6700K 4コア 4GHz
- CPUクーラー: 付属の空冷
- グラボ: GTX 1070
- マザボ: ASRock Z170 EXTREME 4
- メモリ: 16GB2枚(32GB)
- ストレージ: SSD (Windows)とHDD(Linux)のデュアルブート
- 電源: 500W
- PCケース:Cooler Masterの黒いやつ

# 今回揃えた主要パーツ

以下amazon.co.jpのリンクです。CPUとグラボは秋葉原を歩いてて運が良ければ買えるかも、くらいの入手難易度です。プレミア付いても良ければいつでも買える程度。

- CPU: [AMD Ryzen 9 5900X](https://amzn.to/37MUJ91)
- CPUクーラー: [MasterLiquid ML360R RGB (簡易水冷)](https://amzn.to/3nU044i) (光る)
- グラボ: [INNO3D RTX 3080](https://amzn.to/3hfCEUo) (光る)
- マザボ: [ASRockX570 Taichi Razer edition](https://amzn.to/3nPZKmN)(光る)
- メモリ: [CORSAIR DDR4-3200MHz](https://amzn.to/3mW67Ec) 16GBメモリ2枚 (光る)
- ストレージ: [WDのM.2 SSD 2枚](https://amzn.to/3plQAio)で WindowsとLinuxのデュアルブート
- 電源: [Corsair CX750F RGB -Black- 750W ](https://amzn.to/2KZN3as)(光る)
- PCケース: [Razer Tomahawk](https://amzn.to/3aECGnv) (光る)

***
# 今回覚えたこと

## 実は前のマシンのマザボにはM.2 SSDスロットが1つあった

マニュアル読めよ、という話ですけどね。4年前も結構ひさしぶりだったのでM.2 SSD自体を知らずに組んでいたので、気付いてなかったです。2年くらい前にDELLのPC触った時に初めてM.2 SSDを知って、小ささに驚きました。

## ARGB - アドレサブルRGB

ただ光らせるだけならRGBのピン(4 pin)を使えば良いが、デバイス別に制御したい場合にアドレサブルRGBのピン(3 pin)を使う。パーツによって、このケーブルはRGB、こっちはARGBなど明記してあるので、間違えないように。

***

# 失敗したこと

## 簡易水冷の設置がめっちゃ大変だった

ケースの仕様では360mmラジエータ対応とは書いてあるものの、天井に設置するには背面ファンをはずさないと入りませんでした。そのことに気付くまで20分くらい掛かりました。とりあえずラジエータのファンは3つあるし、前面と背面から吸気する感じで良いかな。良いか悪いかはよくわからないです。

あと、途中ガチャガチャしてる内にポンプをマザボにぶつけて、基盤じゃないところに傷を付けてしまいました。これは自分の不注意。

またサイズだけでなく、ARGBのケーブル配線がめっちゃ大変で、これだけで30分以上掛かりました。マニュアルが不親切なので、マニュアルだけで設置するのは光るパーツ初見の人には無理そう。youtubeで何件か動画見て配線しました。5cmくらいのコントローラ + ケーブルの数もかなり多く、結構かさばりました。

あとケースの全面の外し方がわからず前面に付けるのを見送ったんですが、後で頑張ったら思い切り引っ張ると外れる事に気付きました。

## 電源は光らなくて良かった

ATX版のTomahawkは底部の部屋の中に電源を入れるのと、ファンを下に向けて設置するので、光っても見えません。

## 中古グラボを買ったら光らなかった

これは運ですが、msiの gaming trio x RTX 2080を税込み5万円以内で買えたのでラッキーと思ったらLEDが光りませんでした。一応光るパソコンにしたかったので、返品。

帰りに寄ったソフマップでRTX 3080が買えたので、そいつを採用しました。

## ケースがめちゃ重

ケースそのものが13Kgあります。ガラスのせい?とか思ったけど、側面の2枚のガラス外してもかなり重いです。

***

# まだわかってないこと

## USB Type-Cの 急速充電

まだフロント側だけしか確認していないですが、Android端末を繋いだ時に急速充電の表示にはなるけど、300mAくらいで給電されていて謎。急速って1Aくらいじゃなかったっけ?
背面の口はバッテリーが100%近いときにしか確認できていないけど、同様。

100%近いと給電控え目になるとかかもしれないので、背面は後日また確認します。

***

# よかったこと

## M.2 SSD は良い

ストレージはM.2 SSDのみにしたので、その分の電源ケーブルとSATAケーブルが不要になり、内部がスッキリしました。

あとLinuxもSSD起動にしたことでOSやAndroid Studioの起動が爆速になりました。ビルドはそんなに爆速感ないけど、ちょっと速くなったな、という気分です。

## 背面にケーブル隠せる

最近のPCケース事情はよくわかりませんが、結構ケーブルを隠すためのスペースが確保されているので、マザボ側の部屋は割とスッキリしました。

## 高いマザボは高機能

Razer editionじゃない方のTaichiは1万円くらい安いので、コスパ微妙なんですが、wifi 6対応してたり M.2 SSD 3枚刺せたりと結構便利。

ただ、自宅のネット回線は全然速くないので、wifi 6はローカル通信でのみ効果があるという。。。

## 光る

光る。うれしい。