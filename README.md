# 採掘タイピングゲーム

採掘タイピングゲームは、キーを打って鉱石を採掘し、スコアを稼ぐゲームです。
また、キーロガーの役目を果たしており、不正な入力の発見。累計のタイプ数、最多キー、
BackSpaceを押した回数なども記録することにも使用することが出来ます。
鉱石所持数の横にある確率は、現在の所有している鉱石の割合になります。
スコアの上限値は不可説不可説転までとなります。

鉱石出現確率:1/10

コモン        : 90%
アンコモン    : 9%
レア          : 0.9%
エピック      : 0.09%
レジェンダリー: 0.009%
ミシカル      : 0.00018%
エンシェント  : 0.0000067%
(理論値)

## 概要

このプログラムは、Python の Tkinter ライブラリを使用して GUI ベースのタイピングゲームを実装しています。
プレイヤーはキーボードを使ってキーを打ち、ランダムに生成される鉱石を採掘します。採掘した鉱石には異なるレア度があり、それぞれ異なるスコアが与えられます。
プレイヤーはスコアを稼ぎながら、多くのキーを打ち高レアな鉱石の採掘を目指します。

*合成機能
合成機能では採掘した鉱石を合成し、スコアを得ることができます。
また、ルビー（エンシェント）のみ合成に成功すると、アレキサンドライトが獲得できます。
アレキサンドライトを獲得するとスコア倍率が上昇します。

**加算されるスコア倍率割合
＋１ : 60%
X ２ : 30%
X ５ : 10%

スコア倍率があがると全ての獲得出来るスコアに影響します。

消費する鉱石量
銅         : 100個
アルミ     : 50個
サファイア : 20個
ダイヤ     : 10個
エメラルド : 5個
ルビー     : 2個

合成成功確率 50%

*確率変動
確変状態に移行すると、鉱石全体の出現確率が以下のようになります。
通常時:1/10
　　　　↓
確変時:1/3

確変突入:約1/11111
確変継続:約2999/3000

確変中は文字が黄色になります。

## 使用方法

1. プログラムを実行すると、ゲームウィンドウが表示されます。
2. ゲームウィンドウでキーボードを使用してキーを打ちます。（バックグラウンドでも動作します）
3. ゲーム中にランダムに鉱石が生成され、プレイヤーがキーを打つたびに採掘が行われます。
4. 採掘した鉱石の種類に応じてスコアが加算されます。
5. ゲーム中にスコアや鉱石の数などの情報が表示されます。
6. ゲームを終了すると、自動的にゲームデータが保存されます。

## 注意事項

- ゲームデータは `game_data.pickle` ファイルに保存されます。プログラムが正しく終了しない場合は、データが失われる可能性がありますので、定期的にセーブしてください。
- ゲーム中にログリセットを押すと、タイプ数や履歴などのデータがリセットされますが、回数がリセットされるだけですのでプログラムが重い場合はプログラムの再起動をおすすめします。
- メニューからセーブ間隔を変更することができますが、短すぎる間隔に設定するとプログラムの動作が重くなる可能性があります。
- このプログラムはゲームであり、キーのログから個人情報の搾取などは一切行いません。
  また、記録される内容は、スコア、鉱石の数です。キーの情報は含まれません。

##プログラムのバージョンアップ方法

最新バージョンをダウンロード後、解凍したフォルダに前バージョンの`game_data.pickle`をコピーして下さい。


# Mining Typing Game

The Mining Typing Game is a game where you earn points by mining ores through typing. Additionally, it can function as a keylogger to detect unauthorized inputs, track the total number of keystrokes, the most frequently used keys, the number of times BackSpace was pressed, and more. The probability next to the number of ores indicates the percentage of each type of ore you currently possess. The maximum score is set to an incredibly large number, often referred to as *不可説不可説転*.

Ore Appearance Probability: 1/10

- Common: 90%
- Uncommon: 9%
- Rare: 0.9%
- Epic: 0.09%
- Legendary: 0.009%
- Mythical: 0.00018%
- Ancient: 0.0000067%
  (Theoretical Values)

## Overview

This program implements a GUI-based typing game using Python's Tkinter library. Players use the keyboard to type, mining ores that are randomly generated. The mined ores have varying rarities, with each type of ore granting different amounts of points. Players aim to earn high scores while striking as many keys as possible to mine rare ores.

### *Synthesis Feature*
The synthesis feature allows players to combine mined ores to earn points. Additionally, if a player successfully synthesizes rubies (Ancient), they can obtain Alexandrite. Acquiring Alexandrite increases the score multiplier.

**Score Multiplier Rate Increase:**
- +1: 60%
- x2: 30%
- x5: 10%

When the score multiplier increases, it affects all the points that can be earned.

**Ore Consumption Rates:**
- Copper: 100 pieces
- Aluminum: 50 pieces
- Sapphire: 20 pieces
- Diamond: 10 pieces
- Emerald: 5 pieces
- Ruby: 2 pieces

**Synthesis Success Rate:** 50%

### *Probability Fluctuation*
When the game enters a "lucky" mode, the appearance probability of ores changes as follows:

- Normal Mode: 1/10
  - ↓
- Lucky Mode: 1/3

**Lucky Mode Entry Probability:** 1/11,111
**Lucky Mode Continuation Probability:** Approximately 2,999/3,000

During Lucky Mode, the text color turns yellow.

## Usage Instructions

1. When the program is executed, the game window will appear.
2. In the game window, use the keyboard to type (the game also works in the background).
3. Ores are randomly generated during the game, and every time the player types, mining occurs.
4. Points are added based on the type of ore mined.
5. Information such as scores and the number of ores is displayed during the game.
6. When the game is exited, the game data is automatically saved.

## Notes

- Game data is saved in the `game_data.pickle` file. If the program does not terminate properly, data may be lost, so please save regularly.
- Pressing the "Reset Log" button during the game will reset data such as the number of keystrokes and history. However, this only resets the count, so if the program becomes sluggish, restarting it is recommended.
- The save interval can be adjusted from the menu, but setting the interval too short may cause the program to slow down.
- This program is a game and does not collect any personal information from key logs. Only scores and ore counts are recorded. Keystroke data is not included.

## Updating the Program Version

After downloading the latest version, copy the `game_data.pickle` file from the previous version into the extracted folder.

2024-7-19 @waruto

