---
title: "Cyber Physical Firewall: Spoofing Attackから守るアナログ信号向けファイアウォールのデザイン"
excerpt: "アナログ信号を対象としたアクセス制御機構 Cyber-Physical Firewall (CPFW) のソフトウェア・ハードウェア実装<br/><img src='/images/cpfw-overview.png'>"
collection: portfolio
date: 2026-01-20
---

超音波やレーザなどのアナログ信号を使ってセンサに偽の入力を与える Spoofing Attack から，サイバーフィジカルシステム (CPS) を守るためのアクセス制御フレームワーク Cyber-Physical Firewall (CPFW) を設計・実装しました．従来の対策はセンサへの入力側 (Ingress) で攻撃を検知するものが中心でしたが，CPFW は攻撃の発信源となりうるデバイスの出力側 (Egress) でも信号を監視・規制する点が特徴です．アナログ信号として出力される前のディジタル信号をポリシーに基づいて制御するため，物理空間のノイズや受信回路の非線形性の影響を受けにくく，攻撃を根本から抑止できます．

本研究では CPFW をソフトウェア (Raspberry Pi) とハードウェア (Zybo Z7-10 FPGA) の両方で実装し，音声信号を対象に実機で評価しました．処理遅延はソフトウェア実装で 3.219 ms，ハードウェア実装で 310 ns と約 10<sup>4</sup> 倍の差があり，ハードウェア実装の回路規模の増加は 5.88% にとどまることから，実用的な規模で組み込めることを示しています．

- Ryo Iijima, Tatsuya Takehisa, and Tatsuya Mori, “Software and Hardware Implementations of a Cyber-Physical Firewall,” ACM Transactions on Cyber-Physical Systems, Vol. 10, No. 1, Article 9, pp. 1–27, January 2026. [https://doi.org/10.1145/3777453](https://doi.org/10.1145/3777453)
- Ryo Iijima, Tatsuya Takehisa, and Tatsuya Mori, “Cyber-Physical Firewall: Monitoring and Controlling the Threats Caused by Malicious Analog Signals,” ACM International Conference on Computing Frontiers (CF’22), May 2022. [https://doi.org/10.1145/3528416.3530997](https://doi.org/10.1145/3528416.3530997)

本研究は JSPS 科研費 22K17890 および NEDO 委託事業 (JPNP25006) の支援を受けています．

![CPFW の概要：入力側 (Ingress) と出力側 (Egress) のアクセス制御](/images/cpfw-overview.png)
