---

marp: true
paginate: true

---

# Dive into the World of Web Technologies

## OIWA@Kanazawa Izumigaoka H.S.

---

# Outline

1. インターネットの仕組みと歴史
2. Webの仕組みと歴史
3. HTMLを記述してみよう

--- 

# 1. インターネットの仕組みと歴史

---

> インターネットは、世界中のネットワークが接続されたネットワークです。会社や学校などのネットワークが、それぞれの契約しているプロバイダによって、インターネットに接続されています。

>インターネットで情報の行き先を管理するために利用されているのが、それぞれのコンピュータに割り振られているIPアドレスと呼ばれる数字です。このIPアドレスは、世界中で通用する住所のようなもので、下記の例のような数字の組み合わせによって表記されるのが一般的です。

---

>IPアドレスは、各国ごとに設置された機関がIPアドレスを利用者に配布しています。日本では社団法人日本ネットワークインフォメーションセンター（JPNIC）という組織が、このIPアドレスを管理しています。

    IPアドレスの例: 127.0.0.1

---

>通常、電子メールでは“mail.soumu.go.jp”、ホームページのアドレスでは“www.soumu.go.jp”のように指定します。これはドメイン名を使用した記述方法で、これらのアドレスを受け取ったDNSサーバーが、IPアドレスに自動的に変換することで行き先を見つける仕組みになっています。

https://www.soumu.go.jp/main_sosiki/joho_tsusin/security_previous/kiso/k01_inter.htm

---

># 軍事用途からはじまったインターネット
>インターネットのルーツは、私たちの生活とはかけ離れた軍事用コンピュータ・システムにあるとされています。1969年、米国内の大学と研究所にある４台のコンピュータを電話回線でつないだ「ARPANET」です。その後、世界各国で研究機関や大学、コンピュータ関連大手民間企業のコンピュータをつないだネットワークが続々と登場、相互接続することでネットワークが拡大していきます。日本では1984年に、東京大学、東京工業大学、慶應義塾大学のコンピュータをつないだ「JUNET」がスタートとされます。

https://jpn.nec.com/kotohajime/meet02.html

---

# 2. Webの仕組みと歴史

---

># クライアントとサーバー
>ウェブに接続されたコンピューターはクライアント (client) とサーバー (server) と呼ばれます。これらがどのように相互作用するかを概略図で表すと次のようになります。

---

![](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works/simple-client-server.png)

>クライアントとサーバーを表す 2 つの円。リクエストと書かれた矢印は、クライアントからサーバーへ、レスポンスと書かれた矢印は、サーバーからクライアントへと向かっている。

---

>クライアントは、一般的なウェブユーザーが使うインターネットに接続された端末 (例えば Wi-Fi に接続されているコンピューターや、モバイルネットワークに接続されているスマートフォン) と、これらの端末で利用できるウェブにアクセスするソフトウェア (ふつうは Firefox や Chrome などのウェブブラウザー) のことです。

>サーバーとは、ウェブページ、サイト、アプリを格納しているコンピューターのことです。クライアント端末がウェブページにアクセスしたいときは、ウェブページのコピーがサーバーからクライアントにダウンロードされ、ユーザーのウェブブラウザーに表示されます。

https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works

---

# 3. HTMLを記述してみよう

>HTML (Hypertext Markup Language、ハイパーテキスト・マークアップ・ランゲージ)は、ウェブサイトのコンテンツの構造を作るために使うコードです。例えば、コンテンツは段落、箇条書きのリスト、画像の使用、データテーブルなどの組み合わせで構成されています。

https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/HTML_basics

---

要素 | コード例
----|-----
段落 | <p>paragraph</p>
リンク | <a href="youtube.com">YouTube</a>
画像 | <img src="https://cdn.pixabay.com/photo/2020/05/18/13/39/apple-5186339_1280.jpg" alt="apple">

---

# 実演: codepen.io を利用してHTMLを記述する

1. codepen.io にアクセス
2. HTMLを記述する

---

# もっと学び続けるには？


1. MDN Web docs を読む
2. 書籍を購入し全体像を把握する
3. 自分でコーディングする

---

# 参考

- 総務省 国民の為の情報セキュリティサイト
https://www.soumu.go.jp/main_sosiki/joho_tsusin/security_previous/kiso/k01_inter.htm

- NEC Corporation インターネットって何？
https://jpn.nec.com/kotohajime/meet02.html

- MDN Web Docs
https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/HTML_basics


---

# Thank you for your listening.
