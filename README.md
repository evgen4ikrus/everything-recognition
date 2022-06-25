# everything-recognition
Проект основан на библиотеке [opencv](https://pypi.org/project/opencv-python/), распознает объекты на видео с веб-камеры.

## Как установить
Скачайте код. Python3 должен быть уже установлен. Установите зависимости командой:
```
pip install -r requirements.txt
```

## Как запустить
Для запуска используйте команду:
```
python run.py
```
Запускается окно в котором транслируется изображение с веб-камеры и распознанные объекты, которые выделяются прямоугольниками (синий-лицо, зеленые-глаза). Для завершения работы программы используется клавиша q на клавиатуре.

Если не удалось установить соединение с веб-камерой, в консоль выводится ошибка, и программа завершает работату.

## Как настроить
В файле config.py задаются параметры поиска объектов. Доступные объекты: Face front, Face profile, Smile, Eyes, Full body, Cat face.

Параметры обекта:
* path - путь к файлу c объектом;
* color - цвет рамки (BGR);
* draw - флаг для включения поиска объекта.

Например, для распознавания улыбки и выделения её зеленой рамкой, нужно прописать:
``` Python
"Smile": {
        "path": "haarcascades/faces/haarcascade_smile.xml",
        "color": (0, 255, 0),
        "draw": True
    }
```

## Цель проекта
Код написан в образовательных целях на онлайн-курсе для веб-разработчиков dvmn.org.
