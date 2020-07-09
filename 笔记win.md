# 用 virtualenv 管理开发环境：

1.  pip install virtualenv
    F:
    mkdir Development
    cd Development
    mkdir myproject
    cd myproject

        virtualenv venv
        venv\Scripts\activate
        venv\Scripts\deactivate.bat
        pip install django

git init

git remote add origin git@github.com:
git add .
git commit -m "from wins"
git push -u origin master
git log

pip freeze > requirements.txt
pip install -r requirements.txt

2.  开始新的项目
    django-admin startproject \<项目名称>\
    python manage.py runserver

3.  Django Apps
    app 和 project 是 Django 里两个重要的概念
    app 通常由 models (database tables), views, templates, tests 组成
    project 则包含这些 apps 和配置（configuration）
    python manage.py startapp \<app 名称>\

4.  将新创的 App 加入 setting.py 中的 INSTALLED_APPS

5.  在 Apps（boards）文件 views.py 中编辑网页将要展示的内容（非 template）
    from django.http import HttpResponse

        def home(request):
            return HttpResponse('Hello, World!')

    然后在 urls.py 中提供对应的 urlpatterns
    from django.conf.urls import url
    from boards import views

        urlpatterns = [
            url(r'^$', views.home, name='home'),
            url(r'^admin/', admin.site.urls),
        ]

6.  创建 superuser
    python manage.py createsuperuser

github ssh
ssh-keygen -t rsa -b 4096 -C "yujiangdong8@gmail.com"
(/c/Users/Yu Jiangdong/.ssh/id_rsa):
eval \$(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
clip < ~/.ssh/id_rsa.pub

pip freeze > requirements.txt
pip install -r requirements.txt
