# D13.4
Задание начинается с 187 строчки кода. Здесь я постарался выполнить все задания. Все вроде бы работает, вопрос только в mail_admins. 
Как отправлять сообщения уровней ERROR и выше из django.request и django.server по формату, как в errors.log. Тут я что-то до конца не разобрался. 
В задании я хотел имитировать отправку почты Django. То есть письма должны записываться в локальный файл вместо реальной отправки. 
Для этого я использовал соответствующий почтовой бекенд email_backend и написал такую строчку в settings.py EMAIL_FILE_PATH = 'email-messages'. 
В mail_admins добавил 'email_backend': 'django.core.mail.backends.filebased.EmailBackend' – это 263 ст. 
 
