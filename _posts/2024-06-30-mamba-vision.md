---
layout: post
title: Mamba in Computer Vision
date: 2024-05-10 00:00:00
description: An Introduction to Mamba in Computer Vision
tags: computer-vision mamba
categories: paper-review
featured: true
---

## TL;DR

Vim and VMamba were the first to apply Mamba to Computer Vision. (The two papers came out almost simultaneously, just one day apart. Although Vim was submitted to a conference, VMamba's GitHub community is very active and shows better results. If you want to get started, VMamba is recommended.)

Vim is very similar to ViT (Block*24, homography), mainly changing the token scan from a simple 1D flatten to 1D flatten plus flipped 1D flatten.
VMamba is very similar to Swin-T (Stage*4, hierarchy), with token scan becoming 4 types: horizontal (forward+backward) + vertical (forward+backward).
LocalMamba introduces a windowed concept for scanning, allowing the model to learn itself (7 choices in total). It shows good improvements when added to both Vim and VMamba.
EfficientVMamba proposes Atrous scan, which can be understood as skipping one token between every two scanned tokens.

---
Vim 跟 VMamba 首先提出將 Mamba 用於 Computer Vision 領域。（兩篇論文幾乎同時，只差一天，雖然 Vim 已投稿上會議，但 VMamba GitHub 社群非常活躍，效果也比較好，如果要上手會推薦 VMamba）

- Vim 與 ViT (Block*24, homography) 非常相似，主要在 token scan 中由單純 1d flatten 轉為 1d flatten 加上 flipped 1d flatten。
- VMamba 與 Swin-T (Stage*4, hierarchy) 非常相似，token scan 變成 4 種: horizontal (forward+backward) + vertical (forward+backward)。
- LocalMamba 針對 scan 的方法提出 windowed 的概念並讓模型自己學習 (共有 7 種選擇)，加在 Vim 與 VMamba 中皆有不錯的提升。
- EfficientVMamba 提出 Atrous scan，可以理解成 scan 兩個 token 之間 skip 一個 token。

## Presentation
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTR-vVTsWMzrNyL2hMQGG3uIxF05lhaKQjq0baTJPNU3EiumVA5dsc5iMe4C7oA7qA1P2L_NmM0b2fA/embed?start=false&loop=false&delayms=60000" frameborder="0" width="900" height="675" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
