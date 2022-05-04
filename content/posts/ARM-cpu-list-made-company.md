---
title: "GAFAMやその他企業の独自プロセッサやSoCのまとめ"
date: 2022-03-07T01:12:25+09:00
draft: false
categories: ["programming","cpu"]
---


# はじめに
ARMはARM社にロイヤリティを支払えば独自のプロセッサを製作することや既存のIPを使用することができます。 \
ほかにも近年OSSでロイヤリティフリーのRISC-Vも台頭してきています。\
そこで今回はそれらのプロセッサやSoCについて調べてみました。

# プロセッサ

|名前|企業|命令セット|用途|
|---|---|---|---|
|TPU|Google|独自?|ディープラーニング用のプロセッサ、GPUとの違いは計算精度を犠牲にしてワット当たりの演算量を増やしている。一般販売はなくクラウド上で使用できる|
|TPU Edge|Google|独自?|ディープラーニング用のプロセッサ、こちらは推論のみに使える。こちらは一般販売あり。IoTをごりごり意識している|
|Google Tensor|Google|ARM|スマートフォンPixel 6に搭載される予定のSoC|
|M1|Apple|ARM|Mac Bookなどに搭載されているSoC。「ワット当たりのCPU性能は世界最高」とうたっている。ゲームは苦手|
|Aシリーズ|Apple|ARM|iPhone、iPadなどで採用されているSoC。AMDもAシリーズCPUを販売していてややこしい、そちらは全く別物。M1チップがiPad proに採用されたためお株が奪われないか不安|
|Graviton|Amazon|ARM|サーバー用プロセッサ。AWSで使用することができる。AWSで既存のプロセッサに比べて時間当たりのコストが安くなるらしい|
|Microsoft SQ2|Microsoft|ARM|ノートパソコンSurfaceに使用されたSoC。Qualcomm社のSnapdragonがベースになっているらしい|
|Kirinシリーズ|Huawei(HiSilicon)|ARM|Huaweiが設計しているSoc。米中貿易戦争でTSMCで製造できなくなったため[武漢で製造する計画が進んでいるらしい](https://iphone-mania.jp/news-378707/)|
|Kunpeng シリーズ|Huawei(HiSilicon)|ARM|Huaweiが設計しているSoc。こちらはサーバー向け|
|Rockchip シリーズ|Rockchip Electronics|ARM|中国メーカーのSoC。小型用のものらしいがノートパソコンにも使われていた|
|Snapdragon シリーズ|Qualcomm|ARM|有名なスマートフォン向けSoC、大きなシェアを握っている|
|Helio シリーズ|MediaTek|ARM|こちらも有名なスマートフォン向けSoC、大きなシェアを握っている|
|Nvidia Tegra|Nvidia|ARM|Nvidiaが設計したSoC。GPUメーカーだけあってグラフィック性能が高いらしい。Nintendo Switchに採用された|
|A64FX|富士通|ARM|スーパーコンピュータ「富岳」に使われているプロセッサ。一つ前の世代の「京」は命令セットをSPARCにしていたためアプリケーションの互換性に苦しみ、今回はARMにしたらしい|
|Powerシリーズ|IBM|Power|ワークステーションなどで使われるプロセッサ。古参だが[いまだに新しいプロセッサが出ている](https://www.ibm.com/blogs/systems/jp-ja/ibm-power-systems-announces-power10-processor/)|
|SiFive RISC-V Core IP |SiFive|RISC-V|これから来るだろうなと思っていたら案の定SiFiveはIntelに買収された。IPコアだけではなく評価ボードも提供しているらしい|
|Rocket-Chip|カリフォルニア大学バークレイ校|RISC-V|RISC-VのIPコア。ScalaのDSLの半導体設計言語Chiselで記述されている|
|Xuantie 910|Alibaba(Pingtouge Semiconductor)|RISC-V|中国EC大手のAlibabaが作ったRISC-Vプロセッサ。「最も早いRISC-Vベースのプロセッサ」とうたっている|


# おわりに
IntelやAMDなどは話し始めるとおそらく一記事分作れてしまうので割愛。ほかの所にたくさん記事あるでしょうし、そちらをあたってください。\
NvidiaやAMDのGPUも割愛しています。\
こうしてみるとGAFAMも半導体専業ではないのに独自プロセッサを作っていますね。\
それにしても命令セットだと本当にARMが強い。
