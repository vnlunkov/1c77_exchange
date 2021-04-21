# 1c77_exchange

## Назначение ##

Обработка предназначена для автоматической синхронизации данных между информационными базами 1С:Предприятие 8.X и информационной базой на платформе 1C:Предприятие 7.7. Формат обмена **1С:Конвертация данных 2.х**.

Обработка настроена для работы в конфигурации 1С:Предприятие 7.7 на выгрузку и загрузку измененных документов и справочников.

## Требования ##

- 1С Предприятие 7.7 для SQL
- Наличие внешней компоненты *1cpp.dll* (для прямых запрос к SQL)  
- Наличие внешней компоненты *v7plus.dll* (для работы с XML)
- Наличие УРБД (для регистрации изменных данных)

## Установка ##

В режиме конфигуратора, через меню *Администрирование - Распределенная ИБ - Управление*, добавляем новую периферийную ИБ (код EDI, только получатель). Выгрузку данных не производить.


![Администрирование - Распределенная ИБ - Управление](https://raw.githubusercontent.com/vnlunkov/1c77_exchange/master/Img/ReadMe_01.png)


![Окно управления распределенными ИБ](https://raw.githubusercontent.com/vnlunkov/1c77_exchange/master/Img/ReadMe_02.png)


В окне управления распределенными ИБ задать параметры текущей ИБ, нажав **Центральная ИБ**. **Важно!** Код ИБ должен быть двузначным, формата: [пробел]XX, где XX - код ИБ.


![Установка параметров текущей ИБ](https://raw.githubusercontent.com/vnlunkov/1c77_exchange/master/Img/ReadMe_03.png)


Ввести параметры центральной ИБ и нажать кнопку **ОК**.


![Подтверждение создания распределенной ИБ](https://raw.githubusercontent.com/vnlunkov/1c77_exchange/master/Img/ReadMe_04.png)


При первичной настройке распределенной ИБ система запросит подтверждение, необходимо нажать кнопку **ОК**.


![Добавление нового узла ИБ](https://raw.githubusercontent.com/vnlunkov/1c77_exchange/master/Img/ReadMe_06.png)


Добавляем переферийную ИБ, с которой будет осуществляться обмен, нажав **Новая перефирийная ИБ**. Ввести параметры переферийной ИБ и нажать кнопку **ОК**. **Важно!** Код ИБ должен быть двузначным, формата: [пробел]XX, где XX - код ИБ.


![Результат настройки](https://raw.githubusercontent.com/vnlunkov/1c77_exchange/master/Img/ReadMe_07.png)
