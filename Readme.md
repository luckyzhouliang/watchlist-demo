# Flask 入门实践

**目标**:开发一个简单的Watchlist程序

## 准备工作

### 使用git

`git init`

`vim .gitignore`

`git remote add origin git@github.com:...`

### 创建虚拟环境

**venv模块**

创建`python3 -m venv env`

激活`. env/bin/activate`

退出`deactivate`

### 安装Flask

`pip install flask`

更新`pip install -U flask` 

### 提交改动

```bash
git add .
git commit -m 'Ready'
git push -u origin main
```

## Hello Flask

### 修改视窗函数名称

url_for(endpoint),返回视窗函数对应的url

### 环境变量

FLASK_APP:文件名不为app.py时修改

FLASK_DEBUG:1为调试模式

### URL规则

传入变量`'/user/<name>'`...

## 模板

### 模板语法

`{{...}}`变量

`{%...%}`语句

`{#...#}`注释

`{{变量|过滤器}}`

### 渲染主页模板

`render_template()`

## 静态文件

对应模板文件,不需要动态生成.ex:图片,CSS文件,JavaScript脚本

### 生成静态文件url

在html文件中,引入静态文件需要给出资源所在url

`url_for('static',filename='')`

html中无需导入url_for,存在上下文环境

### 添加Favicon

```html
<link rel="icon" href="{{ url_for('static',filename='images/favicon.ico') }}">
```

### 添加CSS

```html
<link rel="stylesheet" href="{{url_for('static',filename='style.css')}}" type="text/css">
```

增加对应的class属性关联



