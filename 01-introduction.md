---
marp: true
lang: ja
size: 16:9
theme: newt
paginate: true
footer: "ポートフォリオサイトを作ろうハンズオン by newt239"
---

<!-- _class: lead -->

# 1. 基本編

---

### このセクションのゴール

- HTML/CSS が書けるようになる
- GitHub Pages で公開できるようになる

---

### 目次

1. 準備
1. Web サイトの仕組み
1. HTML とは
1. CSS とは
1. GitHub Pages での公開

---

<!-- _class: lead -->

## 1-1. 準備

---

### 事前準備

#### 必要なソフト

- [Git](https://git-scm.com/)
  - バージョン管理ツール
- [Visual Studio Code](https://code.visualstudio.com/)
  - コードエディタ

#### 必要なアカウント

- [GitHub](https://github.com/)
  - リモートリポジトリのホスティングサービス

---

### GitHub アカウントの作成

1. [GitHub](https://github.com/) にアクセス
1. 右上の`Sign up` をクリック
1. メールアドレス、パスワード、ユーザ名を設定
1. bot テストのミニゲームをクリア
1. メールで送られた認証コードを入力
1. プランは Free を選択

- メールアドレスは個人のものを推奨
- ユーザ名は他人と被っている場合利用できません

![bg right fit](./images/register-github.png)

---

### Git のダウンロード

#### Windows の場合

1. [Git for Windows](https://gitforwindows.org/) にアクセス
1. **Click here to download** をクリック

#### Mac の場合

1. [XCode](https://developer.apple.com/xcode/)にアクセス
1. 右上の Download をクリック
1. App Store が開くので、 XCode をインストール

![bg right fit](./images/git-download-windows.png)

---

### Git のインストール

#### Windows の場合

1. ダウンロードフォルダにある exe ファイルをダブルクリック
1. ウィザードが立ち上がるので、基本的に右下の「Next」をクリックし続ける
1. 「Choosing the default editor used by Git」画面で、Use Visual Studio Code as Git's default editor を指定する

![bg right fit](./images/git-installer-windows.jpeg)

---

### Git の設定

- スタートメニューから Git Bash を起動
  - Mac の場合は「アプリケーション」の「ユーティリティ」フォルダにあるターミナルを起動
- 下記のコマンドを入力して、ユーザ名とメールアドレスを設定

```bash
git config --global user.name "ここにGitHubのユーザ名"
```

```bash
git config --global user.email "ここにGitHubのメールアドレス"
```

- 特にエラーが出ていなければ設定完了

---

### Visual Studio Code のダウンロード

1. [Visual Studio Code](https://code.visualstudio.com/) にアクセス
2. OS に合わせてインストーラをダウンロード
3. インストール

#### 補足

- Microsoft が主導して開発しているオープンソースのコードエディタ
- 一般的に **VSCode** と呼ばれるので、本資料でも以降は VSCode と表記します

---

### Visual Studio Code の設定

#### 拡張機能のインストール

- VSCode を起動し、左側のアイコンから拡張機能を検索
- 「HTML CSS Support」をインストール

![bg right fit](./images/vscode-extension.png)

---

<!-- _class: lead -->

## 1-1. Web の仕組み

---

### Web ページが表示されるまで

---

### 各言語の役割

- HTML: 文書の構造を記述
  - 「ここが見出し」「ここが段落」など
- CSS: デザインを記述
  - 「見出しは赤色」「段落のフォントサイズは 16px」など
- JavaScript: 動的な挙動を記述
  - 「ボタンをクリックしたらローディングアニメーションを表示」など

---

<!-- _class: lead -->

## 1-2. HTML とは

---

### HTML とは

- HyperText Markup Language
  - 「マークアップ言語」であって「プログラミング言語」ではない
- 文書の構造を記述するための言語
- タグで囲まれた要素を使って構造を表現

---

<!-- _class: invert -->

### HTML5 と HTML

- **HTML5**は 2014 年 10 月に W3C によって勧告された HTML のバージョン
- 2021 年 1 月に廃止され、以降は **HTML Living Standard** が有効な規格となっている

---

### HTML の基本構造

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <title>ページのタイトル</title>
  </head>
  <body>
     <!-- これはコメントで、実際には表示されません -->
    <h1>見出し</h1>
    <p>段落</p>
  </body>
</html>
```

---

### HTML の基本的なルール

- 開始タグを書いたら必ず終了タグを書く
  - `<`で始まり`>`で終わっている部分がタグで、とくに`</`で始まっているものが終了タグ
  - `<img/>`タグや`<br/>`タグなど、一部例外あり
- Python などとは異なり、インデントの大きさは問わない
- コメントは`<!--`と`-->`で囲む
- 1 行目の`<!DOCTYPE html>`は 必ず書く
- `<html>`タグの中に`<head>`と`<body>`がある
- `<head>`タグの中にはページの情報を書く
- `<body>`タグの中にはページの内容を書く。ページを開いた時に表示されるのはこの部分

---

### HTML ファイルを作成してみよう

1. 作業用のフォルダを作成する
1. VSCode を起動し、左上の「ファイル」→「フォルダを開く」から作成したフォルダを開く
1. 左側のファイルが表示されるエリアから新しいファイルを作成するアイコンをクリック
1. ファイル名を`index.html`として保存

- フォルダ作成ボタンと間違えないように注意
- もしくは左上の「ファイル」→「新しいファイル」

![bg right fit](./images/vscode-welcome.png)

---

### HTML をブラウザで表示してみよう

- 作成した HTML ファイルに先ほどのコードを書き込む

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <title>ページのタイトル</title>
  </head>
  <body>
    <h1>見出し</h1>
    <p>段落</p>
  </body>
</html>
```

- ファイルを保存し、VSCode 上で右クリックして「Reveal in Explorer」を選択
- ファイルをダブルクリックしてブラウザで開く

---

### HTML をブラウザで表示してみよう

<div style="text-align: center;">

:tada: :tada: :tada:

![w:800px](./images/first-html.png)

</div>

---

### 主に使うタグ

| タグ                      | 説明                                       |
| ------------------------- | ------------------------------------------ |
| `<h1>` - `<h6>`           | 見出しを表現するタグ                       |
| `<p>`                     | 段落を表現するタグ                         |
| `<a>`                     | ハイパーリンクを作成するタグ               |
| `<img>`                   | 画像を表示するタグ                         |
| `<ul>`, `<ol>`, `<li>`    | リストを表現するタグ                       |
| `<table>`, `<tr>`, `<td>` | 表を表現するタグ                           |
| `<div>`, `<span>`         | ブロック要素とインライン要素を表現するタグ |

---

### 別のページにリンクさせる

- VSCode で新しく`about.html`を作成し、以下のコードを書き込む

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <title>aboutページ</title>
  </head>
  <body>
    <h1>aboutページ</h1>
    <p>これはaboutです。</p>
    <a href="./index.html">トップページに戻る</a>
  </body>
</html>
```

- `index.html`の`body`タグ内に以下のコードを追加

```html
<a href="./about.html">aboutページへ</a>
```

---

### 画像を表示させる

- 画像をダウンロードして、HTML ファイルと同じフォルダに保存
  - 分かりやすくするために`images`フォルダなどを作成して配置することが多い
- `index.html`の`body`タグ内に以下のコードを追加
  - `your-image-name.png`はダウンロードした画像のファイル名

```html
<img src="./your-image-name.png" alt="画像の説明文" />
```

---

### 箇条書きを作る

- `index.html`の`body`タグ内に以下のコードを追加

```html
<ul>
  <li>リスト1</li>
  <li>リスト2</li>
  <li>リスト3</li>
</ul>
```

- `ul`は unordered list の略で、順序のないリストを表現
- `li`は list item の略で、リストの各項目を表現

```html
<ol>
  <li>リスト1</li>
  <li>リスト2</li>
  <li>リスト3</li>
</ol>
```

- `ol`は ordered list の略で、順序のあるリストを表現

---

### 表を作る

- `index.html`の`body`タグ内に以下のコードを追加

<div style="display: flex;">

<div style="width: 50%">

```html
<table>
  <thead>
    <tr>
      <th>見出し1</th>
      <th>見出し2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1行目1列目</td>
      <td>1行目2列目</td>
    </tr>
    <tr>
      <td>2行目1列目</td>
      <td>2行目2列目</td>
    </tr>
  </tbody>
</table>
```

</div>

<div>

- `table`は表を表現
- `thead`は表の見出し部分
- `tbody`は表の本体部分
- `tr`は table row の略で、表の行を表現
- `th`は table header の略で、表の見出しを表現
- `td`は table data の略で、表のデータを表現

</div>
</div>

---

<!-- _class: lead -->

## 1-3. CSS とは

---

### CSS とは

- Cascading Style Sheets
- 文書のデザインを記述するための言語
- セレクタとプロパティを使ってデザインを記述

---

### CSS の基本構造

```css
h1 {
  color: red;
}
p {
  font-size: 16px;
}
```

---

<!-- _class: lead -->

## 1-4. GitHub Pages での公開

---

### GitHub Pages とは

- GitHub が提供する静的 Web ホスティングサービス

---

### GitHub アカウントを作成

1. [GitHub](https://github.com/) にアクセス
2. `Sign up` からアカウントを作成
3. メールアドレスの確認

---

### Git をインストール

1. [Git](https://git-scm.com/) にアクセス
2. OS に合わせてインストーラをダウンロード
3. インストール

```

```
