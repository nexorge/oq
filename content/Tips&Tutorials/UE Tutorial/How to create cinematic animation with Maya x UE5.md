---
title: How to create cinematic animation
tags:
  - UE
  - Maya
  - Animation
published: 2025-09-08
source:
date created: Tuesday, October 7th 2025, 7:39:45 am
date modified: Wednesday, October 8th 2025, 8:49:05 am
---
## 意義
- Mayaで制作したカメラ・キャラクターアニメーションをUEへインポートし、レンダリングを行う
- メリットとしてリアルタイムレンダリングによる効率的なライティングとエフェクトの調整が可能となる
- Maya・UE間におけるデータのやりとりや設定が複雑だったため記録する。

## Workflow
1. 背景をUEに読み込み、LOなどを行う
2. Mayaへ背景モデルやリグを読み込み、アニメーションを制作する
3. カメラ、キャラクターのアニメーションをUEへインポート
4. マテリアルの設定を行う
5. ライティングを行う
6. レンダリングを行う

> [!warning]
> 最終セットの完成とレンダリングをUEで行うため、背景アセットをUEでキットバッシュしてからMayaでアニメーション制作を行います。
> 背景を先に決めない場合、位置調整の作業が発生します。



> [!NOTE]- Step1 背景をUEに読み込み、LOなどを行う
> ## 1.UE to Maya (背景)
> > [!abstract]- 
> > 1. 背景モデルをUEへ読み込む  
> > 	1 [Fab](https://www.fab.com/ja)からAssetをダウンロードして使用する場合<br>
> > 	2 自作の背景モデルを使用する場合<br>
> > 2. LOなどを行う
> > 3. Mayaへエクスポートする
> 
> ### 1. 背景モデルをUEへ読み込む
> > [!example]- 1. [Fab](https://www.fab.com/ja)からAssetをダウンロードして使用する場合
> > - 手順１(制作中)
> > - 手順２(制作中)
> 
> > [!example]- 2. 自作モデルを使用する場合の手順
> > - 手順１(制作中)
> > - 手順２(制作中)
> >> [!tip] Tips
> >> - LOを維持したものをImportするにはABCでImportするとよい
> >> - Importの際にUVの設定が必要
> > -  ImportUVの設定
> > ![[Pasted image 20251008074424.png]]
> > ![[Pasted image 20251008074334.png]]
> 
> ### 2. LOなどを行う
> > [!example]- LOの手順
> > - 手順１(制作中)
> > - 手順２(制作中)
> >> [!tip] Tips
> >> - アセットを使用する場合、レベルを保存しないとLO編集が行えない。
> 
> ### 3. Mayaへエクスポートを行う
> > [!example]- エクスポートの手順
> ![[Pasted image 20251008080922.png]]
> >> [!tip] Tips
> >> - メッシュのスケールとMaya上のカメラ設定の関係から、うまく表示されない場合がある。その場合は、Mayaのカメラ設定からクリップレーンの最大値と最小値を調整する。

> [!NOTE]- Step2 Mayaへ背景モデルやリグを読み込み、アニメーションを制作する
> ## 2.Animation in maya
> > [!example]- 手順１
> > - １(制作中)
> > - ２(制作中)
> >> [!tip] Tips
> >> - 座標やスケールはUEを基準として、Maya上でアニメーションを作成する。それにより、UEへ読み込んだ際の位置調整の作業が不要となる。

> [!NOTE]- Step3 カメラ、キャラクターのアニメーションをUEへインポート
> 
> ## 3.Camera, Character animation to UE
> > [!example]- エクスポートの手順（Maya to UE）
> > - カメラ：fbx形式でエクスポートする
> >> [!tip] Tips
> >> - コンストレインとベイクを行う。（詳細後述）(制作中)
> > - キャラクター：Alembic Cache(abc)形式でエクスポートする
> >> [!tip] Tips
> >> - 基本的にベイクを行い、abc形式でエクスポートする。エクスポート後は再生専用となるためUEでのアニメーション調整は基本的に不可能と考える。
> >> - Animated Sweepなどで作成したNurbsメッシュは直接abc形式でエクスポートすることができないため、Geometry Cache(mcx)形式でキャッシュのみエクスポートし、再度元となるPolygonメッシュへキャッシュ情報を付与し、abc形式でエクスポートする。（詳細後述）(制作中)

> [!NOTE]- Step4 制作中
> Contents

> [!NOTE]- Step5 制作中
> Contents

> [!NOTE]- Step6 制作中
> Contents

