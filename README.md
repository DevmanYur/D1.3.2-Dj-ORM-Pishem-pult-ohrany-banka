# Пульт охраны банка

## Синопсис
Скрипт по обеспечению пропускного режима в хранилище Банка, который позволяет:
- следить за актуальностью действия пропусков сотрудников
- просматривать список сотрудников, которые находятся на текущий момент в хранилище Банка
- просматривать всю историю посещения отдельно взятого сотрудника
- выявлять подозрительные посещения

Данный репозиторий *невозможно* запустить без доступа к Базе Данных (далее БД). 
Но вы можете свободно использовать код вёрстки или посмотреть как реализованы запросы к БД.

## Как установить
1. Python3 должен быть уже установлен. 
2. Используйте `pip` (или `pip3`, есть конфликт с Python2) для установки зависимостей:

```pip install -r requirements.txt```
3. Запуск программы осуществляется из терминала командой:

```python manage.py runserver 0.0.0.0:8000```

## Code Example

Укажите время в минутах, после которого визит будет считаться подозрительным
>datacenter
>>functions.py
>>>def is_visit_long(value):
>>>>minutes = **60**

## Описание запросов
**active_passcards_view.py**\
запрос списка сотрудников с активными пропусками

**storage_information_view.py** \
запрос списка сотрудников находящихся в хранилище банка

**passcard_info_view.py** \
запрос списка визитов по отдельно взятому сотруднику