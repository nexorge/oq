---
date created: Wednesday, October 8th 2025, 6:31:35 pm
date modified: Thursday, October 9th 2025, 3:39:26 pm
---

## Applibot-rig Activation

> [!NOTE]- セットアップ手順
> 1. アプリボット社提供のMaya用フリーリグを[ダウンロード](https://github.com/applibot-inc/applibot-rig?tab=readme-ov-file)
> 2. ab_rig_A(B or C)フォルダ内のpickerフォルダを使用するプロジェクトフォルダの直下へコピー
> 3. sourceimagesの内容をプロジェクトのsourceimagesへコピー
> 4. 制作を行うプロジェクトのシーンを開き、rigフォルダ内のab_rig_A(B or C).maをインポート
> 5. マテリアルビューでテクスチャを確認
>    ![[Pasted image 20251009145740.png]]
> 6. ハイパーシェードで該当のsourceimagesを割り当てる
>    ![[Pasted image 20251009145846.png]]

## Picker Activation
[ARPicker](https://area.autodesk.jp/column/tutorial/maya-rigging-technique/03-picker/)の[Picker file](https://abc-anime.app.box.com/s/6e03tgsphwfvjb5so96a10vh5858ejyc/folder/274467052442)をダウンロードし、Mayaのプロジェクトフォルダ下のscriptフォルダへ展開する。

> [!NOTE]- Picker起動コマンド
> 
> ```python
> import sys
> sys.path.append(r'E:\projects\AB_Project\script')
> # r'E:\projects\AB_Project\script'の部分を、自分のプロジェクトフォルダ下のscriptフォルダのPathに変更する。
> from picker import picker
> picker.main()
> ```

> [!NOTE]- シェルフ登録
> 
> ![[Pasted image 20251009151837.png]]
> 起動コマンドを全選択し、中クリックドラッグ＆ドロップで任意のシェルフへ登録する。
> アイコンを右クリック→編集を行い、アイコンや表示名などを変更可能。

> [!warning]- リグインポート時にプレフィックスがついている場合、ピッカーが機能しない。
> リグRename手順
> - Window→General→Name Space Editor
> - Delet Prefix→ Merge root

> [!NOTE]- Pickerの編集
> 1. 編集モードへ切り替える（Ctrl ＋E）  
>    ![[Pasted image 20251009152948.png]]
> 2. 編集したいボタンを右クリック→Edit button  
>    ![[Pasted image 20251009153032.png]]
> 3. Pick Objects:の名前が動かしたいオブジェクトの名前と一致している必要がある。
>    ![[Pasted image 20251009153420.png]]
> 4. 設定後はCtrl + Sで内容を保存
> 5. 編集モード終了（Ctrl ＋ E）
