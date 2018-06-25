---
layout: post
#标题
title:  Python Web常见的框架
#时间配置
date:   2018-05-08 16:03:31 +0800
#大类配置
categories: 知识
#小类配置
tag: python
---
 
* content
{:toc} 

### 相关链接
---

* <a href="https://www.djangoproject.com/" target="_blank">Django：全能型Web框架</a><br>
* <a href="http://webpy.org/" target="_blank">web.py：一个小巧的Web框架</a><br>
* <a href="http://bottlepy.org/" target="_blank">Bottle：和Flask类似的Web框架</a><br>
* <a href="http://www.tornadoweb.org/" target="_blank">Tornado：Facebook的开源异步Web框架</a><br>





### Flask相关示例
---

```python
from flask import Flask
from flask import request

app = Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def home():
    return '<h1>Home</h1>'

@app.route('/signin', methods=['GET'])
def signin_form():
    return '''<form action="/signin" method="post">
              <p><input name="username"></p>
              <p><input name="password" type="password"></p>
              <p><button type="submit">Sign In</button></p>
              </form>'''

@app.route('/signin', methods=['POST'])
def signin():
    # 需要从request对象读取表单内容：
    if request.form['username']=='admin' and request.form['password']=='password':
        return '<h3>Hello, admin!</h3>'
    return '<h3>Bad username or password.</h3>'

if __name__ == '__main__':
    app.run()
```

### Django的使用
---

```ruby
$ pip3 install django
```

![IMAGE]({{ site.img_url }}6B4B3A8D802FCC1764BAD5BFC8DEA0EE.jpg)
