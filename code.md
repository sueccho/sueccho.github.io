# 記法

## Markdown記法 サンプル集

### 見出し
1個から6個シャープで見出しを記述する。1個はページタイトル。
※シャープと見出し文字の間には半角スペースを1つ入れること
#### 記述例
~~~
# タイトル
## 見出し1
### 見出し2
#### 見出し3
##### 見出し4
###### 見出し5
~~~

#### 表示例
# タイトル
## 見出し1
### 見出し2
#### 見出し3
##### 見出し4
###### 見出し5

### リスト
ハイフン、プラス、アスタリスクのいずれかで箇条書きリストを記述可能。
※ハイフン、プラス、アスタリスクと箇条書きの項目の間には半角スペースを1つ入れること
#### 記述例
~~~
- リスト1
    - ネスト リスト1_1
        - ネスト リスト1_1_1
        - ネスト リスト1_1_2
    - ネスト リスト1_2
- リスト2
- リスト3
~~~
#### 表示例
- リスト1
    - ネスト リスト1_1
        - ネスト リスト1_1_1
        - ネスト リスト1_1_2
    - ネスト リスト1_2
- リスト2
- リスト3

### 番号付きリスト
数値+半角ドットで番号付きリストを記述可能。
番号の内容は何でもいい。実際に表示される際に適切な番号で表示される。
そのため、一般的にはすべて `1. 内容` で記載すると変更に強く楽です。
※数値+半角ドットと箇条書きの項目の間には半角スペースを1つ入れること
#### 記述例
~~~
1. 番号付きリスト1
    1. 番号付きリスト1_1
    1. 番号付きリスト1_2
1. 番号付きリスト2
1. 番号付きリスト3
~~~
#### 表示例
1. 番号付きリスト1
    1. 番号付きリスト1_1
    1. 番号付きリスト1_2
1. 番号付きリスト2
1. 番号付きリスト3


### 引用

#### 記述例
~~~
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。
~~~
#### 表示例
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。

### 二重引用
#### 記述例
~~~
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。
>> お世話になります。 yyyです。
>> 
>> あの新機能バグってるっすね
~~~
#### 表示例
> お世話になります。xxxです。
> 
> ご連絡いただいた、バグの件ですが、仕様です。
>> お世話になります。 yyyです。
>> 
>> あの新機能バグってるっすね

### pre記法(スペース4 or タブ)
半角スペース4個もしくはタブで、コードブロックをpre表示できます。
#### 記述例
~~~
    # Tab
    class Hoge
        def hoge
            print 'hoge'
        end
    end

---

    # Space
    class Hoge
      def hoge
        print 'hoge'
      end
    end
~~~
#### 表示例
    # Tab
    class Hoge
        def hoge
            print 'hoge'
        end
    end

---

    # Space
    class Hoge
      def hoge
        print 'hoge'
      end
    end

### code記法
バッククォートで文字列を囲むことでコードの一部を表示可能です。
#### 記述例
~~~
インストールコマンドは `gem install hoge` です
~~~
#### 表示例
インストールコマンドは `gem install hoge` です

### 強調：&lt;em&gt;
アスタリスクもしくはアンダースコア1個で文字列を囲むことで強調します。
見た目は斜体になります。
#### 記述例
~~~
normal *italic* normal
normal _italic_ normal
~~~
#### 表示例
normal *italic* normal
normal _italic_ normal

### 強調：&lt;strong&gt;
アスタリスクもしくはアンダースコア2個で文字列を囲むことで強調にします。
見た目は太字になります。
#### 記述例
~~~
normal **bold** normal
normal __bold__ normal
~~~
#### 表示例
normal **bold** normal
normal __bold__ normal

### 強調：&lt;em&gt; + &lt;strong&gt;
アスタリスクもしくはアンダースコア3個で文字列を囲むことで <em> と <strong> による強調を両方適用します。
見た目は斜体かつ太字になります。
#### 記述例
~~~
normal ***bold*** normal
normal ___bold___ normal
~~~
#### 表示例
normal ***bold*** normal
normal ___bold___ normal

