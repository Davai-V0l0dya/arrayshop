Создание виртуальной среды
python - m venv env/arrayshop
установка джанго
pip instal django
создание админа
python manage.py createsuperuser
запуск сервера
python manage.py runserver

чеки отправляются через smtp метод, который может завершиться ошибкой или получать задержки
Поэтому для снижения нагрузки на сервер используется celery b rabbitmq
pip instal celery

В терминал
docker pull rabbitmq
создание контейнера в докере
docker run -it rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:management

guest\guest

celery -A arrayshop worker -l info

платежный шлюз на stripe
pip install stripe
Stormcaller2007@yandex.ru

для проверки запросов к stripe используется перхватчик
в терминале переходим в папку где скачан файл со страйпа
srtipe login
вводим код с почты
stripe listen --forward-to localhost:8000/payment/webhook/
получаем секрет кей для вх


для печати чеков 
pip instal weasyprint

MSYS2
pacman -S mingw-w64-x86_64-pango

gtk3runtime

для рекомендаций 
pip instal redis

docker pull redis
docker run -it --name redis 6379:6379 redis

python manage.py shell
from shop.models import Product
qp = Product.objects.get(name='имя товара')
from shop.recommender import Recommender
r = Recommender()
r.products_bought([qp,wp]) - можно менять  переменные метсами или добавить новые чекрез запятую

gettext
xgettext --version

(django admin makemessages \ compilemessages)

pip install rosetta
pip install djangocms-rosetta

pip install django-parler - приложение для создания таблицы с переводами

pip install django-localflavor
