# 強調語法

強調，例如義大利斜體，可以使用 *asterisks* 或 _underscores_。

加重語氣的強調，例如粗體，可以用 **asterisks** 或 __underscores__。

你還可以混用這兩種 **asterisks and _underscores_**。

替文字加上刪除線，像這樣 ~~Scratch this.~~

# 清單
1. 第一則列表項目
2. 另一個項目
⋅⋅* 無序的次清單。
1. 數字本身是否排序並不重要，通通使用相同的數字也可以。
⋅⋅1. 排序的次清單。
4. 另一個項目

⋅⋅⋅你可以在一則項目中使用縮進的段落格式。注意上面的**空行**，還有本段前的**空格**（至少一個，我們使用了三個，讓呈現更清楚）。

⋅⋅⋅在一個段落中**強制換行**，在語句後方加入兩個**空格**。⋅⋅
⋅⋅⋅這個被強制設定的獨立行，依舊在同一個段落中。⋅⋅
⋅⋅⋅（有些人覺得使用空格強制換行太麻煩，例如 GFM 就根本不需要）。

* 可以使用星號建立無序清單
- 或是短橫線（負號）
+ 使用半形加號也可以

# 連結設定
[這是一個行內連結](https://www.google.com)

[這是一個帶有標題的行內連結](https://www.google.com "Google's Homepage")

[這是一個參考連結][Arbitrary case-insensitive reference text]

[這是一個對應到 Git 倉儲檔案的相對參考連結](../blob/master/LICENSE)

[參考標的物也可以使用數字][1]

直接使用文字對應也可以 [這段文字連到參考項目]

參考項目可以寫在文檔的最後，有點像書內的註解（註腳）。

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[這段文字連到參考項目]: http://www.reddit.com


# 註腳 Footnotes

Text prior to footnote reference.[^2]  
[^2] Comment to include in footnote.  

Here is some text containing a footnote.[^somesamplefootnote]  
[^somesamplefootnote]: Here is the text of the footnote itself.  
[somelink]:http://somelink.com  

# 圖片
這是我們的 logo （將滑鼠移到圖片上會顯示圖片標題）：

行內格式：
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 標題文字範例一")

參考連結格式：
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 標題文字範例二"


# 程式代碼與語法高亮標示
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
s = "Python syntax highlighting"
print s
```

```
No language indicated, so no syntax highlighting.
But let's throw in a <b>tag</b>.
```

# 表格
冒號（Colons）是用來對齊的（擺左齊左、擺右齊右，都擺就置中）。

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

最外圍的豎線（|）不是絕對需要，在原始文檔中你可以不要太在意美觀，實際轉成網頁或電子書時會呈現得很好。你也可以在表格內使用行內格式。

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

# 引言
> 引言（Blockquotes）常常出現在電子郵件中，表示摘錄來信原句並回覆。
> 這一行是引言的一部分。

Quote break.

> 這是一段非常長的引言區塊，只要在句首使用了正確的符號與空格，你可以持續不間斷的撰寫，整段文字都還是會被包含在引言區塊中。當然你依舊可以在引言區塊中 *使用* **Markdown** 的行內格式標記語法。


# 行內 HTML

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>


# Youtube 影片
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg"
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
