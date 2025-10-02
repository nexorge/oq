---
title: 生成AIを活用したCGデザイン
date created: Thursday, October 2nd 2025, 4:08:29 pm
date modified: Thursday, October 2nd 2025, 5:08:04 pm
---
## **第一章　序論**

近年、生成AIは世界中で注目を浴び、市場規模は今後も成長を続けると予測されている（総務省, 2025）。実際の肌感覚としても我々の生活に生成AIを活用したアプリやツールが浸透してきていることを実感する。

こうした中、我々CGデザイナーを志す学生においても、生成AIとの付き合い方について考えることは避けられない。本レポートでは、生成AIを活用したCG制作の事例の調査と実践を通して今後の生成AIとの付き合い方を考察する。

## **第二章　前提の整理**

議論の前提となるAI（人工知能）、生成AI、CGデザインの各用語について定義を試みた。しかし、これらの概念、とりわけ技術発展が著しい生成AIに関しては、その定義が多様であり、現時点で単一の厳密な定義を定めることは困難であった。

そこで本レポートでは、現時点で一般的と見なされる概念理解を議論の土台とし、具体的な考察を進めていくこととする。

### 1. AIとは何か
一般的にAI（人工知能）とは、「知的な機械、特に、知的なコンピュータープログラムを作る科学と技術」(John McCarthy, 2007)と見なされている。
### 2. 生成AIとは何か
一般的に生成AIとは、「既存のデータから学習し、新しいコンテンツを作成するために使用される人工知能の一種」(IBM, 2024)と見なされている。
### 3.CGデザインとは何か
一般的にCGデザイナーとは、「コンピュータを使用して、図形、絵、映像、アニメーションなどのコンピュータグラフィック（CG）を制作する。CGクリエイターと呼ばれることもある。」(厚生労働省, n.d.)と見なされている。


**以上より、CGデザインとは、「クライアントの要望やプロジェクトの目的を達成するために、コンピュータグラフィックス技術を駆使して、視覚表現を設計・制作すること。」とする。**

