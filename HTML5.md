# HTML5

* < !DOCTYPE html >：用來聲明這是一份採用HTML5語法標準的文件
* < html >：HTML文件的根元素
* < head >：指不會被顯示在頁面上的內容，==樣式設定需寫在head裡面==
* < title >：指定該==網頁的標題==，通常會顯示在瀏覽器的頁籤上
* < body >：會顯示在頁面上的==內容==
* h1,h2,h3...：為一段文字的標題
* p：文字段落
* < !-- -- >：註解，不會出現在畫面
* :pushpin: [英文資料參考](https://www.w3schools.com/tags/)

```html
<!DOCTYPE html>
<html lang="zh-Hant-TW">

<head>
    <meta charset="UTF-8">    
    <title>我是標題</title>
</head>
<body>
    <h1>這裡是文章標題</h1>
    <p>文字段落</p>
    <!-- 這裡是註解文字，不會出現在畫面 -->
</body>
</html>
```

***

## 全域屬性(global attributes)

> 可以在所有的元素中使用

:pushpin: [中文資料參考](https://www.fooish.com/html/global-attributes.html)

### id(identifier)

* 元素唯一識別符號
* 不可重複
* 用作`<a>`連結的錨點名稱
* 用在 JavaScript 可以透過 id **存取**該元素
* 用在 CSS 可以用 id 當**選擇器**

:heavy_exclamation_mark:==id 命名規則== :heavy_exclamation_mark:

1. 有區分大小寫 apple vs Apple
2. 至少包含一個字元
3. 不能以數字開頭
4. 不能包含空格

***

### class(class names)

* 元素類別名稱
* 每個元素可以有多個類別
* 可以用**空格**分開不同類別名稱
* 不同元素可以使用同樣的類別
* 用在 JavaScript 可以透過 class 存取該元素
* 用在 CSS 可以用 class 當選擇器

:heavy_exclamation_mark: ==class 命名規則== :heavy_exclamation_mark:

1. 一個 A-Z 或 a-z 字開頭
2. 接著這些任意的 A-Z a-z 0-9 - _ 字元
3. class name 是大小寫有別

***

## < html >標籤

> 為整份文件的根元素，一份文件**只會有一個**

### lang屬性

* 網頁上的語言
* 語言的規則：語言-字體-地區 (language-script-region)

:pushpin: [查詢語言代碼](https://www.w3schools.com/tags/ref_language_codes.asp)

***

## < head >標籤

>作用上是當作一個容器，裡面包含著不同用途的HTML tags，而這些tag的內容通常不會被顯示在頁面上，僅用來說明關於該網頁的元資訊

:bulb: 放給機器看的內容

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Head</title>
    <link href="page.css" rel="stylesheet">
  </head>
  <body>
    <!-- blah blah -->
  </body>
</html>
```

### 包含在head裡的標籤

* < title >：文件標題
* < meta >：文件相關資訊
* < link >：文件之間的關聯
* < style >：嵌入CSS樣式表
* < script >：JavaScript 程式碼
* < noscript >：網頁不支援 JavaScript 時的處理
* < base >：base URL

:pushpin: [英文資料參考](https://www.w3schools.com/tags/tag_head.asp)

***

### meta(metadata)

>描述 HTML 文件的元資訊，透過 meta我們可以設定很多不同類型的網頁資訊

```html
<meta charset="UTF-8">
<meta name="description" content="Free Web tutorials">
<meta name="keywords" content="HTML, CSS, JavaScript">
<meta name="author" content="John Doe">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

* meta charset 指定網頁所使用的編碼
* meta description 網頁說明
* meta keywords 網頁關鍵字
* meta author 網頁作者資訊
* meta viewport 手機行動版網頁螢幕資訊
* meta refresh 自動跳轉網頁
* meta robots 搜尋引擎標記

:pushpin: [英文資料參考](https://www.w3schools.com/tags/tag_meta.asp)
:pushpin: [中文資料參考](https://www.fooish.com/html/meta-tag.html)

***

### style

> 使用CSS樣式排版

```html
<style>
  h1 {color:red;}
  p {color:blue;}
</style>
```

#### 連結外部CSS樣式表(stylesheet)

> 需使用`<link>`

```html
<link rel="stylesheet" href="styles.css">
```

#### inline CSS

> 所有的HTML標籤都可以用style屬性來指定該HTML元素的CSS樣式

```html
<p style="color:red">This is a paragraph.</p>
```

***

## < body > 標籤

> 標籤作用是用來呈現網頁的主要內容，body裡面會再包含有不同用途和語意的HTML tags來描述和架構出網頁內容

:bulb: 主要是放使用者從螢幕上看得到的內容

```html
<!DOCTYPE html>
<html>
  <head>
    .....
  </head>
  
  <body>
    <h1>Hello world!</h1>
    <p>body 裡面會有不用的tags來描述和架構出網頁的主要內容</p>
  </body>
  
</html>
```

***

### < h1 > ~ < h6 > (heading)

> 定義 HTML 文件內容的標題，1-6 表示不同的重要程度

~~~html
<h1>apple</h1>
<h2>apple</h2>
<h3>apple</h3>
<h4>apple</h4>
<h5>apple</h5>
<h6>apple</h6>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\h內容標題.jpg)

***

### < P >文字段落 (paragraph)

> 段落`<p>`:paragraph 預設會在段落間幫你做換行和留邊距

~~~html
<p>地址：408台中市南屯區公益路二段51號18樓</p>
<p>電話：(04) 2326-5860</p>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\p段落.jpg)

***

### < br >換行

> 用做內容換行的效果，為空元素不需要結束標籤

```html
<p>To force<br> line breaks<br> in a text,<br> use the br<br> element.</p>
```

顯示結果：![](https://hackmd.io/_uploads/rkNV-iclp.jpg)

***

### < hr >分隔線(horizontal rule)

> 用來做文字段落的焦點或場景轉換，視覺效果上則是一條水平分隔線；為空元素不需要結束標籤

~~~html
<p>§1: The first rule of Fight Club is: You do not talk about Fight Club.</p>
<hr>
<p>§2: The second rule of Fight Club is: Always bring cupcakes.</p>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\hr分隔線.jpg)

***

### < div > 區塊元素

> 用來當作容器，用來包裹其他 HTML，將 HTML 文件的內容整理出不同獨立區塊，用途是方便給 CSS 做樣式排版或方便給 JavaScript做互動操作，本身沒任何特殊意義也不帶任何標籤語意

~~~html
<head>
    <style>
		.shadowbox {
  			width: 15em;
  			border: 1px solid #333;
  			box-shadow: 8px 8px 5px #444;
  			padding: 8px 12px;
  			background-image: linear-gradient(180deg, #fff, #ddd 40%, #ccc);
}
    </style>
</head>
<body>
  <div class="shadowbox">
  	<p>paragraph 1</p>
  	<p>paragraph 2</p>
  	<p>paragraph 3</p>
  </div>
</body>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\div.jpg)

- ==div 主要是用作區塊容器，如果是包裹單一行內 (inline) 的情況，則是使用span==

***

### < span >

> 主要是用作行內 (inline) 容器，用來包裹文字 (text) 或其他行內 (inline) 的 HTML；本身沒任何特殊意義也不帶任何標籤語意

~~~ html
<p>My mother has <span class="highlight">blue</span> eyes.</p>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\span.jpg)

***

### 空白字元(white space)

#### `&nbsp;`

~~~html
<body>
    cat&nbsp;dog
</body>
~~~

顯示結果：![顯示結果](D:\EEIT73\筆記\圖片\空白字元.jpg)

* `&ensp;`：半形空格
* `&msp;`：全形空格
* `&thinsp;`：窄空格

:pushpin: [HTML特殊字符編碼表](https://www.ifreesite.com/html-entities.htm)

***

### < strong > 強調重要性

> 用來強調一段內容特別的重要，瀏覽器預設的 strong 樣式會用粗體字顯示

~~~html
<p>When doing x it is <strong>imperative</strong> to do y before proceeding.</p>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\strong.jpg)  

####  < strong > 和 < b > 標籤的差異:bangbang:

`<b>` 標籤雖然也會將包裹的內容文字變成是粗體字的效果，但`<b>` 僅止於樣式的用途，標籤本身沒有任何語意，不像是 `<strong> `有==特殊語意表示內容的重要性==，所以 `<strong>  `和`<b>` 標籤對於 SEO 搜尋引擎理解網頁內容是有極大的根本性差異的。通常也會建議少用`<b>` ，如果真的想用粗體字效果的話，其實你應該使用 CSS。

***

### < pre > 預先格式化 (preformatted)

> 用來保存原始文字內容的格式，意思是文字內容中的空白、換行都會保留下來，而瀏覽器預設樣式會以等寬字型 顯示其內容

~~~html
<pre>
	cat     dog
	apple
</pre>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\pre.jpg)

***

### 項目列表清單

| 列表清單類型                | 說明                                                         |
| --------------------------- | ------------------------------------------------------------ |
| 無序列表 (unordered lists)  | `<ul>` 表示無序列表，配合 `<li>` 實現，預設使用●符號顯示     |
| 有序列表 (ordered lists)    | `<ol> `表示有序列表，`<li>`表示列表中的每一項，預設使用阿拉伯數字編號 |
| 定義列表 (definition lists) | `<dl>` 與`<dt>`、`<dd>` 配合實現，`<dt>` 充當清單的標題，`<dd>` 是對 `<dt>` 的解釋說明 |

***

#### < ul > 無序列表 (unordered lists)

> 表示無順序的列表清單；``<ul>`` 作為列表的容器 (container)，而用 `<li>` 來描述個別的項目內容

~~~html
<ul>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\ul.jpg)

