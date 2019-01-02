# python을 활용한 인터넷 크롤링

## 두번째 시간

### 파이썬 코드작성

```python
#동시에 여러개의 인터넷 창을 검색할 경우
import webbrowser
q_list =["bts","아이유","블랙핑크","위너"]
url = "https://google.com"
url = "https://www.google.com/search?&q="

for q in q_list:
    webbrowser.open(url+q)
```

```python
#파일이름 변경하는 방법
import os
#import glob

os.chdir(r'C:\Users\student\nokgu\SSAFY지원자')

for filename in os.listdir("."):
    new_filename = filename.replace("SAMSUNG_","SSAFY_")
    os.rename(filename, new_filename)
```

```python
#환율정보에 관해 크롤링한 코드
import requests
from bs4 import BeautifulSoup

url = "http://m.exchange.daum.net/mobile/exchange/exchangeMain.daum"
res = requests.get(url).text
soup = BeautifulSoup(res,'html.parser')
song = soup.select('table.dtable.clr tbody tr')

for songs in song :
    print(songs.select_one('td:nth-of-type(1) a').text,end=" ")
    print(songs.select_one('td:nth-of-type(2)').text)
    
```

```python
#벅스 음악 차트 크롤링
import requests
from bs4 import BeautifulSoup

url = "https://music.bugs.co.kr/chart"
res = requests.get(url).text
soup = BeautifulSoup(res,'html.parser')
song = soup.select('table.list.trackList.byChart tbody tr')
for songs in song :
    print(songs.select_one('th:nth-of-type(1) p a').text)
    print(songs.select_one('td:nth-of-type(5) p a').text)
    

```





