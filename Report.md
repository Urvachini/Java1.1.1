# Отчёт о тестировании <Домашнее задание 1.1.1>

## Краткое описание

29.02.2020 - 29.02.2020 было проведено мануально-функциональное тестирование приложения KeyValidator.

На тестирование затрачено: 5 часов

Результат тестирования документации и установки без дефектов:

* Документация протестирована, багов не выявлено.
* Установка OpenJDK 11 проведена успешно
* Проверка в командной строке java -version выдает результат:
    PS C:\Домашняя работа по НЕТОЛОГИИ\JAVA\Java1.1.1> java -version
    openjdk version "11.0.6" 2020-01-14
    OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.6+10)
    OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.6+10, mixed mode)

В результате тестирования выявлены следующие дефекты:

* Запуск KeyValidator из командной строки запускается с ошибкой https://github.com/Urvachini/Java1.1.1/issues/1
* Валидные ключи не являются валидными https://github.com/Urvachini/Java1.1.1/issues/2
* Невалидные ключи являются валидными https://github.com/Urvachini/Java1.1.1/issues/3

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* Описание дефектов в Issues github


В качестве тестовых данных использовались данные из Руководства использования KeyValidator https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md (с указанием ожидаемого результата):

* Запуск приложения с использованием ключей валидации java KeyValidator 00000000-0000-0000-0000-000000000000 00000000-0000-0000-0000-000000000001. Ожидаемый результат: Result for 00000000-0000-0000-0000-000000000000: OK
Result for 00000000-0000-0000-0000-000000000001: FAIL
* Валидные ключи:
    8f05e6a7-70e9-33d7-bfe7-b19eae0d8998: ОК
    80b427f8-92cd-3aae-ba04-3927fbe17c6: ОК
    b295bc63-9f03-3b4b-af80-969b39f8c262: ОК
    387eedc6-12e9-3b32-9881-63b6b5e85317: ОK
    c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180: OK
* Невалидные ключи:
    18252235-78e0-44a5-8720-556f0c7da17a: FAIL
    e66075b6-ddad-445e-baf6-161b3289522b: FAIL
    b6d53250-f07e-4352-a293-6102ddf7f1ca: FAIL
    c2bc778a-1cb9-46c6-b435-0489649d2a42: FAIL
    2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1: FAIL

Тестирование производилось в следующем окружении:

* Windows 10 home
* openjdk version "11.0.6" 2020-01-14
* OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.6+10)
* OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.6+10, mixed mode)