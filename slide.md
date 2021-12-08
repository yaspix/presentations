---
marp: true
paginate: true
---

# YouTube動画を課金無しで安全にダウンロードする技 - はじめてのUNIXシェル -

### 大岩 泰史

---
# Agenda

以下の3つのテーマについて知る

1. UNIXとは何か。私たちに何をもたらしたのか。
2. CLIについて
3. YouTube動画をダウンロードする方法

--- 

# UNIXとは何か。私たちに何をもたらしたのか。

コンピュータ用のオペレーティングシステム(OS)の一種である。OSは基本ソフトウェアともよばれ、各種装置の基本的な制御や管理を行う。

## 特徴

「移植可能なオペレーティングシステムという新境地を開拓した」(UNIXという考え方 その設計思想と哲学)
機種ごとにOSやソフトウェアを開発する必要がなくなった。

## 歴史
1969年にAT&T(ベル研究所)のケン・トンプソンらが発明したとされている。
90年代以降に独自に改良を加えて、MacOS や Linux が誕生した。
以後UNIXを原型としたOSも含めて、UNIXと表現する。

---

# UNIXとは何か。私たちに何をもたらしたのか。

現代社会はUNIXに支えられている。
UNIXのデータをみていこう。

---

## Desktop Operating System Market Share Worldwide 

Nov 2020 - Nov 2021 (https://gs.statcounter.com/ 2021/12/8閲覧)

OS | シェア 
-----|------
Windows | 74.2 % 
MacOS | 16.0 %
ChromeOS|2.5 %
Linux|2.0 %

考察: Windows以外のUNIXで20%超を占める

---



## Percentages of websites using various operating systems
(W3Techs.com, 8 December 2021)

OS | シェア 
-----|------
UNIX | 78.6 % 
Windows | 21.6 %

UNIXは、UNIXから派生したOS(ほとんどがLinux)を含む
Webサイトを提供するサーバでは、約8割がUNIX

---

# Agenda

以下の3つのテーマについて知る

1. UNIXとは何か。私たちに何をもたらしたのか。
2. CLIにふれよう
3. YouTube動画をダウンロードする方法

--- 

# CLIに触れよう
## CLI (Command Line User Interface)

文字入力のみによりコンピュータを操作するしくみ

「キーボード等からの文字列を入力とし、文字列が表示されるウィンドウや古くはラインプリンタで印字される文字などを出力とする、ユーザインタフェースの様式である。」(wikipedia)

--- 

# CLIの特徴

多くのネットワーク機器は「CUIを標準搭載している。また、パーソナルコンピュータ (PC) やサーバ向けのオペレーティングシステム (OS) には、既定のインターフェイスがGUIであってもコマンドラインターミナルなどのCUI環境が標準で用意されている。」(wikipedia)

要するに、原則として「CLIのみ」と「CUIとGUI両方」の２パターンしか存在しない。


OS | 名前
---|---
Windows| PowerShell, コマンドプロンプト
MacOS | ターミナル

実際に、上記のソフトウェアでCLI環境にアクセスできる
ChromeOS は開発者モードにしないとシステムの根幹にアクセスできない

---
# CLIにふれよう
## 特徴

「初期のコンピュータは、CUIによる対話環境が主流であった。その後、コンピュータの性能が向上したことにより、GUI環境を標準搭載しているパーソナルコンピュータ (MacintoshやWindows 95など）がオフィスや一般家庭にも普及し、CUIの利用頻度は減っていった。」(wikipedia)

---

# CLIにふれよう
## CLIからコンピュータを操作する利点

- ある程度使い方を習得すると、マウスを使うより速く操作ができる
- 作業の自動化が容易
- CLIでは利用できるがGUIでは利用できない素晴らしいツールがたくさんある
---

# YouTube 動画をダウンロードする方法

## 従来
- 怪しいウェブサイトを介して...
- 怪しいスマホアプリを介して...

問題点：マルウェアをダウンロード・実行してしまう可能性がある

- YouTube Premium に課金して...

---

# YouTube 動画をダウンロードする方法

- youtube-dl というツールを利用し、安全かつ課金なしでダウンロードする方法を紹介・実演する
- もっと知りたいと思ったら自分で「youtube-dl」で検索
- 公式サイト: https://yt-dl.org/ に記載された内容をもとにした内容

--- 

# 注意

1. 利用規約に抵触する可能性あり
2. 著作権法を遵守
3. 最後は自己責任

---

# youtube-dl
## 概要

- ソースコードがインターネット上で公開されている
- 有志によって開発されている
- 無料で使用可能
- Pythonで実装されている
- パソコンがあると便利

---

# youtube-dl
## 環境構築

> To install it right away for all UNIX users (Linux, OS X, etc.), type:

    sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl

    sudo chmod a+rx /usr/local/bin/youtube-dl

---

# youtube-dl
## 環境構築

UNIX環境として Google Cloud Platform を利用
Google のサーバ上の自由に使える領域にダウンロードする

    OS: Debian GNU/Linux 10 (buster) x86_64
    CPU: Intel Xeon (4) @ 2.200GHz

なお、Windows にもインストールできる。

---

# youtube-dl
## 環境構築

1. ブラウザで console.cloud.google.com にアクセス
2. isk.ed.jpドメインではない、個人用のGoogleアカウントでログイン
3. 利用規約に同意する
4. 画面右上の「Cloud Shell を有効にする」ボタンをクリック

---

# 実演：環境構築してみよう

---

# youtube-dl
## 環境構築

> To install it right away for all UNIX users (Linux, OS X, etc.), type:

    sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl

    sudo chmod a+rx /usr/local/bin/youtube-dl

(https://github.com/ytdl-org/youtube-dl/blob/master/README.md#installation より)

一行ずつコピペして実行する
$記号の表示が次の操作を受け付けるサイン

---

# youtube-dl
## ダウンロード

    youtube-dl [URL...]

1. youtube-dl の後にURLをコピペしてEnterを押す
画面に再び$が表示されるとダウンロード終了のサイン

---

# youtube-dl
## ダウンロード

2. 画面上部の３点リーダをクリック
3. 「ダウンロード」をクリックしファイルを選択。ダウンロードボタンをクリック。

---

# 実演：YouTube に世界で初めて投稿された動画をダウンロードしてみよう

URL: https://www.youtube.com/watch?v=jNQXAC9IVRw

    Produced by	Jawed Karim (Youtubeの共同創業者のひとり)
    Release date	April 23, 2005, 8:31:52 p.m. (PDT); 16 years ago
    Running time	0:19
    Country	United States
    Language	English 
    (wikipedia)

--- 

# まとめ

1. UNIXはOS(基本ソフトウェア)の一種・現代社会に多大な貢献
2. CLIは文字入力のみでコンピュータを操作する仕組み・ほとんどの環境で利用可能
3. youtube-dl を用いると安全かつ課金なしでYouTube動画をダウンロードできる。

---

# ご静聴ありがとうございました

スライドのPDFファイルは公式サイトからご覧になれます。
