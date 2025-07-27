##  112-1 師大科技系程式語言
* <em><strong>姓名：李騰騏
* 授課教師：蔡芸琤老師</strong></em>
---
### 介紹：在PL的課程中，會利用Python 進行一些簡易的資料分析，通過網路蒐集資料集(以CSV file為主)，回答每周在程式碼中的內容。
* [HW1](https://github.com/mason45ok/PL-Repo/tree/main/HW1) - 為台灣及日本在人口紅利上的分析，通過對GDP及人口的疊圖，使之能夠直觀觀察人口對比及兩者的GDP對比 - 日本GDP與人口紅利的關聯較小
* [HW2](https://github.com/mason45ok/PL-Repo/tree/main/HW2) - 在探討預期壽命與GDP的關聯性，由於預期壽命通常與醫療水平、經濟情況的內容有關，同時又正好於COVID-19疫情有關，所以藉此分析GDP與預期壽命關聯性 - GDP可以當作預期壽命的參考因素
* [HW3](https://github.com/mason45ok/PL-Repo/tree/main/HW3) - 從HW3開始加入Python的爬蟲內容，通過簡易練習開始(PTT的網頁爬蟲)，通過網頁爬蟲可以更快速的抓取網路上的資料，並快速整理成資料集
* [HW4](https://medium.com/@mason45ok/程式語言-文字雲-d06b582c15a3) - HW4為資料視覺化，通過點雲的使用，可以更快的抓取文中重點，此次以俄烏戰爭中，俄方受到的制裁，維基百科頁面來爬蟲與整理，通過資料正則化可以擋下許多餘字詞及連接詞
* [HW5](https://medium.com/@mason45ok/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80-voyant-facf2326d74c) - 練習哈利波特文本，通過自動詞庫進行正則化 (詞庫：nltk)
* [Final - Project](https://github.com/PLRepo-FP/PLRepo-FP) - 課程的期末專題 - 花語爬蟲抓取與網頁demo (Made with Figma)
---
#### :file_folder: 筆記  
若要在Python中抓取網頁資料並用BeautifulSoup解析:  
```
import requests
from bs4 import BeautifulSoup
url = "your url right here"
headers = {
    "user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
}

res = requests.get(url, headers=headers)
soup = BeautifulSoup(res.text, "html.parser")
```
若要進行資料正則化:  
```
import re

# 將 ResultSet 轉換為字符
text = "\n".join([content.get_text() for content in contents])

# 使用正則表達式去除不需要的内容
# 不需要的內容在chars_to_replace中目前為:的 和 在 日 月 對 年
chars_to_replace = r"的|和|在|日|月|對|年"
cleaned_text = re.sub(r'[A-Za-z!@#$%^&*()_+{}[\]:;"\'<>,.?~\\/\-|=]', '', text)
cleaned_text = re.sub(chars_to_replace, '', cleaned_text)
cleaned_text = re.sub(r'\s+', '', cleaned_text)
```
# :page_facing_up: 作業繳交區  
>[#HW0-TEST](https://github.com/mason45ok/PL-Repo/tree/main/PL-test-set)  
>[#HW1](https://github.com/mason45ok/PL-Repo/tree/main/HW1)  
>[#HW2](https://github.com/mason45ok/PL-Repo/tree/main/HW2)  
>[#HW3](https://github.com/mason45ok/PL-Repo/tree/main/HW3)  
>HW3的內容通過網路上的教學內容輔助完成，順序為解析首頁，翻頁，解析五頁  
>其參考連結為[此](https://www.youtube.com/watch?v=O6h1csENqBc)  
>[#HW4](https://medium.com/@mason45ok/程式語言-文字雲-d06b582c15a3)  
>[#HW5](https://medium.com/@mason45ok/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80-voyant-facf2326d74c)