:bulb: `<ul>`一般和`<li>`一起使用，不會單獨出現；`<ul>`下一層只能放`<li>`，但是`<li>`下面可以放其他元素

##### 改變項目符號的圖示

list-style-type=" ==● disc==、==○ circle==、==■ square==、==none== "

~~~html
<ul style="list-style-type":這邊選擇你想要的圖示;>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>
~~~

***

#### < ol > 有序列表 (ordered lists)

>表示有順序的列表清單；`<ol>` 作為列表的容器，而用`<li> `來描述個別的項目內容

~~~ html
<ol>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ol>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\ol.jpg)
:bulb: `<ol>`一般和`<li>`一起使用，不會單獨出現；`<ol>`下一層只能放`<li>`，但是`<li>`下面可以放其他元素

##### 改變編號類型

type=" ==ABC==、==i ii iii== "
start=" ==567...== " (從<font color="red">中間</font>數字開始)

***

#### 定義列表 (definition lists)

> `<dl>` 標籤用於建立定義清單。 它是由定義標題和定義描述兩部分組成的，而且至少要包含一條定義標題或定義描述  

~~~html
<dl>
  <dt>Denim (semigloss finish)</dt>
  <dd>Ceiling</dd>
  <dt>Denim (eggshell finish)</dt>
  <dt>Evening Sky (eggshell finish)</dt>
  <dd>Layered on the walls</dd>
