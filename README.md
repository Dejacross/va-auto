# va-auto
Auto-run to daily mission for  vividarmy.

## 準備

1. BlueStacks4 インストール
https://www.bluestacks.com/ja/bluestacks-4/multi-instance.html
   * test
     * tests
   * 設定
     1. BlueStacksマルチインスタンスマネージャーを起動
     2. [設定]-[ディスプレイ]
        * 解像度: 縦画面 (スマホモード)
        * 720x1280
     3. [設定]-[エンジン]
        * フレームレート: 20fps
     4. 画面サイズ調整
        手動でウィンドウサイズを調整してください。
        * サイズ:425x794
     5. テンプレートとして保存する
     6. 新規インスタンス を作成
        "TEMPATE"から複製する
     7. アカウント移転
        1. 新規作成したインスタンスを起動 
        1. chrome を起動してゲームurlへアクセス
        1. 右中央のGマークからログイン

1. uwsc インストール
https://www.vector.co.jp/soft/winnt/util/se115105.html
任意の場所に配置してください。
   * version: UWSC5.3.0.2

1. 施設配置設定

   * "img\home.bmp" を参考に施設を配置してください。

1. スクリプト編集
"menu.UWS"を編集します。
"BlueStacks_1" の部分をBluestacksで作成したインスタンス名に修正してください。
    ```:menu.UWS
//    DIM WINDOWNAME[] = "BlueStacks_1","BlueStacks_2"
    DIM WINDOWNAME[] = "BlueStacks_1"

    DIM MENU[] = "デイリー補給","金貨購入","メール回収","工場回収","金貨収集","連盟ギフト回収"

    SLCT = SLCTBOX(SLCT_BTN,0,0,0,"",MENU)

    SELECT SLCT
    ...
    ```
以降、"TEMPLATE"から作成したインスタンスを "," で区切って追加すれば、連続でスクリプトが流れます。

## スクリプト実行

**※スクリプト実行前は、[世界←→基地]を往復して基地配置を初期化してください。**

   1. uwsc を起動
   2. タスクトレイのアイコンを右クリックして[タスクトレイから出す]をクリック
   3. [読み込み]をクリックして、"menu.UWS" を開く
   4. [再生]をクリック
   5. メニューから選択する

