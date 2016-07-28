--- 
layout: template1 
---
# Table of Contents
1. [Gitのインストール-Windows版](#git-windows)
2. [Gitのインストール-Mac版](#git-mac)
3. [githubアカウント作成](#github)
4. [demoアプリをforkしてみよう](#demofork)
5. [demoアプリをcloneしてみよう](#democlone)
6. [アプリを動かしてみよう](#section)
7. [アプリを編集してみよう](#section-1)
8. [commitしてpushしてみよう](#commitpush)
9. [事前課題](#section-2)
10. [次のステップ下記を読んで勉強してみよう](#section-3)

## Gitのインストール-Windows版
1. [git for windows](https://git-for-windows.github.io/)というサイトにアクセスします。
	- ![]({{site.baseurl}}/screenshots/git_windows01.png)
2. ダウンロードが完了すると、ダウンロードした実行形式ファイル(.exe)を実行してインストールしていきます。
	- ![]({{site.baseurl}}/screenshots/git_windows02.png)
3. ひたすら**Next**
	- ![]({{site.baseurl}}/screenshots/git_windows03.png)
    - ![]({{site.baseurl}}/screenshots/git_windows04.png)
    - ![]({{site.baseurl}}/screenshots/git_windows05.png)
    - ![]({{site.baseurl}}/screenshots/git_windows06.png)
4. 
太字で"**Adjusting your PATH environment**"と書かれた設定画面に移ります。そこではGit Bashのみを使用するため、一番上の「Use Git Bash only」を選択してNextボタンをクリックしてください。
    - ![]({{site.baseurl}}/screenshots/git_windows07.png)
5. 太字で"**Configuring the line ending conversions**"と書かれた改行コードの変換画面に移ります。そこでは、GitHubでで使用されているLF(Line Feed)で改行が行われています。一方WindowsはCRLF(Carriage Return + Line Feed)で改行するのでGitが自動変換を行ってくれる設定があるのでその設定である一番上の「Checkout Windows-style,commit Unix-style line endings」を選択してください。
    - ![]({{site.baseurl}}/screenshots/git_windows08.png)
3. ひたすら**Next**
	- ![]({{site.baseurl}}/screenshots/git_windows09.png)
    - ![]({{site.baseurl}}/screenshots/git_windows10.png)
    
## Gitのインストール-Mac版	
[こちら(HomebrewでGitをインストールする)](http://qiita.com/micheleno13/items/133aee005ae37c28960e)をみてインストールしてみてください。　投げやりですみません。。

## githubアカウント作成
1. [github](https://github.com/) というサイトにアクセスします。
	- **Pick a username**にユーザ名
	- **Your email address**にあなたのメールアドレス
	- **Create a password**にパスワードを入れます
	- 最後に**Sign up for Github**をクリックします
	- ![]({{site.baseurl}}/screenshots/github01.png)
2. https://github.com/join/plan というページに遷移しています。
	- **Unlimited public repositories for free**.が選択されていることを確認します
	- **Continue**をクリックします
	- ![]({{site.baseurl}}/screenshots/github02.png)
3. https://github.com/join/customize というページに遷移しています。
	- **skip this step**をクリックします
	- ![]({{site.baseurl}}/screenshots/github03.png)
4. https://github.com/dashboard というページに遷移したら　アカウント作成完了!
	- ![]({{site.baseurl}}/screenshots/github04.png)
5. 最後にメールを確認
	- **[GitHub] Please verify your email address**. というメールが着ているのを確認
    - **Verify email address** をクリック
    
## demoアプリをforkしてみよう
1. [https://github.com/freddiefujiwara/nikotama-2016-aug-frontend/](https://github.com/freddiefujiwara/nikotama-2016-aug-frontend/) というページにアクセスします。
	- 右上にある**Fork**というアイコンをクリック
    - ![]({{site.baseurl}}/screenshots/fork01.png)
2. https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend というページができたらfork完了

## demoアプリをcloneしてみよう
1. https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend/ にアクセスします。
	- 緑のボタンClone or downloadをクリックします
    - ![]({{site.baseurl}}/screenshots/clone01.png)
2. 中に表示されているテキストボックスをコピーしておきます.
3. キーボードのWindowsマーク![]({{site.baseurl}}/screenshots/clone02.png)を押下します
3. 右下の方に検索窓があるので **Git Bash**と打ち込み Git Bashを探します見つかったらクリック
	- ![]({{site.baseurl}}/screenshots/clone03.png)
4. 下記のような黒い画面が見えたらあなたも**プログラマ**　さぁ黒い画面と格闘していきましょう
	- ![]({{site.baseurl}}/screenshots/clone04.png)
5. 黒い画面に下記を打ち込んで($のあとの文字列をタイプして最後はエンターを押下!)いきます

```bash
$ git clone https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend.git                             
```
そうすると。。。

```bash
Cloning into 'nikotama-2016-aug-frontend'...
remote: Counting objects: 203, done.
remote: Compressing objects: 100% (97/97), done.
remote: Total 203 (delta 51), reused 0 (delta 0), pack-reused 103
Receiving objects: 100% (203/203), 1.13 MiB | 650.00 KiB/s, done.
Resolving deltas: 100% (88/88), done.
Checking connectivity... done.
```
上記のような表示がでてきて... done.となったらclone完了

4. ファイルを確認してみよう
下記のコマンドを打ってclone したフォルダに移動しています

```bash
$ cd nikotama-2016-aug-frontend/ 
```
続けて。。

```bash
$ ls -lha
```

そうすると下記のようにファイルが見えるはずです(表示は環境によって異なるので、**下記のような**表示になればOKです)

```bash
total 1.9M                                                                                                                    
drwxrwxr-x  4 [あなたのOS上のアカウント] [あなたのOS上のグループ] 4.0K Jul 23 11:11 .
drwxr-xr-x 24 [あなたのOS上のアカウント] [あなたのOS上のグループ] 1.9M Jul 23 11:11 ..
drwxrwxr-x  2 [あなたのOS上のアカウント] [あなたのOS上のグループ] 4.0K Jul 23 11:11 api
drwxrwxr-x  8 [あなたのOS上のアカウント] [あなたのOS上のグループ] 4.0K Jul 23 11:11 .git
-rw-rw-r--  1 [あなたのOS上のアカウント] [あなたのOS上のグループ] 1.1K Jul 23 11:11 index.html
-rw-rw-r--  1 [あなたのOS上のアカウント] [あなたのOS上のグループ] 1.1K Jul 23 11:11 LICENSE
-rw-rw-r--  1 [あなたのOS上のアカウント] [あなたのOS上のグループ]   29 Jul 23 11:11 README.md
```

## アプリを動かしてみよう 
1. ファイルの場所を探そう

```bash
$ pwd 
```
そうすると。。下記のような表示になるとおもいます

```bash
/c/Users/[あなたのOS上のアカウント]/nikotama-2016-aug-frontend/ 
```

2. つまりC:\Users\[あなたのOS上のアカウント]\nikotama-2016-aug-frontend\index.html というファイルがアプリですこれををブラウザ(Google ChromeやFirefoxやInternet Explorerの事です)で開いてみます。
そうすると。。　下記のような"Click ME!"というボタンがあるのでおしてみてください。

{% include click_me.html %}

## アプリを編集してみよう
1. index.html を**メモ帳**で開いてみよう

![]({{site.baseurl}}/screenshots/app01.png)

```JavaScript
$nikotama.get('https://rawgit.com/freddiefujiwara/nikotama-2016-aug-frontend/master/api/get.js',function(res){
```

という行を

```JavaScript
$nikotama.get('https://api.github.com/users/freddiefujiwara',function(res){
```

に変更して保存しよう

2. index.html をもう一回ブラウザで開いてみます.
そうすると。。　下記のような"Click ME!"というボタンがあるのでおしてみて　前と動きが変わったことを確認してください

{% include click_me_github.html %}

## commitしてpushしてみよう
さてまた**黒い画面**に戻りましょう!

- gitにあなたの名前とメールアドレスを設定しましょう

```bash
$ git config --global user.name "[あなたの名前]"
```

```bash
$ git config --global user.email [あなたのメールアドレス]
```

- index.htmlを保存したら下記のコマンドをうってみよう

```bash
$ git commit -m 'first commit' -a
```
**上級編: -m　をつけずにcommitしてみよう**

- push!!

```bash
$ git push origin master                                                         
Username for 'https://github.com':[あなたのアカウント]
Password for 'https://[あなたのアカウント]@github.com':[あなたのパスワード]
```

そうすると下記のような表示になったら完成

```bash
Counting objects: 6, done.                    
Delta compression using up to 2 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 351 bytes | 0 bytes/s, done.
Total 3 (delta 2), reused 0 (delta 0)
To https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend.git
ac2f0d6..a3cdcbc  master -> master
```

- https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend/blob/master/index.html にいって変更が反映されたことを確認してみよう

## 事前課題
上記まですすめたら
https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend
をメールに返信してください

## 次のステップ下記を読んで勉強してみよう

### HTML/JavaScript
- [超絶初心者のためのフロント入門（HTML、CSS、JavaScript）](http://qiita.com/shuntaro_tamura/items/c9b2fec0f3a9f7d1e987)
- [JavaScript入門](http://qiita.com/akiinu/items/5d1178fa1102b939cd71)
- [nikotama.js(上記アプリで使っているライブラリ)](https://github.com/freddiefujiwara/nikotama/blob/master/src/nikotama.js)

### git
- [gitflow](http://danielkummer.github.io/git-flow-cheatsheet/index.ja_JP.html)
- [git入門(全22回)](http://dotinstall.com/lessons/basic_git)
