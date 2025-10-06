---
title: How to create cinematic animation
tags:
  - UE
  - Maya
  - Animation
published: 2025-09-08
source:
date created: Tuesday, October 7th 2025, 7:39:45 am
date modified: Tuesday, October 7th 2025, 7:44:30 am
---
## 意義
- Mayaで制作したアニメーションをUEでレンダリングを行う
- リアルタイムレンダリング＝ライティング＋VFX

## Workflow
1. 背景をUEに読み込み、LOなどを行う
2. Mayaへ背景モデルやリグを読み込み、アニメーションを制作する
3. カメラ、キャラクターのアニメーションをUEへ読み込む
4. マテリアルの設定を行う
5. ライティングを行う
6. レンダリングを行う

> [!warning]
> 最終セットの完成とレンダリングをUEで行うため、背景アセットをUEでキットバッシュしてからMayaでアニメーション制作を行います。
> 背景を先に決めない場合、位置調整の作業が発生します。



## UE to Maya (背景)
### Outline
> [!abstract]- 
> 1. 背景モデルをUEへ読み込む  
> 	1 [Fab](https://www.fab.com/ja)からAssetをダウンロードして使用する場合<br>
> 	2 自作の背景モデルを使用する場合<br>
> 2. LOなどを行う
> 3. Mayaへエクスポートする

### 1. 背景モデルをUEへ読み込む
> [!example]- 1. FabからAssetをダウンロードして使用する場合
> - 手順１
> - 手順２

> [!example]- 2. 自作モデルを使用する場合の手順
> - 手順１
> - 手順２
>> [!tip] Tips
>> - LOを維持したものをImportするにはABCでImportするとよい
>> - Importの際にUVの設定が必要

### 2. LOなどを行う
> [!example]- LOの手順
> - 手順１
> - 手順２
>> [!tip] Tips
>> - アセットを使用する場合、レベルを保存しないとLO編集が行えない。

### 3. Mayaへエクスポートを行う
> [!example]- エクスポートの手順
> - 手順１
> - 手順２
>> [!tip] Tips
>> - 制作中