</dl>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\dl.jpg)

:bulb: `<dl>`一般和`<dt>`、`<dd>`一起使用，不會單獨出現

***

### < a > 超連結(hyperlink)

> 建立超連結 (hyperlink) -- 通往其他頁面、檔案、Email 地址、或其他 URL 的超連結

#### href 

- 指定一個 URL 看連結要連到哪邊

~~~html
<a href="http://www.google.com/">Google首頁</a>
~~~

#### target

- 指定在什麼地方打開連結
  - `_self:`預設值，在當前視窗開啟
  - `_blank:` 在新視窗開啟
  - `_parent:`在上一層父視窗開啟
  - `_top:`在最頂層父視窗開啟

~~~html
<a href="https://www.google.com/" target="_self">當前視窗開啟</a>
<a href="https://www.google.com/" target="_blank">新視窗開啟</a>
<a href="https://www.google.com/" target="_parent">上一層父視窗開啟</a>
<a href="https://www.google.com/" target="_top">最頂層父視窗開啟</a>
~~~

:pushpin: 其餘屬性查詢：[中文資料](https://www.fooish.com/html/hyperlink-a-tag.html)、[英文資料](https://www.w3schools.com/tags/tag_a.asp)

***

#### 連結錨點

> 連結至網頁內元素 (#id)

~~~html
<body>
    <a href="#apple">跳到章節</a>
    
    <h3 id="apple">章節標題</h3>
</body>
~~~

點擊後，會跳到id為apple的元素區塊

***

### < img > (images)

> 在html文件中加入圖片，搭配`src`屬性來指定圖片位址

~~~html
<img src="圖片位址">
~~~

| 屬性   | 說明                                                     |
| ------ | -------------------------------------------------------- |
| src    | 指定圖片位址，為必需屬性                                 |
| alt    | 圖片替代文字，當圖片無法顯示時，瀏覽器會顯示此文字       |
| title  | 可以指定一段文字，在當滑鼠滑過圖片時，會自動顯示這段文字 |
| width  | 圖片寬度像素                                             |
| height | 圖片高度像素                                             |

***

### < video >

> 嵌入影片檔案

~~~html
<video src="影片位址" control></video>
~~~

| 屬性     | 說明                                                         |
| -------- | ------------------------------------------------------------ |
| control  | 控制面板                                                     |
| loop     | 循環播放                                                     |
| muted    | 設置靜音                                                     |
| autoplay | 自動播放 :bulb:必須先設置靜音muted，才可以設置autoplay<br>https://developer.chrome.com/blog/autoplay |
| poster   | 影片封面圖片                                                 |

***

### < table > 表格

> `<table>` 標籤做為表格的容器，裡面有不同用途的標籤像是 `<tr>`,` <td>` 組成一個完整的表格

- `<tr>`：列
- `<td>`：欄
- `<th>`：欄位標題

![](C:\Users\a1358\OneDrive\EEIT73\筆記\圖片\表格table.jpg)

#### 使用`<tr>`跟`<td>`

~~~html
<table>
  <tr>
    <td>國家</td>
    <td>首都</td>
    <td>人口</td>
    <td>語言</td>
  </tr>
  <tr>
    <td>USA</td>
    <td>Washington D.C.</td>
    <td>309 million</td>
    <td>English</td>
  </tr>
  <tr>
    <td>Sweden</td>
    <td>Stockholm</td>
    <td>9 million</td>
    <td>Swedish</td>
  </tr>
</table>
~~~

網頁顯示效果：![](D:\EEIT73\筆記\圖片\table.jpg)

####　使用`<tr>`跟`<th>` 、`<td>`

~~~html
<table>
  <tr>
    <th>國家</th>
    <th>首都</th>
    <th>人口</th>
    <th>語言</th>
  </tr>
  <tr>
    <td>USA</td>
    <td>Washington D.C.</td>
    <td>309 million</td>
    <td>English</td>
  </tr>
  <tr>
    <td>Sweden</td>
    <td>Stockholm</td>
    <td>9 million</td>
    <td>Swedish</td>
  </tr>
</table>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\th.jpg)

***

#### 合併儲存格

> 可利用`:colspan`(水平合併)、`:rowspan`(垂直合併)這兩種屬性來合併儲存格

![](C:\Users\a1358\OneDrive\EEIT73\筆記\圖片\合併儲存格.jpg)

##### rowspan 垂直合併

~~~html
<td rowspan="要合併幾個橫列"></td>
~~~

**範例**：

~~~html
<table>
  <tr>
    <th>項目</th>
    <th>金額</th>
    <th>總金額</th>
  </tr>
  <tr>
    <td>iPhone 11</td>
    <td>$24,900</td>
    <td rowspan="2">$31,390</td>
  </tr>
  <tr>
    <td>AirPods</td>
    <td>$6,490</td>
  </tr>
</table>
~~~

網頁顯示效果：![](D:\EEIT73\筆記\圖片\rowspan.jpg)

##### colspan 水平合併

~~~html
<td colspan="要合併幾個直行"></td>
~~~

**範例**：

~~~html
<table>
  <tr>
    <th>項目</th>
    <th>金額</th>
  </tr>
  <tr>
    <td>iPhone 11</td>
    <td>$24,900</td>
  </tr>
  <tr>
    <td>AirPods</td>
    <td>$6,490</td>
  </tr>
  <tr>
    <td colspan="2">總金額: $31,390</td>
  </tr>
</table>
~~~

網頁顯示效果：![](D:\EEIT73\筆記\圖片\colspan.jpg)

***

### < form > 表單

> 建立一個html表單容器

| 屬性         | 說明                                                         |
| ------------ | ------------------------------------------------------------ |
| action       | 用來指定一個位址 告訴瀏覽器當 user 按送出表單後，要將表格的內容送去哪邊 |
| method       | 用來指定資料傳輸時用的 HTTP 協議，最常用的是 `get` 或 `post` |
| target       | 用來指定瀏覽器要在何處顯示表單送出後伺服器回應的結果         |
| autocomplete | 指示這個表單中的欄位是否啟用瀏覽器自動完成機制               |

**範例**：建立了一個表單，且宣告這個表單的資料會被用 http post 的方法送到 "/formprocess.php" 

~~~html
<form action="/formprocess.php" method="post">
  
  <!-- ....表單 HTMLs .... -->
  
</form>
~~~

:pushpin: [常見表單元素屬性](https://www.fooish.com/html/form.html)

#### 常用表單元素

##### < label > 表單欄位標題

> 用來給表單的控制元件一個說明標題，可以搭配 <label> 的像是 input, textarea, select, button, meter, output, progress 這些表單元件

**範例**：

~~~html
<div>
    <label>Do you like cheese?</label>
    <input type="checkbox">
</div>
<div>
    <label>Do you like peas?</label>
    <input type="checkbox">
</div>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\label.jpg)

##### label常用屬性

###### for

> 將 for 的屬性值設定為某表單元件的 `id` 值，用來增加表單元件的可點擊範圍

**範例**：

~~~html
<label for="emailadd">Email address: </label>
<input type="email" name="emailadd" id="emailadd">
~~~

***

##### < input >

> HTML 表單裡最重要也最特別的元素，根據類型屬性的設定轉換成不同的輸入型態，與使用者互動並讓使用者輸入資料

###### Type 類型

~~~html
<input type="輸入類型">
~~~

| Type     | 說明                                        |
| -------- | ------------------------------------------- |
| text     | 文字輸入欄位 ( 預設值 )                     |
| radio    | 單選選單的選項                              |
| checkbox | 多選選單的選項                              |
| submit   | 送出按鈕，等同 type 為 submit 的 `<button>` |
| button   | 按鈕，等同 type 為 button 的 `<button>`     |

:pushpin: [其餘type查詢](https://steam.oxxostudio.tw/category/html/tags/input.html#a3)

###### 屬性

- name：欄位名稱，用來指定送出的資料要用什麼名稱，讓遠端伺服器透過定義好的名稱去取相對應的欄位值

~~~html
<input name="myfield">
~~~

上述範例想像當表單送出時，這個欄位會以類似 "myfield=輸入內容" 的形式傳給遠端伺服器

- value：指定初始值

~~~html
<input value="我的初始值">
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\value.jpg)

:pushpin: [其餘屬性查詢](https://www.fooish.com/html/input-tag.html)

***

##### < select > 下拉式選單

> 用來建立下拉式選單，讓使用者可以從一堆選項中選擇出一個或多個選項

- 本身做為選單的容器，在 select 裡面用 `<option>` 標籤來建立個別選項

~~~html
<select>
    <option>請選擇你最愛的寵物</option>
    <option>Dog</option>
    <option>Cat</option>
    <option>Hamster</option>
    <option>Parrot</option>
    <option>Spider</option>
    <option>Goldfish</option>
</select>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\select.jpg)

| 屬性     | 說明                   |
| -------- | ---------------------- |
| name     | 聲明欄位名稱           |
| disabled | 將欄位設定為禁用的狀態 |
| required | 將欄位設定為必填       |

***

##### < option > 

> 用來建立選項，而選項內容放在 `<option></option>` 標籤裡面

| 屬性     | 說明                                                         |
| -------- | ------------------------------------------------------------ |
| value    | 指定選了該選項，表單要傳送該值給遠端伺服器，若沒設定 value，預設是傳 `<option>` 的內容 |
| selected | 設定預先選取此選項                                           |
| label    | 說明選項的含義，有設定時會被瀏覽器顯示為選項內容             |
| disabled | 將選項設定為不可選的狀態                                     |

**範例**：

~~~html
<select name="pets">
    <option value="">請選擇你最愛的寵物</option>
    <option value="dog">Dog</option>
    <option value="cat" selected>Cat</option>
    <option value="hamster">Hamster</option>
    <option value="parrot">Parrot</option>
    <option value="spider" disabled>Spider</option>
    <option value="goldfish">Goldfish</option>
</select>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\option.jpg)

