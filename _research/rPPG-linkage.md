---
title: "rPPG を用いた匿名化動画に対する生理信号リンク攻撃"
excerpt: "目隠し・モザイク処理された動画からでも rPPG で個人を紐付けられることを示し，その対策を提案<br/><img src='/images/rppg-linkage.png'>"
collection: portfolio
date: 2026-10-27
---

遠隔光電容積脈波 (remote photoplethysmography, rPPG) は，通常のカメラ映像に写った肌の色のわずかな時間変化から，非接触で脈波を推定する技術です．目隠しやモザイクなどの視覚的な匿名化処理は顔の見た目を隠しますが，rPPG の元となる肌の色変化は残ってしまいます．本研究では，この残存した生理信号を手がかりに，匿名化された動画の人物を特定する「生理信号リンク攻撃」を提案し，その脅威を評価しました．

攻撃シナリオとして，(1) 匿名化された健康記録に含まれるセンサ由来の PPG 信号と，本人が特定できる動画から抽出した rPPG 信号を照合するクロスモーダルリンク，(2) 匿名化処理された動画の rPPG 信号と，未処理の参照動画の rPPG 信号を照合するクロスビデオリンク，の 2 つを想定しています．UBFC-Phys データセットを用いて，Dynamic Time Warping による波形類似度の分析と，CNN-LSTM 分類器による本人判定の評価を行った結果，目隠し・モザイクを施しても個人を紐付けられる生理情報が残ることを示しました（F1 スコアの中央値 0.83〜0.87，最大値は目隠しで 0.994，モザイクで 0.987）．さらに，緑チャネルにフレーム単位のランダム摂動を加えることで rPPG 推定を妨げる対策手法を提案し，その有効性を確認しています．

- Ryo Iijima, Koki Hasegawa, Ryo Kawaoka, and Tatsuya Mori, “Physiological Linkage Attacks against Visually Obfuscated Videos Using rPPG,” Workshop on Cybersecurity in Healthcare (HealthSec 2026), co-located with ACSAC 2026, December 2026 (to appear)
- 飯島 涼，長谷川 幸己，河岡 諒，森 達哉，“rPPG 信号に基づく個人識別攻撃の提案と対策”，コンピュータセキュリティシンポジウム 2024 論文集，pp. 46–53，2024年 (CSS2024 優秀論文賞)

本研究は内閣府 BRIDGE プログラム (R7H05) の支援を受けています．

![rPPG に基づく生理信号リンク攻撃の概要](/images/rppg-linkage.png)
