Файлы
-----
system.py - файл, в котором описывается модель системы. Состоит классов System, Component, User.

treats.csv - файл, в котором описаны угрозы с индикаторами в журналах (пока там только sysmon). Формат получал через таблицу
https://docs.google.com/spreadsheets/d/1-pbw87ZahzkjTVuMQdd03BlBxKRZ2SBr8Z3HkDf83RA/edit?usp=sharing

antimalware.py, firewall.py, warnings.py - файлы, в которых я попробовал сделать самые просые модели антивируса, файервола и опасного события. Как-то они могут потом прогодиться, пока не знаю.

Окружение
---------
Использовал conda, настройки по умолчанию

TODO
----
1. Сделать пример json-файла из файла sysmon с угрозами из treats.csv. Полезные ресурсы
https://www.varonis.com/blog/sysmon-threat-detection-guide/
https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx?i=j

2. Написать функции в классе System, которые проходят по логу в json-формате, обнаруживают угрозы и выводят сообщение о том, где, когда и какая вознкла угроза, и с каким номером в файле

3. Добавить в классы antimalware и firewall функции, которые используют сторонние белые и серые списки (для анималрваря это еще может быть программа)

4. Придумать, как привязать возможные угрозы к разным компонентам по дефлоту, чтобы проверка на угрозы проходила автоматически. Например, если я добавил в систему роутер, то какие угрозы сразу возникают? Попробовать помоделировать в microsoft threat modelling. Пройти по техикам att&ck