## **第三章　研究方法**
### 1. 概要
本レポートの考察は、具体的な事例研究の手法を用いて行う。先行事例として、生成AIであるMidjourneyをリアルタイムVFXの制作に活用した事例報告(Alex Fedorov, 2022）に着目した。

本研究では、この事例で提示されているワークフローを実際に適用・分析し、その過程と結果を通じて、以下の2つの問いについて考察を深める。
1. CG制作プロセスにおける生成AIの最適な活用法は何か。
2. 生成AI時代のCGデザイナーに求められる新たなスキルは何か。

### 2. ワークフローの分析

Alex Fedorovによる事例の全体的なワークフローについては下記の通り。

1. Midjourneyによる画像生成
2. Substance 3D Designerによる画像加工
3. Unreal Engine 5によるエフェクト制作

ここでは1.Midjourneyによる画像生成のプロセスに着目する。この段階の目的は、煙、タイル状のノイズ、放射状のマスク、軌跡用のテクスチャなど、エフェクトの素材となるテクスチャを効率的に作成することにある。

方法は、「smoke, magic, texture, tile, pattern, visual effects」といった具体的なテキストプロンプトをAIに与えることで、制作者の意図するイメージに近い画像を生成させることである。

プロンプト調整のコツとして、望んだ結果が得られるまでプロンプトを調整し、繰り返し画像を生成すること。それから、有望な画像が生成された後は、その画像をもとにしてバリエーションをAIに作成させることで、より質の高い素材を追求すること。以上の2点が述べられていた。

### 3. 実践方法
今回はMidjourneyの使用が有償となっていたため、代わりにAdobe Fireflyを使用し、下記のワークフローでエフェクト制作を行った。

1. Adobe Fireflyによる画像生成
2. Substance 3D Designerによる画像加工
3. Unreal Engine 5によるエフェクト制作

Adobe Fireflyを使用することで検証結果に差が生じることを懸念し、先行事例に使用されていたプロンプト「smoke, magic, texture, tile, pattern, visual effects」を使用して結果を確認したが、問題なく類似した結果が出たため、上記ワークフローを採用。

## **第四章　実践結果**
### 1. **炎の素材作成**
プロンプトの作成についてはテキスト生成AIであるGeminiを使用した。
Geminiへの指示内容は以下の通り。
```Gemini
アニメ調の火のエフェクトを作成したいのでAdobe Fireflyを使用し、最終的にUE5でSubUV素材として使用できる画像を作成するためのプロンプトを書いてください。
```
Adobe Fireflyへの指示は以下の通り。
```Adobe Firefly
anime style fire, vibrant orange and red, simple sharp shapes, cel-shaded, 4x4 sprite
```

### 2. 煙の素材作成
使用したプロンプト
```Adobe Firefly
stylized hand-drawn dense fog loop, painterly texture, game asset, isolated on black
```
何度か生成した素材の中から理想に近い画像を選択し、参照へ設定した。これにより、より理想に近い素材を作成することができた。
### 3. エフェクト制作
上記素材をUnreal Engine 5のNiagara Systemを使用し、簡易的なエフェクト制作を行った。


## **第五章　考察**
### 1. 生成AI使用のメリット・デメリット
実際の生成AIを活用したエフェクト制作を通して感じた生成AIのメリットとデメリットについて述べる。

メリット
1. 手描きでは到底及ばない速度で素材の数と種類を生成することができる。
2. 正しいプロンプトを使用することで、画像調整のステップを必要としない場合がある。
3. 一度使用したプロンプトを繰り返し使用することができるので、使用頻度が高いほど効率が上がる。

デメリット
1. 同じプロンプトを使用しても結果が大きく異なる場合がある。
2. 必ずしもプロンプト通りにならない場合がある。
3. 簡単に作成できる半面、同じような結果になりがち。
4. 狙い通りの素材を作ったり、アウトプットの差別化を図るためには、AIの特性理解と美術用語など知識が求められる。
5. 安定的な再現性と細かい調整を求めるとプロンプトが複雑になりかえって非効率になる可能性がある。

### 2. 生成AIの最適な活用法
コンセプトアートや素材を制作する工程において、生成AIの活用が一つの手段として加えられたというのが、今回の検証における所感である。他の工程においても活用できるかは現状不明。しかしながら、３Dモデルやテクスチャ、リグ、アニメーション、地形、レイアウトなどを生成AIを活用して作成するツールがあることについても今回の調査で確認できた(※)ため、今後はエフェクトそのものがプロンプトにより生成されるだろうと推察される。

現状においては、どのツールに関してもプロンプトや参照を使用して生成するという手法は変わらないため、最適な活用法としては、プロンプトや参照の扱いを心得ることと結論付ける。

### 3. ＣＧデザイナーとして生成AIの使用に求められるスキル
今後のCGデザイナーが生成AIを使用するにあたって求められるスキルは、美術的な概念の理解と視覚的な表現を言語化するスキルであると、今回の検証を通して実感した。

現状は、画像参照の機能があるとはいえ、基本的にはテキストベースで指示を出し、結果を出力するという形式であるため、どうしても言語化は避けられない。

また、出力された結果をもとに、何をどう修正するべきか、何をもって良しとするかは、クライアントのニーズを理解するスキルやデザイナーの観賞眼による部分が多く、求められるスキルとしては従来のそれと変わらない。
## **第六章　まとめ**
今回の調査を通じて、生成AIの適切な活用はCG制作を加速させ、働き方も身に着けるべきスキルも変わるだろうと伺える。しかしながら、CGデザイナーとして、クライアントのビジュアル課題を解決するという役割は、新たに生成AIの活用という手段が加わったとしても、大きく変わることはないだろうと思われる。

近年のAI事業投資の傾向や開発競争激化の背景を鑑みて、より変化が加速することが予測される。CGデザイナーも積極的に新たなテクノロジーを活用することや、変化を味方に付ける姿勢が求められると考える。
## **参考文献**
総務省. (2024, July 30). 令和6年版 情報通信白書.
https://www.soumu.go.jp/johotsusintokei/whitepaper/ja/r06/pdf/index.html. Retrieved August 9, 2025.

総務省. (2025, July 8). 令和7年版 情報通信白書.
https://www.soumu.go.jp/johotsusintokei/whitepaper/ja/r07/pdf/index.html. Retrieved August 9, 2025.

人工知能学会. (n.d.). AIって何？.
 https://www.ai-gakkai.or.jp/whatsai/AIwhats.html#REMARK1. Retrieved August 9, 2025.

John McCarthy. (2007, November 12). WHAT IS ARTIFICIAL INTELLIGENCE?. Stanford University. 
https://www-formal.stanford.edu/jmc/whatisai/whatisai.html. Retrieved August 9, 2025.

IBM. (2024, March 22). What is generative AI?.
https://www.ibm.com/think/topics/generative-ai. Retrieved August 9, 2025.

厚生労働省. (n.d.). CGデザイナー - job tag（職業情報提供サイト（日本版O-NET）
https://shigoto.mhlw.go.jp/User/Occupation/Detail/329. Retrieved August 9, 2025.

Alex Fedorov. (2022, September 6). Creating VFX in Unreal Engine 5 from Midjourney-Generated Textures. Epic Games.
https://dev.epicgames.com/community/learning/tutorials/z4R7/creating-vfx-in-unreal-engine-5-from-midjourney-generated-textures. Retrieved August 9, 2025.

80.lv. (2022, November 23). A Beginner's Guide to Creating VFX in Unreal Engine 5. YouTube. 
https://www.youtube.com/watch?v=N7ksJ_wiOSA. Retrieved August 10, 2025.

24ad0215.(2025, August 10). Test AI VFX. YouTube.
https://www.youtube.com/watch?v=jOgztqtmRNg. Retrieved August 10, 2025.

今回CG制作における生成AIツールとして下記を見つけたが、それぞれの用途のみ確認しただけで、実際に使用してはいないため詳細については不明。
- Meshy（3Dモデル・テクスチャ生成） https://www.meshy.ai/discover
- KAEDIM(3Dモデル生成) https://www.kaedim3d.com/
- Cascadeur(リグ・アニメーション補間) https://cascadeur.com/
- Plask(AIによるモーションキャプチャ)　https://plask.ai/ja
- Promethean AI(レイアウト) https://www.prometheanai.com/
- Gaea(地形生成) https://quadspinner.com/