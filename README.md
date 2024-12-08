# АНАЛИЗ ДАННЫХ В РАЗРАБОТКЕ ИГР [in GameDev]
Отчет по лабораторной работе #3 выполнил:
- Сысолятин Данил Ильич
- НМТ-233929
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: "Workshop#3-Баланс в играх", Сысолятин Данил Ильич, НМТ-233929, 1,2,3.
- Цель работы.
- Задание 1.
- Фото выполненого задания (если применимо).
- Задание 2.
- Фото выполненого задания (если применимо).
- Задание 3.
- Ссылка на репозиторий GitHub (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
- Установка программного обеспечения.

## Задание 1
### Расширьте варианты доступного оружия в игре. Используйте шаблон таблицы для визуализации оружия игры Save RTF.
Ход работы:
- Добавим новые оружия, которые отличаются от основного эквипа в игре. Добавим такие gun's как "Базука", "Огнемёт", "Гранатомёт" и "Гранату". У каждого этого оружия есть разнообразные механики, которые отличаются от игрового вооружения. Например:
  - Базука, есть огромный урон вблизи, но есть соответствующий минус - урон самому себе при выстреле около себя. То есть это оружие нужно использовать с умом, когда на средней дистанции есть куча врагов.  
  - Огнемёт, оружие которое 100% попадает во врагов с 1 метра, так как у него нет разброса патрон и он стреляет по области куда напрвлен прицел игрока, но как и всех оружий у него есть свои минусы. Первый заключается в том что стреляет он не на 10 метров, а на 4 максимум, и то последний может не долететь то врага, так как шквал огня не постоянен. Второй минус заключается в том что после того как он выстрелил, земля на которой был выстрел загорится и на неё нельзя будет наступать какое-то время. PS: у имбового оружия должны быть не менее жёсткие условия.
  - Граната, оружие, которое является орудием сплэш-урона, может убить как врата, так и самого игрока, имеет огромный урон, но управлятся им сложно. Игрок своими руками может бросить гранату на 6 метров.
  - Гранатомёт (секретное оружие, спрятанное), орудие которое предназначено с использование гранатой, позволяет кидать гранату на дальние растояния. Плюс этого оружия заключается в том что теперь граната не будет наносить урон вблизи. У этого оружия нет минуса, так как его нужно найти и он является секретным дополнительным *ганом*.
- Запишем сколько "Выстрелов в ед. времени" может сделать то или иное оружие, запишем вероятность "Вероятность промаха в зависимости от расстояния". Формулой выведем все остальные нужные данные в таблицу "Вероятность пападания в процентах", "Средний Урон". Формулой наглядно напишем показатели палочками ( ||| ) какой урон имеет то или иное оружие "Damage".
- Результат выполненной работы:
https://docs.google.com/spreadsheets/d/1V72_7OJF7xP8i-Ou-T13RhdHoq0791MSocld0fdOHqA/edit?usp=sharing  
Таблица с новыми видами оружия
![image](https://github.com/user-attachments/assets/45bee2f6-d8ae-4893-8d53-b5ecaf60d3b1)
![image](https://github.com/user-attachments/assets/5793f947-b4aa-4025-b719-42c601ae6f0d)
![image](https://github.com/user-attachments/assets/8d0494ce-94d1-40eb-b618-ba36f4ac8c68)
![image](https://github.com/user-attachments/assets/0688e115-9756-4c5b-bcc5-85f530ba99e1)

## Задание 2
### Визуализируйте параметры оружия в таблице. Используйте шаблон таблицы для визуализации оружия игры Save RTF. Постройте примеры для следующих математических величин (см. пример в презентации):
- Среднеквадратическое отклонение (СКО)
- Разброс урона оружия
- Вариативность времени отклика игрока (реакция на события)
Ход работы:
- Визуализируйте параметры оружия в таблице.
  
![image](https://github.com/user-attachments/assets/f36b10c3-d15a-41d9-822c-7158b641fbd4)

![image](https://github.com/user-attachments/assets/d0fecf0c-d0b6-4745-8725-34fa0975fd84)

- Среднеквадратическое отклонение (СКО)

Разберём пример на огнемёте:
![image](https://github.com/user-attachments/assets/c40b22c9-0931-4a72-81cc-f08b1e2bad06)

![image](https://github.com/user-attachments/assets/5dfac3b2-2c96-4cac-acbb-1148c4c03414)

Так как огнемёт стреляет не пулями, а областью огня, то зададим ему радиус попадания (s=800) больше чем у пули в 8 раз (можно увеличить если потребуется).
А так же уменьшим растояние на которое он может стрелять (4 метра = радиус 2 = scale)

- Разброс урона оружия

![image](https://github.com/user-attachments/assets/8a02ae05-b9f8-4319-bc66-c9982a68f381)

![image](https://github.com/user-attachments/assets/192de912-8ffc-4603-8c40-0074d46c5838)


- Вариативность времени отклика игрока (реакция на события)

![image](https://github.com/user-attachments/assets/14854684-d826-4711-aec9-86031bc38e67)

![image](https://github.com/user-attachments/assets/802b50c3-c56d-4919-8f46-1017337a449d)


## Задание 3
### Решение в 80+ баллов должно визуализировать данные из google-таблицы, и с помощью Python передавать переменные в проект Unity. В Python данные также должны быть визуализированы.
Ход работы:
- abs

## Выводы

abs

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
