

![[Recording 20230111155344.webm]]

```text
{:height="50%" width="50%"}
```




==字体大小==  ==回复退还甲方==

 ![[QQ图片20230108184607.jpg|175]]

| test1  | test2  | test3 | fsdfdsf |
|:------:|:------:|:-----:|:-------:|
| sadsad |  sff   | wfewf |  scsdc  |
| wfwef  | wfesfg | efefe | sdvcsd  |


```python
import requests  
import random  
from lxml import etree  
header = {  
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/108.0.0.0 Safari/537.36 Edg/108.0.1462.54'  
}  
url = 'https://www.pearvideo.com/category_5'  
urls = []  
page_text = requests.get(url=url, headers=header).text  
tree = etree.HTML(page_text)  
li_list = tree.xpath('//ul[@id="listvideoListUl"]/li')  
for li in li_list:  
    detail_url = 'https://www.pearvideo.com/' + li.xpath('./div/a/@href')[0]  
    name = li.xpath('./div/a/div[2]/text()')[0] + '.mp4'  
    print(detail_url, name)  
    contId = re.findall('_(.*)', detail_url)[0]  
    # print(contId)  
    mrd = random.random()  
    params = {  
            "contId": contId,  
            "mrd": mrd  
    }  
    video_url = "https://www.pearvideo.com/videoStatus.jsp"  
    header["Referer"] = detail_url  
    video_response = requests.get(url=video_url, headers=header, params=params).text  
    # print(video_response)  
    fake_video_url = re.findall('"srcUrl":"(.*?)"', video_response)[0]  
    # print(fake_video_url)  
    url1 = re.findall('https://.*?/.*?/.*?/.*?/(.*?)-', fake_video_url)[0]  
    real_video_url = re.sub(url1, 'cont-' + contId, fake_video_url)  
    print(real_video_url)  
    dic = {  
        'name': name,  
        'url': real_video_url  
    }  
    urls.append(dic)
```

```C++
#include "iostream"
using namespace std;
int main(){
}
```



## 一些问题

#### 如何快速对数组全体元素赋0？

for循环遍历赋值，但...似乎可以更简便

可以使用`void *memset(void *str, int c, size_t n)` 函数

- <mark style="background: #D2B3FFA6;">解释</mark>：复制字符 c（<mark class="hltr-yellow">一个无符号字符</mark>）到参数 str 所指向的字符串的前 n 个字符
- <mark style="background: #FFB86CA6;">作用</mark>：是在一段内存块中填充某个给定的值，它是对较大的结构体或数组进行清零操作的一种最快方法
- <mark style="background: #FFF3A3A6;">头文件</mark>：C中`#include<string.h>` ，C++中`#include<cstring>`

#dsfdf #dsvsdv #vsdvsvfd #egfesgrg #thtyhj

> vsdvfdvd
> sdvsvsdvf
> dvdfbdfb

$$
W_{t, d}=\left(1+\log tf_{t, d}\right) \cdot \log \frac{N}{d f_{t}}
$$
$$
\begin{aligned}
A & =d R+\left[\frac{(1-d)}{N}\right] e e^{T} \\
& =0.85\left[\begin{array}{ccc}
0 & 0 & 0 \\{\color{Blue} } 
0.5 & 0 & 1 \\
0.5 & 1 & 0
\end{array}\right]+0.05\left[\begin{array}{ccc}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{array}\right] \\
& =\left[\begin{array}{ccc}
0.05 & 0.05 & 0.05 \\
0.475 & 0.05 & 0.9 \\
0.475 & 0.05 & 0.05
\end{array}\right]
\end{aligned}
$$


```ad-check
title: Check_test
这是一个注意框

```

```ad-tip
title: Tip_test
collapse: open
<mark style="background: #ABF7F7A6;">这是一个注意框</mark>

```

> [!abstract]+ Abstract_test
> 这是一个测试框