### 水平線
アンダースコア、アスタリスク、ハイフンなどを3つ以上連続して記述することで水平線を表示します。
※連続するハイフンなどの間にはスペースがあっても良い
#### 記述例
~~~
***

___

---

*    *    *
~~~
#### 表示例
***

___

---

*    *    *

### リンク
`[表示文字](リンクURL)` 形式でリンクを記述できます
#### 記述例
~~~
[Google先生](https://www.google.co.jp/)
~~~
#### 表示例
[Google先生](https://www.google.co.jp/)

### 定義参照リンク
Markdownの文書の途中に長いリンクを記述したくない場合は、
同じリンクの参照を何度も利用する場合は、リンク先への参照を定義することができます。
#### 記述例
~~~
[こっちからgoogle][google]
その他の文章
[こっちからもgoogle][google]

[google]: https://www.google.co.jp/
~~~
#### 表示例
[こっちからgoogle][google]
その他の文章
[こっちからもgoogle][google]

[google]: https://www.google.co.jp/

### 単行コメント
#### 記述例
~~~
[](
コメントアウトしたい内容
)
~~~
### 複数行コメント
#### 記述例
~~~
[](
複数行のときは\
改行直前に\
バックスラッシュがないと\
ダメっぽい
)
~~~


## GitHub Flavored Markdown(GFM)
GitHub Flavored Markdown(GFM)はGitHubの独自仕様を加えたMarkdown記法。
以降、GFMと記載します。

### GFM:リンクテキスト簡易記法
URLは記述するだけで自動的にリンクになります。
#### 記述例
~~~
https://www.google.co.jp/
~~~
#### 表示例
https://www.google.co.jp/

### GFM:取り消し線
チルダ2個で文字列を囲むことで取り消し線を利用できます。
#### 記述例
~~~
~~取り消し線~~
~~~
#### 表示例
~~取り消し線~~

### GFM:pre記法(チルダ×3)
#### 記述例
~~~
　~~~
　class Hoge
　  def hoge
　    print 'hoge'
　  end
　end
　~~~
~~~
#### 表示例
　~~~
　class Hoge
　  def hoge
　    print 'hoge'
　  end
　end
　~~~

### GFM:pre記法(バッククォート×3)
#### 記述例
　```
　class Hoge
　  def hoge
　    print 'hoge'
　  end
　end
　```
#### 表示例
　```
　class Hoge
　  def hoge
　    print 'hoge'
　  end
　end
　```

### GFM:pre記法(シンタックスハイライト)
チルダ、もしくはバッククォート3つの後ろに対象シンタックスの言語名を記述します。
#### 記述例
~~~
　~~~ruby
　class Hoge
　  def hoge
　    print 'hoge'
　  end
　end
　~~~
~~~
#### 表示例
　~~~ruby
　class Hoge
　  def hoge
　    print 'hoge'
　  end
　end
　~~~

### GFM:表組み
#### 記述例
~~~
|header1|header2|header3|
|:--|--:|:--:|
|align left|align right|align center|
|a|b|c|
~~~
#### 表示例
|header1|header2|header3|
|:--|--:|:--:|
|align left|align right|align center|
|a|b|c|

### GFM:ページ内リンク
GitHubのMarkdownを利用すると、見出し記法を利用した際に
アンカーが自動的に作成されます。
そのアンカーを利用したページ内リンクを簡単に作成できます。
#### 記述例
~~~
## menu
* [to header1](#header1)
* [to header2](#header2)

<!-- some long code -->

[return to menu](#menu)
### header1
### header2
~~~
少し省略してますが、こんなかんじのHTMLになります。

#### 表示例
## menu
* [to header1](#header1)
* [to header2](#header2)

<!-- some long code -->

[return to menu](#menu)
### header1
### header2








