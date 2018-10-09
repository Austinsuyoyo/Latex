---
description: 為了解決PDFCloseDoc.edt裡面版本錯誤的問題，有了以下簡單的解決方法
---

# 解決PDF不能自動關掉問題

如1果無法自動關閉PDF並遇到下列BUG的訊息，可以嘗試本篇解決方法

![](../.gitbook/assets/image%20%2812%29.png)

1. Options -&gt; Execution Modes
2. 從PDF Viewer頁面下面找到Adobe DDE Service Blues欄位
3. 如果是用Adobe Acrobat Reader DC 2018版的請改成**AcroviewR18\(其餘需要自己搜尋\)**

![](../.gitbook/assets/image%20%281%29.png)

改好後，如果編譯前有打開PDF，軟體會自動幫你關掉。



