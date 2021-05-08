# Django_prj

[Django DOCS](https://docs.djangoproject.com/en/3.2/)  
[Youtube Python Django Tutorial 2020 - Full Course for Beginners](https://www.youtube.com/watch?v=JT80XhYJdBw)  
語系設定
setting.py
LANGUAGE_CODE = 'zh-hant'
TIME_ZONE = 'Asia/Taipei'

cmd 
python manage.py runserver  
python manage.py startapp polls  
python manage.py makemigrations polls 建立Models裡面的資料庫  
python manage.py sqlmigrate polls 0001  
python manage.py migrate  
python manage.py shell  開啟資料庫管理CMD  
python manage.py createsuperuser  



01. 安裝Django套件  
$ conda create --name django  
$ activate django  
$ cd prj資料夾  
$ conda install django  #安裝django預設模組  
$ django-admin startproject testsite  #建立網站資料夾  
$ cd 網站資料夾  
$ python manage.py migrate  #創建數據庫  
$ python manage.py runserver  
  127.0.0.1:8000/  ＃預設網址  
  修改語系 testsite/testsite/settings.py  
  LANGUAGE_CODE = 'zh-hant'
  TIME_ZONE = 'Asia/Taipei'
02.  建立網頁code資料夾  
$ python manage.py startapp polls  
  修改polls/view.py, 新增polls/urls.py  寫入url路徑  
  修改testsite/urls.py,  寫入url路徑  
  path()有四個參數, 第一參數 route, 第二參數 view, 第四參數 name(以name直接指定網址)  
03.  建立網頁用資料庫  
  修改polls/models.py  建立資料庫欄位  
  修改testsite/settings.py INSTALLED_APPS 新增 'polls.apps.PollsConfig',  
$ python manage.py test  自動檢測資料庫欄位設定  
$ python manage.py makemigrations polls  創建資料庫  
  django會自動建立 migrations資料夾, 並登記資料庫變更紀錄  
$ python manage.py migrate  承認變更交易  
$ python manage.py shell  進入資料庫 cmd  
cmd
> from pools.models import User, Message
  新增資料庫資料  
  modelClass.objects.filter(條件)  查詢操作,取得ClassSet  
  modelClass.objects.get(條件)  查詢操作，只取第一個  
  pk=1 ; primaryKey = 1  
> msg = Message(msg='Hellow!', sender=usr)  
> usr = User.objects.get(pk=1)  
