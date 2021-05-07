# Django_prj

[Django DOCS](https://docs.djangoproject.com/en/3.2/)  
[Youtube Python Django Tutorial 2018 for Beginners](https://www.youtube.com/playlist?list=PL-J2q3Ga50oOpni_xS2PPUe4mf9lM96dD)  
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
% conda create -n django  
% activate django  
% cd prj資料夾  
% conda install django  #安裝django預設模組  
% django-admin startproject testsite  #建立網站資料夾  
% cd 網站資料夾  
% python manage.py migrate  #創建數據庫  
% python manage.py runserver  
# http://127.0.0.1:8000/  ＃預設網址  



