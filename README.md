# D13.4
&emsp;Задание начинается с 187 строчки кода. Здесь я постарался выполнить все пунты. Все вроде бы работает, вопрос только в mail_admins. 
Как отправлять сообщения уровней ERROR и выше из django.request и django.server по формату, как в errors.log. Тут я что-то до конца не разобрался. 
В задании я хотел имитировать отправку почты Django. То есть письма должны записываться в локальный файл вместо реальной отправки. 
Для этого я использовал соответствующий почтовой бекенд email_backend и написал такую строчку в settings.py EMAIL_FILE_PATH = 'email-messages'. 
В mail_admins добавил 'email_backend': 'django.core.mail.backends.filebased.EmailBackend' – это 263 ст. 
<hr>
Проверял все на простом представлении.
<br>
view.py в приложении News_Portal.
<br>
logger = logging.getLogger('console_logger_ERROR_and_CRITICAL')
<br>
def indexx(request):<br>
&emsp;logger.error('Hello')<br>
&emsp;return HttpResponse("Hello logging world.")
<hr>
ursl.py
<br>
from django.urls import path
<br>
from .views import indexx
<br>
urlpatterns = [<br>
&emsp;path('indexx/', indexx, name='indexx')<br>
]
