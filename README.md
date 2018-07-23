# flying


#### 项目介绍
框架使用Flask, 前端使用jinja2模版+layui,其余多使用flask三方库,例如flask-pymongo,flask-login,flask-mail等
实现功能有:注册(邮件激活)登录、发帖、回帖、点赞、回复、采纳、删帖等功能
数据库: mongodb
架构设计: MTV



#### 项目使用

git clone https://github.com/wylycool/flying.git

需要安装mongodb和redis
同时邮箱需要设置smtp服务器和账号授权码

pip install -r requirements.txt  可以安装项目所需的包

python3 manage.py runserver -d -r
```

#### 使用说明

首次打开会自动往MongoDB新增一些默认数据（管理员账号和默认配置项），后台管理（flask-admin简单实现）: http://127.0.0.1:5000/admin

全局函数：

    1）get_page(collection_name, pn=1, size=10, sort_by=None, filter1=None) 分页查询 pn页码 sort_by为tuple类型，目前只支持单字段排序
    2）get_list(collection_name, sort_by=None, filter1=None, size=None) 列表查询
    3）find_one(collection_name, filter1=None) 获取单条
    4）date_cal(d1, num, is_add=True) 计算日期
