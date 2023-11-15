# :desktop_computer: 112-1 師大科技系程式語言
* <em><strong>姓名：李騰騏
* 系級：科技系2年級 
* 授課教師：蔡芸琤老師</strong></em>
# :file_folder: 筆記  
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
HW3的內容通過網路上的教學內容輔助完成，順序為解析首頁，翻頁，解析五頁  
其參考連結為[此](https://www.youtube.com/watch?v=O6h1csENqBc)  
>[#HW4](https://medium.com/@mason45ok/程式語言-文字雲-d06b582c15a3)  
>[#HW5](https://medium.com/@mason45ok/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80-voyant-facf2326d74c)
