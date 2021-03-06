# Allspace file structure

> Шаблон для создания идеальной файловой структуры

## Какую проблему решает

Существует куча проблем с папками по умолчанию в любой операционной системе - что-то из файлов сохраняется на системный диск, что-то - на вторичный. 

С этим тяжело работать, а перенос всех данных превращается в ад...

## Описание

`Allspace file structure` - это спецификация универсальной файловой системы.

Корень - директория `Allspace` размещается на диске с пользовательскими даннными (`D` для Windows, `/users/<username>` в Linux). 

В ее основе лежит **доменная модель**. Например, если есть задача "хочу куда-то сохранить университетскую работу по программированию", то возможны два подхода сохранения её в директорию: 
1. `Программирование/Университет/Название предмета/<название работы>`
2. `Университет/название предмета/<название работы>`

Личный опыт и эксперименты показали, что второй подход - наиболее удобный, так как позволяет логически разделить наибольшее количество директорий.

`Allspace file structure` содержит все необходимые абстракции для хранения:
1. Личных файлов
2. Собственной базы знаний
3. Университетских проектов
4. Рабочих проектов

## Какие преимущества даёт
1. Каждый раз при создании новых файлов убирает необходимость напрягаться, придумывая для них подходящее место
2. Поддерживает структуру в порядке, защищая ее от захламления при сохранении однотипных файлов в разные места
3. Защищает структуру от неудаляемых навязываемых ОС системных файлов
4. Убирает зависимость от дефолтных директорий операционных систем
5. Позволяет легко копировать все данные и переносить их на другой компьютер/операционную систему

## Основные фичи
1. Файловая структура продумана заранее для практически всех задач
2. Введена директория "Буфер", которая защищает структуру от свалки временных файлов

