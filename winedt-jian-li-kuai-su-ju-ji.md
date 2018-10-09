# WinEdt建立快速巨集

## 介紹

**主要重點**

* 為了讓BibTex可以編譯需要先執行一次XeLaTex
* 要執行兩次 XeLaTex目錄才會正確

所以執行步驟為

> XeLaTex -&gt; BibTex -&gt;  XeLaTex-&gt;  XeLaTex

下面介建立快速巨集的方法

## 設定步驟

1. 主頁面上打開Options-&gt;Options Interface
2. 打開按鈕設定檔Menu and Toolbar -&gt; Main Menu
3. 搜尋**`MENU="TeX_Menu"`**
4. 新增以下按鈕，貼在
5.   {% code-tabs %}
   {% code-tabs-item title="MainMenu.ini" %}
   ```text
   MENU="TeX_Menu"
     CAPTION="Te&X"
     CONFIG_FILTER="Default;MiKTeX;TeX Live"
     // ===========以下為新增內容===========
     ITEM="ButtonByAustin"
       CAPTION="MacroByAustin"
       IMAGE="MacroRun"
       SAVE_INPUT=1
       MACRO="Exe('%b\Exec\TeX\XeLaTeX.edt');Exe('%b\Exec\TeX\BibTeX.edt');Exe('%b\Exec\TeX\XeLaTeX.edt');Exe('%b\Exec\TeX\XeLaTeX.edt');Exe('%b\Exec\PDF\PDF Preview.edt');"
       REQ_FILTER=:"%!M=TeX"|"%!M=TeX:STY"|"%!M=TeX:AUX"    
   ```
   {% endcode-tabs-item %}
   {% endcode-tabs %}

6. 新增好後，先儲存\(Ctrl + S\)，在使用\(Ctrl + Shift + F9\)更新介面
7. 以後可以使用`MacroByAustin`按鈕進行所有編譯動作 

{% hint style="info" %}
記得要開啟tex檔案才能按鈕才能使用
{% endhint %}

![](.gitbook/assets/image%20%2820%29.png)



設定好後以後不用再分四次按，只要按一次就可以了

