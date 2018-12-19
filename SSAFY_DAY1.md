

# SSAFY_DAY1

## 첫번째 시간

### 파이썬 코드작성

```python
import random

# 1. menu 리스트를 만들어주세요.
menu = ['영암매력한우수완점','신전떡볶이 광주수완점','양동통닭','광주식당','회마켓','원조나주곰탕50년']

choice = random.choice(menu)
print(choice)

phonebook = {'영암매력한우수완점':'062-383-8118',
            '신전떡볶이 광주수완점':'062-956-2334',
             '양동통닭':'062-471-9277',
             '광주식당':'062-962-8284 ',
             '회마켓':'062-952-2026',
             '원조나주곰탕50년':'062-951-3255'
            }
print(phonebook[choice])
```

```python
import requests
from bs4 import BeautifulSoup
url = 'http://openapi.airkorea.or.kr/openapi/services/rest/ArpltnInforInqireSvc/getCtprvnRltmMesureDnsty?serviceKey=' + key + '&numOfRows=10&pageSize=10&pageNo=1&startPage=1&sidoName=%EA%B4%91%EC%A3%BC&ver=1.3'
request = requests.get(url).text
soup = BeautifulSoup(request,'xml')
dong = soup('item')[7]
location = dong.stationName.text
time = dong.dataTime.text
dust = int(dong.pm10Value.text)

print("{0} 기준 {1}의 미세먼지 농도는 {2}입니다.".format(time,location,dust))

if(dust>150):
  print("매우나쁨!!!마스크 쓰세요!!!")
elif(80 < dust <= 150):
  print("나쁨!!알아서쓰세요!!")
elif(30 < dust and dust <= 80):
  print("보통!!!")
else :
  print("좋음!!")
  
```

```python
#로또
import random
numbers = range(1,46)
a = random.sample(numbers,6)
print(a)
```

```python
#반복구문
greeting = "bonjour"
print(greeting)
print(greeting)
print(greeting)
print(greeting)
print(greeting)
```

