# Intro
対象とする読者は、今からプログラムを書いてみたいと思っている人。中学生以上くらいの方を想定しています。そして、パソコンを持っている人。Windows とか Mac とか。  
あとは、英語のアルファベットを使っても大丈夫な人。英単語の意味はググりながらで大丈夫、っていう人。

今からプログラムをやってみようと思う場合、どの言語を学ぼうか迷うと思うので、「いろいろな言語」でテトリスを書いてみるとどうなるか、ということを紹介しようと思います。

テトリスは、言語を学ぶにはちょうど良い長さのプログラムになるため、これを題材として選びました。

プログラムのことはまったく知らなくていいのですが、ファイルとかフォルダ（ディレクトリ）の考え方と、ドラッグアンドドロップは知っておいてください、、、。エクセルとかワードなんかを使ったことがあって、ファイルを作ったことがあればいいのだけど。

# Javascript
とりあえず、一番簡単なのが Javascript であるため、まずはこれを使ってみようと思う。

## step 0
まずは、VS Code（Microsoft社製の無料で利用できるエディタです）を準備しましょう。VSCode 以外の好きなエディタがあれば、そちらを使ってくださいね。

VS Code のインストールの方法については、インターネットにたくさんの記事があるので、ブラウザ（Edge や Chrome など）で「vscode　インストール」を検索してもらえるようお願いします！

![01](https://github.com/user-attachments/assets/18d746eb-ed14-494b-98b2-8ea01dd0fad4)

## step 1
まずは、ブラウザ（Edge とか Chrome など）を利用して、画面に「こんにちは」を表示してみよう。

VS Code をインストールして起動すると、以下のような画面になると思います。色が異なっていたり、表示されている文字が異なるかもしれませんが気にしないで下さい。

![01](https://github.com/user-attachments/assets/626e3baa-a8c5-41f2-8f6c-532a4925278a)

この VS Code の画面のどこでもいいのでクリックして、Ctrl + Nキー を押して下さい。（Ctrl キーと N キーを同時に押して下さい。）そうすると以下のようになると思います。日本語で表示されている場合もあるかもしれませんが、気にしないで下さいね。

![1681394583455-NtpI90hylj](https://github.com/user-attachments/assets/a00d5389-01e4-4803-869c-e0ecee71bd15)

そうしたら、以下の画面のように、「こんにちは」と入力してみましょう。

![01](https://github.com/user-attachments/assets/1a5685b7-6e88-4ede-a3ca-d5d48f25f141)

次に、Ctrl + Sキー を押してください。保存をするダイアログが出てくると思います。  
下のようなダイアログが出たら、ファイル名のところに「tetris」と入力し、ファイルの種類を「HTML」にして「保存」を押して下さい。

保存する場所はどこでも良いです。「保存する場所」という意味が分かりにくければ、そのまま保存してしまってください。どこであっても問題ないので。

![1681395599367-mTQkrxTErl](https://github.com/user-attachments/assets/01f690b2-b855-46dc-ad9b-cc1f9afbd638)

次に、下図で示した書類のようなマークをクリックしてみてくだい。

![01](https://github.com/user-attachments/assets/a3867b14-2881-4d3a-8743-edbd00d2f06e)

そうすると、下図のように、画面の左側にファイルの一覧を示す画面が表示されます。

![02](https://github.com/user-attachments/assets/b43e9204-5298-44d8-afb0-6639dc4b6ca7)

左側のファイル一覧のところにある、「tetris.html」をドラッグしてみてください。（マウスの左ボタンを押したまま動かしてみて下さい。）  
今はドラッグできることを試しているだけですので、下図のようにドラッグできたら、マウスのボタンから手を離して、ドラッグを解除して下さい。

![04](https://github.com/user-attachments/assets/ad5f3ea0-f928-41d0-bd48-fec1d7ef0792)

次に、Google Chrome を起動して下さい。（Edge や Firefox でも大丈夫です。）もう一度、上の画面のようにドラッグして、Google Chrome のタイトルバーのところ（下の図でいうと、上端の灰色の帯の部分）にドロップしてください。（Google Chrome のタイトルバーのところまでドラッグしてきて、適当な場所でマウスのボタンを離して下さい。）

次に、Google Chrome を起動して下さい。（Edge や Firefox でも大丈夫です。）  
もう一度、上の画面のようにドラッグして、Google Chrome のタイトルバーのところ（下の図でいうと、上端の灰色の帯の部分）にドロップしてください。（Google Chrome のタイトルバーのところまでドラッグしてきて、適当な場所でマウスのボタンを離して下さい。）

![06](https://github.com/user-attachments/assets/11781201-27d3-4568-b3e7-84c82caacbdb)

下のような画面が表示されたらオッケーです！

![07](https://github.com/user-attachments/assets/aa7ca920-5ded-443d-a360-ac9a9a5e8096)

## step 2
この step では、下のプログラムを利用して、「テトリス」という文字を表示してみましょう。下のプログラムの意味が分かる人は、この step を読み飛ばして下さいね。

```
const ge_title = document.createElement('div');
ge_title.textContent = "テトリス";
document.body.appendChild(ge_title);
```

上のプログラムを、「tetris.html」に貼り付けてみましょう。

![08](https://github.com/user-attachments/assets/b6264e5d-e4c1-486d-99e2-15b07ac2b5e4)

そして、これを実行してみましょう。  
実行するには、step 1 でやってみたように `tetris.html` を Chrome にドラッグ＆ドロップしてもいいですし、Chrome の画面がさっきの状態で残っていれば、Chrome の画面を更新して下さい。（Chrome の画面の更新は、下図の赤枠で囲った部分のボタンを押して下さい。）

![09](https://github.com/user-attachments/assets/aa198bbb-5ea3-4f64-a391-86f0212dc440)

そうすると、Chrome の画面が以下のようになったと思います。

![10](https://github.com/user-attachments/assets/213798d5-9263-4aee-a72f-975b1c2b20ee)

`tetris.html` の内容が、そのまま表示されました。これは、`tetris.html` の内容がプログラムと認識されなかったためです。  
プログラムと認識させる一番簡単な方法が、プログラムを以下のように `<body><script>` と `</body></script>` で囲むことです。

![11](https://github.com/user-attachments/assets/62b961ac-0de6-4336-9694-d509383ba0da)

この状態で、プログラムを実行すると、下図のように「テトリス」と表示されるでしょう。

![12](https://github.com/user-attachments/assets/4b7cd304-6d72-423c-bb3b-26ecc0539743)

さて、少しだけプログラムの解説をしてみましょう。  
Chrome などのブラウザは、`div` というブロック単位で画面に表示を行います。  
そのため、最初に `document.createElement('div');` で、新しく `div` を作り、その `div` に `ge_title` という名前を付けています。  
そして、新しく作った `div` に「テトリス」というテキスト情報（文字列情報）を `ge_title.textContent = "テトリス";` で与えます。

新しく作った `div` は、そのままじゃ表示されないので、それを画面表示に追加してください、という意味で `document.body.appendChild(ge_title);` とします。

補足しておきますと、`document` は `Chrome などのブラウザ` を表し、`body` は `表示される画面` を表します。  
そして、`document.body.appendChild(ge_title);` によって、表示される画面に `ge_title` が追加されるため、画面に「テトリス」と表示されることになります。

