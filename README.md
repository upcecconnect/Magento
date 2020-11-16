# Magento
Plugin UPC e-Commerce Connect for Magento
 
Инструкция по использованию платежного плагина eCommerceConnect для системы Magento 1.x (1.9.0.1)

1.	Установка
 Для установки модуля
•	Распакуйте модуль в директорию с установленным магазином на Magento.
•	Ключи нужно залить в папку keys: \magentoEcc\media\keys
•	Очистить кэш в Admin -> System -> Cache Management -> Flush Cache
2.	Настройка 
2.1 Настройка на стороне сайта
Базовая валюта магазина должна быть установлена Украинская гривна.
Настройки модуля находятся в 
Admin -> System -> Configuration -> Payment Methods -> eCommerceConnect General Settings
 Здесь вы должны ввести Merchant ID и Terminal ID которые получили от нас.
 Ниже активируйте платежный метод в разделе 
eCommerceConnect General Settings.
•	eCommerceConnect Settings - используйте этот платежный метод если вам необходимо дать возможность пользователю выбрать метод оплаты на сайте eCommerceConnect.
 
eCommerceConnect Settings – тут включите плагин чтобы он отображался на сайте Enabled – Yes
Title – название платежной системы – которое будет отображаться на сайте – eCommerceConnect

2.2	Настройка Notify_Url, Success_Url and Fail_Url

Для настройки данный ответов с платежного шлюза зайдите в личный кабинет мерчанта и в своем терминале в настройках
Success_Url  == http://YOURDOMAIN.COM/paymaster/payment/success
Fail_Url ==  http:// YOURDOMAIN.COM/paymaster/payment/fail
Notify_Url == http:// YOURDOMAIN.COM/paymaster/payment/callback
Вместо YOURDOMAIN.COM –подставить свой URL сайта.
Відмінити транзакцію після неуспішної доставки повідомлення на NOTIFY_URL – и это поле включить в состояние ТАК
Скриншот по настройкам представлен ниже
 


3.	Тест
Для проверки корректности установки и настройки плагина, необходимо провести пробную покупку.
После выбора способа оплаты «eCommerceConnect» будет открыта платежная страница:

 


4.	Удаление модуля
Для того чтобы полностью удалить модуль из системы удалите следующие файлы и папки:
#rm -rf app/code/community/Voronoy app/design/frontend/base/default/template/paymaster app/etc/modules/Voronoy_Paymaster.xml app/locale/en_US/Voronoy_Paymaster.csv app/locale/ru_RU/Voronoy_Paymaster.csv app/locale/uk_UA/Voronoy_Paymaster.csv