***

##### < optgroup > 選項分區

> 用來將同樣性質的選項分區來顯示，而在`<optgroup>`上有一個 `label` 屬性是用來設定該分區的名稱

**範例**：

~~~html
<select name="catordog">
  <optgroup label="Cats">
    <option>Tiger</option>
    <option>Leopard</option>
    <option>Lynx</option>
  </optgroup>
  <optgroup label="Dogs">
    <option>Grey Wolf</option>
    <option>Red Fox</option>
    <option>Fennec</option>
  </optgroup>
</select>
~~~

顯示結果：![](D:\EEIT73\筆記\圖片\optgroup.jpg)

***

##### < datalist > input 欄位自動完成，輸入資料選擇清單

>用來建立一組資料清單和`input`欄位結合，在`input`欄位會出現一個下拉選單，提供使用者從資料清單中直接選擇一個值

**範例**：

~~~html
<label for="food">請輸入喜歡的食物:</label>
    <input list="foodlist" type="text" id="food" name="food">
    <datalist id="foodlist">
        <option value="麥當勞">
        <option value="肯德基">
        <option value="漢堡王">
    </datalist>
~~~

顯示結果：![](C:\Users\a1358\OneDrive\EEIT73\筆記\圖片\datalist.jpg)

:bulb: 當使用者一邊在`<input>`輸入框中打字時，瀏覽器也會自動過濾只出現`datalist`中符合字串的`option`

***

### < fighre > 引用區塊

> 用來引用任何內容像是文字段落、圖片、圖表或程式碼片段等；`<figcaption>` 則是該引用區塊的標題

~~~html
<figure>
  <figcaption>《春曉》作者：孟浩然</figcaption>
  春眠不覺曉，處處聞啼鳥。夜來風雨聲，花落知多少。
</figure>
<figure>
  <figcaption>《夜思》作者：李白</figcaption>
  床前明月光，疑是地上霜。舉頭望明月，低頭思故鄉。
</figure>
~~~

顯示結果：![](C:\Users\a1358\OneDrive\EEIT73\筆記\圖片\figure.jpg)

***

### 引用文字

> 使用以下元素來引用段落文字

| 引用文字元素 | 說明                                                 |
| ------------ | ---------------------------------------------------- |
| blockquote   | 引用比較多的文字，使用後獨立一個區塊呈現             |
| q            | 引用較少的文字，使用後會自動替文字的左右邊加上雙引號 |
| cite         | 表示引用內容的標題，使用後會自動將文字改成斜體       |

~~~html
<p>
  <cite>唐詩三百首</cite> <q>作者李白</q>
  <br>
  床前明月光，疑是地上霜，舉頭望明月，低頭思故鄉。
</p>
<p>
  <blockquote>
  <cite>唐詩三百首 作者李白</cite>
  <br>
  床前明月光，疑是地上霜，舉頭望明月，低頭思故鄉。
  </blockquote>
</p>
~~~

顯示結果：![blockquote](C:\Users\a1358\OneDrive\EEIT73\筆記\圖片\blockquote.jpg)

***

